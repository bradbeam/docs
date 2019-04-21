---
title: Init
menu:
  main:
    parent: Services
---

The init process exposes the following configuration options: `cni`.

## CNI

Talos currently supports the following CNI providers:

- flannel
- calico

## Config
```yaml
services:
  init:
    cni: [flannel|calico]
```

