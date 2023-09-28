# Trabajando con Volúmenes

#### El primer paso es, crear un repositorio con el nombre `Trabajando_Volumenes` y cambiamos la rama de **master** a **main**. 

## 1. Descargamos la imagen de `httpd`
Para desargar la imágen de `httpd` usaremos el comando.

    docker pull htttpd:2.4
![imagen1](https://github.com/cristianmoreiraa/Trabajando_Volumenes/blob/main/img/image-3.png)

Y para comprobar si se ha instalado correctamente:

    docker images
![imagen2](https://github.com/cristianmoreiraa/Trabajando_Volumenes/blob/main/img/image-4.png)

## 2. Creamos contenedor `dam_web1`

Para este segundo paso debemos:

    docker run --name dam_web1 -d  httpd:2.4

    [name] ---> nos permite darle el nombre que queremos al contenedor

![imagen3](https://github.com/cristianmoreiraa/Trabajando_Volumenes/blob/main/img/image-5.png)

En la imágen anterior trás poner el comando se nos crea el contenedor y podremos comprobar que se ha creado correctamente mediante el comando `docker ps`

![imagen4](https://github.com/cristianmoreiraa/Trabajando_Volumenes/blob/main/img/image-6.png)

## 3. ¿Cómo acceder desde el navegador?

Es tan sencillo como escribir nuestra `ip` en nuestro navegador

    localhost: *puerto donde lo tengamos mapeado*

Antes de eso necisitaremos saber la `IP` de nuestro equipo.

## 4. Utilizar bind mount para que el directorio `htdocs` se sitúe en el directorio elegido

Una vez borrado el contenedor creado anteriormente, utilizaremos el siguiente comando:

`docker run --name dam_web1 -p 8000:80 -v C:\Users\crist\Documents\2DAM\SXE\Trabajando_con_volumenes\htdocs:/usr/local/apache2/htdocs httpd:2.4`

Ya hemos vinculado el directorio, además ya hemos mapeado los puertos añadiendo la variable `-p` **puertoMaquina:puertoContenedor**.

Y para poder ver si ha funcionado debemos escribir en el buscador:

    localhost:8000

Si se ha creado de manera correcta nos deberá aparecer:

![imagen6](https://github.com/cristianmoreiraa/Trabajando_Volumenes/blob/main/img/image.png)


