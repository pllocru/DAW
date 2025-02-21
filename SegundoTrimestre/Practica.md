# Instalación de WordPress en instancia Debian (o Ubuntu) EC2 con soporte de base de datos RDS y EFS

## Introducción

La idea de este manual es configurar un servidor web Apache montado en una instancia EC2 Debian (o Ubuntu) con un sistema de almacenamiento en EFS y la base de datos gestionada por RDS en una subred privada.

Para ello necesitaremos primeramente un VPC que tenga dos subredes públicas y dos privadas.

El objetivo de crear dos subredes públicas es construir, al final del ejercicio, un balanceador de carga que permita servir contenidos en función de la carga de los servidores.

Para crear las subredes, consulta la documentación de la sesión 1 en el apartado VPC. Para mayor facilidad, las vamos a crear a partir del asistente VPC y desde el servicio VPC.

## Creación de instancias

Lanzaremos una instancia con una AMI debian dentro de la subred pública 1.

La llamaremos servidorwordpress. Asegúrate que esté en la VPC anteriormente creada, esta VPC se llama proyecto

![Captura](https://github.com/user-attachments/assets/d4e62eea-1772-47a9-bff6-dd8af973c1af)

Esta tendrá:

![2](https://github.com/user-attachments/assets/29cdae94-bb41-47d4-9c2f-eade53d1c993)


El grupo de seguridad lo llamaremos seguridadwordpres. 
Nos aseguramos de que el puerto 80 está abierto.

