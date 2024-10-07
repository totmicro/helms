# netbird

![Version: 1.1.0](https://img.shields.io/badge/Version-1.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.30.0](https://img.shields.io/badge/AppVersion-0.30.0-informational?style=flat-square)

NetBird VPN management platform

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| fullnameOverride | string | `""` |  |
| management.affinity | object | `{}` |  |
| management.autoscaling.enabled | bool | `false` |  |
| management.autoscaling.maxReplicas | int | `100` |  |
| management.autoscaling.minReplicas | int | `1` |  |
| management.autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| management.configmap | string | `""` |  |
| management.deploymentAnnotations | object | `{}` |  |
| management.dnsDomain | string | `"netbird.selfhosted"` |  |
| management.env | object | `{}` |  |
| management.envRaw | object | `{}` |  |
| management.image.pullPolicy | string | `"IfNotPresent"` |  |
| management.image.repository | string | `"netbirdio/management"` |  |
| management.image.tag | string | `""` |  |
| management.imagePullSecrets | list | `[]` |  |
| management.ingress.annotations | object | `{}` |  |
| management.ingress.className | string | `""` |  |
| management.ingress.enabled | bool | `false` |  |
| management.ingress.hosts[0].host | string | `"example.com"` |  |
| management.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| management.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| management.ingress.tls | list | `[]` |  |
| management.ingressGrpc.annotations | object | `{}` |  |
| management.ingressGrpc.className | string | `""` |  |
| management.ingressGrpc.enabled | bool | `false` |  |
| management.ingressGrpc.hosts[0].host | string | `"example.com"` |  |
| management.ingressGrpc.hosts[0].paths[0].path | string | `"/"` |  |
| management.ingressGrpc.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| management.ingressGrpc.tls | list | `[]` |  |
| management.init.env | object | `{}` |  |
| management.init.envRaw | object | `{}` |  |
| management.init.image.repository | string | `"marcportabellaclotet/vals"` |  |
| management.init.image.tag | string | `"0.37.1"` |  |
| management.lifecycle | object | `{}` |  |
| management.nodeSelector | object | `{}` |  |
| management.persistentVolume.accessModes[0] | string | `"ReadWriteOnce"` |  |
| management.persistentVolume.enabled | bool | `true` |  |
| management.persistentVolume.size | string | `"100Mi"` |  |
| management.podAnnotations | object | `{}` |  |
| management.podCommand.args[0] | string | `"--port=80"` |  |
| management.podCommand.args[1] | string | `"--log-file=console"` |  |
| management.podCommand.args[2] | string | `"--log-level=info"` |  |
| management.podCommand.args[3] | string | `"--disable-anonymous-metrics=false"` |  |
| management.podCommand.args[4] | string | `"--single-account-mode-domain=netbird.example.com"` |  |
| management.podCommand.args[5] | string | `"--dns-domain=netbird.selfhosted\""` |  |
| management.podSecurityContext | object | `{}` |  |
| management.replicaCount | int | `1` |  |
| management.resources | object | `{}` |  |
| management.securityContext | object | `{}` |  |
| management.service.port | int | `80` |  |
| management.service.type | string | `"ClusterIP"` |  |
| management.serviceAccount.annotations | object | `{}` |  |
| management.serviceAccount.create | bool | `true` |  |
| management.serviceAccount.name | string | `""` |  |
| management.tolerations | list | `[]` |  |
| nameOverride | string | `""` |  |
| relay.affinity | object | `{}` |  |
| relay.autoscaling.enabled | bool | `false` |  |
| relay.autoscaling.maxReplicas | int | `100` |  |
| relay.autoscaling.minReplicas | int | `1` |  |
| relay.autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| relay.deploymentAnnotations | object | `{}` |  |
| relay.image.pullPolicy | string | `"IfNotPresent"` |  |
| relay.image.repository | string | `"netbirdio/relay"` |  |
| relay.image.tag | string | `""` |  |
| relay.imagePullSecrets | list | `[]` |  |
| relay.ingress.annotations | object | `{}` |  |
| relay.ingress.className | string | `""` |  |
| relay.ingress.enabled | bool | `false` |  |
| relay.ingress.hosts[0].host | string | `"example.com"` |  |
| relay.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| relay.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| relay.ingress.tls | list | `[]` |  |
| relay.logLevel | string | `"info"` |  |
| relay.nodeSelector | object | `{}` |  |
| relay.podAnnotations | object | `{}` |  |
| relay.podSecurityContext | object | `{}` |  |
| relay.replicaCount | int | `1` |  |
| relay.resources | object | `{}` |  |
| relay.securityContext | object | `{}` |  |
| relay.service.name | string | `"http"` |  |
| relay.service.port | int | `33080` |  |
| relay.service.type | string | `"ClusterIP"` |  |
| relay.serviceAccount.annotations | object | `{}` |  |
| relay.serviceAccount.create | bool | `true` |  |
| relay.serviceAccount.name | string | `""` |  |
| relay.tolerations | list | `[]` |  |
| signal.affinity | object | `{}` |  |
| signal.autoscaling.enabled | bool | `false` |  |
| signal.autoscaling.maxReplicas | int | `100` |  |
| signal.autoscaling.minReplicas | int | `1` |  |
| signal.autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| signal.deploymentAnnotations | object | `{}` |  |
| signal.image.pullPolicy | string | `"IfNotPresent"` |  |
| signal.image.repository | string | `"netbirdio/signal"` |  |
| signal.image.tag | string | `""` |  |
| signal.imagePullSecrets | list | `[]` |  |
| signal.ingress.annotations | object | `{}` |  |
| signal.ingress.className | string | `""` |  |
| signal.ingress.enabled | bool | `false` |  |
| signal.ingress.hosts[0].host | string | `"example.com"` |  |
| signal.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| signal.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| signal.ingress.tls | list | `[]` |  |
| signal.logLevel | string | `"info"` |  |
| signal.nodeSelector | object | `{}` |  |
| signal.podAnnotations | object | `{}` |  |
| signal.podSecurityContext | object | `{}` |  |
| signal.replicaCount | int | `1` |  |
| signal.resources | object | `{}` |  |
| signal.securityContext | object | `{}` |  |
| signal.service.name | string | `"grpc"` |  |
| signal.service.port | int | `80` |  |
| signal.service.type | string | `"ClusterIP"` |  |
| signal.serviceAccount.annotations | object | `{}` |  |
| signal.serviceAccount.create | bool | `true` |  |
| signal.serviceAccount.name | string | `""` |  |
| signal.tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.13.1](https://github.com/norwoodj/helm-docs/releases/v1.13.1)
