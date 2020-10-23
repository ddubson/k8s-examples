---
title: "Deployments"
date: 2020-10-16T18:46:11-04:00
draft: false
anchor: "deployments"
weight: 4
---

⚡️ **Action**: Create a Deployment

✨ **Effect**: Creates a new Deployment; auto-creates a managed ReplicaSet with N number of Pods based on `replicas` number.

```shell script
# Declarative way: via definition file
kubectl create -f <deployment-definition-yml>

# Generate a Deployment definition from dry run create
kubectl create deployment <deployment-name> --image=<docker-image> --replicas=<num-of-replicas> --dry-run=client -o yaml
# ...but also write it to a file
kubectl create deployment <deployment-name> \
  --image=<docker-image> --replicas=<num-of-replicas> --dry-run=client -o yaml > deployment-definition.yml
```

[Sample Deployment definition](https://github.com/ddubson/k8s-examples/blob/main/src/3_simple_deployment.yml)

⚡️ **Action**: Get Deployment by name

```shell script
kubectl get deployment <deployment-name>

# Get deployment with extra information
kubectl get deployment -o wide

# Export a deployment's configuration to deployment-definition.yml
kubectl get deployment -o yaml > deployment-definition.yml
```

⚡️ **Action**: Get all Deployments

```shell script
# Get all deployments in default namespace
kubectl get deployments

# Get all deployments with extra information
kubectl get deployments -o wide

# Get all deployments in specific namespace
kubectl get deployments -n <namespace-name>
```

⚡️ **Action**: Update a Deployment

✨ **Effect**: An existing deployment is replaced with a new Deployment based on configuration

```shell script
# Declarative way: via definition file
kubectl replace -f deployment-definition.yml

# Imperative way: via command line params
kubectl create deployment <deployment-name> --image=<docker-image>
# ...create a base deployment definition file
kubectl create deployment <deployment-name> --image=<docker-image> --dry-run=client -o yaml > deployment-definition.yml

# Imperative way: scaling a deployment (affects ReplicaSet associated)
kubectl scale deployment <deployment-name> --replicas=<number-of-replicas>
```

⚡️ **Action**: Delete a Deployment

✨ **Effect**: removes Deployment; removes ReplicaSets associated with Deployment; removes Pods associated with ReplicaSet;

```shell script
kubectl delete deployment <deployment-name>
```