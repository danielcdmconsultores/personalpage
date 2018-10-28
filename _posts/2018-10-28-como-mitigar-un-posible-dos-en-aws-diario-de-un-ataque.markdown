---
title: Cómo mitigar un posible DoS en AWS - Diario de un ataque.
date: 2018-10-28 11:15:00 +01:00
---

Ha sido un domingo 25 de Marzo de 2018 calentito, aunque el tiempo no acompañara, incluido el cambio de horario en España. Recibí una llamada de SOCORRO de un buen conocido, que tras 48 horas de parada de servicio, no conseguía que su sistema WEB se levantara.


Su aplicación hecha en #Drupal (Linux, Nginx, PHP, MySQL) alberga varias webs de países de una conocida ONG a nivel mundial y había sido migrada recientemente a Amazon Web Services. Pero ahora, me alertaba de un posible DoS y los síntomas es que se "para" la máquina. Ante esta situación, me pidió ayuda y como no, me remangué la camisa para ver qué ocurría. Teniendo en mente que hay que tener mucho cuidado con sistemas que no son tuyos, ni has tenido nada que ver en "el parto" del proyecto. Pero no se negarme a la ayuda, es como si encuentras un accidente de tráfico: detente y ayuda...

En mi mente ya visualizaba el método: Analiza, Repasa, Prioriza y por último Actúa.
Analiza: Qué está ocurriendo en el sistema, observa las máquinas, logs en las últimas horas. Revisa con detalle los logs. El poder del CloudWatch metrics, incluso en básico, da mucha información.

Repasa: Qué otras acciones se han realizado en los últimos días y si han intervenido "colegas", qué han hecho exactamente. Ver el histórico de comandos en las máquinas Linux con history

Prioriza: ¿Qué es lo más importante para los usuarios de la aplicación? y ¿Para el cliente? Responde constantemente a estas preguntas y prioriza las acciones. En este caso, fue poner online la web y mitigar los ataques hasta estabilizar el servidor.

Actúa: Pon mucho cuidado en lo que vas hacer, y ten una hoja en blanco o doc, para saber qué instrucción ejecutas cada vez y apúntala o [CTRL + V].

Observé con calma el Monitor de CloudWatch (que en la opción básica te muestra mucha información de los últimos 15 días) y vi un comportamiento muy alto de uso CPU. La primera alarma, es que la instancia EC2 es de tipo T2. Comprobé que al consumir los créditos de CPU, se quedaba bloqueada.

(vista de la utilización de CPU)


(comparándola con la vista de la utilización del crédito de CPU)


La perdida de crédito de CPU en las instancias T2, hace que la instancia quede casi bloqueada.
Activamos el T2 UNLIMITED en la instancia en cuestión, para que no se bloqueara por falta de créditos , ya que la prioridad número uno mantener online la aplicación. Ver el siguiente enlace:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/t2-unlimited.html


¿Que son los créditos de las instancias T2? LEE INMEDIATAMENTE el siguiente enlace, si no sabes que son:

https://docs.aws.amazon.com/es_es/AWSEC2/latest/UserGuide/t2-credits-baseline-concepts.html

Nota: Se puede activar el T2UNLIMITED sin parar la instancia.



Manos a la obra, ahora que NO se nos bloquea la máquina, por falta de créditos de CPU, decidí entrar en la instancia por SSH y mi primer comando fue el que me ayuda a ver que distribución tenemos entre manos:

cat /proc/version

Linux version 3.16.0-5-amd64 (debian-kernel@lists.debian.org) (gcc version 4.8.4 (Debian 4.8.4-1) ) #1 SMP Debian 3.16.51-3+deb8u1 (2018-01-08)

Reflexioné sobre lo que han intentado hacer otros usuarios (sysadmins) anteriores para mitigar el problema, y que iba a hacer yo que ellos no habían pensado (esto me llevó varios minutos)..............

#Muestrame todos los comandos anteriroes con el usuario del login
history
# Muetra todos los comandos del superuser (root)
sudo su
history

Revisé el fichero log del servidor de aplicaciones NGINX, en tiempo real.

cd /var/log/nginx/

tail -f access.log
Durante varios minutos, observé un montón de IPs forzando una consulta de php (scrolling constante), estas IP siempre hacen la misma consulta, ¿la misma? que raro.......

(ejemplo simulado, no real.)


Comprobé el origen de las IP con iplocation.net y la sorpresa fue que TOD@S las ip son de China, pensé en el poder de IPTABLES y su configurador CSF ConfigServer Security & Firewall (requiere perl por si lo quieres instalar).

# reviso las entradas 
sudo nano /etc/csf/csf.deny
# edito el configurador de CSF
sudo nano /etc/csf/csf.conf
# busco CC_DENY y remplazo para bloquear ips de Rusia y China
Añado la línea: CC_DENY="RU,CN"
# reiniciamos las reglas del CSF
sudo csf -r
A partir de los anteriores comandos y reiniciar el IPTABLES, la CPU bajó al 5%. Solucionando el problema en gran medida, y estabilizando el servidor con lo cual cumplí el primer objetivo.

Por último, revisé el SECURITY GRUOPS y hay algunas recomendaciones de seguridad para mi colega como no tener el puerto 22 abierto a ALL, Instalar un Load Balancer, crear reglas para avisos de CLoudWatch, etc... y desactivar el T2 UNLIMITED pasados unos días una vez estabilizada la instancia.

Paso nota a los desarrolladores de la aplicación para que analicen el por qué #Drupal engancha tanta CPU en la consulta y por supuesto todas las acciones realizadas. ¡¡Esto es DevOps!!!

Por último: DOCUMENTAR TODO LO REALIZADO y disfrutar el domingo en familia!!!!

¿Se te ocurren otras recomendaciones? No te las calles y mejora el post........