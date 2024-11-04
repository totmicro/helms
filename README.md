# TOT MICRO Helm Charts

Welcome to the TOTMICRO Helm repository, offering Helm charts to easily deploy and manage NetBird and its dashboard in your Kubernetes environment.

## How to Use

To use these Helm charts, you will first need to add this repository to Helm.

### Add Helm Repository

Run the following command to add this Helm repository:

```bash
helm repo add totmicro https://totmicro.github.io/helms
```

### Installing Charts

Once the repository is added, you can install any of the charts as follows:

1. **NetBird Chart**:

```bash
helm install netbird totmicro/netbird
```

### Updating Charts

To get the latest version of the charts, run:

```bash
helm repo update
```

### Uninstalling Charts

You can uninstall the charts using Helm’s `uninstall` command:

1. **Uninstall NetBird**:

```bash
helm uninstall netbird
```

## Releasing New Helm Chart Versions

New chart versions are automatically published through [GitHub Actions](./.github/workflows/release.yml). To deploy a new version, make sure to increment the chart version; otherwise, it will not be published.

## Contributing

Feel free to open issues or pull requests if you would like to contribute to these Helm charts.

