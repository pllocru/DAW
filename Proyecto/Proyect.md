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

![1](https://github.com/user-attachments/assets/73c2f727-69a2-4b0f-9634-8c36df5f204c)


Habilitamos los sitios y módulos requeridos:

![enable](https://github.com/user-attachments/assets/e7463301-fd97-4402-ac74-dc6078981722)
![a2ensiteconf](https://github.com/user-attachments/assets/33c1eb04-142e-4a03-a33d-4ed7f1ab7ea8)


## Crear el script Python 

Coloca el archivo app.py en el directorio principal de departamentos.centro.intranet:

![2](https://github.com/user-attachments/assets/ab99d5a6-02d4-4cba-b47b-4ce82793599f)

Agrega el siguiente contenido:

![medio](https://github.com/user-attachments/assets/3de36e62-e9c2-4d73-bef1-33fe17d3dfcb)


Haz que el script sea ejecutable:

![3](https://github.com/user-attachments/assets/ba19fec6-5502-4ef7-af98-678bf0e3154e)

## Reseteamos apache

![restart](https://github.com/user-attachments/assets/a250c4f4-b91d-4642-b717-87750d9b3028)

Y vemos los resultados:

Wordpress:

![worrrrr](https://github.com/user-attachments/assets/1a7b1967-92fb-4ea6-9a10-3020aea22c8d)

Y python:
Nos dirije a este index:

![PY](https://github.com/user-attachments/assets/7554a563-d6be-4c34-ae57-6686b795c866)

![final](https://github.com/user-attachments/assets/449af36f-9b0c-426c-86c5-f2396e3d0cba)

# 2.Activar los módulos necesarios para ejecutar php y acceder a mysql

**Instalar PHP y MySQL:**

Instala PHP y módulos necesarios: PHP es el lenguaje que vas a usar para interactuar con MySQL.
También instalaremos los módulos mysqli y pdo_mysql que permiten a PHP conectarse a MySQL.

![instalar1](https://github.com/user-attachments/assets/8942b617-9c21-44b8-acb2-6302c88c43d0)

Instala MySQL (base de datos):

![mysql](https://github.com/user-attachments/assets/f8e585f3-6454-49e4-9f2d-500a3bb643c7)

Verificar PHP: Crea un archivo de prueba info.php en el directorio de tu servidor web (/var/www/html):

![nanophp](https://github.com/user-attachments/assets/24c77ed6-c508-4afd-8327-008e6b8e06e0)

Agrega lo siguiente en el archivo:

![phprueba](https://github.com/user-attachments/assets/5eafe2ff-cf51-46b3-a4af-f66774f6028e)

Luego, abre tu navegador y visita http://localhost/info.php. Deberías ver la página de información de PHP que muestra la configuración de PHP y los módulos instalados.

![exito](https://github.com/user-attachments/assets/f7bcb430-d787-407a-a26d-db3740e165d8)

Activamos MySQL y comprobamos de que está activo:

![activamossql](https://github.com/user-attachments/assets/4b68ea0b-3abb-40ce-b298-1e62324d518d)






