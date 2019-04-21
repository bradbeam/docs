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

## CertificateKey

The certificate key is used for something

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
