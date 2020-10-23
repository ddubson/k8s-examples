---
title: "Cron Jobs"
date: 2020-10-14T16:47:04-04:00
draft: false
anchor: "cron-jobs"
weight: 99
---

⚡️ **Action**: Create a CronJob from a CronJob definition file

✨ **Effect**: CronJob object created with appropriate Pods, and a Schedule as to when it should execute

```shell script
kubectl create -f <cronjob-definition-yml>
```

⚡️ **Action**: Get CronJobs in the default namespace

```shell script
kubectl get cronjob
```

⚡️ **Action**: Delete a specific cronjob by name 

✨ **Effect**: Deletes CronJob object; Deletes Pods that were created by the cronjob

```shell script
kubectl delete cronjob <cron-job-name>
```