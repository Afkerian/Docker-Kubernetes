# Actividad de Docker: Configuración de Backend, Frontend y Base de Datos

En esta actividad, configuraremos un entorno de desarrollo Docker para una aplicación web que consta de un backend Flask en Python, un frontend estático y una base de datos MongoDB. Utilizaremos Docker Compose para orquestar los contenedores y asegurarnos de que se comuniquen correctamente.

## Instrucciones:

### 1. Preparación del proyecto:

- Clona el repositorio del proyecto desde GitHub: [enlace al repositorio](https://github.com/tu_usuario/repo_docker).
- Asegúrate de tener instalado Docker y Docker Compose en tu máquina.

### 2. Configuración del backend Flask:

- Abre el archivo `backend/app.py`.
- Implementa la lógica necesaria para tu backend Flask. Puedes comenzar con una aplicación mínima que responda "Hello, World!" en la ruta raíz `/`.
- Define las dependencias de Python en un archivo `requirements.txt`.

### 3. Configuración del frontend estático:

- Prepara tu aplicación web estática en el directorio `frontend`. Puedes usar HTML, CSS y JavaScript para esto.
- Asegúrate de tener un archivo `index.html` que sirva como punto de entrada para tu frontend.

### 4. Configuración de la base de datos:

- Utilizaremos MongoDB como base de datos para esta aplicación.
- Asegúrate de que tu backend Flask esté configurado para conectarse a una instancia de MongoDB. Puedes configurar la conexión a través de variables de entorno en tu aplicación Flask.

### 5. Configuración de Docker:

- Crea un Dockerfile para el backend Flask en el directorio `backend`.
- Crea un Dockerfile para el frontend estático en el directorio `frontend`.
- Define un archivo `docker-compose.yml` en el directorio raíz del proyecto que orqueste los contenedores para el backend, frontend y la base de datos MongoDB.

### 6. Construcción y ejecución de los contenedores:

- Ejecuta `docker-compose up` en el directorio raíz del proyecto para construir y ejecutar los contenedores.
- Verifica que tu aplicación esté funcionando correctamente accediendo a `http://localhost` en tu navegador web.

### 7. Pruebas y ajustes:

- Realiza pruebas para asegurarte de que el backend, el frontend y la base de datos se comuniquen correctamente.
- Haz los ajustes necesarios en los archivos Dockerfile y docker-compose.yml según sea necesario para solucionar cualquier problema.

### 8. Envío de la actividad:

- Sube tu código a tu repositorio GitHub.
- Envía el enlace al repositorio junto con cualquier instrucción adicional o comentario relevante.

## Recursos adicionales:

- [Documentación de Docker](https://docs.docker.com/)
- [Documentación de Docker Compose](https://docs.docker.com/compose/)
- [Flask Documentation](https://flask.palletsprojects.com/en/2.1.x/)
- [Documentación de MongoDB](https://docs.mongodb.com/)
