# Insomnius Kubernetes Template

## Metallb

Install metallb for loadbalancing kubernetes to host, make sure you have an IP for it to export.

### 1. Installing metallb native

Apply the native configuration

```
kubectl apply -f https://raw.githubusercontent.com/insomnius/k0s-templating/master/metallb/native.yaml
```

Apply pool config, change the IP address based on your available IPs.

```
kubectl apply -f https://raw.githubusercontent.com/insomnius/k0s-templating/master/metallb/metallb-l2pool-production.yaml -e
```