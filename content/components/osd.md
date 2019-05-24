---
title: osd
menu:
  main:
    parent: components
---

Talos is unique in that it has no concept of host-level access.
There is no ssh daemon.
There is no interactive console session.
There are no shells installed.
Only what is required to run Kubernetes.
Furthermore, there is no way to run any custom processes on the host level.

To make this work, we needed an out-of-band tool for managing the nodes.
In an ideal world, the system would be self-healing and we would never have to touch it.
But, in the real world, this does not happen.
We still need a way to handle operational scenarios that may arise.

The `osd` daemon provides a way to do just that.
Based on the Principle of Least Privilege, `osd` provides operational value for cluster administrators by providing an API for node management.

Interactions with `osd` are handled via [osctl](/components/osctl) which communicates via gRPC.
