---
title: kubeadm
menu:
  main:
    parent: Services
    identifier: services_kubeadm
---

The following options are exposed for configuring kubeadm:

## Configuration

The configuration section contains the various kubeadm configs as a yaml block of yaml configs.

```yaml
services:
  kubeadm:
    configuration: |
      apiVersion: kubeadm.k8s.io/v1beta1
      kind: InitConfiguration
      ...
      ---
      apiVersion: kubeadm.k8s.io/v1beta1
      kind: ClusterConfiguration
      ...
      ---
      apiVersion: kubelet.config.k8s.io/v1beta1
      kind: KubeletConfiguration
      ...
      ---
      apiVersion: kubeproxy.config.k8s.io/v1alpha1
      kind: KubeProxyConfiguration
      ...
```

## ExtraArgs

The extraargs section contains an additional list of arguments that can be passed into kubeadm.

```yaml
services:
  kubeadm:
    extraArgs:
      - some arg
      - some arg
      ...
```

## InitToken

The inittoken should only be provided for one of the master node configuration files. Presence of this token and validity ( token generation time is less than 1 hour old ) denote that this node should bootstrap the Kubernetes cluster. This token is a UUIDv1 token and can be generated via `osctl gen token`.

```yaml
services:
  kubeadm:
    initToken: d4171920-80f1-11e9-aeb1-acde48001122
```

## IgnorePreflightErrors

The ignorepreflighterrors section allows you to specify a list of preflight errors to ignore.

```yaml
services:
  kubeadm:
    ignorePreflightErrors:
      - Swap
      - SystemVerification
      ...
```
