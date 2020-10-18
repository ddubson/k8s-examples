---
title: "Ingress"
date: 2020-10-18T16:38:44-04:00
draft: false
anchor: "ingress"
weight: 99
---

⚡️ **Action**: Get all Ingress resource

```shell script
# Get ingress from default namespace
kubectl get ingress

# Get ingress from all namespaces
kubectl get ingress --all-namespaces
```

⚡️ **Action**: Update an existing Ingress resource

✨ **Effect**: Replaces an existing Ingress resource

```shell script
# After modifying an existing ingress definition, run
kubectl replace -f ingress-definition.yml

# If any additional entries are needed to be added, use edit
kubectl edit ingress <ingress-name>
```