---
title: Trustd
menu:
  main:
    parent: Services
---

Trustd can be configured through the following

## Username

The username/password fields define the auth info for trustd. The values defined here will be the credentials trustd will use.
```yaml
services:
  trustd:
    username: trusty
```

## Password

The username/password fields define the auth info for trustd. The values defined here will be the credentials trustd will use.
```yaml
services:
  trustd:
    password: mypass
```

## Endpoints

The endpoints denote the other trustd instances
```yaml
services:
  trustd:
    endpoints:
      - endpoint
```

## CertSANs
```yaml
services:
  trustd:
    certSANs:
      - san
```

## BootstrapNode
```yaml
services:
  trustd:
    bootstrapNode: nodename
```

## Environment Variables
```yaml
services:
  trustd:
    env:
      <string>: <string>
```

# Example Configuration

```yaml
services:
  trustd:
    username: '99_ASDe6qXULQ_fR0-%r'
    password: 'h[9hjnjkj0u4J094@YB$#Zsz'
    endpoints:
      - 10.2.3.5
      - 10.2.3.6
    certSANs:
      - 10.2.3.4
```
