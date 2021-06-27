# Simple ReplicaSet

This ReplicaSet:

- defines the Pod definition inline in `template` section. Pod definitions
  need not necessarily be defined in a ReplicaSet definition.
- sets the selector on the labels of the inline Pod definition

```bash
# Create the replicaset
kubectl apply -f simple-replica-set.yml

# Get all replicasets
kubectl get replicasets -n default
kubectl get rs -n default # shorthand

# View all related pods created by ReplicaSet
kubectl get pods -n default

# Scaling replicas - change `replicas` field and run
kubectl replace -f simple-replica-set.yml

# Delete ReplicaSet
kubectl delete replicaset myapp-replicaset
kubectl delete rs myapp-replicaset
```
