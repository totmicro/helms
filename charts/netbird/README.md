# netbird

![Version: 1.0.1](https://img.shields.io/badge/Version-1.0.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.27.10](https://img.shields.io/badge/AppVersion-0.27.10-informational?style=flat-square)

NetBird VPN management platform

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| configuration | string | `"\nconfigmap: |-\n  # Sample configuration to use authentik as idp and read secrets from k8s\n  # Adjust the vals references to fit your needs\n  # {\n  #   \"Stuns\": [\n  #     {\n  #       \"Proto\": \"udp\",\n  #       \"URI\": \"stun:ref+k8s://v1/Secret/netbird/netbird-management/stunServer+\",\n  #       \"Username\": \"\",\n  #       \"Password\": \"\"\n  #     }\n  #   ],\n  #   \"TURNConfig\": {\n  #     \"TimeBasedCredentials\": false,\n  #     \"CredentialsTTL\": \"12h0m0s\",\n  #     \"Secret\": \"secret\",\n  #     \"Turns\": [\n  #       {\n  #         \"Proto\": \"udp\",\n  #         \"URI\": \"turn:ref+k8s://v1/Secret/netbird/netbird-management/turnServer+\",\n  #         \"Username\": \"ref+k8s://v1/Secret/netbird/netbird-management/turnServerUser+\",\n  #         \"Password\": \"ref+k8s://v1/Secret/netbird/netbird-management/turnServerPassword+\"\n  #       }\n  #     ]\n  #   },\n  #   \"Signal\": {\n  #     \"Proto\": \"https\",\n  #     \"URI\": \"netbird.example.com:443\",\n  #     \"Username\": \"\",\n  #     \"Password\": \"\"\n  #   },\n  #   \"HttpConfig\": {\n  #     \"LetsEncryptDomain\": \"\",\n  #     \"CertFile\": \"\",\n  #     \"CertKey\": \"\",\n  #     \"AuthAudience\": \"ref+k8s://v1/Secret/netbird/netbird-management/idpClientID+\",\n  #     \"AuthIssuer\": \"https://authentik.example.com/application/o/netbird/\",\n  #     \"AuthUserIDClaim\": \"\",\n  #     \"AuthKeysLocation\": \"https://authentik.example.com/application/o/netbird/jwks/\",\n  #     \"OIDCConfigEndpoint\": \"https://authentik.example.com/application/o/netbird/.well-known/openid-configuration\",\n  #     \"IdpSignKeyRefreshEnabled\": false\n  #   },\n  #   \"IdpManagerConfig\": {\n  #     \"ManagerType\": \"authentik\",\n  #     \"ClientConfig\": {\n  #       \"Issuer\": \"https://authentik.example.com/application/o/netbird\",\n  #       \"TokenEndpoint\": \"https://authentik.example.com/application/o/token/\",\n  #       \"ClientID\": \"ref+k8s://v1/Secret/netbird/netbird-management/idpClientID+\",\n  #       \"ClientSecret\": \"\",\n  #       \"GrantType\": \"client_credentials\"\n  #     },\n  #     \"ExtraConfig\": {\n  #       \"Password\": \"ref+k8s://v1/Secret/netbird/netbird-management/idpServiceAccountPassword+\",\n  #       \"Username\": \"ref+k8s://v1/Secret/netbird/netbird-management/idpServiceAccountUser+\"\n  #     },\n  #     \"Auth0ClientCredentials\": null,\n  #     \"AzureClientCredentials\": null,\n  #     \"KeycloakClientCredentials\": null,\n  #     \"ZitadelClientCredentials\": null\n  #   },\n  #   \"DeviceAuthorizationFlow\": {\n  #     \"Provider\": \"hosted\",\n  #     \"ProviderConfig\": {\n  #       \"ClientID\": \"ref+k8s://v1/Secret/netbird/netbird-management/idpClientID+\",\n  #       \"ClientSecret\": \"\",\n  #       \"Domain\": \"authentik.example.com\",\n  #       \"Audience\": \"ref+k8s://v1/Secret/netbird/netbird-management/idpClientID+\",\n  #       \"TokenEndpoint\": \"https://authentik.example.com/application/o/token/\",\n  #       \"DeviceAuthEndpoint\": \"https://authentik.example.com/application/o/device/\",\n  #       \"AuthorizationEndpoint\": \"\",\n  #       \"Scope\": \"openid\",\n  #       \"UseIDToken\": false,\n  #       \"RedirectURLs\": null\n  #     }\n  #   },\n  #   \"PKCEAuthorizationFlow\": {\n  #     \"ProviderConfig\": {\n  #       \"ClientID\": \"ref+k8s://v1/Secret/netbird/netbird-management/idpClientID+\",\n  #       \"ClientSecret\": \"\",\n  #       \"Domain\": \"\",\n  #       \"Audience\": \"ref+k8s://v1/Secret/netbird/netbird-management/idpClientID+\",\n  #       \"TokenEndpoint\": \"https://authentik.example.com/application/o/token/\",\n  #       \"DeviceAuthEndpoint\": \"\",\n  #       \"AuthorizationEndpoint\": \"https://authentik.example.com/application/o/authorize/\",\n  #       \"Scope\": \"openid profile email offline_access api\",\n  #       \"UseIDToken\": false,\n  #       \"RedirectURLs\": [\n  #         \"http://localhost:53000\"\n  #       ]\n  #     }\n  #   },\n  #   \"StoreConfig\": {\n  #     \"Engine\": \"postgres\"\n  #   },\n  #   \"ReverseProxy\": {\n  #     \"TrustedHTTPProxies\": null,\n  #     \"TrustedHTTPProxiesCount\": 0,\n  #     \"TrustedPeers\": null\n  #   }\n  # }"` |  |
| env | object | `{}` |  |
| envRaw | object | `{}` |  |
| fullnameOverride | string | `""` |  |
| management.affinity | object | `{}` |  |
| management.autoscaling.enabled | bool | `false` |  |
| management.autoscaling.maxReplicas | int | `100` |  |
| management.autoscaling.minReplicas | int | `1` |  |
| management.autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| management.deploymentAnnotations | object | `{}` |  |
| management.dnsDomain | string | `"netbird.selfhosted"` |  |
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
| management.initPod.image.repository | string | `"marcportabellaclotet/vals"` |  |
| management.initPod.image.tag | string | `"0.37.1"` |  |
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
| management.podCommand.args[4] | string | `"--dns-domain=netbird.selfhosted\""` |  |
| management.podCommand.xtraArgs | object | `{}` |  |
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
