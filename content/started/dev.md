---
title: Local
menu:
  main:
    parent: started
---

The quickest way to get started with Talos is to test out the local docker setup. This uses docker compose to bring up a 3 master, 1 worker node environment.

## Bring up the Docker Environment

```bash
osctl cluster create
```

Startup times can vary, but it typically takes ~45s-1min for the environment to be available.

## Apply PSP and CNI

Once the environment is available, the pod security policies will need to be applied to allow the control plane to come up. Following that, the default CNI (flannel) configuration will be applied.

```bash
osctl kubeconfig | sed -e 's/10.5.0.2:/127.0.0.1:6/' > kubeconfig
kubectl --kubeconfig ./kubeconfig apply -f hack/dev/manifests/psp.yaml
kubectl --kubeconfig ./kubeconfig apply -f hack/dev/manifests/flannel.yaml
```

## Interact with the environment

Once the environment is available, you should be able to make use of `osctl` and `kubectl` commands.
You can view the current running containers via `osctl ps` and `osctl ps -k`. You can view logs of running containers via `osctl logs <container>` or `osctl logs -k <container>`
