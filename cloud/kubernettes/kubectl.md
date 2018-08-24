
# Kubectl
```
kubectl describe pods|services|deployments|ingress
```

## Create kube objects using yaml file
```
kubectl create -f CONFIG.yaml
```

## Update item using config yaml file
```
kubectl apply -f CONFIG.yaml
```

## Create a Deployment that manages a Pod based on docker image
```
kubectl run DEPLOYMENTNAME --image=IMAGENAME:VERSION --port=8080
```

## Update the image for a deployment
```
kubectl set image deployment DEPLOYMENTNAME api=api:v3 --record
```

## Create Secrets file based on output from ./update-tls.sh
```
kubectl create secret generic tls-certs --from-file=tls/
```

## Create Docker Hub registry secret
```
kubectl create secret docker-registry dockerhubreg --docker-username=USERNAME --docker-password=PASSWORD --docker-email=EMAIL
```

## Create configmap used
```
kubectl create configmap nginx-frontend-conf --from-file=fontend.conf
```

## Update configmap with File
```
kubectl create configmap nginx-frontend-conf --from-file=nginx/frontend.conf --dry-run -o yaml | kubectl replace -f -
```

## Forward port traffic from kube cluster to localhost
```
kubectl port-forward PODNAME LOCALPORT:PODPORT
```