---
title: "Jobs"
date: 2020-10-14T16:35:39-04:00
draft: false
anchor: "jobs"
weight: 2
---

⚡️ **Action**: Create a Job from a Job definition file

✨ **Effect**: Job object created with appropriate Pods

```bash
kubectl create -f <job-definition-yml>
```

⚡️ **Action**: Get Jobs in the default namespace

```bash
kubectl get jobs
```

⚡️ **Action**: Delete a specific job by name 

✨ **Effect**: Deletes Job object; Deletes Pods that were created by the job

```bash
kubectl delete job <job-name>
```