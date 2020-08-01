FROM ubuntu:latest
MAINTAINER JEISON alarcon_osorio@hotmail.com
RUN apt-get update && apt-get install -y tzdata
RUN apt-get -y install apache2
expose 80
CMD /usr/sbin/apache2ctl -D FOREGROUND
