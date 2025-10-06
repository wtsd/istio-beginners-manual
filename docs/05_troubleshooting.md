# Troubleshooting

| Problem | Cause | Solution |
|----------|--------|-----------|
| No traffic reaching service | Gateway misconfiguration | Check `host` and `selector` in Gateway |
| Pods not part of mesh | Sidecar not injected | Check namespace label `istio-injection=enabled` |
| Access denied | Authorization policy too strict | Adjust rules or disable policy temporarily |
| Connection timeout | mTLS conflict | Ensure both sides have same mTLS mode |


Useful commands:
```bash
istioctl proxy-status
istioctl analyze
kubectl get virtualservices
kubectl get gateways
kubectl get destinationrules
```

