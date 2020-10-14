---
title: "Pods"
date: 2020-10-14T16:35:39-04:00
draft: false
weight: 1
anchor: "pods"
---

⚡️ **Action**: Create a Pod in the default namespace via definition file.

```bash
kubectl create -f <definition-file-yml>
```

[Sample Pod definition](../src/1_simple_pod.yml)

⚡️ **Action**: Get all Pods

```bash
# List all pods in the default namespace
kubectl get pods

# With extra information
kubectl get pods -o wide

# List all pods in a specific namespace
kubectl get pods --namespace=<my-namespace>
```

⚡️ **Action**: Get logs of a Pod

```bash
kubectl logs <pod-name>
```