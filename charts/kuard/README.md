## kuard Helm Chart

This chart deploys the KUAR demo application (kuard).

### Installing the Chart

```bash
helm install kuard ./charts/kuard \
  --set image.repository=gcr.io/kuar-demo/kuard-amd64 \
  --set image.tag=blue
```

### Upgrading the Chart

```bash
helm upgrade kuard ./charts/kuard --reuse-values
```

### Uninstalling the Chart

```bash
helm uninstall kuard
```

### Configuration

See `values.yaml` for the full list of configurable values. Common options:

- `service.type` (ClusterIP|NodePort|LoadBalancer)
- `ingress.enabled`, `ingress.className`, `ingress.hosts`
- `replicaCount`, `resources`
- `args` for passing kuard flags like `--debug`, `--address=:8080`

