---
title: OS
menu:
  main:
    parent: Networking
    identifier: networking_os
---

OS level networking can be configured through the following options


## Devices

Devices represents the individual interfaces that can be configured on the host. It consists of of a list of interfaces and their respective configuration.


```yaml
networking:
os:
	devices:
	- interface: eth0
		cidr: <ip/mask>
		dhcp: bool
		routes:
			- network: <ip/mask>
				gateway: <ip>
```
