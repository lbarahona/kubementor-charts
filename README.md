# KubeMentor Helm Charts

Official Helm charts for [KubeMentor](https://kubementor.io) - AI-powered Kubernetes observability.

## Usage

```bash
# Add the repo
helm repo add kubementor https://charts.kubementor.io
helm repo update

# Install KubeMentor (all components)
helm install kubementor kubementor/kubementor \
  --namespace kubementor \
  --create-namespace

# Or install individual components
helm install kubementor-agent kubementor/kubementor-agent -n kubementor
helm install kubementor-api kubementor/kubementor-api -n kubementor
helm install kubementor-dashboard kubementor/kubementor-dashboard -n kubementor
```

## Available Charts

| Chart | Description |
|-------|-------------|
| `kubementor` | All-in-one installation (recommended) |
| `kubementor-agent` | Metrics collector agent |
| `kubementor-api` | Backend API server |
| `kubementor-dashboard` | Web dashboard |

## Configuration

See the [values.yaml](https://github.com/lbarahona/kubementor-platform/blob/master/helm/kubementor/values.yaml) for configuration options.

## Documentation

- 📖 [Full Documentation](https://kubementor.io/docs)
- 🐛 [Report Issues](https://github.com/lbarahona/kubementor-platform/issues)

## License

Apache 2.0
