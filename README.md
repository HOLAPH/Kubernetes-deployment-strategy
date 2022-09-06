# Kubernetes-deployment-strategy
In this repository we will work on k8s deployment strategy.

## Blue-Green Deployemnt

### Steps for blue green deployment POC

Follow the commands

* minikube start
* kubectl apply -f Blue-green/
* kubectl port-forward service/my-nginx 80:80
* browse localhost in local browser

### How to switch to other deployment

* Stop port-forwarding
* change service.yml file
  * Replace selector `run: my-nginx` to `runblue: my-nginx-1`
* kubectl apply -f Blue-green/    
* kubectl port-forward service/my-nginx 80:80
* browse localhost in local browser
