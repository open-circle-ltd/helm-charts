# Helm Charts

Helm chart repository for OpenCircle, published via GitHub Pages.

## Charts

| Chart | Description |
|-------|-------------|
| [rails-app-with-database](charts/rails-app-with-database) | Generic Rails app with DB migrations and optional Sidekiq worker |
| [rails-app-without-database](charts/rails-app-without-database) | Generic Rails app without database |
| [retro-board](charts/retro-board) | Retro Board (based on rails-app-with-database) |

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
