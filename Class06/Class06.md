# Docker Register

Para gestionar imágenes de contenedores, Docker ofrece una serie de comandos útiles. Aquí tienes una guía básica para trabajar con Docker Registry:

- **Construir la imagen**:

```sh
docker build -t afkerian/test:v1 .
```
Este comando construye una imagen con la etiqueta `afkerian/test:v1` utilizando el Dockerfile presente en el directorio actual (`.`).

- **Subir la imagen a Docker Hub**:

```sh
docker push afkerian/test:v1
```
Este comando sube la imagen `afkerian/test:v1` al registro de Docker Hub.

- **Eliminar una imagen de Docker Hub**:

```sh
docker rmi afkerian/test:v1
```
Este comando elimina la imagen `afkerian/test:v1` del registro de Docker Hub.

- **Descargar una imagen desde Docker Hub**:

```sh
docker pull afkerian/test:v2
```
Este comando descarga la imagen `afkerian/test:v2` desde el registro de Docker Hub.

# Kubernetes

Kubernetes (K8s) es una herramienta poderosa para la gestión de contenedores. A continuación, algunos comandos útiles para administrar clusters de Kubernetes:

- **Verificar la instalación**:

```sh
kubectl cluster-info
```
Este comando muestra información sobre el clúster de Kubernetes, como la dirección del servidor API y el estado de los nodos.

- **Ver el contexto actual**:

```sh
kubectl config current-context
```
Este comando muestra el contexto actual de Kubernetes que se está utilizando.

- **Listar los contextos disponibles**:

```sh
kubectl config get-contexts
```
Este comando lista todos los contextos de Kubernetes configurados en tu sistema.

- **Cambiar de contexto**:

```sh
kubectl config use-context [Nombre del Contexto]
```
Este comando cambia al contexto especificado de Kubernetes.

- **Renombrar un contexto**:

```sh
kubectl config rename-context [Nombre Antiguo] [Nombre Nuevo]
```
Este comando permite renombrar un contexto de Kubernetes.

- **Eliminar un contexto**:

```sh
kubectl config delete-context [Nombre del Contexto]
```
Este comando elimina un contexto de Kubernetes.

# Kubernetes - Declarativo e Imperativo

En Kubernetes, hay dos enfoques principales para trabajar con recursos: declarativo e imperativo.

- **Imperativo**:

```sh
kubectl create deployment [Nombre del Despliegue] --image=nginx
```
Este comando crea un despliegue con el nombre especificado, utilizando la imagen de NGINX.

- **Declarativo**:

```sh
kubectl apply -f deploy-text.yaml
```
Este comando aplica la configuración definida en el archivo `deploy-text.yaml`, lo que puede incluir la creación o actualización de recursos en Kubernetes.

# Namespace

Los namespaces en Kubernetes permiten organizar y separar recursos en diferentes entornos, como desarrollo, pruebas y producción.

- **Listar los namespaces**:

```sh
kubectl get namespaces
```
Este comando muestra todos los namespaces en el clúster de Kubernetes.

- **Crear un nuevo namespace**:

```sh
kubectl create namespace [Nombre del Namespace]
```
Este comando crea un nuevo namespace en el clúster de Kubernetes.

- **Eliminar un namespace**:

```sh
kubectl delete namespace [Nombre del Namespace]
```
Este comando elimina un namespace y todos sus recursos del clúster de Kubernetes.

- **Ver todos los pods en todos los namespaces**:

```sh
kubectl get pods --all-namespaces
```
Este comando muestra todos los pods en todos los namespaces del clúster de Kubernetes.

