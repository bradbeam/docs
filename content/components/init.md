---
title: "init"
date: 2018-10-29T19:40:55-07:00
draft: false
weight: 20
menu:
  main:
    parent: 'components'
    weight: 20
---

A common theme throughout the design of Talos is minimalism.
We believe strongly in the UNIX philosophy that each program should do one job well.
The `init` included in Talos is one example of this.

We wanted to create a focused `init` that had one job - run Kubernetes. To that extent, `init` is relatively static in that it does not allow for arbitrary user defined services. Only the services necessary to run Kubernetes and manage the node are available.
There simply is no mechanism in place to do anything else.
