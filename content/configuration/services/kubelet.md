---
title: kubelet
menu:
  main:
    parent: Services
---

The kubelet can be configured through the following

## Env

```yaml
services:
  kubelet:
    env:
      key: value
      ...
```

## ExtraMounts

```yaml
services:
  kubelet:
    extraMounts:
      - < opencontainers/runtime-spec/mounts >
```
