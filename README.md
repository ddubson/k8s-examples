# k8s-examples

[k8s command cheatsheet](https://hopeful-nightingale-b34dd8.netlify.app/)

## Sample definitions

### Pods

1. [Simple POD definition](src/k8s-objects/pods/simple-pod.yml) - [README](./src/k8s-objects/pods/simple-pod.md)
1. [Pod with attached Persistent Volume Claim](src/k8s-objects/pods/pod-with-persistent-volume-claim.yml)
1. [Pod with plain key-value env vars](src/k8s-objects/pods/pod-with-plain-env-vars.yml)
1. [Pod with resource requests](src/k8s-objects/pods/pod-with-resource-requests.yml)

### ReplicaSets

1. [Simple ReplicaSet definition](src/k8s-objects/replica-sets/simple-replica-set.yml) - [README](./src/k8s-objects/replica-sets/simple-replica-set.md)

### Deployments

1. [Simple Deployment definition](src/k8s-objects/deployments/simple-deployment.yml) - [README](./src/k8s-objects/deployments/simple-deployment.md)

### Services

1. [Simple Service definition - NodePort](./src/k8s-objects/services/simple-service-nodeport.yml) - [README](./src/k8s-objects/services/simple-service-nodeport.md)
1. [Simple Service definition - ClusterIP](./src/k8s-objects/services/simple-service-clusterip.yml)

### ConfigMaps

1. [Simple ConfigMap](./src/k8s-objects/config-maps/simple-configmap.yml)
1. [ConfigMap injected into a Pod](./src/k8s-objects/config-maps/configmap-inject-into-pod.yml)

### Secrets

1. [Simple Secret](./src/k8s-objects/secrets/simple-secret.yml)
1. [Secret injected into a Pod](./src/k8s-objects/secrets/secret-inject-into-pod.yml)

### Jobs

1. [Simple Job definition](./src/k8s-objects/jobs/job-definition.yml)
1. [Multiple-Pod Job definition](./src/k8s-objects/jobs/job-definition-multipod.yml)
1. [Parallel Multiple-Pod Job definition](./src/k8s-objects/jobs/job-definition-multipod-parallel.yml)
   
### CronJobs

1. [Simple CronJob definition](./src/k8s-objects/cronjobs/cronjob-definition.yml)

### Network Policies

1  [Network Policy - Ingress definition](src/k8s-networking/simple-network-policy.yml)

### Persistent Volumes & Claims

1. [Simple Persistent Volume definition](./src/k8s-objects/volumes/simple-persistent-volume-definition.yml)
1. [Simple Persistent Volume Claim definition](./src/k8s-objects/volumes/simple-persistent-volume-claim-definition.yml)

