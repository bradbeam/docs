---
title: OS
menu:
  main:
    parent: Security
---

OS Security consists primarily of a CA certificate and key pair and is configured through the following:

## CA
```yaml
security:
  os:
    ca:
      crt: <base64 encoded x509 pem certificate>
      key: <base64 encoded x509 pem certificate key>
```

## Identity
```yaml
security:
  os:
    identity:
      crt: <base64 encoded x509 pem certificate>
      key: <base64 encoded x509 pem certificate key>
```
