# Instalación de WordPress en instancia Debian (o Ubuntu) EC2 con soporte de base de datos RDS y EFS

## Introducción

La idea de este manual es configurar un servidor web Apache montado en una instancia EC2 Debian (o Ubuntu) con un sistema de almacenamiento en EFS y la base de datos gestionada por RDS en una subred privada.

Para ello necesitaremos primeramente un VPC que tenga dos subredes públicas y dos privadas.

El objetivo de crear dos subredes públicas es construir, al final del ejercicio, un balanceador de carga que permita servir contenidos en función de la carga de los servidores.

Para crear las subredes, consulta la documentación de la sesión 1 en el apartado VPC. Para mayor facilidad, las vamos a crear a partir del asistente VPC y desde el servicio VPC.

