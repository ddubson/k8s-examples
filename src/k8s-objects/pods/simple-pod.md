# Using simple-pod.yml

> You can omit `-n` namespace flags if you have the namespace set already. Examples are verbose for demo purposes

> 
```bash
# Deploy POD to cluster (`default` namespace)
kubectl apply -n default -f simple-pod.yml

# See all pods in default namespace
kubectl get pods -n default

# Get myapp-pod info
kubectl describe pod myapp-pod -n default
kubectl desc p myapp-pod -n default 

# Dump running pod's configuration to yml
kubectl get pod myapp-pod -o yaml -n default > myapp-pod.yml

# Delete pod
kubectl delete pod myapp-pod

# Edit running pod
kubectl edit pod myapp-pod
```
