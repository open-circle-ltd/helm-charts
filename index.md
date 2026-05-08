## Usage

```bash
helm repo add open-circle https://open-circle-ltd.github.io/helm-charts
helm repo update
```

## Charts

| Chart | Description |
|-------|-------------|
| rails-app-with-database | Generic Rails app with DB migrations |
| rails-app-without-database | Generic Rails app without database |
| retro-board | Retro Board (based on rails-app-with-database) |

### Install a chart

```bash
helm install my-app open-circle/rails-app-with-database -f values.yaml
```

### Search for available charts

```bash
helm search repo open-circle
```
