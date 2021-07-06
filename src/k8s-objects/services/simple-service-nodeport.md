# Simple NodePort Service

NodePort services allow a user to reach the hosted Pods within a Deployment, connected by proper ports
and selectors

```bash
# Create Service and accompanying Deployment
kubectl apply -f simple-service-nodeport.yml

# Check if pods of deployment are available via service (externally available)
curl -X GET $(minikube service --url myapp-service)

# Delete service
kubectl delete service myapp-service
kubectl delete deployment.apps myapp-deployment
```
