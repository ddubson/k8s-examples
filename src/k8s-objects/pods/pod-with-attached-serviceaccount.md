# A Pod with a Service Account attached

To create a service account, run:

```bash
kubectl create serviceaccount simple-service-account  
```

OR

```bash
kubectl apply -f src/k8s-objects/service-accounts/simple-service-account.yml
```

THEN:

```bash
kubectl apply -f src/k8s-objects/pods/pod-with-attached-serviceaccount.yml
```
