# Docker

Los contenedores de docker que solo tienen un nobre son oficiales y se mantienen por docker.

El dockerfile es la definición de la maquina.

## Comandos
`docker ps` -> Lista los comandos que hay en ejecución.
`docker ps -a` -> Lista los comandos que hay en ejecución y parados.
`docker stop <nombreDelContenedor>` -> Para el docker
`docker exec -it <nombreDelContenedor> /bin/sh` -> Para conectarnos al docker
`docker run -name <nombreDeLaMaquina> -d -p80:80 -v $(pwd):ruta <nombreDelContenedor>`
`docker run <nombre del contenedor>` -> Inicia el contenedor.
`docker pull <nombre del contendro>` -> Descarga la imagen de un contenedor el contenedor (como una class de programación).
`docker imges` -> Lista todas la imagienes que hay
`docker rm` -> Lista los contenedores que se han levantado
`docker rm <nombreDelContenedor>` -> Elimina el contenero.
`docker rmi <nombreDeLaImagen>` -> Elimina la imagen, no elimina la imagen si hay intancias de la misma se podria forzar con `--force`



Redireccionar puertos
`-p 80:80` -> El primero representa el anfitrión y el segundo al virtualizado
`-v $(pwd):/usr/src/app \ ` -> Ruta anfitrion : ruta virtual (No se pueden poner puntos)
`-e MAIN_APP_FILE=my-app.rb \` -> Redefinir las variables de entorno o poner nuevas
`-d erikap/ruby-sinatra` -> Nombre de la imagen

`curl localhost:puerto/pagina`

## Dockerfile

FROM ruby:2.3

MAINTAINER Erika Pauwels <erika.pauwels@gmail.com>

ENV RACK_ENV production   ## 	ENV -> Variable de entorno.
ENV MAIN_APP_FILE web.rb

RUN mkdir -p /usr/src/app ## RUN -> Ejecuta un comando.

ADD startup.sh /

WORKDIR /usr/src/app ## WORKDIR -> El directorio sobre el que se trabaja.

EXPOSE 80   ## EXPOSE 80

CMD ["/bin/bash", "/startup.sh"]  ## CMD ejecua un programa?