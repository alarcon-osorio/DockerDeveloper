## DockerDeveloper

**_Docker Projects_**

https://hub.docker.com/

**_Docker Commands_**

##Pasos para instalar Docker en Linux Ubuntu 

Instalar docker en Ubuntu 18.04

1. Primero, actualice su lista existente de paquetes:

sudo apt update

2. Ahora instalamos algunos paquetes de requisitos previos que permitan a apt usar paquetes a través de HTTPS:

sudo apt install apt-transport-https ca-certificates curl software-properties-common

3. Agregamos la clave GPG para el repositorio oficial de Docker a su sistema:

curl -fsSL https://download.docker.com/linux/ubuntu/pgp | sudo apt-key add -

4. Agregue el repositorio de Docker a las fuentes de APT:

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"

5. Actualizamos la base de datos de paquetes con los paquetes de Docker del repositorio recién agregado:

sudo apt update

5. Revisar que Docker este listo para ser instalado en Ubuntu 18.04 asi:

apt-cache policy docker-ce

6. Instalamos docker asi:

sudo apt install docker-ce

7. Ahora Docker debe estar instalado y para comprobar que esta corriendo ejecutamos este comando:

sudo systemctl status docker
#

##Docker Inicios

1. Crear un contenedor de Ubuntu -- Descargar la imagen 

1.1. sudo search docker search ubuntu

1.2. sudo docker pull ubuntu

2. Arrancar la imagen descargada

sudo docker run -it ubuntu

3. Ver imagenes disponibles

sudo docker images

4. Arrancar la imagen 

sudo docker run hello-world

5. Contenedores que se han creado

1.1. sudo docker ps   //Lista contenedores arriba

1.2. sudo docker ps -a   //Lista todos los contenedores

6. Borrar imagen 

sudo docker rmi images 3ee81f9b1670

Donde

3ee81f9b1670 : Es el id de la imagen

7. Detener con Contenedor

sudo docker stop 438a832dbc7b

Donde

438a832dbc7b :es el id de nuestro contenedor.

8. Iniciar Contenedor

sudo docker start 438a832dbc7b

9. Acceder a Contenedor 

sudo docker attach 438a832dbc7b

10. Eliminar Contenedero 

sudo docker rm 438a832dbc7b

## Clonar Contenedores y subirlos a repositorio HUB DOCKER 

1. Clonado 

sudo docker commit -m "Cambios dentro de la imagen" -a "autor-jeison" 438a832dbc7b alarcon777/ubuntu-mysql

Donde:

"Cambios dentro de la imagen" Nombre del cambio.

"autor-jeison" Nombre del autor.

438a832dbc7b Id del contenedor a guardar en la imagen.

alarcon777 Nombre de usuario (de http://hub.docker.com).

ubuntu-mysql Nombre de la imagen.

2. Verificar la imagen 

sudo docker images

3. Crear contenedor apartir de la imagen commitiada 

sudo docker run -it alarcon777/ubuntu-mysql

4. Subir imagen a Hub Docker

sudo docker login -u alarcon777

Donde:

alarcon777 :es en nombre de usuario con el que nos registramos previamente.

5. Subir imagen 

sudo docker push alarcon777/ubuntu-mysql

Donde:

alarcon777 es en nombre de usuario con el que nos registramos previamente.

ubuntu-mysql nombre de la imagen que creamos previamente.
