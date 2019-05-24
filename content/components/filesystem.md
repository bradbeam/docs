---
title: "filesystem"
date: 2018-10-30T09:16:35-07:00
draft: false
weight: 80
menu:
  main:
    parent: 'components'
    weight: 80
---

Talos comes with a reserved block device with three partitions:

- `ESP` partition ( EFI System Partition )
- `ROOT-A` partition mounted as read-only that contains the minimal set of binaries to operate system services
- `ROOT-B` partition mounted as read-only that contains the minimal set of binaries to operate system services
- `DATA` partion that is mounted as read/write at `/var/run`

In AWS and GCE the `ESP` and `ROOT` partitions are static and cannot be modified. The `DATA` partition is automatically resized ( extended ) by `init` on boot to the maximum device size.

When an upgrade is performed, `ROOT-A` and `ROOT-B` will swap roles as the active partition.

In Bare Metal setups, these partition sizes an be defined under the `install` section of the userdata.
