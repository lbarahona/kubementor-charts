# KubeMentor Helm Charts

Official Helm charts for [KubeMentor](https://kubementor.io) - AI-powered Kubernetes observability.

## Quick Install

```bash
# Add the repo
helm repo add kubementor https://charts.kubementor.io
helm repo update

# Install KubeMentor (all components)
helm install kubementor kubementor/kubementor \
  --namespace kubementor \
  --create-namespace

# Check status
kubectl get pods -n kubementor
```

## Available Charts

| Chart | Description |
|-------|-------------|
| `kubementor/kubementor` | All-in-one installation (recommended) |
| `kubementor/kubementor-agent` | Metrics collector agent |
| `kubementor/kubementor-api` | Backend API server |
| `kubementor/kubementor-dashboard` | Web dashboard |

## Configuration

See the [values.yaml](https://github.com/lbarahona/kubementor-platform/blob/master/helm/kubementor/values.yaml) for all options.

### Common Options

```bash
# Set cluster name
helm install kubementor kubementor/kubementor \
  --set global.clusterName="production" \
  -n kubementor --create-namespace

# Enable ingress
helm install kubementor kubementor/kubementor \
  --set dashboard.ingress.enabled=true \
  --set dashboard.ingress.hosts[0].host=kubementor.example.com \
  -n kubementor --create-namespace
```

## Documentation

- 📖 [Full Documentation](https://kubementor.io/docs)
- 🐛 [Report Issues](https://github.com/lbarahona/kubementor-platform/issues)

## License

Apache 2.0
