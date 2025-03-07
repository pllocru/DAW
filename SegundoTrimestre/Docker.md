# Docker. Práctica 1

Instala Docker en Ubuntu

Actualiza el sistema

![update](https://github.com/user-attachments/assets/351ec817-2368-4472-a143-0229a7e7fbfd)

![upgrade](https://github.com/user-attachments/assets/4f415e50-f85d-49a2-81b8-50adde3e82e3)

Instala paquetes necesarios

![1](https://github.com/user-attachments/assets/3bd111eb-bf8c-40b1-a6b0-370e3590cf29)

Añade la clave GPG oficial de Docker (es necesario reiniciar)

![2](https://github.com/user-attachments/assets/36351ee6-a77e-4fa5-b807-cf79947fd1ba)

Verifica que la clave se haya añadido correctamente:

![3](https://github.com/user-attachments/assets/f5e61628-6eaf-4c16-9122-8ff2aa5fa04d)

Añade el repositorio de Docker

![4](https://github.com/user-attachments/assets/2143c9d0-5608-4a7e-9d34-8a77e918aff6)

Actualizamos 

![update](https://github.com/user-attachments/assets/a620b803-3535-4041-96a8-d9562cb5cfe6)

Y instalamos docker

![5](https://github.com/user-attachments/assets/e2c63ed2-a60b-48cc-9752-561306ebb270)

Verificamos que está instalado

![6](https://github.com/user-attachments/assets/35bf5bbc-d649-4346-b091-6b8e698aa92b)

# Docker. Práctica 2

Ejecuta la imagen "hello-world"

![hello-world](https://github.com/user-attachments/assets/29978310-ec49-4caa-baf7-80b39f28c356)

Mostramos las imágenes Docker instaladas y mostramos los contenedores Docker

![contenedore](https://github.com/user-attachments/assets/ed978683-f63f-4152-9193-3d3eceec7a9e)

Para ello creamos un directorio app, donde vamos a instalar dockerfile

![app](https://github.com/user-attachments/assets/b9620486-36d9-4e7f-93e0-913857add7f4)

Editamos el fichero Dockerfile:

![image](https://github.com/user-attachments/assets/64266fd0-bf2b-4e3d-850b-5b068d345b64)

Y introducimos esto:

![dockerfile](https://github.com/user-attachments/assets/c2826609-b187-46f8-b61d-a2c652cca7cb)

Iniciamos sesion en docker hub, y construimos un conetendor:

![contenedor](https://github.com/user-attachments/assets/a8cc6cf0-794f-41e7-8c74-0a86f357f3af)

Y lo construimos en nuestra imagen con el mismo nombre:

![construimos contenerdor](https://github.com/user-attachments/assets/97481529-8a20-40e5-b4e6-2ed6e1fc9ef3)

Y iniciado sesion:

![login](https://github.com/user-attachments/assets/6f3a3f12-f062-4357-bdde-c81d74c4ec46)

Nos pedirá que ingresemos un código:

![docker](https://github.com/user-attachments/assets/8d3c0172-ed2b-4df3-8cbf-3832a5438efd)

![bien](https://github.com/user-attachments/assets/19e5ed82-3ea6-47d9-b907-e414a3b72848)

Comprobaos que hemos iniciado:

![image](https://github.com/user-attachments/assets/a7118596-c495-4c61-9eba-bd0f04125e3b)

Ahora comprobamos que tenemos las imagenes construidas con:

![images](https://github.com/user-attachments/assets/834c317b-4b0f-43cf-afab-7fa8523ecf26)

Y vemos:

![pablooooo](https://github.com/user-attachments/assets/fcc2c18d-76fe-4e27-ba35-b5abc62f0ba6)

Reaizamos un push:

![push](https://github.com/user-attachments/assets/b95e7fd1-9b47-43ec-89bf-dc6d6d528387)

Y ya nos saldría:

![esta](https://github.com/user-attachments/assets/73f2de8c-1747-4ef1-b4dd-a6ae5f74f0ac)


# Docker. Práctica 3


Descargar imágenes:

-Descarga la imagen de ubuntu

![docker pull](https://github.com/user-attachments/assets/de4fb450-c82a-48e0-8f45-120a92a8b3d2)

-Descarga la imagen de hello-world

![hello world](https://github.com/user-attachments/assets/05309d1d-d406-4357-99d1-74e83dbdf97f)

-Descarga la imagen nginx

![image](https://github.com/user-attachments/assets/55b311a8-297b-43d2-ab67-cb5b46764209)


Muestra un listado de todas la imágenes

![image](https://github.com/user-attachments/assets/e1cf1e5a-bc39-43ce-8eee-03859411695f)

![image](https://github.com/user-attachments/assets/4cd7f291-3f49-4c22-bac8-e29f406dc82e)

Ejecutar contenedores hello-world con nombres específicos

-docker run --name myhello1 hello-world

-docker run --name myhello2 hello-world

-docker run --name myhello3 hello-world

![image](https://github.com/user-attachments/assets/81e7c115-ff00-47c5-9bf4-3d5f9ef276ce)

Mostrar los contenedores en ejecución

Para ello ejecutamos docker ps -a

![image](https://github.com/user-attachments/assets/78e4a1bb-7145-4804-8616-3f0cf72bf527)

Parar contenedores

Para el contenedor "myhello1”

![image](https://github.com/user-attachments/assets/7615d878-ffb6-4b63-8608-55587ba6b877)

Para el contenedor "myhello2”

![image](https://github.com/user-attachments/assets/913d094a-9b50-4818-a4d6-dd2367a46ef3)

Borrar el contenedor "myhello1"

![image](https://github.com/user-attachments/assets/94bd7fdb-b035-4f1b-9aee-88a3e4a31d74)

Borra el contenedor “myhello1”

![image](https://github.com/user-attachments/assets/82d5c267-81aa-469e-a5aa-42815a632bd6)

Borra todos los contenedores

![image](https://github.com/user-attachments/assets/635f841a-ed02-4bc1-b2d8-803af7a9b9bd)

Y comprobamos que están borrados todos:

![image](https://github.com/user-attachments/assets/eef432ec-ac29-427b-addd-a4edb27c1678)


# Docker. Práctica 4


Ejemplo 1: Crear volumen y usarlo en un contenedor

![image](https://github.com/user-attachments/assets/420c97d8-73ef-4ce2-b1f0-e81477fb9614)

![image](https://github.com/user-attachments/assets/7d02ac8e-bf3e-405e-9ffc-bafba01be933)

![image](https://github.com/user-attachments/assets/6b8026fa-f8cb-42b5-b4ea-d914a140f10f)

Comprobamos de que está corriendo el contenedor

![image](https://github.com/user-attachments/assets/553881c1-c72d-41bf-88e6-095c78de34aa)


Ejemplo 2: Usar un bind mount

Crea una carpeta en tu máquina:

![image](https://github.com/user-attachments/assets/9340c7cd-c703-4f7e-8758-822ca21f9c08)


Ejecuta Nginx montando esa carpeta:

![image](https://github.com/user-attachments/assets/a8423d61-19ae-4a1a-9f03-cc702ec545e7)

Y comprobamos:

![image](https://github.com/user-attachments/assets/23c5a1ae-f60b-423d-963e-23629392689b)

![image](https://github.com/user-attachments/assets/55158168-bd62-490f-baf6-18e831817ab5)

Ejemplo 3: Crear red bridge personalizada y conectar dos contenedores

![image](https://github.com/user-attachments/assets/67ecea6c-ee7f-4e0f-8623-1489f67a739d)

![image](https://github.com/user-attachments/assets/1ce3d896-d4fa-4c6f-bfb2-0722c01284b4)

![image](https://github.com/user-attachments/assets/576009eb-2318-4489-bc17-8fde40d2c087)

Y comprobamos de que funcione:

![image](https://github.com/user-attachments/assets/43c3628f-ba7d-4967-b66f-2ffd28c39222)


# Docker. Práctica 5

Ejemplo 1: Nginx simple con Docker Compose

Crea una carpeta para el proyecto:

![image](https://github.com/user-attachments/assets/e51bdb55-f0f7-4ae8-a770-efe3f0fb9cfa)

Crea un archivo docker-compose.yml:

![image](https://github.com/user-attachments/assets/3e075e6e-5e3b-487d-a21e-8b1ea42c8652)

![image](https://github.com/user-attachments/assets/c947e6a0-1314-4483-9dba-5ec7dbaf667c)


Levanta el servicio:

![image](https://github.com/user-attachments/assets/f6bee487-7863-42ec-a06c-f4045514b7aa)

Y veriamos:

![image](https://github.com/user-attachments/assets/bc02b500-970d-4595-a720-c877e177fe61)

Ejemplo 2: Nginx sirviendo contenido propio (volumen)

Crea una carpeta para el proyecto y dentro otra carpeta para el contenido:

![image](https://github.com/user-attachments/assets/c46e33c1-7711-4c99-83a8-ceded730e1b3)

Crea el archivo index.html dentro de la carpeta html:

![image](https://github.com/user-attachments/assets/54e44de3-4f9a-4f8a-82db-95ed9829f069)

![image](https://github.com/user-attachments/assets/cb96eeb3-230d-4963-8941-a4a16ea719f9)

Creamos el archivo docker-compose.yml:

![image](https://github.com/user-attachments/assets/ac0a5c99-69b2-41d1-adb3-fddd354722d9)

![image](https://github.com/user-attachments/assets/e9d42eea-2585-4038-9cf6-829936ad788e)

Levanta el servicio:

![image](https://github.com/user-attachments/assets/ec8124e0-1582-4ec7-a0db-540bafc35bc0)

Y comprobamos:

![image](https://github.com/user-attachments/assets/afdcaf28-9db3-4052-bbe9-67aad2bfba56)

Ejemplo 3: Comunicación entre dos contenedores Alpine

![image](https://github.com/user-attachments/assets/300fdbe5-1b00-4cd7-893e-7ab8e9866d09)

Crea el archivo docker-compose.yml:

![image](https://github.com/user-attachments/assets/bf5020e2-115e-4a8c-bbef-562dbf9872ec)

![image](https://github.com/user-attachments/assets/f0611f7d-76fb-416c-8816-ef2a991cacc1)

Levanta los contenedores:

![image](https://github.com/user-attachments/assets/bba56935-5dbb-4581-8565-d6813348902a)

Comrpobamos:

![image](https://github.com/user-attachments/assets/cee03a26-b8c1-487d-928d-be0c387afc2d)

Haz ping de uno al otro para verificar comunicación:

![image](https://github.com/user-attachments/assets/f6937ccc-e51c-4690-b49d-7188aa886d55)

![image](https://github.com/user-attachments/assets/a7cedd16-bf3b-4475-8efe-ba4172c0cc5f)





