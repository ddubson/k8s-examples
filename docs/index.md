## Kubernetes Cheatsheet

Create a Pod in the default namespace via definition file.

```bash
kubectl create -f <definition-file-yml>
```

[Sample Pod definition](../src/1_simple_pod.yml)

---

Get all Pods in the default namespace

```bash
# List all pods
kubectl get pods

# With extra information
kubectl get pods -o wide
```