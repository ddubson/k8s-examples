# Kubernetes Cheatsheet

## Pods

Create a Pod in the default namespace via definition file.

```bash
kubectl create -f <definition-file-yml>
```

[Sample Pod definition](../src/1_simple_pod.yml)

Get all Pods

```bash
# List all pods in the default namespace
kubectl get pods

# With extra information
kubectl get pods -o wide

# List all pods in a specific namespace
kubectl get pods --namespace=<my-namespace>
```

Get logs of a Pod

```bash
kubectl logs <pod-name>
```

---

## Jobs

Create a Job from a Job definition file

✨ **Effect**: Job object created with appropriate Pods

```bash
kubectl create -f <job-definition-yml>
```

Get Jobs in the default namespace

```bash
kubectl get jobs
```

Delete a specific job by name 

✨ **Effect**: Deletes Job object; Deletes Pods that were created by the job

```bash
kubectl delete job <job-name>
```

## CronJobs

Create a CronJob from a CronJob definition file

✨ **Effect**: CronJob object created with appropriate Pods and a Schedule as to when it should execute

```bash
kubectl create -f <cronjob-definition-yml>
```

Get CronJobs in the default namespace

```bash
kubectl get cronjob
```

Delete a specific cronjob by name 

✨ **Effect**: Deletes CronJob object; Deletes Pods that were created by the cronjob

```bash
kubectl delete cronjob <cron-job-name>
```

