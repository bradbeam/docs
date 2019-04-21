---
title: Boot
menu:
  main:
    parent: Install
---

Boot configuration exposes the following options to configure the boot device/partition.

## Kernel

This parameter can be used to specify a custom kernel to use. If this parameter is omitted, the most recent Talos release will be used.

```yaml
install:
  boot:
    kernel: <path or url to vmlinuz>
```

## Initramfs

This parameter can be used to specify a custom initramfs to use. If this parameter is omitted, the most recent Talos release will be used.

```yaml
install:
  boot:
    initramfs: <path or url to rootfs.tar.gz>
```

## Device

```yaml
install:
  boot:
    device: <name of device to use>
```

## Size

```yaml
install:
  boot:
    size: <size in bytes>
```
