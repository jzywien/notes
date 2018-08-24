# Install
```
brew cask install minikube
```

# Minikube
## Install Hyperkit (MacOS)
https://github.com/kubernetes/minikube/blob/master/docs/drivers.md#hyperkit-driver

## Start minikube
```
minikube start --vm-driver=hyperkit
```

## Open minikube dashboard
```
minikube dashboard
```

## Open browser at service url & nodeport
```
minikube service NAME
```

## Enable ingress for minikube
```
minikube addons enable ingress
```

## Set vars needed to build docker images on Minikube VM host
```
eval $(minikube docker-env)
```

## Unset vars needed to build docker images on Minikube VM host
```
eval $(minikube docker-env -u)
```

## Stop the minikube VM
```
minikube stop
```

## Delete the minikube VM
```
minikube delete
```
