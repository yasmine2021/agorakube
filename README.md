# AgoraKube

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Filkilab%2Fagorakube.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Filkilab%2Fagorakube?ref=badge_shield)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/3104/badge)](https://bestpractices.coreinfrastructure.org/projects/3104)
[![Build Status](https://travis-ci.org/ilkilab/agorakube.svg?branch=master)](https://travis-ci.org/ilkilab/agorakube)


<p align="center">
<img src="./images/agorakube-logo.svg" width="450" alt="Agorakube" title="Agorakube" />
</p>
<p>
<img src="https://raw.githubusercontent.com/cncf/artwork/master/projects/kubernetes/certified-kubernetes/versionless/color/certified-kubernetes-color.svg?sanitize=true" width="100" alt="k8s-conformance-v1.16" title="https://github.com/cncf/k8s-conformance/tree/master/v1.16/agorakube"/>
<img src="https://raw.githubusercontent.com/cncf/artwork/master/other/cncf-landscape/stacked/color/cncf-landscape-stacked-color.svg?sanitize=true" width="100" alt="Agorakube is a cncf landscap project" title="Agorakube is a cncf landscap project"/>
</p>

This project is aimed to provide the simplest way to install kubernetes on bare-metal, virtual & Cloud environments.
Actually, Ubuntu 18.04 (Bionic) amd64 and Centos 7/8  are supported, but several other operating systems will be available soon.


Master branch is stable.

Since November 2019, Agorakube has been certified by the "Kubernetes Conformance Program" and is a project of [the cncf landscape](https://landscape.cncf.io/selected=agora-kube).

[![asciicast](https://asciinema.org/a/Y58GrrJG3gPM6GvKsSMCZevbX.svg)](https://asciinema.org/a/Y58GrrJG3gPM6GvKsSMCZevbX)

## Table of Contents

This is a list of points that will be explained in this Readme file for the AgoraKube project :

- [What is AgoraKube](#what-is-agoraKube)
- [How to install](#how-to-install)
- [How to give feedback](#how-to-give-feedback)
- [How to contribute](#how-to-contribute)
- [Community](#community)
- [Licensing](#licensing)

## What is AgoraKube

AgoraKube is an easy-to-use, stable Kubernetes distribution (Kubernetes v1.15, 1.16, 1.17).

By its symplicity, AgoraKube provide a good way to deploy and manage K8S Clusters.

AgoraKube is based on Ansible scripts that install and configure Kubernetes components (control plane and data plane) quickly on bare-metal / VMs / Cloud Instances, as systemd services.

This distribution is also adaptive by offering the opportunity to customize your deployment and fit to your needs : OS (default : Ubuntu 18.04 (Bionic) - amd64), DNS Service (default : CoreDNS), Ingress Controller (default : Traefik), Container Runtime (Default : Containerd), certificats, Service-Mesh (available: Linkerd)...

This project is actually under active development so other customizable options will be added soon.

## How to install

We regularly use a machine to deploy every cluster. We only use it for deployment and destroy it after.

### Setup

#### On the "deployment" node
Execute this command in order to install Ansible and clone the repository :
```
bash <(curl -s https://raw.githubusercontent.com/ilkilab/agorakube/master/setup-deploy.sh)
```
#### On the K8S nodes
Execute this command on each node to update them and install the last version of Python : 
```
bash <(curl -s https://raw.githubusercontent.com/ilkilab/agorakube/master/setup-hosts.sh)
```

### Installation instructions

To deploy your K8S cluster follow these [instructions](docs/instructions.md).

## How to give feedback
voila  la modiffication
Every feedback is very welcome via the
[GitHub site](https://github.com/ilkilab/agorakube)
as issues or pull (merge) requests.

You can also give use vulnerability reports by this way.
## How to contribute

See our [Code Of Conduct](https://github.com/ilkilab/agorakube/blob/master/CODE_OF_CONDUCT.md) and [CONTRIBUTING](https://github.com/ilkilab/agorakube/blob/master/docs/CONTRIBUTING.md) for more information.

## Community

Join Agorakube's community for discussion and ask questions : [Agorakube's Slack](http://slack.agorakube.ilkilabs.io/)

Channels :
- **#general** - For general purpose (news, events...)
- **#developpers** - For people who contribute to Agorakube by developing features
- **#end-users** - For end users who want to give us feedbacks
- **#random** - As its name suggests, for random discussions :)

## Licensing

All material here is released under the [APACHE 2.0 license](./LICENSE).
All material that is not executable, including all text when not executed,
is also released under the APACHE 2.0.
In SPDX terms, everything here is licensed under APACHE 2.0;
if it's not executable, including the text when extracted from code, it's
"(APACHE 2.0)".

Like almost all software today, this software depends on many
other components with their own licenses.
Not all components we depend on are APACHE 2.0-licensed, but all
*required* components are FLOSS. We prevent licensing issues
using various processes (see [CONTRIBUTING](./docs/CONTRIBUTING.md)).


[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Filkilab%2Fagorakube.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Filkilab%2Fagorakube?ref=badge_large)
