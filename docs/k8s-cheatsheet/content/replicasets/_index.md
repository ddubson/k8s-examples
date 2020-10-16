---
title: "ReplicaSets"
date: 2020-10-15T12:05:23-04:00
draft: false
anchor: "replicasets"
weight: 2
---

⚡️ **Action**: Create a ReplicaSet

✨ **Effect**: ReplicaSet created with defined number of Pods (based on `replicas` field)
 
```shell script
# Declaritive way: via definition file
kubectl create -f <replicaset-definition-yml>
```

[Sample ReplicaSet definition](https://github.com/ddubson/k8s-examples/blob/main/src/2_simple_replica_set.yml)

⚡️ **Action**: Get ReplicaSets

```shell script
kubectl get replicasets

# With extra information
kubectl get replicasets -o wide

# Get a specific ReplicaSet by name
kubectl get replicaset <replica-set-name>
```

⚡️ **Action**: Update/Scale ReplicaSet

✨ **Effect**: Updates an existing ReplicaSet based on new definition. Potentially scales up or down based on change the
Pods within the ReplicaSet

```shell script
# Replace via updated definition file
kubectl replace -f <replica-set-definition-yml>

# Scale manually without modifying definition file
kubectl scale --replicas=<num-of-replicas> -f <replica-set-definition-yml>

# Scale manually by replica set name
kubectl scale --replicas=<num-of-replicas> replicaset <replica-set-name>
```

⚡️ **Action**: Delete a ReplicaSet

✨ **Effect**: Deletes the ReplicaSet and destroys any Pods controlled by the ReplicaSet

```bash
kubectl delete replicaset <replica-set-name>
```