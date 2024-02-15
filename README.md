# kubernetes-grafana
This repository deploys an Grafana instance in a kubernetes cluster.

## Installation
### 1. Create the Grafana namespace
```
kubectl apply -f grafana-namespace.yaml
```

### 2. Create the Grafana Artifacts
Create the Grafana PVC, Deployment and service with:
```
kubectl apply -f grafana-pvc.yaml
kubectl apply -f grafana-deployment.yaml
kubectl apply -f grafana-service.yaml
```

### 3. Access the UI
Once the deployment is ready, you can access to Grafana instance follwing your network configuration.

http://grafana.calfolguera.com:3000

You can use admin/admin as default credentials.

## GitOps
You can also deploy a Grafana instance through an ArgoCD application.
Use the example in: https://github.com/hfolguera/kubernetes-argocd/blob/main/applications/grafana-application.yaml

Clone or download the repo, update and deploy it:
```
wget https://raw.githubusercontent.com/hfolguera/kubernetes-argocd/main/applications/grafana-application.yaml
vim grafana-application.yaml
kubectl apply -f grafana-application.yaml
```

## References
Get the official documentation at https://grafana.com/docs/grafana/latest/installation/kubernetes/

## Next steps
* Configuration as code

## Known Issues
TODO
