# Simple Deployment

```bash
# Create new deployment
kubectl apply -f simple-deployment.yml -n default

# See all deployments
kubectl get deployments

# Delete deployments
kubectl delete deployment.apps myapp-deployment
```
