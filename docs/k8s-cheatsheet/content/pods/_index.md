---
title: "Pods"
date: 2020-10-14T16:35:39-04:00
draft: false
weight: 1
anchor: "pods"
---

⚡️ **Action**: Create a Pod in the default namespace. (`k8s v1.19`)

```shell script
# Imperative way: via arguments
kubectl run nginx --image=<docker-image> --labels='<key=value>' --generator=run-pod/v1

# Imperative way: via arguments, simulating creation (dry run), and output a manifest
kubectl run <pod-name> --image=<docker-image> --dry-run -o yaml

# Declarative way: via definition file
kubectl create -f <definition-file-yml>
```

[Sample Pod definition](https://github.com/ddubson/k8s-examples/blob/main/src/1_simple_pod.yml)

⚡️ **Action**: Get all Pods

```shell script
# List all pods in the default namespace
kubectl get pods

# With extra information
kubectl get pods -o wide

# List all pods in a specific namespace
kubectl get pods --namespace=<my-namespace>
```

⚡️ **Action**: Get information on a specific pod

```shell script
# Get short info on a Pod
kubectl get pod <pod-name>

# Get pod information and write it to a pod definition file
kubectl get pod <pod-name> -o yaml > pod-definition.yaml

# Get detailed info on a Pod
kubectl describe pod <pod-name>
```

⚡️ **Action**: Get logs of a Pod

```shell script
kubectl logs <pod-name>
```

⚡️ **Action**: Delete a Pod

✨ **Effect**: Completely removes a specific Pod from the cluster

```shell script
kubectl delete pod <pod-name>
```