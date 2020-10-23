---
title: "Services"
date: 2020-10-23T18:10:36-04:00
draft: true
anchor: "services"
weight: 5
---

Services allow binding a set of Pods together and act as a channel by which to access them. Another
name for a service could be: gateway.

There are four types of access methods:

- **ClusterIP (default)** - Exposes the Service on an internal IP in the cluster. 
  This type **makes the Service only reachable from within the cluster**.
- **NodePort** - Exposes the Service on the same port of each selected Node 
  in the cluster using NAT. **Makes a Service accessible** from outside the cluster 
  using `<NodeIP>:<NodePort>`. Superset of ClusterIP.
- **LoadBalancer** - Creates an external load balancer in the current cloud (if supported) 
  and **assigns a fixed, external IP to the Service**. Superset of NodePort.
- **ExternalName** - Exposes the Service using an arbitrary name (specified by externalName 
  in the spec) by returning a **CNAME record with the name**. No proxy is used. This type requires v1.7
  or higher of kube-dns.

⚡️ **Action**: Create a Service

✨ **Effect**: Service created and binds to specific Pods based on Selector matches.
 
```shell script
# Declarative way: via definition file
kubectl create -f <service-definition-yml>
```

[Sample NodePort Service definition](https://github.com/ddubson/k8s-examples/blob/main/src/4_simple_service_nodeport.yml)
[Sample ClusterIP Service definition](https://github.com/ddubson/k8s-examples/blob/main/src/5_simple_service_clusterip.yml)

⚡️ **Action**: Get Services

```shell script
kubectl get services

# With extra information
kubectl get services -o wide

# Get a specific ReplicaSet by name
kubectl get service <service-name>

# Get Services and flush its definition to a Services definition file
kubectl get service <service-name> -o yaml > services-definition.yaml
```

TODO: continue here

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