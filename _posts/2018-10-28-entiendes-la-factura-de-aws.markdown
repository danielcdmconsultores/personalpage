---
title: "¿Entiendes la factura de AWS?"
date: 2018-10-28 11:14:00 +01:00
---

La primera vez que me llegó una factura de Amazon Web Services, me recordó un poco a las facturas de operadores de telefonía, no la entiendes bien pero la pagas. El otro día una clienta me preguntó si le podía explicar bien, su factura, esto me hizo pensar que es más frecuente de lo que parece. Aquí una explicación, que espero ayude a otros clientes y usuarios de AWS.

Para empezar las facturas están en DOLARES, ojo que en este caso te hace la conversión a EUROS con un total: 171,10 € 

Lo primero que hay que recordar es que en AWS se paga "atomizado" por cada uno de los servicios que dispone (actualmente más de 100), tanto usas tanto pagas. (ver listado completo de servicios)

El detalle de la factura, hace referencia a esa atomización de servicios pero los he agrupado en este caso en:

VISOR DE ALARMAS, TRANSFERENCIA DE DATOS, BASE DE DATOS, EMAIL (SNS) y ALMACENAMIENTO S3. todo ellos muy típico y utilizados por la mayoría.




El siguiente nivel de detalle es el uso en cada región, actualmente AWS tiene 18 y en cada región el precio es diferente, por eso en la web de AWS con los detalles de precios debes de seleccionar la región ( ver ejemplos de Aurora)

Para este ejemplo. tiene cargos en París con el servicio de computo "SERVIDOR" (EC2) está pagando 81,34 $ y para la BASE DE DATOS (RDS) está pagando 114,76 $.

En el ALMACENAMIENTO (S3) donde se guardan objetos y copias de seguridad de ficheros de la aplicación del servidor, está pagando 3,60 $ por usar 115 GB, aproximadamente 0,024 $ por GB.

Una RECOMENDACIÓN, para este caso, es pasar a MODALIDAD DE PAGO RESERVADO, tanto para el computo como para la Base de datos RDS.
Esa recomendación es realizar un COMPROMISO con AWS de 1 AÑO o 3 AÑOS para un tipo fijo de máquina o servicio y pagar anticipadamente, ahorrando entre un 40% y un 70% de descuento. ver instancias reservadas y RDS reservadas. Si lo tienes claro con el tipo de servicio usado a largo plazo, aquí encuentras una buena forma de ahorrar la factura.

Observé un servicio no utilizado, que posiblemente fue una prueba inicial o test: Una (Elastic IP) en Ohio que no USA y se la puedo anular, para ahorrar un 3,60 $ al mes

En resumen, revisa bien la factura y entiéndela, la factura de AWS es clave para saber por que pagamos. Recuerda usar el servicio de alerta de umbral de facturas para poner avisos por Límites de importes.

