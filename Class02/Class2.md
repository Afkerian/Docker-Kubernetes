# Guía de Comandos Básicos de Docker

Ccomandos básicos para trabajar con Docker:

## Descargar Imágenes de Docker Hub

```bash
docker pull [Nombre de la Imagen]
```

## Correr un Contenedor

```bash
docker run [Nombre de la Imagen]
```

## Correr un Contenedor en Segundo Plano

```bash
docker run -d [Nombre de la Imagen]
```

## Iniciar un Contenedor Pausado

```bash
docker start [Nombre del Contenedor]
```

## Listar Contenedores en Ejecución

```bash
docker ps
```

## Listar Todos los Contenedores

```bash
docker ps -a
```

## Detener un Contenedor

```bash
docker stop [Nombre del Contenedor]
```

## Eliminar un Contenedor

```bash
docker rm [Nombre del Contenedor]
```

## Eliminar un Contenedor Forzosamente

```bash
docker kill [Nombre del Contenedor]
```

## Inspeccionar Especificaciones de una Imagen

```bash
docker image inspect [Nombre de la Imagen]
```

## Límites de Recursos en Docker

### Limitar la Memoria

```bash
docker run --memory="128m" [Nombre de la Imagen]
```

### Limitar el Uso de CPUs

```bash
docker run --cpus="0.6" [Nombre de la Imagen]
```

# Ejercicio 1: Crear un Servidor Web

```bash
docker run --publish 80:80 --name webserver nginx
```

Para verificar que el servidor se está ejecutando:

```bash
docker ps
```

Para detener y eliminar el contenedor:

```bash
docker stop webserver
docker rm webserver
```

# Vincular una Terminal a un Contenedor

Para acceder a la terminal de un contenedor en ejecución:

```bash
docker run -it nginx /bin/bash
```

Para acceder a una terminal PowerShell en un contenedor en ejecución:

```bash
docker run -it microsoft/powershell:nanoserver
```

Para vincular una terminal a un contenedor en ejecución:

```bash
docker container exec -it [Nombre del Contenedor] bash
```

Recuerda reemplazar `[Nombre de la Imagen]` y `[Nombre del Contenedor]` con los valores correspondientes según tu caso.