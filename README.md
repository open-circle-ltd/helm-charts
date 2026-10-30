# Helm Charts

Helm chart repository for OpenCircle, published via GitHub Pages.

## Charts

| Chart | Description |
|-------|-------------|
| [rails-app-with-database](charts/rails-app-with-database) | Generic Rails app with DB migrations and optional Sidekiq worker |
| [rails-app-without-database](charts/rails-app-without-database) | Generic Rails app without database |
| [ruby-app-without-database](charts/ruby-app-without-database) | Generic Ruby app without database |
| [retro-board](charts/retro-board) | Retro Board (based on rails-app-with-database) |
| [meta-control](charts/meta-control) | Meta Control (based on rails-app-with-database) |
| [ops-planner](charts/ops-planner) | Ops-Planner (based on rails-app-with-database) |
| [metric-screen](charts/metric-screen) | Metric Screen (based on ruby-app-without-database) |
| [mattermost-pi](charts/mattermost-pi) | Mattermost PI (based on rails-app-with-database) |
| [data-visualizer](charts/data-visualizer) | Data Visualizer (based on rails-app-without-database) |

## Usage

```bash
helm repo add open-circle https://open-circle-ltd.github.io/helm-charts
helm repo update
```

Install a chart:

```bash
helm install my-app open-circle/rails-app-with-database -f values.yaml
```

## Releasing

Charts are automatically packaged and published when changes are pushed to `main`. The [chart-releaser-action](https://github.com/helm/chart-releaser-action) handles packaging, creating GitHub releases, and updating the `gh-pages` branch that serves as the Helm repository index.

To release a new version of a chart, bump the `version` in its `Chart.yaml` and merge to `main`.
