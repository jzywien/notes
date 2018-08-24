# Install
Download the latest Istio release from https://github.com/istio/istio/releases and Extract

## Install Istio to k8s
This is the unsecured demo where intra-service communication does not use TLS
```
kubectl apply -f ./kubernetes/istio-demo.yaml
```

Label the default namespace so that it uses the sidecar injection by default
```
kubectl label namespace default istio-injection=enabled
```