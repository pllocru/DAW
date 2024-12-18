## Actividad AWS

Usando una instancia AWS debemos instalar Apache con las siguientes opciones de configuración:

# Creamos una instancia:

Esta la generamos con ubuntu, y añadimos todo por defecto.

![ubuntu](https://github.com/user-attachments/assets/02c0e8de-837a-4249-8a88-75e46e592d14)

El par de claves vockey.pem,

![vockey](https://github.com/user-attachments/assets/f47da64a-b1d2-469b-a0c5-793f87bf7274)


Y añadir los puertos ssh, http y https. 

![http](https://github.com/user-attachments/assets/f5fc5fc0-6d3a-440f-8a96-ce816897858a)


Una vez le demos a crear instancia nos saldra en la consola esto:

![lanzar instaancias](https://github.com/user-attachments/assets/6c049ef0-a534-402d-9048-dce52cd43546)

Y le daremos a conectar.Una vez dentro nos saldrá algo parecido a:

![consola](https://github.com/user-attachments/assets/56aaba94-70c7-4a29-a3f1-4e0beb77eb2d)

Si nos sale esto,lo hemos hecho bien,ahora vamos a instalar apache.

# Instalamos Apache

Antes de instalar nada,actualizamos el sistema:

![actualizar](https://github.com/user-attachments/assets/f5fbde69-bcc6-4187-b270-d2bb58eddbd4)

Una vez actualizado,ahora si,lo instalamos:

![apache](https://github.com/user-attachments/assets/b10e96f0-d47f-4116-b68b-84ec6bf23f84)


Y lo inicamos y comporbamos que funciona:

![startyenable](https://github.com/user-attachments/assets/2b258ab3-71ba-436b-afe8-835e5b60b1a2)

Comprobamos:

![apacheestaenable](https://github.com/user-attachments/assets/e0655b0d-c4c1-41eb-9e50-4b7380104ef7)


# Activar la autenticación con MySql 

Instalamos mysql

![instalar mysql](https://github.com/user-attachments/assets/8f563116-4ee0-48f6-9817-18bb8235832b)

Accedemos con sudo:

![sudomysql](https://github.com/user-attachments/assets/3729565d-52a2-48e2-8281-bc7c76384e3e)

Y creamos uan base de datos:

![crear databse](https://github.com/user-attachments/assets/b7cab70e-a6f4-4e98-b136-c8089a521668)

Habilitamos los modulos necesarios:

![activar modulos](https://github.com/user-attachments/assets/ac7c02b4-dfcf-43f3-8e65-3cd0daac87d7)

Accedemos con nano a la configuracion para agregar la configuración de DBD y autenticación:

![VH](https://github.com/user-attachments/assets/94f7430d-74bb-4a9a-a51b-92d26ea45bad)

Y una vez haya realizado todos estos pasos,una vez coloquemos la url nos debería salir algo asi:

![final](https://github.com/user-attachments/assets/afd915ee-fa49-4257-ba2a-1c5e39ed9fee)

#  Activar el Módulo SSL y Crear un Certificado Autofirmado

Instala los módulos necesarios para SSL:

![ej1](https://github.com/user-attachments/assets/9939209c-bd62-4107-90f1-9df89eb68d6a)

Genera un certificado autofirmado:(se pueden inventar los datos):

![ej2 mejor](https://github.com/user-attachments/assets/cf9bceea-2a73-4c85-b8f3-742aa9d60a55)

![ej2 cont](https://github.com/user-attachments/assets/3f7744b1-75bc-4f49-b843-5574c61f88ac)

Configura Apache para usar SSL:

![a2enmod](https://github.com/user-attachments/assets/28c0fc5e-d88e-4df4-837c-4dc68d981da2)

![segundo aenmod](https://github.com/user-attachments/assets/84c6774a-de03-4f5a-8770-e79da1c4c48f)

Y reiniciamos:

![reinicio](https://github.com/user-attachments/assets/4a1f9510-0709-44b0-825c-4d2ee9bafc01)

Si ponemos la ip de la instancia,nos dará como resultado:

![ssl final](https://github.com/user-attachments/assets/5e8ca457-4624-471e-9f48-f378407c555c)



