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

