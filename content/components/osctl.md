---
title: "osctl"
date: 2018-10-29T19:40:55-07:00
draft: false
weight: 70
menu:
  main:
    parent: 'components'
    weight: 70
---

The `osctl` CLI is the client to the [osd](/components/osd) service running on every node. `osctl` should provide enough functionality to be a replacement for typical interactive shell operations. With it you can do things like:

- retrieve container logs
- restart a service
- reset a node
- reboot a node
- retrieve kernel logs
- generate pki resources
- inject data into node configuration files
- view running services
- view node resources
