# Instalación de Apache en Ubuntu

Esta guía describe cómo instalar el servidor web Apache como parte de una pila LAMP en Ubuntu.

## Arquitectura Web: Modelo de Tres Capas

La arquitectura web de tres capas es un modelo de diseño de software que divide el sistema en tres partes principales:

1. **Capa de Presentación (Frontend)**: Es la interfaz que interactúa directamente con el usuario. Muestra la información y recibe las entradas de los usuarios, generalmente mediante tecnologías como HTML, CSS y JavaScript en el navegador.

2. **Capa de Lógica de Negocio (Backend)**: Maneja la lógica de la aplicación. Procesa las solicitudes del usuario, realiza cálculos y determina la lógica de presentación de los datos. Lenguajes como PHP, Python, Java y frameworks como Node.js se utilizan en esta capa.

3. **Capa de Datos (Base de Datos)**: Se ocupa de almacenar y gestionar los datos de la aplicación. Las bases de datos como MySQL, PostgreSQL o MongoDB almacenan la información y la proporcionan cuando es necesario.

## Plataformas Web: LAMP y WISA

### LAMP
- **Linux**: Sistema operativo base.
- **Apache**: Servidor web que maneja las solicitudes HTTP y distribuye el contenido web.
- **MySQL**: Sistema de gestión de bases de datos relacional.
- **PHP**: Lenguaje de programación para el desarrollo de la lógica del servidor (se pueden emplear también Python o Perl).

### WISA
- **Windows**: Sistema operativo base.
- **IIS (Internet Information Services)**: Servidor web de Microsoft para gestionar las solicitudes web.
- **SQL Server**: Sistema de gestión de bases de datos de Microsoft.
- **ASP.NET**: Framework de Microsoft para construir aplicaciones web y servicios API.

## Pasos para la instalación de Apache en Ubuntu

1. **Actualizar el sistema**:
   ```bash
   sudo apt update
   sudo apt upgrade

2. **Instalar Apache:**:
   ```bash
   sudo apt install apache2

3. **Verificar el estado de Apache:**:
   ```bash
   sudo systemctl status apache2

4. **Configurar el firewall:**:
   ```bash
   sudo ufw allow 'Apache'
   sudo ufw status

5. **Prueba de instalación:**:
    Abre el navegador y visita http://your_server_ip para verificar que Apache esté funcionando correctamente.

## Recursos

- [Guía de instalación de LAMP en DigitalOcean (Ubuntu 18.04)](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-ubuntu-18-04)
- [Guía de instalación de LAMP en DigitalOcean (Ubuntu 20.04)](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-20-04-es)
- [Más información sobre `apt-get`](http://www.ubuntu-guia.com/2011/01/comando-apt-get-en-ubuntu.html)
- [Guía para instalar Ubuntu en VirtualBox](https://www.neoguias.com/instalar-ubuntu-windows-virtual-box/)


