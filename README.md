# Kubernetes-deployment-strategy
In this repository we will work on k8s deployment strategy.

## Blue-Green Deployemnt

### Steps for blue green deployment POC

Follow the commands

1. minikube start
2. kubectl apply -f Blue-green/
3. kubectl port-forward service/my-nginx 80:80
4. browse localhost in local browser

### How to switch to other deployment

1. Stop port-forwarding
2. change service.yml file
    a. Replace selector `run: my-nginx` to `runblue: my-nginx-1`
3. kubectl apply -f Blue-green/    
4. kubectl port-forward service/my-nginx 80:80
5. browse localhost in local browser
