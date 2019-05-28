---
title: Production
menu:
  main:
    parent: started
---

## Generate configuration

When considering Talos for production usage, the best way to get started is by using the `osctl config generate`.

Talos requires 3 static IPs, one for each of the master nodes. After allocating these addresses, you can generate the necessary configs with the following commands:

```bash
osctl config generate <cluster name> <master-1 ip,master-2 ip, master-3 ip>
```

This will generate 5 files - `master-{1,2,3}.yaml`, `worker.yaml`, and `talosconfig`. The master and worker config files contain just enough config to bootstrap your cluster, and be further customized as necessary. These config files should be supplied as machine userdata or some internally accessible url so they can be downloaded during machine bootup.

## Cluster interaction

After the machines have booted up, you'll want to manage your talos config file. The default location the `osctl` tool looks for configuration is under `~/.talos/config`. The location can also be specified at runtime via `osctl --talosconfig myconfigfile`. Next, we'll need to generate the kubeconfig for our cluster. This can be achieved via `osctl kubeconfig` command.

## Finalizing Kubernetes Setup

Once your machines boot up, you will want to apply a Pod Security Policy (PSP). There is a basic example that can be used found at `hack/dev/manifests/psp.yaml` or you can create your own. Following this, you'll want to apply a CNI plugin. You'll want to take note of the kubeadm `networking.podsubnet` parameter and ensure the network range matches up.
