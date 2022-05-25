# Prometheus-K8s-Cluster-Setup-Helm
This repository contains the steps to setup a Prometheus cluster setup using Helm Charts. Easy and straightforward to make it.


# Pre-Requiste
You should have a clean minikube/ docker-desktop kubernetes cluster ready.
Helm Should also be installed. For installation links, check here -> https://helm.sh/docs/intro/install/

# Commands to run 

"helm repo add prometheus-community https://prometheus-community.github.io/helm-charts"

"helm repo update"

"helm install prometheus prometheus-community/kube-prometheus-stack"

### This would have installed all the services and deployments required to have prometheus in your cluster.
To Verify this, just run "kubectl get all "

# We can know more information about the deployment by parsing the details in a yaml file like the below commands:

"kubectl get statefulset"
"kubectl describe statefulset prometheus-prometheus-kube-prometheus-prometheus > prom.yaml"
"kubectl describe deployment prometheus-kube-prometheus-operator> operator.yaml"



