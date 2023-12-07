# Installation Step 
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm repo update

helm install prometheus prometheus-community/kube-prometheus-stack

## Show Values 
helm show values prometheus-community/kube-prometheus-stack

## Show Prometheus Pids 
kubectl --namespace default get pods -l "release=prometheus"

# The service providing Connectivity : prometheus-kube-prometheus-prometheus
change it to NodePort 

or :  kubectl port-forward prometheus-prometheus-kube-prometheus-prometheus-0 9090
