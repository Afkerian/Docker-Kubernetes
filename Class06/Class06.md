# Docker Register

docker build -t [afkerian/test:v1]    Construir la Imagen

docker push [afkerian/test:v1]        Emoujar/Subir la imagen a Docker Desktop

docker rmi [afkerian/test:v1]       Eliminamos la imagen de Docker Hub

docker pull [afkerian/test:v2]      Nos bajamos la imagen de docker hub


# Kubernetes

KUBECTL es parecido a docker

kubectl cluster-info    Verifica la Instalacion

kubectl config current-context  No indica el contexto actual 

kubectl config get-contexts     Listar los contextos

kubectl config use-context [Context Name]  Cambiar de Contexto

kubectl config rename-context [Old Name] [New Name]     Renombrar un Contexto

kubectl config delete-context [Context Name]    Eliminar Contexto

# Kubernetes - Declarativo e Imperativo


## Imperativa

kubectl create deploy [Deploy Name] --image=nginx 

## Declarativa

kubectl create -f deploy-text.yaml 

# Namespace

Servidor de Desarrollo, Servidor de QA/Pruebas, Produccion

Saparar los recursos de Kubernetes en direfentes entonrnos, como:
    - Desarrollo
    - Pruebas
    - Produccion

kubectl get ns       Lista los namespaces

---
apiVersion: v1
kind: Namespaces
metadata:
    name: develop
---

---
apiVersion: v1
kind: Namespaces
metadata:
    name: develop
spec:
    containers:
    - name: nginx-server
    - iamge: nginx
---

# Comandos Namespaces

kubectl get namespace    Lista todos los namespaces
kubectl get ns      Vistaso de los espacios de memoria
kubectl config set-context --currentt --namespace=[Name Space]
kubectl create ns [Namespace Name]
kubectl delete ns [Namespace Name]
kubectl get pods --all-namespaces   Listamos todos los pods en todos los namespaces
