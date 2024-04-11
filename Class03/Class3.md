# Clean Containers

docker rm [Container Name]      Remueve el contenedor 

dcoker rm $(docker ps -a -q)    Remueve todos los contenedores detenidos

docker images   Lista las imagenes

docker rmi [Image Name]     Elimina la imagen

docker system prune -a      Remueve todas las imagenes que no estan en uso por ningun contenedor

# Contruir un Contenedor 

Archivo Dockerfile

docker build -t [name:tag] .        Construir en el directorio actual que contiene Dockerfile
docker build -t [name:tag] -f [File Name]   Construir el contenedor con el Dockerfile en otro folder/directorio

Que es un Dockerfile = Es receta para construir una imagen!

# Dockerfile

FROM nginx:alpine  Imagen Base

COPY . /usr/share/nginx/html Copiar de la maquina local al contenedor 

# Dockerfile 2

