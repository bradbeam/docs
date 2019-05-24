---
title: init
menu:
  main:
    parent: components
    weight: 20
---

A common theme throughout the design of Talos is minimalism.
We believe strongly in the UNIX philosophy that each program should do one job well.
The `init` included in Talos is one example of this.

We wanted to create a focused `init` that had one job - run Kubernetes. To that extent, `init` is relatively static in that it does not allow for arbitrary user defined services. Only the services necessary to run Kubernetes and manage the node are available. This includes:

- [containerd](/components/containerd)
- [kubeadm](/components/kubeadm)
- kubelet
- [networkd](/components/networkd)
- [ntpd](/components/ntpd)
- [osd](/components/osd)
- [proxyd](/components/proxyd)
- [trustd](/components/trustd)
- udevd
