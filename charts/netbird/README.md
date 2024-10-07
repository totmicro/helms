# netbird

![Version: 1.1.0](https://img.shields.io/badge/Version-1.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.30.0](https://img.shields.io/badge/AppVersion-0.30.0-informational?style=flat-square)

# NetBird Helm Chart

This Helm chart installs and configures the [NetBird](https://github.com/netbirdio/netbird) services within a Kubernetes cluster. The chart includes the management, signal, and relay components of NetBird, providing secure peer-to-peer network connections across various environments.

## Prerequisites

- Helm 3.x
- Kubernetes 1.19+

## Installation

To install the chart with the release name `netbird`:

```bash
helm repo add totmicro https://totmicro.github.io/helms
helm install netbird totmicro/netbird
```

You can override default values by specifying a `values.yaml` file:

```bash
helm install netbird totmicro/netbird -f values.yaml
```

### Uninstalling the Chart

To uninstall/delete the `netbird` release:

```bash
helm uninstall netbird
```

This will remove all the resources associated with the release.

## Configuration

The following table lists the configurable parameters of the NetBird Helm chart and their default values.

| Parameter                          | Description                                                                                 | Default                                |
|------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------|
| `nameOverride`                     | Override the chart name                                                                     | `""`                                   |
| `fullnameOverride`                 | Override the full chart name                                                                | `""`                                   |
| `management.replicaCount`          | Number of management pod replicas                                                           | `1`                                    |
| `management.image.repository`      | Management image repository                                                                 | `netbirdio/management`                 |
| `management.image.tag`             | Management image tag                                                                        | Chart app version                      |
| `management.image.pullPolicy`      | Management image pull policy                                                                | `IfNotPresent`                         |
| `management.service.port`          | Port for the management service                                                             | `80`                                   |
| `management.persistentVolume.size` | Persistent volume size for management                                                       | `100Mi`                                |
| `management.autoscaling.enabled`   | Enable autoscaling for the management component                                              | `false`                                |
| `signal.replicaCount`              | Number of signal pod replicas                                                               | `1`                                    |
| `signal.image.repository`          | Signal image repository                                                                     | `netbirdio/signal`                     |
| `signal.image.tag`                 | Signal image tag                                                                            | Chart app version                      |
| `signal.image.pullPolicy`          | Signal image pull policy                                                                    | `IfNotPresent`                         |
| `signal.service.port`              | Port for the signal service                                                                 | `80`                                   |
| `relay.replicaCount`               | Number of relay pod replicas                                                                | `1`                                    |
| `relay.image.repository`           | Relay image repository                                                                      | `netbirdio/relay`                      |
| `relay.image.tag`                  | Relay image tag                                                                             | Chart app version                      |
| `relay.image.pullPolicy`           | Relay image pull policy                                                                     | `IfNotPresent`                         |
| `relay.service.port`               | Port for the relay service                                                                  | `33080`                                |
| `ingress.enabled`                  | Enable ingress for the management, signal, or relay services                                | `false`                                |
| `ingress.className`                | Ingress class name                                                                          | `""`                                   |
| `persistentVolume.enabled`         | Enable persistent volume for management                                                     | `true`                                 |
| `autoscaling.enabled`              | Enable autoscaling for management, signal, or relay components                              | `false`                                |
| `dnsDomain`                        | DNS domain for the NetBird management service                                               | `netbird.selfhosted`                   |

For more configuration options, refer to the `values.yaml` file.

You can find a working example [here](./values-example.yaml)

## Contributing

We welcome contributions to improve this chart! Please submit a pull request to the GitHub repository with any changes or suggestions.

