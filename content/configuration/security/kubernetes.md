---
title: Kubernetes
menu:
  main:
    parent: Security
    identifier: security_kubernetes
---

Kubernetes Security consists primarily of a CA certificate and key pair and is configured through the following:

## CA
```yaml
security:
  kubernetes:
    ca:
      crt: <base64 encoded x509 pem certificate>
      key: <base64 encoded x509 pem certificate key>
```
