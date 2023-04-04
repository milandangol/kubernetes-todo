# kubernetes-todoapp

First of all huge thanks to ![Train With Shubham](https://github.com/LondheShubham153/django-todo-cicd) for making this amazing app on python. Where i could use my kubernetes knowledge to it.

## Docker image.
If you are lazy like me and don't want to build your image and push it to docker hub and then again use it for kubenetes. Then worry not I have already pushed a docker image to my docker hub where you can use following code to pull it.

```bash
docker pull akamanishh/todoapp:v1
```
Okay i get it you are not lazy as i am so use following command to build your own image and push it to docker hub.

```bash
docker build -t <docker-hub-id>/todoapp:v1
docker push <docker-hub-id>/todoapp:v1
```
## Kubernetes Pod Deployments 
Use following command to deploy a pod.
```bash
kubectl apply -f pod.yaml
```
## Kubernetes Deployments
```bash
kubectl apply -f deploy.yaml
```
## Kubernetes Service
```bash
kubectl apply -f service.yaml
```
# Let's access our application from outside minikube cluster
```bash
minikube service --url todo-service 
```