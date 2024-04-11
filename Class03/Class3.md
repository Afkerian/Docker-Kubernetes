
# Clean Container

Descripción | Comando
--- | ---
Remueve el contenedor especificado. | `docker rm [Nombre del Contenedor]`
Remueve todos los contenedores detenidos. | `docker rm $(docker ps -a -q)`
Lista todas las imágenes. | `docker images`
Elimina la imagen especificada. | `docker rmi [Nombre de la Imagen]`
Remueve todas las imágenes que no están en uso por ningún contenedor. | `docker system prune -a`

# Construir un Contenedor

Para construir un contenedor, necesitas un archivo Dockerfile. Este archivo es esencialmente una receta para construir una imagen de Docker.

Descripción | Comando
--- | ---
Construye la imagen utilizando el Dockerfile en el directorio actual. | `docker build -t [nombre:etiqueta] .`
Construye la imagen utilizando el Dockerfile especificado en otro directorio. | `docker build -t [nombre:etiqueta] -f [Nombre del Archivo]`

# Dockerfile

Un Dockerfile es un archivo de texto que contiene una serie de instrucciones que Docker utiliza para construir una imagen.

Ejemplo:

```Dockerfile
FROM nginx:alpine  # Define la imagen base.
COPY . /usr/share/nginx/html  # Copia los archivos desde la máquina local al contenedor.
```

# Dockerfile 2

Aquí hay otro ejemplo de un Dockerfile más complejo que incluye la instalación de Node.js y npm, y la exposición de un puerto.

```Dockerfile
FROM alpine

RUN apk add -update nodejs nodejs-npm
COPY . /src
WORKDIR /src
RUN npm install
EXPOSE 80
ENTRYPOINT ["node", "./app.js"]
```

# Volúmenes

Los volúmenes en Docker son directorios montados desde el sistema host en un contenedor, lo que permite persistencia de datos.

Descripción | Comando
--- | ---
Crea un nuevo volumen. | `docker volume create [Nombre del Volumen]`
Lista todos los volúmenes. | `docker volume ls`
Proporciona información detallada sobre un volumen. | `docker volume inspect [Nombre del Volumen]`
Elimina el volumen especificado. | `docker volume rm [Nombre del Volumen]`
Elimina los volúmenes que no están montados o en uso por ningún contenedor. | `docker volume prune`


