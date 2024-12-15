## Actividad AWS

Usando una instancia AWS debemos instalar Apache con las siguientes opciones de configuración:

# Creamos una instancia:

Esta la generamos con amazon, y añadimos todo por defecto,el par de claves vockey.pem,
y añadir los puertos ssh, http y https. 

![instancia amazon](https://github.com/user-attachments/assets/8ab5d64b-5781-4e88-9c46-0e751deab552)

Una vez le demos a crear instancia nos saldra en la consola esto:

![consola](https://github.com/user-attachments/assets/88cdff40-941c-41e7-ab3a-8c5fa8381d84)

Y le daremos a conectar.Una vez dentro nos saldrá algo parecido a:

![dentro](https://github.com/user-attachments/assets/b07bce6b-196a-4259-a5fe-ebd84076e4ff)

Si nos sale esto,lo hemos hecho bien,ahora vamos a instalar apache.

# Instalamos Apache

Antes de instalar nada,actualizamos el sistema:

![actualizamos](https://github.com/user-attachments/assets/4eaf539b-c889-40f1-b0f0-90d1db068c1f)

Una vez actualizado,ahora si,lo instalamos:

![instalamos](https://github.com/user-attachments/assets/cfc90205-e0f4-49a4-863d-aeba1ab8f852)

Y lo inicamos:

![startyenabled](https://github.com/user-attachments/assets/c37acb5f-e440-4fcb-ab66-6476cf424b53)

Y comporbamos que funciona:

![funciona apache](https://github.com/user-attachments/assets/7013a9a4-5dbb-4c64-a2c1-e5a17721fe88)


# Activar la autenticación con MySql 

![instalamos mysql](https://github.com/user-attachments/assets/65f54809-3913-4d6e-9634-2c25a807b81c)

Y instalamos el mod_authn_mod para la autenticación:





