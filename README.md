# Trabajando con Volúmenes

#### El primer paso es, crear un repositorio con el nombre `Trabajando_Volumenes` y cambiamos la rama de **master** a **main**. 

## 1. Descargamos la imagen de `httpd`
Para desargar la imágen de `httpd` usaremos el comando.

    docker pull htttpd:2.4
![imagen1](image-3.png)

Y para comprobar si se ha instalado correctamente:

    docker images
![imagen2](image-4.png)

## 2. Creamos contenedor `dam_web1`

Para este segundo paso debemos:

    docker run --name dam_web1 -d  httpd:2.4

    [name] ---> nos permite darle el nombre que queremos al contenedor

![imagen3](image-5.png)

En la imágen anterior trás poner el comando se nos crea el contenedor y podremos comprobar que se ha creado correctamente mediante el comando `docker ps`

![imagen5](image-6.png)