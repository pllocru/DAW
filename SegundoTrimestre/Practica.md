# Instalación de WordPress en instancia Debian (o Ubuntu) EC2 con soporte de base de datos RDS y EFS

## Introducción

Se desplegará un servidor Apache en una instancia EC2 ubicada en una VPC (con 2 subredes públicas y 2 privadas). 
La base de datos MySQL se gestionará con RDS (en subred privada) y se usará EFS para almacenar archivos multimedia de WordPress.

## Creación de la Instancia EC2

Lanzaremos una instancia con una AMI debian dentro de la subred pública 1.

La llamaremos servidorwordpress. Asegúrate que esté en la VPC anteriormente creada, esta VPC se llama proyecto

![Captura](https://github.com/user-attachments/assets/d4e62eea-1772-47a9-bff6-dd8af973c1af)

Esta tendrá las subredes correspondientes:

![2](https://github.com/user-attachments/assets/29cdae94-bb41-47d4-9c2f-eade53d1c993)


El grupo de seguridad lo llamaremos seguridadwordpres. 

![asignar subred](https://github.com/user-attachments/assets/2eb7fd34-1d65-42d4-bd5c-65e104da783a)

(es importante que lo habilitemos)

![nueva ec2](https://github.com/user-attachments/assets/7dd14a52-b936-4b17-b605-3102c3fbeee2)

Nos aseguramos de que el puerto 80 está abierto.

## Apache y PHP

En la consola de Ubuntu,ponemos los siguientes comandos:

Update para actualizar el sistema:

![update](https://github.com/user-attachments/assets/47995b2a-b000-41da-9972-8ae896000b5b)

**Instalamos apache:**

![install apache](https://github.com/user-attachments/assets/9079b4e5-bfcc-4d5b-9491-317ac33331bf)

Iniciamos apache y comprobamos:

![runapache](https://github.com/user-attachments/assets/63c410a8-cb1c-4e0e-b1cb-28dc3536f22e)

![apache](https://github.com/user-attachments/assets/847b9f33-326f-42c5-a0cd-de27b2b02d17)

**Ahora php:**

Confirmamos que el paquete amazon-linux-extras está instalado en nuestro servidor.

![php1](https://github.com/user-attachments/assets/9d09bde9-854b-4d27-bce3-63ae425aa7c6)

Y instalamos la version de php 7.4 con mysql

![php7 4](https://github.com/user-attachments/assets/f1ea6563-35b4-480b-97d7-7a487baab381)

Reiniciamos apache y comprobamos que esta php instalado:

![reiniciamos y version](https://github.com/user-attachments/assets/ddb8dc32-56d5-410f-b994-ffee444b8135)

## Creación de la base de datos.

Creamos una base de datos mysql con todos estos ajustes:

![RDS](https://github.com/user-attachments/assets/ec21694a-8a07-4413-90e3-1eb6dcc5c3aa)

![plantilla](https://github.com/user-attachments/assets/cbef14f7-c933-4163-98f3-5c519c2abbb1)

![contraseña y usuario](https://github.com/user-attachments/assets/6562400b-d916-4d7e-a2fb-ea0088c9645f)

![config](https://github.com/user-attachments/assets/09461c94-8658-4c98-baf1-cfc45f77a13f)

![almacenamiento](https://github.com/user-attachments/assets/cf6914fa-5f42-4b2a-932c-dae95ef42d5c)

![conectividad](https://github.com/user-attachments/assets/dafc2132-17ef-47d7-8728-cfe1eca9cb8d)

![configadicional](https://github.com/user-attachments/assets/13c13f5f-6bbe-47e9-badc-529358998382)

![creada](https://github.com/user-attachments/assets/b8f4e783-296f-492b-ab6f-a0d8e096534a)

Una vez la creemos, la enlazamos a nuestra instancia:

![establecemos la base en el EC2](https://github.com/user-attachments/assets/26f43ed1-4db5-4340-8b0e-b29f13cec0a5)

![configuramos](https://github.com/user-attachments/assets/5433426c-f083-477f-88cc-a1886b7926d9)

Y nos dará un enlace que nos servirá para conectarnos a wordpress:

![ruta](https://github.com/user-attachments/assets/d9cdd432-7384-4584-9b65-8d6f0eb22efc)

## Elastic File System.

Ahora deberemos crear el sistema de almacenamiento externo que vamos a conectar a la instancia y que más tarde conectaremos a wordpress.

![EFS](https://github.com/user-attachments/assets/95102d83-4d53-49d1-b65c-98338a81292d)

Una vez lo tengamos creamos,le damos a asociar:

![asociar](https://github.com/user-attachments/assets/28dd3817-3684-4430-b934-77819f9122f2)

Y veremos que hay un código que deberemos de copiar para más adelante:

![codigo](https://github.com/user-attachments/assets/c86b321c-e0ee-468c-9ee4-edf0268ae957)

Aunque en EFS nos vamos a red y veremos este codigo de seguridad que lo recordaremos:

![red](https://github.com/user-attachments/assets/5513a25c-32fd-4083-ac29-153ef5ffa267)

Nos vamos ahora a editar las reglas de entrada en EC2 > security groups, y aquí cambiaremos las reglas de entrada,
le daremos al que tenga el mismo codigo de seguridad:

![grupos](https://github.com/user-attachments/assets/927ac301-05ba-4b75-a097-112d84315fd8)

Y lo editamos, es importante poner el servidorwordpress para que funcione y así enlacemos la EC2 con la EFS

![entrada](https://github.com/user-attachments/assets/87153746-26ca-4a6b-a93e-725a9e667b2d)

Ahora nos vamos a la consola,creamos una carpeta llamada efs

![creamos carptea](https://github.com/user-attachments/assets/ca126878-5cd8-48a1-8ef3-bfa98fec1af4)

Hacemos una actualizacion:

![instalamos esto](https://github.com/user-attachments/assets/aae08ba3-5833-4915-bd33-784db37b565c)

Y lo conectamos:

![conectamos](https://github.com/user-attachments/assets/ad54517a-c816-492d-af26-726be3b61381)







