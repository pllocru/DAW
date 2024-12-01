## Instalacion del servidor web Apache
# Instalar Apache

![1](https://github.com/user-attachments/assets/201432ba-9037-4cb0-b1f1-8cb8344bf19d)

![2](https://github.com/user-attachments/assets/1faf8439-a0e4-4087-a2cc-38b11a9f865c)

# Editar el archivo hosts

![2 5](https://github.com/user-attachments/assets/14f9b9fc-34e9-4463-9162-22884c42b545)

![3](https://github.com/user-attachments/assets/17744b30-0710-4077-996e-a6c847c983fa)

# Configurar Apache para los dos dominios

Crear archivos de configuración para los dominios:

    centro.intranet (WordPress):

sudo nano /etc/apache2/sites-available/centro.intranet.conf

Contenido del archivo:

<VirtualHost *:80>
    ServerName centro.intranet
    DocumentRoot /var/www/centro.intranet
    <Directory /var/www/centro.intranet>
        AllowOverride All
    </Directory>
</VirtualHost>

departamentos.centro.intranet (Python):

sudo nano /etc/apache2/sites-available/departamentos.centro.intranet.conf

Contenido del archivo:

    <VirtualHost *:80>
        ServerName departamentos.centro.intranet
        DocumentRoot /var/www/departamentos.centro.intranet
        WSGIScriptAlias / /var/www/departamentos.centro.intranet/app.wsgi
        <Directory /var/www/departamentos.centro.intranet>
            Require all granted
        </Directory>
    </VirtualHost>

Habilitar los sitios:

sudo a2ensite centro.intranet.conf
sudo a2ensite departamentos.centro.intranet.conf
sudo systemctl reload apache2


## Activar los módulos necesarios para ejecutar php y acceder a mysql

Habilitar módulos necesarios:

sudo a2enmod php
sudo a2enmod rewrite

Reiniciar Apache:

sudo systemctl restart apache2

Instalar dependencias:

sudo apt install php libapache2-mod-php php-mysql mysql-server

Configurar base de datos MySQL:

sudo mysql
CREATE DATABASE wordpress;
CREATE USER 'wpuser'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON wordpress.* TO 'wpuser'@'localhost';
FLUSH PRIVILEGES;
exit;


    
