# Hazelops Helm Charts

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/HazelOps)](https://artifacthub.io/packages/search?repo=hazelops&sort=relevance&page=1)

## HazelOps Library for Kubernetes

Applications, provided by [HazelOps](https://hazelops.com), ready to launch on Kubernetes using [Kubernetes Helm](https://github.com/helm/helm).

## Prerequisites

- Kubernetes 1.24+
- Helm 3.8.0+

## Setup a Kubernetes Cluster

To install Kubernetes Cluster, please refer to the Kubernetes [getting started guide](https://kubernetes.io/docs/getting-started-guides/).

## Install Helm

Helm is a tool for managing Kubernetes charts. Charts are packages of pre-configured Kubernetes resources.

To install Helm, refer to the [Helm install guide](https://github.com/helm/helm#install) and ensure that the `helm` binary is in the `PATH` of your shell.

## Using Helm

Once you have installed the Helm client, you can deploy a Bitnami Helm Chart into a Kubernetes cluster.

Please refer to the [Quick Start guide](https://helm.sh/docs/intro/quickstart/) if you wish to get running in just a few commands, otherwise the [Using Helm Guide](https://helm.sh/docs/intro/using_helm/) provides detailed instructions on how to use the Helm client to manage packages on your Kubernetes cluster.

## Useful Helm Client Commands:


### Add repo

```console
helm repo add hazelops https://hazelops.github.io/charts/
helm repo update
```

### Install a chart:

```console
helm install [RELEASE_NAME] hazelops/[CHART]
```

### Upgrade application: 

```console
helm upgrade [RELEASE_NAME] [CHART] --install
```

## License

Copyright &copy; 2023 HazelOps OÜ

Licensed under the Apache License, Version 2.0 (the "License")

You may not use this file except in compliance with the License.

You may obtain a copy of the License at

<http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
