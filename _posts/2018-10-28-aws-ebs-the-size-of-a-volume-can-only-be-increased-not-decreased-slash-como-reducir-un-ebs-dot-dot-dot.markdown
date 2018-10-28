---
title: AWS EBS - The size of a volume can only be increased, not decreased. / Cómo
  reducir un EBS ...
date: 2018-10-28 11:13:00 +01:00
---

How can I decrease/shrink a Elastic Block Store? This post is about how to do it, in Windows 2012 Server image from 500Gb to 150Gb. Remember the EBS only can upgrade easily, but not decrease. (see the main picture)

/ Como reducir/encoger el tamaño de un Elastic Block Store? Este artículo trata sobre como hacerlo, en una imagen con Windows 2012 Server con 500Gb hasta dejarlo en 150Gb. Recuerda que el EBS solamente es puede ampliar fácilmente pero no reducir. (ver la imagen principal)

STEP 1 / PASO 1

Take the last snapshot to get a good backup, first at all.

/ Toma una última snapshot como backup antes de nada.

STEP 2 / PASO 2

Create a new empty EBS with the new size, in the same Availability Zone, in this example 150 GBytes. [Create Volumen]

/ Crear una nueva imagen EBS vacía, en la misma zona/región, con el tamaño deseado, en este ejemplo de 150 Gbytes. [Create Volumen]




STEP 3 / PASO 3

Attach the new smaller ELB to your Windows Instance from [Actions / Attach Volume]

/ Agrega el pequeño nuevo ELB a tu instancia Windows desde [Actions / Attach Volume] .


STEP 4 / PASO 4

Use a clone program to Clone it from 500 Gb to 150 Gb (Of course you should not have more than 150 GB in data). For me, the best program to do it is HDClone from Miray (german company). We use Professional Edition v8 & It's has never failed me (adjusts all the values of the MBR, partition table, automatically). It has taken about 30 minutes to clone 100Gbytes

/ Usa un programa para clonarlo desde el de 500Gb al de 150Gb. (Por supuesto no debe tener ocupados con datos más de 150GB.). Para mi, el mejor programa para realizarlo es HDClone de Miray (Empresa alemana). Nosotros usamos Professional Edition v8 y nunca me ha fallado (ajusta todos los valores de la MBR, tabla de particiones, de forma automática). Ha tardado unos 30 minutos en copiar 100 Gbytes de datos.


STEP 5 / PASO 5

Stop the instance, Detach both ELBs. TIP!: Attach the smaller ELB with Device /dev/sda1

/ Para la Instancia, "quita" los dos ELBs. Ojo!: Adjunta el menor ELB a la Instancia como Device /dev/sda1


STEP 6 / PASO 6

Start the Windows Server instance and test all services & apps, sometimes some programs detect the new ELB. And remmember create new procedure of backups/snapshots of the new ELB.

/ Inicia la instancia de Windows y prueba sus servicios y aplicaciones, Algunas veces algunos programas detectan el cambio de tamaño. Recuerda modificar tus escripts para snapshots al nuevo ELB.

WHY? - ¿POR QUE?

Reduce the Bill / Reducción de costes importante, ya que el precio del GB en ELB es valioso
Reduce time to do snapshots / Reducción del tiempo en crear snapshots.
LINKS / Links de Interes

https://cloudacademy.com/blog/amazon-ebs-shink-volume/