# Spring Boot + minikube + fabric8
[![Build Status](https://travis-ci.org/vivekwpatil/springboot-minikube-fabric8.svg?branch=master)](https://travis-ci.org/vivekwpatil/springboot-minikube-fabric8)

## Install minikube locally

https://kubernetes.io/es/docs/tasks/tools/install-minikube/

### Windows10
If you are using chocolatey. Install minikube with following command
```
choco install docker-desktop
choco install minikube
minikube start
```

### OSX
```
brew install minikube
minikube start
```

## Kubernates tutorials
https://kubernetes.io/es/docs/tutorials/kubernetes-basics/create-cluster/cluster-interactive/

##How  to create docker image of the application

```
#mvn fabric8:build
```

##create the kubernets and openshift deplyment scripts
```
mvn fabric8:resource
```

##deploy application
```
mvn fabric8:deploy
```

##check pods
```
kubectl get pods
kubectl get svc
```
##check application url
```
minikube ip
kubectl get svc
CLUSTER= $(minikube ip)
curl $CLUSTER:31764/api/hello/Vivek
```
##Reference:
- https://github.com/fabric8io/fabric8-maven-plugin



