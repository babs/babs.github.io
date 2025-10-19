---
#title: "Welcome"
date: 2024-08-17T00:59:44+02:00
layout: home
---

# projects

## multiping

https://github.com/babs/multiping

`multiping` is a ping cli tool to monitor several targets at once using pings or TCP probing with optional logging of transition between states in a file.

### `multiping` demo
![Demo01](https://raw.githubusercontent.com/babs/multiping/master/_demo/demo-001.svg)

## ecr-repo-creator

https://github.com/babs/ecr-repo-creator

`ecr-repo-creator` is a small tool to create AWS ECR repository if missing, staticly built to have no dependencies.
It can also apply policies on newly created repos.

There is also an example of Gitlab CI component that using it in glci-example ;-)

## runstats

https://github.com/babs/runstats

`runstats` is a lightweight command wrapper that measures and reports resource usage metrics for any command. It executes a command and collects detailed resource usage statistics, including memory consumption, CPU time, I/O operations, and context switches. It outputs metrics as JSON to stderr while transparently passing through the command's stdin, stdout, and stderr.

## fastapi-structured-logging

https://github.com/babs/fastapi-structured-logging

`fastapi-structured-logging` is a lightweight Python module that provides structured logging utilities and a configurable FastAPI access logging middleware. It configures `structlog` for JSON or console output, enriches log events with OpenTelemetry trace and span identifiers, and exposes an `AccessLogMiddleware` for comprehensive request logging.

## externalsecret-refresh

https://github.com/babs/externalsecret-refresh

`externalsecret-refresh` is a container to be used as Kubernetes Job that triggers ExternalSecrets to refresh by patching their annotations and monitors the refresh status. It's designed for integration with Helm Charts or ArgoCD applications.

## ebpf4fun-ring

https://github.com/babs/ebpf4fun-ring

`ebpf4fun-ring` is an eBPF playground and experimentation project for DNS packet capture using BPF ring buffers. It monitors network interfaces and captures DNS queries/responses for inspection and analysis.

## oci-toolbox

https://github.com/babs/oci-toolbox

`oci-toolbox` is an OCI image with multiple tools to manipulate OCI images, manifests, and Helm charts. It includes tools like skopeo, oras, helm, jq, yq, ecr-repo-creator, and more for container image operations.

## pre-commit-hooks
(replaces check-argocd-yaml)

https://github.com/babs/pre-commit-hooks (replaces https://github.com/babs/check-argocd-yaml)

* `check-argocd-yaml` is a pre-commit hook to validate some readability and maintainability check for ArgoCD Application manifests

## helm-charts

https://github.com/babs/helm-charts

My helm charts (mainly helpers)

```bash
helm repo add babs https://babs.github.io/helm-charts
```

* `babs/extra-objects` a simple chart that instantiate objects from `extraObjects` array. Useful to add some resources in ArgoCD application when primary helm lacks this kind of support.

## Teams Notifier

https://github.com/teams-notifier

Teams Notifier is a project to replace and enhance deprecated webhooks. The goal is to have an interactive bot to get token to be able to easily send/update/delete messages to MS Teams.


## phpipam2dns

https://github.com/babs/phpipam2dns

First goal of this project was to learn go. As primary side effect, it is a tool that applies phpIPAM changelog to DNS via dynamic updates (RFC2845)


## observium-header-authentication

https://github.com/babs/observium-header-authentication

`observium-header-authentication` is a simple php file that allows authentication and authorisation to be based on http headers, therefore you to use [oauth2-proxy](https://oauth2-proxy.github.io/oauth2-proxy/) to have OIDC authentication for [observium](https://www.observium.org/).

## phpipam-enhancer.user.js

https://github.com/babs/phpipam-enhancer.user.js

Simple helper [tampermonkey](https://www.tampermonkey.net/) script for daily use of [phpipam](https://www.tampermonkey.net/).

The script adds 3 links next to IPs and hostnames:
 - http: opens ip or hostname as http link in a new tab
 - https: opens ip or hostname as https link in a new tab
 - copy: copy ip or hostname to clipboard

### Examples on demo.phpipam.net

![Example on subnet view](https://raw.githubusercontent.com/babs/phpipam-enhancer.user.js/main/img/demo.phpipam.net-subnetview.png)

![Example on search result](https://raw.githubusercontent.com/babs/phpipam-enhancer.user.js/main/img/demo.phpipam.net-search-result-dark.png)

## blibs

https://github.com/babs/blibs

My default helper for configuring logs with colored output, among aother things

```python
from blibs import init_root_logger
init_root_logger(level=10)
```

## ram-eater

https://github.com/babs/ram-eater

Small tool in C to consume RAM per GB, just to test behaviors when reaching ressource limitations, it's also available as docker image [beardedbabs/ram-eater](https://hub.docker.com/r/beardedbabs/ram-eater)

## dokuwiki-plugin-stlviewer

https://github.com/babs/dokuwiki-plugin-stlviewer

Embed your STL as render using Viewstl.com excellent library v1.13 in your dokuwiki instance.

## filtering-dns-reverseproxy

https://github.com/babs/filtering-dns-reverseproxy

`filtering-dns-reverseproxy` is a simple Filtering DNS Reverse Proxy allowing to expose publicly part of some zones (ie lets encrypt certs, domain delegation etc) without leaking private informations without falling into split horizon DNS.

## k8s-ps1.sh

https://github.com/babs/k8s-ps1.sh

Bash shell extention to see on which kube server the shell is currently operating on. (needs some doc).

```bash
source k8s-ps1.sh
# inject ${K8S_EXT} in your $PS1 (preferably in your .bashrc)
PS1="${K8S_EXT}\001\e[1;34m\002[\t]\001\e[1;${USERCOLOR}m\002[\u@\h] \001\e[0;36m\002\w${GIT_EXT} ${CHAR}\001\e[0m\002 "

# Then press Ctrl+T to toggle the line
```


## keycloak-phpipam-is-admin-mapper

https://github.com/babs/keycloak-phpipam-is-admin-mapper

Simple SAML2 keycloak mapper for phpIPAM / SAML2 users (inc. an exemple of keycloak docker multistage build)

## formula-k8s

https://github.com/babs/formula-k8s

Salt formula to bootstrap kube cluster and nodes.

## formula-autostate

https://github.com/babs/formula-autostate

Salt formula to apply states based on pillar values (takes advantage of external pillar :))

## formula-TEMPLATE

https://github.com/babs/formula-TEMPLATE

Template used for formulas, simpler than the official but includes manifest for management at scale.

## cnc-linuxcnc-nowforever_vfd

https://github.com/babs/cnc-linuxcnc-nowforever_vfd

My old `nowforever_vfd` control script for LinuxCNC, need a more recent update I think :)
I've a new one but RPM value read from the vfd seems to behave weirdly.

## oauth2-rp

https://github.com/babs/oauth2-rp

An oauth2 reverseproxy for keycloak with a dedicated behavior on the filtering of api routes (api key vs headers)

## amqp2mongo

https://github.com/babs/amqp2mongo

App to dump rabbitmq messages into mongodb (useful for tracking messages with an TTL index)

## marlin-config-tracking-build-script

https://github.com/babs/marlin-config-tracking-build-script

`marlin-config-tracking-build-script` eases the tracking of changes between firmware build and configuration change when using PlatformIO framework on linux.

## pyrowl

https://github.com/babs/pyrowl

pyrowl/pynma is a simple python module for the NotifyMyAndroid API.

## android-customfonthtml

https://github.com/babs/android-customfonthtml

Custom font html is an Android library to handle custom font, via custom loaders, with a Html.fromHtml like function.

## MuninNode.net

https://github.com/babs/MuninNode.net

A reimplementation of MuninNone in .net