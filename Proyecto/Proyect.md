# 1.Instalación y Configuración de un Servidor Web Apache con Dominios Internos

## Requisitos Previos
- Sistema operativo basado en Linux (ej. Ubuntu/Debian).
- Acceso como usuario con privilegios administrativos.

---

## Instalación del Servidor Web Apache

**Actualizar el sistema**:

![Captura](https://github.com/user-attachments/assets/e4cb9564-9c7a-4445-8a99-9abafa5eddea)


**Instalamos apache2**:
   
![apache](https://github.com/user-attachments/assets/c8b2d535-c0b3-4e09-ad18-a1d26d07c94f)

Y abrimos el servidor apache, y comprobamos que realmente está abierto

![apacheserver](https://github.com/user-attachments/assets/a06cfaa0-b4c4-4ec4-b2cd-a561ab6231c4)


## Configuración de los Dominios

**Configuración del Archivo Hosts**

Editamos el archivo hosts:

![nano archivo](https://github.com/user-attachments/assets/db9b1b5a-0201-4d2d-88b0-46cd3c9f7589)

Y añadimos las siguientes líneas:

![ips](https://github.com/user-attachments/assets/62e5ae89-2bbc-4eb8-995e-151813086828)

## Crear directorios para ambos dominios

![mkdir](https://github.com/user-attachments/assets/ad6c8e88-d252-46cc-8dfa-95541902fcde)

![mkdir](https://github.com/user-attachments/assets/d9c531ee-c78e-4c49-93a8-70eb0b26af19)

Aseguramos de asignar permisos:

![chown permisos](https://github.com/user-attachments/assets/a7110abe-9a03-48a6-acfc-d3eccc5b68da)

## Configurar Virtual Hosts para Apache

Para centro.intranet (WordPress):

![nano 1](https://github.com/user-attachments/assets/f1b72688-abd1-4401-a715-3ce167a3e4a4)

Contenido:

![serverhost](https://github.com/user-attachments/assets/88e75154-c974-429e-b8f1-a92d677e40a8)

Para departamentos.centro.intranet:

![pyconfi](https://github.com/user-attachments/assets/213e3c98-fbb9-4861-9f79-40e830855c93)

Contenido:

![confi](https://github.com/user-attachments/assets/0172b7a2-5aaa-421e-abd5-82ca36bc7a5c)

Habilitamos los sitios y módulos requeridos:

![enable](https://github.com/user-attachments/assets/e7463301-fd97-4402-ac74-dc6078981722)
![a2ensiteconf](https://github.com/user-attachments/assets/33c1eb04-142e-4a03-a33d-4ed7f1ab7ea8)

Reseteamos apache

![restart](https://github.com/user-attachments/assets/a250c4f4-b91d-4642-b717-87750d9b3028)

## Instalar y configurar WordPress

**Instalar PHP y MySQL:**

![instalar sql](https://github.com/user-attachments/assets/22390496-579a-4e83-9881-e09ee23309c7)

Accede a MySQL:

![acces](https://github.com/user-attachments/assets/37ec9326-88ef-4e3e-8487-3a1590644f13)

Ejecuta los siguientes comandos para crear la base de datos y usuario:

![creamos base](https://github.com/user-attachments/assets/4d39a179-07c8-422c-9d27-37af68b5bb3e)

Descargar WordPress:




