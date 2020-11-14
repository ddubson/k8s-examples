---
title: "Persistent Volumes"
date: 2020-11-14T16:41:49-05:00
draft: true
anchor: "persistent_volumes"
weight: 99
---

⚡️ **Action**: Create Persistent Volume

✨ **Effect**: A Persistent Volume created but not bound to any Pod, and have a lifetime past any Pod

```
kubectl create -f <persistent-volume-definition-yml>
```

[Sample Persistent Volume definition](https://github.com/ddubson/k8s-examples/blob/main/src/volumes/simple_persistent_volume_claim_definition.yml))