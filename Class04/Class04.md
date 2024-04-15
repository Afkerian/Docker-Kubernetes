# Docker Volume y Contenedores

## Creación de Volumen y Operaciones Básicas

- `docker volume create vol01`: Crea un volumen llamado "vol01".
- `docker volume ls`: Lista todos los volúmenes disponibles.
- `docker run -d --name testvol -v vol01:/app nginx:latest`: Ejecuta un contenedor con el nombre "testvol" y monta el volumen "vol01" en el directorio "/app" utilizando la imagen de nginx más reciente.

## Interactuando con el Contenedor

- `docker exec -it testvol bash`: Ingresa al contenedor "testvol" para ejecutar comandos.
- `apt-get update`: Actualiza los paquetes del sistema dentro del contenedor.
- `apt-get install neofetch`: Instala la herramienta de visualización de información del sistema, neofetch.
- `neofetch`: Muestra información detallada del sistema en el contenedor.
- `apt-get install nano`: Instala el editor de texto nano dentro del contenedor.
- `ls`: Lista el contenido del directorio actual.
- `cd app`: Cambia al directorio "app".
- `pwd`: Muestra la ruta completa del directorio actual.
- `nano integrantes.txt`: Abre el archivo "integrantes.txt" en el editor de texto nano para su edición.
- `cat integrantes.txt`: Muestra el contenido del archivo "integrantes.txt".

## Operaciones de Docker Volumes

- `docker volume create [nombre_del_volumen]`: Crea un nuevo volumen con el nombre especificado.
- `docker volume ls`: Lista todos los volúmenes disponibles en el sistema.

## Contenido del Archivo "integrantes.txt"

```plaintext
# 12-04-2024

KEVIN

ISAAC

EDITH

RIKI

KEVIN

VICTOR

```

---
```
docker volume create vol01

docker volume ls

docker run -d --name testvol -v vol01:/app nginx:latest
ef585deb23a076bc495dd2113338f41722db645a762bf83a3e081f92819d3414

docker exc -it testvol bash

root@ef585deb23a0:/# apt-get update

root@ef585deb23a0:/# apt-get install neofetch

root@ef585deb23a0:/# neofetch

root@ef585deb23a0:/# neofetch 
       _,met$$$$$gg.          root@ef585deb23a0 
    ,g$$$$$$$$$$$$$$$P.       ----------------- 
  ,g$$P"     """Y$$.".        OS: Debian GNU/Linux 12 (bookworm) on Windows 10 x86_64 
 ,$$P'              `$$$.     Kernel: 5.15.133.1-microsoft-standard-WSL2 
',$$P       ,ggs.     `$$b:   Uptime: 22 mins 
`d$$'     ,$P"'   .    $$$    Packages: 261 (dpkg) 
 $$P      d$'     ,    $$P    Shell: bash 5.2.15 
 $$:      $$.   -    ,d$$'    CPU: Intel i7-10510U (8) @ 2.304GHz 
 $$;      Y$b._   _,d$P'      GPU: ec69:00:00.0 Microsoft Corporation Basic Render Driver 
 Y$$.    `.`"Y$$$$P"'         Memory: 1358MiB / 7843MiB 
 `$$b      "-.__
  `Y$$                                                
   `Y$$.                                              
     `$$b.
       `Y$$b.
          `"Y$b._
              `"""

root@ef585deb23a0:/# apt-get install nano

root@ef585deb23a0:/# neofetch 
root@ef585deb23a0:/# ls
app  boot  docker-entrypoint.d   etc   lib    media  opt   root  sbin  sys  usr
bin  dev   docker-entrypoint.sh  home  lib64  mnt    proc  run   srv   tmp  var
root@ef585deb23a0:/# cd app
root@ef585deb23a0:/app# pwd
/app
root@ef585deb23a0:/app# nano integrantes.txt
root@ef585deb23a0:/app# cat integrantes.txt 
# 12-04-2024

kEVIN

ISAAC

EDITH

RIKI

KEVIN

VICTOR
root@ef585deb23a0:/app# exit

```