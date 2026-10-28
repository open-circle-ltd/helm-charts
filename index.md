## Usage

```bash
helm repo add open-circle https://open-circle-ltd.github.io/helm-charts
helm repo update
```

## Charts

| Chart | Description | Latest version |
|-------|-------------|----------------|
| [meta-control](https://github.com/open-circle-ltd/helm-charts/tree/main/charts/meta-control) | Meta-Control (based on rails-app-with-database) | 0.1.3 |
| [metric-screen](https://github.com/open-circle-ltd/helm-charts/tree/main/charts/metric-screen) | Metric-screen (based on ruby-app-without-database) | 0.1.6 |
| [rails-app-with-database](https://github.com/open-circle-ltd/helm-charts/tree/main/charts/rails-app-with-database) | A Helm chart for a generic Rails app with DB migrations | 0.2.1 |
| [rails-app-without-database](https://github.com/open-circle-ltd/helm-charts/tree/main/charts/rails-app-without-database) | A Helm chart for a generic Rails app without database | 0.2.2 |
| [retro-board](https://github.com/open-circle-ltd/helm-charts/tree/main/charts/retro-board) | Retro Board (based on rails-app-with-database) | 0.3.3 |
| [ruby-app-without-database](https://github.com/open-circle-ltd/helm-charts/tree/main/charts/ruby-app-without-database) | A Helm chart for a generic Ruby app without database | 0.1.1 |

### Install a chart

```bash
helm install my-app open-circle/rails-app-with-database -f values.yaml
```

### Search for available charts

```bash
helm search repo open-circle
```
