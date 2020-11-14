# k8s-examples

[k8s command cheatsheet](https://hopeful-nightingale-b34dd8.netlify.app/)

## Sample definitions

### Pods

1. [Simple POD definition](src/pods/simple_pod.yml)
1. [Pod with attached Persistent Volume Claim](src/pods/pod_with_pvc.yml)

### ReplicaSets

1. [Simple ReplicaSet definition](./src/2_simple_replica_set.yml)

### Deployments

1. [Simple Deployment definition](./src/3_simple_deployment.yml)

### Services

1. [Simple Service definition - NodePort](./src/4_simple_service_nodeport.yml)
1. [Simple Service definition - ClusterIP](./src/5_simple_service_clusterip.yml)

### Jobs / CronJobs

1. [Simple Job definition](./src/x_job_definition.yml)
1. [Multiple-Pod Job definition](./src/x_job_definition_multiple_pods.yml)
1. [Parallel Multiple-Pod Job definition](./src/x_job_definition_multiple_pods_parallel.yml)
1. [Simple CronJob definition](./src/x_cronjob_definition.yml)

### Network Policies

1  [Network Policy - Ingress definition](./src/x_network_policy.yml)

### Persistent Volumes & Claims

1. [Simple Persistent Volume definition](./src/volumes/simple_persistent_volume_definition.yml)
1. [Simple Persistent Volume Claim definition](./src/volumes/simple_persistent_volume_claim_definition.yml)
