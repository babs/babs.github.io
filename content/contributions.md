---
title: "Contributions"
hideMeta: true
ShowToc: true
TocOpen: false
---

Open source contributions to projects I don't maintain — bug fixes, features, translations, and docs.

## root-gg/plik

Added generic OIDC authentication with security hardening.

* [Extract id_token claims, enforce email_verified, harden sub validation](https://github.com/root-gg/plik/pull/590) — 2026
* [Add generic OIDC authentication provider](https://github.com/root-gg/plik/pull/548) — 2026

## rustfs/rustfs

* [Add existingSecret handling and support for extra manifests (Helm)](https://github.com/rustfs/rustfs/pull/992) — 2025

## nabsul/k8s-ecr-login-renew

* [Add post-install/upgrade Job + refactor CronJob templates](https://github.com/nabsul/k8s-ecr-login-renew/pull/81) — 2025

## chainguard-forks/kaniko

* [Fix ENV syntax in Dockerfile](https://github.com/chainguard-forks/kaniko/pull/33) — 2025

## hacf-fr/freebox-api

* [Add get_backup_lte_status](https://github.com/hacf-fr/freebox-api/pull/808) — 2025

## external-secrets/external-secrets

* [Fix GitLab group variable regression](https://github.com/external-secrets/external-secrets/pull/4379) — 2025

## kyverno/kyverno & kyverno/policies

* [Add OpenTelemetry inject-otel-environment-variable policy](https://github.com/kyverno/policies/pull/1212) — 2024
* [Fix global context error message logic](https://github.com/kyverno/kyverno/pull/11815) — 2024
* [Remove policy exception dependency from globalcontext](https://github.com/kyverno/kyverno/pull/11788) — 2024

## rdvencioneck/aws-vpn-client-docker

* [Update Dockerfile with OpenVPN 2.6.12 support](https://github.com/rdvencioneck/aws-vpn-client-docker/pull/6) — 2024

## mdaverde/jsonpath

* [Add SetKeepNilAsNull to set null values](https://github.com/mdaverde/jsonpath/pull/6) — 2024

## helm-unittest/helm-unittest

* [Attempt to fix #471](https://github.com/helm-unittest/helm-unittest/pull/476) — 2024

## GoogleContainerTools/kaniko

* [Add flag to remap registries for any registry mirror](https://github.com/GoogleContainerTools/kaniko/pull/2935) — 2024

## project-zot/zot & zui

* [Add generic OIDC with customizable name](https://github.com/project-zot/zot/pull/1691) — 2023
* [Add customizable generic OIDC login button](https://github.com/project-zot/zui/pull/375) — 2023
* [Fix apikey case in docs](https://github.com/project-zot/zot/pull/1693) — 2023

## kopia/kopia

* [Add Custom Root CA option for S3](https://github.com/kopia/kopia/pull/2845) — 2023

## keel-hq/keel

* [Allow change of pollDefaultSchedule via env var](https://github.com/keel-hq/keel/pull/709) — 2023

## oauth2-proxy/oauth2-proxy

Session management, Keycloak provider, and unix socket upstream support.

* [Fix test race condition on htpasswd file](https://github.com/oauth2-proxy/oauth2-proxy/pull/1882) — 2022
* [Session aware logout with backend logout URL](https://github.com/oauth2-proxy/oauth2-proxy/pull/1876) — 2022
* [Fix uninitialized user claim](https://github.com/oauth2-proxy/oauth2-proxy/pull/1873) — 2022
* [Add support for unix socket as upstream](https://github.com/oauth2-proxy/oauth2-proxy/pull/1866) — 2022
* [Keycloak provider — retain user and preferred_username](https://github.com/oauth2-proxy/oauth2-proxy/pull/1815) — 2022

## acme-dns/acme-dns

* [Use LastUpdate to also track creation date](https://github.com/acme-dns/acme-dns/pull/321) — 2022

## lensapp/lens

* [Fix AppImage windows not showing application icon](https://github.com/lensapp/lens/pull/6444) — 2022

## saltstack/salt

Multiple contributions across Elasticsearch, apt, git, and MongoDB modules.

* [Fixes #62662 — apt pkgrepo.managed signed-by and test=true](https://github.com/saltstack/salt/pull/62663) — 2022
* [Fix sources.list multi-arch definition](https://github.com/saltstack/salt/pull/62134) — 2022
* [Add ssl argument to Mongo connection](https://github.com/saltstack/salt/pull/59927) — 2021
* [Fix git state identity lacking user expansion](https://github.com/saltstack/salt/pull/48462) — 2018
* [Fix elasticsearch.index_template_present on ES <6.x](https://github.com/saltstack/salt/pull/48445) — 2018
* [Fix elasticsearch.index_template_present with check_definition](https://github.com/saltstack/salt/pull/47703) — 2018
* [Add doc about state.sls_id mods comma separated list](https://github.com/saltstack/salt/pull/38054) — 2016

## duncs/clusterssh

* [Override config via cssh_* environment variables](https://github.com/duncs/clusterssh/pull/138) — 2021

## jacopotediosi/OctoPrint-Telegram

* [Add silent message option for chosen events](https://github.com/jacopotediosi/OctoPrint-Telegram/pull/256) — 2020

## minio/mc

* [Fix code block issue in doc's remote section](https://github.com/minio/mc/pull/3531) — 2020

## strdn/rundeck-jdbc-executor-plugin

* [Add jdbc-password-storage-path in README.md](https://github.com/strdn/rundeck-jdbc-executor-plugin/pull/7) — 2019

## michaelluich/phpIPAM

* [Factorization and docstring cleanup](https://github.com/michaelluich/phpIPAM/pull/2) — 2017

## espressif/esptool

* [Add optional progress while reading flash](https://github.com/espressif/esptool/pull/88) — 2016
* [Look at env before using default values](https://github.com/espressif/esptool/pull/87) — 2016

## kleiram/transmission-php

* [Add comment field to Torrent model](https://github.com/kleiram/transmission-php/pull/57) — 2016

## collectd/collectd

* [Named IRQ plugin with AppendNum](https://github.com/collectd/collectd/pull/1373) — 2015

## bojidar-bg/dokuwiki-callflow-plugin

* [Add order directive and colwidth directives](https://github.com/bojidar-bg/dokuwiki-callflow-plugin/pull/7) — 2015

## pilot51/voicenotify

* [Enable fast scroll in application list](https://github.com/pilot51/voicenotify/pull/48) — 2015

## nullptrlabs/pgmodeler

French translation maintainer — 20+ PRs including translations, bug fixes, shortcut conflicts, and startup tuning.

* [Fixed shortcut translation making it inoperant](https://github.com/nullptrlabs/pgmodeler/pull/145) — 2013
* [All pgmodeler PRs](https://github.com/nullptrlabs/pgmodeler/pulls?q=is%3Apr+author%3Ababs)

## bottlepy/bottle

* [Plugins](https://github.com/bottlepy/bottle/pull/99) — 2010
