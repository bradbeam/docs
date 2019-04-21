---
title: Root
menu:
  main:
    parent: Install
---

Root configuration exposes the following options to configure the root device/partition.

## Rootfs

This parameter can be used to specify a custom root filesystem to use. If this parameter is omitted, the most recent Talos release will be used.

```yaml
install:
  root:
    rootfs: <path or url to rootfs.tar.gz>
```

## Device

```yaml
install:
  root:
    device: <name of device to use>
```

## Size

```yaml
install:
  root:
    size: <size in bytes>
```

