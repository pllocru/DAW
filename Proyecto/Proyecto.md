## 1.Instalacion del servidor web Apache
# Instalar Apache

![1](https://github.com/user-attachments/assets/201432ba-9037-4cb0-b1f1-8cb8344bf19d)

![2](https://github.com/user-attachments/assets/1faf8439-a0e4-4087-a2cc-38b11a9f865c)

# Editar el archivo hosts

![2 5](https://github.com/user-attachments/assets/14f9b9fc-34e9-4463-9162-22884c42b545)

![3](https://github.com/user-attachments/assets/17744b30-0710-4077-996e-a6c847c983fa)

## 2.Activamos los módulos php y mysql

![php](https://github.com/user-attachments/assets/90c51eb4-ba90-4adc-a28d-f2a9f6dd412b)

Y reiniciamos:

![restart](https://github.com/user-attachments/assets/b5af4c42-a452-4ca0-8aa8-2eba03432ebd)


## 3.Instalación y configuración de WordPress
Instalar MySQL y crear una base de datos para WordPress:

![mysql](https://github.com/user-attachments/assets/a31a693b-2b77-4963-aa46-54f53c9d8448)

Accedemos a mysql:

![acceso](https://github.com/user-attachments/assets/5e047a63-21d4-460a-8d5e-299d17b48ea2)

Creamos una base de datos:

![create](https://github.com/user-attachments/assets/1aa7e017-ba50-405a-8fe3-decc82ad0646)

![bye](https://github.com/user-attachments/assets/5e625efc-7bef-457c-a7be-f5f17b793cd0)

Descargamos e instalamos WordPress:

![wordpress install](https://github.com/user-attachments/assets/04581fd7-a45b-4a4d-9877-265d528052bc)

![tar](https://github.com/user-attachments/assets/473ff2fb-5359-4b5b-b115-fef64e4ea1ed)

![vh](https://github.com/user-attachments/assets/b9518909-da6e-4753-bfc7-bd66b9fa7a88)

![permisos](https://github.com/user-attachments/assets/80145567-c495-4aa5-b01a-2a63fd7df2eb)

Configuramos un vortualHost para Wordpress:

![confi](https://github.com/user-attachments/assets/2046f7bb-40d5-47e3-8222-bac03ba42313)

Contenido:

![contenido](https://github.com/user-attachments/assets/34bc15d6-7f56-4c95-b0fe-de1a736824d6)

Habilitamos el sitio y reiniciamos con apache

![fin wordpress](https://github.com/user-attachments/assets/49f6adb3-ce80-4bfe-8715-118ed1d85b1b)

Y comprobamos que haya funcionado,introducimos http://centro.intranet y nos da:

![accesowordpress](https://github.com/user-attachments/assets/c4836949-db5e-40a8-b71e-e70988566c42)

## 4.Activar el módulo “wsgi” para permitir la ejecución de aplicaciones Python

![WSGI](https://github.com/user-attachments/assets/897328e2-ec28-4a68-a12f-216af1dedbe9)


## 5.Crea y despliega una aplicacion python para comprobar que funciona

Creamos un directorio con el archivo:

![mkdir](https://github.com/user-attachments/assets/f64ff179-13ca-43ec-85ff-a4d98afd5f08)

Y accedemos a un archivo py dentro del directorio ya añadimos el siguiente codigo:

![code](https://github.com/user-attachments/assets/2fff8317-e99b-4e68-b58b-3058deb809de)

Configuramos el virtualHost:

![nano2](https://github.com/user-attachments/assets/7541633a-efc0-4ae2-b536-d7380527e7a3)

Contenido:

![contenido](https://github.com/user-attachments/assets/485717eb-87e5-4759-9754-f6a43fe46c16)

## 6.Añadimos adicionalmente una proteccion al acceso de python para comporbar que funciona

![password](https://github.com/user-attachments/assets/d67b275b-1156-4922-a23f-8221a03292f8)

Le hemos añadido (hola) como contraseña

![final](https://github.com/user-attachments/assets/ffec23c9-3f20-442e-9ced-eb1a025ee351)

Y comprobamos que todo ha salido bien:

![comprobacion](https://github.com/user-attachments/assets/377ff6d0-7caf-4a3d-9d07-01593ccc6a0f)

## 7.Instalamos y configuramos awstat.

Instalamos AWStats:

![instalar](https://github.com/user-attachments/assets/f77a7c57-78e5-4e52-81c3-94bddee812dc)

Configuramos AWstats para Apache:

![cp](https://github.com/user-attachments/assets/9b5c740d-5497-4dc7-8e54-dec3051fd45b)

Editamos el archivo:

![nano](https://github.com/user-attachments/assets/04c44a28-1ebc-4eaf-81dd-b89940919219)

Y tenemos que cambiar el SiteDomain="centro.intranet"

Actualizamos las características:

![sudo](https://github.com/user-attachments/assets/846617c1-ef9a-43ec-bc3c-ef4e79cbb45d)

Y habilitamos el cgi:

![final](https://github.com/user-attachments/assets/4d8d22b4-08f4-4d8a-8317-5395658b1021)

Buscamos http://centro.intranet/cgi-bin/awstats.pl?config=centro.intranet como resultado:

![FINALAWS](https://github.com/user-attachments/assets/dcdb7447-6023-44b7-991f-f8cb2899fbe5)

## 8.Instala un segundo servidor bajo el dominio servidor2.centro.intranet

Actualizamos sistema

![1](https://github.com/user-attachments/assets/50706075-62a9-44b9-b913-870a35e6685a)

E instalamos Nginx y PHP:

![instalamos](https://github.com/user-attachments/assets/cc433bd7-7711-43fd-a1b8-7d9074e72f6a)

Crear un archivo de configuración para servidor2.centro.intranet:

![acceder nano](https://github.com/user-attachments/assets/4b2191ed-e450-4820-b500-b8377bc2815f)

Contenido:

![info](https://github.com/user-attachments/assets/56aba196-9040-4cc6-9d88-f8c24d7c80e7)

Activamos la configuracion:

![ln](https://github.com/user-attachments/assets/d3078199-d43e-4ee3-9c70-c0f0bda0b348)

![ngixxx](https://github.com/user-attachments/assets/b61ab87b-a4e5-47d0-a06f-4b90f4ab94ed)

Creamos un archivo html para que se muestre:

![archivohtml](https://github.com/user-attachments/assets/e3c1ee9b-ee60-41c8-bb3b-0cd85e2d7416)

Damos permisos y creamos un directorio raiz:

![mkdir](https://github.com/user-attachments/assets/d10e6fdb-d15f-4f63-99af-577132cbe9ed)

![permisos](https://github.com/user-attachments/assets/6f710727-8c30-4239-9059-2129b72bacc9)

Abrimos el etc/hosts y añadimos la ruta:

![hosts](https://github.com/user-attachments/assets/8b38cc22-6b57-44ad-88a5-a0d13f53bacf)


Y reiniciamos:

![reiniciamos](https://github.com/user-attachments/assets/a9479054-b4ff-4604-84f1-f311fe675f15)

Dando como resultado:

![funciona](https://github.com/user-attachments/assets/13b3031d-3ec9-4897-b0f1-a8f4e345dd74)



