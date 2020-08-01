## DockerDeveloper

**_Docker Projects_**

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
