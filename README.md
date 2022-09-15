# Assignment 1 

1. Do a Blue/Green deployment with your nginx image which was done
2. When accessing the blue pod , it should say hello blue ( the index.html ) page
3. When accessing the green pod, it should say hello green 

# Assignment 2 

1. Do a canary deployment
2. version 1 is serving traffic then deploy version 2
3. create a new "canary" ingress with traffic splitting enabled
4. wait enought time to confirm that version 2 is stable and not throwing unexpected errors
5. delete the canary ingress
6. point the main application

---
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

## Canary Deployment

*Work still progress*
