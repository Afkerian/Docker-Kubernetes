# Declarativos
Los enfoques declarativos en Kubernetes se centran en describir el estado deseado del sistema. Se utilizan principalmente archivos YAML o JSON que contienen la descripción de los recursos que se desean crear o modificar. Kubernetes se encarga de llevar el sistema al estado definido en estos archivos.

Ejemplo de un archivo YAML que describe un Pod:

```
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
spec:
  containers:
  - name: nginx-container
    image: nginx:latest
    ports:
    - containerPort: 80
```

