# Docker Compose

El archivo de configuración de Docker Compose tiene la extensión `.yaml`.

## Comandos de Docker Compose

- `docker-compose build`: Construye las imágenes.
- `docker-compose start`: Inicia los contenedores.
- `docker-compose stop`: Detiene el contenedor.
- `docker-compose up -d`: Construye e inicia los contenedores en modo daemon.
- `docker-compose ps`: Lista los contenedores en ejecución.
- `docker-compose rm`: Elimina los contenedores detenidos.
- `docker-compose down`: Detiene y elimina los contenedores.
- `docker-compose logs`: Obtiene los registros/logs.
- `docker-compose exec [Nombre del Contenedor] bash`: Ingresa al contenedor para ejecutar comandos.

## Comandos Avanzados de Docker Compose

---

### Gestión de Proyectos

- `docker-compose up -d`: Inicia el proyecto la primera vez.
- `docker-compose -p [nombre instancia] up -d`: Inicia un proyecto con un nombre de instancia específico.

---

- `docker-compose ls`: Lista los proyectos en ejecución.
- `docker-compose cp [ID del Contenedor]:[RUTA_ORIGEN] [DESTINO]`: Copia archivos desde el contenedor al host.
- `docker-compose cp [RUTA_ORIGEN] [ID del Contenedor]:[DESTINO]`: Copia archivos desde el host al contenedor.

## Políticas de Reinicio

- `no`: No se reinicia el contenedor.
- `always`: El contenedor se reinicia siempre que se detenga.
- `on-failure`: El contenedor se reinicia solo si se produce un error o una salida inesperada.
- `unless-stopped`: Reinicia el contenedor a menos que se detenga manualmente.

