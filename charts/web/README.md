# web

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/web)](https://artifacthub.io/packages/helm/hazelops/web) ![Version: 0.4.1](https://img.shields.io/badge/Version-0.4.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.3.0](https://img.shields.io/badge/AppVersion-1.3.0-informational?style=flat-square)

A simple web application using Istio and Ingress-nginx.


## Requirements

Kubernetes: `>=1.20.0-0`

Ingress-Nginx: `>=4.8.3`

Istio: `>=1.19`


## Usage

### Get Repo Info

```console
helm repo add hazelops https://hazelops.github.io/charts/
helm repo update
```

### A simple install with default values:

**Important:** only helm3 is supported

```console
helm install [RELEASE_NAME] hazelops/web
```

The command deploys web chart on the Kubernetes cluster in the default configuration.

_See [configuration](#configuration) below._

_See [helm install](https://helm.sh/docs/helm/helm_install/) for command documentation._


### To install with some set values:

```console
helm install [RELEASE_NAME]  hazelops/web --set values_key1=value1 --set values_key2=value2
```

### To install with Istio enabled:

```console
helm install [RELEASE_NAME]  hazelops/web --set global.istio.enabled=true --set global.ingress.enabled=false
```

### To install with Ingress-Nginx enabled:

```console
helm install [RELEASE_NAME]  hazelops/web --set global.istio.enabled=false --set global.ingress.enabled=true
```

### Uninstall Chart

```console
helm uninstall [RELEASE_NAME]
```

This removes all the Kubernetes components associated with the chart and deletes the release.

_See [helm uninstall](https://helm.sh/docs/helm/helm_uninstall/) for command documentation._

### Upgrading Chart

```console
helm upgrade [RELEASE_NAME] [CHART] --install
```

_See [helm upgrade](https://helm.sh/docs/helm/helm_upgrade/) for command documentation._


## Configuration

See [Customizing the Chart Before Installing](https://helm.sh/docs/intro/using_helm/#customizing-the-chart-before-installing). To see all configurable options with detailed comments, visit the chart's [values.yaml](./values.yaml), or run these configuration commands:

```console
helm show values hazelops/web
```


## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| global.app.command | string | `""` |  |
| global.app.containerName | string | `""` |  |
| global.app.domain | string | `"domain.local"` |  |
| global.app.image.imagePullPolicy | string | `"Always"` |  |
| global.app.image.repository | string | `"<aws-account-id>.dkr.ecr.<aws-region>.amazonaws.com/<app-name>"` |  |
| global.app.image.tag | string | `"dev-latest"` |  |
| global.app.name | string | `"app"` |  |
| global.app.region | string | `"aws-region"` |  |
| global.app.replicas | int | `1` |  |
| global.app.variables.list.APP_NAME | string | `""` |  |
| global.env | string | `"local"` |  |
| global.gateway.tlsIssuer | string | `""` |  |
| global.iam_roles.r53 | string | `""` |  |
| global.iam_roles.ssm | string | `""` |  |
| global.ingress.create_certificate | bool | `false` |  |
| global.ingress.domain | string | `"domain.local"` |  |
| global.ingress.enabled | bool | `false` |  |
| global.ingress.port | int | `3000` |  |
| global.ingress.tls_certificate_name | string | `""` |  |
| global.istio.create_certificate | bool | `false` |  |
| global.istio.domain | string | `"domain.local"` |  |
| global.istio.enabled | bool | `false` |  |
| global.istio.port | int | `3000` |  |
| global.istio.tls_certificate_name | string | `""` |  |
| global.secrets.app | string | `""` |  |
| global.secrets.list[0] | string | `""` |  |
| global.service.port | int | `3000` |  |
| global.service.targetPort | int | `3000` |  |

----------------------------------------------
