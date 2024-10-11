# netbird-dashboard

![Version: 1.1.0](https://img.shields.io/badge/Version-1.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.6.0](https://img.shields.io/badge/AppVersion-2.6.0-informational?style=flat-square)

UI for the NetBird VPN management platform
# NetBird Dashboard Helm Chart

This Helm chart installs and configures the [NetBird-Dashboard](https://github.com/netbirdio/dashboard) services within a Kubernetes cluster. The chart includes the dashboard to manage netbird.

## Prerequisites

- Helm 3.x
- Kubernetes 1.19+

## Installation

To install the chart with the release name `netbird-dashboard`:

```bash
helm repo add totmicro https://totmicro.github.io/helms
helm install netbird totmicro/netbird-dashboard
```

You can override default values by specifying a `values.yaml` file:

```bash
helm install netbird totmicro/netbird-dashboard -f values.yaml
```

### Uninstalling the Chart

To uninstall/delete the `netbird-dashboard` release:

```bash
helm uninstall netbird-dashboard
```

This will remove all the resources associated with the release.

## Configuration

The following table lists the configurable parameters of the NetBird Helm chart and their default values.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| auth.audience | string | `"netbird-dashboard"` |  |
| auth.authority | string | `"http://keycloak.localtest.me:9000/realms/helm-charts"` |  |
| auth.clientID | string | `"netbird-dashboard"` |  |
| auth.supportedScopes | string | `"openid profile email offline_access api"` |  |
| auth.userIDClaim | string | `"sub"` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| fullnameOverride | string | `""` |  |
| global.namespace | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"netbirdio/dashboard"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| netbird.disableIPv6 | bool | `true` |  |
| netbird.managementApiEndpoint | string | `"http://localtest.me:8081"` |  |
| netbird.managementGrpcApiEndpoint | string | `"http://localtest.me:8081"` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| secretName | string | `""` |  |
| securityContext | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |

For more configuration options, refer to the `values.yaml` file.

You can find a working example [here](./values-example.yaml)

## Contributing

We welcome contributions to improve this chart! Please submit a pull request to the GitHub repository with any changes or suggestions.

