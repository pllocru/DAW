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






