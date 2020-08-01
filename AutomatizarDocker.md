## Proceso de automatizacion de Docker

1. Opcional: Crear carpeta DockerWeb

2. Crear arcchivo Dockerfile
#

**_3. Contenido archivo Dockerfile:**_

FROM ubuntu:latest

MAINTAINER JEISON alarcon_osorio@hotmail.com

RUN apt-get update && apt-get install -y tzdata

RUN apt-get -y install apache2

expose 80

CMD /usr/sbin/apache2ctl -D FOREGROUND

Donde:

ubuntu:latest :  Sistema operativo donde se van a montar los programas

JEISON Alarcon_osorio@hotmail.com : Nombre y correo de la persona que creo el contenedor

RUN apt-get update : Aplicaciones a instalar y/o actualizar

tzdata: Instalar zona horaria

expose 80 : Puerto que va a quedar abierto 

CMD /usr/sbin/apache2ctl -D FOREGROUND : Ejecutar en la terminal como Demonio.
#

4. Tener presente la ruta relativa donde se creo el archivo

5. Ejecutar contenido del Dockerfile 

sudo docker build -t web **_ruta_relativa_**

Donde:

web : Nombre que se le asignara a la nueva imagen que crearemos.

**_ruta_relativa_** : Path donde esta nuestro Dockerfile previamente creado.

6. Comprobar Imagen 

sudo docker images

7. Crear contenedor y ejecutar los servicios instalados

sudo docker run -d -p 8085:80 web

Donde:

-d : Corre el contenedor en background.

-p 8085:80 : Lee el puerto 80 del contenedor y lo corre en el puerto 8085 de la maquina anfitrion.

web : Nombre de la imagen a correr.

