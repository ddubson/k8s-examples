---
title: "Minikube"
date: 2020-10-14T18:39:00-04:00
draft: false
anchor: "minikube"
weight: 99
---

## Install on MacOS

```shell script
brew install kubectl
brew cask install virtualbox
brew install minikube
minikube start --driver=virtualbox
minikube status
# ...
minikube stop
```

https://kubernetes.io/docs/tasks/tools/install-minikube/

### Accessing a service

To find the Service URL in your cluster, run:

```shell script
minikube service --url <service-name>
```