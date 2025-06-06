# burp-suite-enterprise-edition

![Version: 2025.3.1-namespace-only-with-pvc-and-ingress](https://img.shields.io/badge/Version-2025.3.1--namespace--only--with--pvc--and--ingress-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2025.3.1-21156](https://img.shields.io/badge/AppVersion-2025.3.1--21156-informational?style=flat-square)

A helm chart to deploy Burp Suite DAST on a Kubernetes cluster. See the release notes at https://portswigger.net/burp/releases/enterprise-edition-2025-3-1.

**Homepage:** <https://portswigger.net/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| PortSwigger | <hello@portswigger.net> |  |

## Source Code

* <https://github.com/portswigger/enterprise-helm-charts/>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| applicationName | string | `"bsee"` |  |
| connectionCheckContainerCpu | string | `"1400m"` |  |
| connectionCheckContainerMemory | string | `"2Gi"` |  |
| containerRegistry | string | `"public.ecr.aws"` | The container registry used to get the Enterprise images |
| createPersistentVolumeClaim | bool | `false` | Controls whether to create the persistent volume claim or not |
| database.enterpriseServerConnectionUsername | string | `""` | Connection username for the Enterprise Server database connection. Required if connection username differs from internal username e.g. if @hostname suffix is mandated (Azure) |
| database.enterpriseServerPassword | string | `""` | Password for the Enterprise Server database connection |
| database.enterpriseServerUsername | string | `""` | Username for the Enterprise Server database connection |
| database.idleTimeout | int | `60000` | Idle timeout (ms) for the database connection |
| database.maxLifetimeTimeout | int | `120000` | Maximum lifetime timeout (ms) for the database connection |
| database.scanningResourceConnectionUsername | string | `""` | Connection username for the Scanning Resource database connection Required if connection username differs from internal username e.g. if @hostname suffix is mandated (Azure) |
| database.scanningResourcePassword | string | `""` | Password for the Scanning Resource database connection |
| database.scanningResourceUsername | string | `""` | Username for the Scanning Resource database connection |
| database.url | string | `""` | JDBC connection URL for the database |
| defaultCpuPerContainer | string | `"100m"` |  |
| defaultMemoryPerContainer | string | `"128Mi"` |  |
| defaultRequestCpuPerContainer | string | `"100m"` |  |
| defaultRequestMemoryPerContainer | string | `"128Mi"` |  |
| enterpriseServerContainerCpu | string | `"1400m"` |  |
| enterpriseServerContainerMemory | string | `"4Gi"` |  |
| imagePullSecrets | list | `[]` |  |
| maxCpuPerContainer | string | `"4000m"` |  |
| maxMemoryPerContainer | string | `"8Gi"` |  |
| minCpuPerContainer | string | `"100m"` |  |
| minMemoryPerContainer | string | `"128Mi"` |  |
| persistentVolumeClaim | string | `"bsee-pvc"` | Name of the persistent volume claim used for shared storage between the Enterprise Pods |
| scanContainerCpu | string | `"1400m"` |  |
| scanContainerMemory | string | `"8Gi"` |  |
| services.enterpriseServer.installationEnvironment | string | `"KUBERNETES"` |  |
| services.webServer.createIngress | bool | `false` | Controls whether to create the ingress |
| services.webServer.domain | string | `"example.com"` | Domain name for host-based ingress routing if the ingress creation is enabled |
| services.webServer.httpPort | string | `"8080"` |  |
| services.webServer.httpsCertificateSecret.key | string | `"certificate"` |  |
| services.webServer.httpsCertificateSecret.name | string | `"bsee-web-server-https"` |  |
| services.webServer.httpsPassphraseSecret.key | string | `"passphrase"` |  |
| services.webServer.httpsPassphraseSecret.name | string | `"bsee-web-server-https"` |  |
| services.webServer.httpsPort | string | `"8443"` |  |
| services.webServer.installationEnvironment | string | `"KUBERNETES"` |  |
| services.webServer.label | string | `"app.portswigger.net/ingress: web-server"` |  |
| services.webServer.useDeprecatedHttpConfigFromDatabase | bool | `false` |  |
| services.webServer.useHttps | bool | `false` |  |
| webServerContainerCpu | string | `"1400m"` |  |
| webServerContainerMemory | string | `"4Gi"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/tag/v1.14.2)