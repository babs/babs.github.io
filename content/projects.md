---
title: "Projects"
hideMeta: true
ShowToc: true
TocOpen: false
---

## Featured

A curated subset — the most technically interesting work, where the challenge was non-trivial.

* **[mcp-auth-proxy](#mcp-auth-proxy)** — OAuth 2.1 authorization server fronting any OIDC IdP for MCP clients. STRIDE-modeled, replay-protected, rate-limited discovery surface, per-tool metrics with cardinality cap.
* **[inkwest](#inkwest)** — AI-powered Kubernetes debugging assistant. Read-only kubectl proxy with multi-cluster, OIDC, budget management, multi-provider LLM backends.
* **[cosanet](#cosanet)** — Prometheus exporter that walks every container sandbox on a node to expose conntrack, `/proc/net/snmp`, and netstat metrics — no per-pod instrumentation.
* **[ebpf4fun-ring](#ebpf4fun-ring)** — eBPF playground capturing DNS via BPF ring buffers, with dynamic interface attach and pod resolution.
* **[claude-quota](#claude-quota)** — Cross-platform systray (Linux/Windows/macOS) reading Claude OAuth credentials, polling usage API, and rendering live burn-rate projection.
* **[bifrons](#bifrons)** — Database access portal: auth-remapping proxies (MySQL/PostgreSQL/MongoDB) + Go control plane with dual-gate approval and OIDC login.
* **[claude-watcher](#claude-watcher)** — Multi-frontend monitor for Claude Code sessions (GTK, TUI, web UI): live working/waiting status, per-session topics, subagent tracking.
* **[grip-live-diff](#grip-live-diff)** — Markdown preview with GitHub's look, word-level diff of every save, and in-page annotations an agent answers through a JSON5 sidecar.
* **[Teams Notifier](#teams-notifier)** — Bot + APIs replacing retired MS Teams webhooks: per-conversation tokens, message lifecycle (post/update/delete), GitLab MR and Jira cards.
* **[multiping](#multiping)** — ICMP/TCP multi-target probing CLI with state-transition logging. 31 stars on GitHub.
* **[phototag](#phototag)** — Offline photo-tagging tool — RAM++ open-vocab labels, CLIP embeddings, UMAP+HDBSCAN clustering, RetinaFace/ArcFace face pipeline. CLI + FastAPI UI.
* **[aNag](#anag)** — Unofficial Nagios/Icinga/Thruk Android client. 100K+ installs, 4.7★ on Google Play.

## AI & LLM Tooling

### Inkwest

https://github.com/inkwest/inkwest

`inkwest` is an AI-powered Kubernetes debugging assistant. A shared web interface that lets developers diagnose cluster issues in plain language — the AI runs kubectl commands and explains what's going on. Acts as a controlled read-only proxy, removing the need for direct cluster access. Features multi-cluster support, session persistence, OIDC authentication, budget management, and multiple AI provider backends.

### claude-quota

https://github.com/babs/claude-quota

`claude-quota` is a systray widget that displays Claude API quota utilization. Reads OAuth credentials from Claude Code CLI, polls the usage API, and renders a color-coded icon with live percentages. Multiple indicator styles (pie, bar, arc), burn-rate projection, and self-update from GitHub releases. Cross-platform: Linux, Windows, macOS.

|         Systray icon          |              Hover tooltip              |             Context menu              |
| :---------------------------: | :-------------------------------------: | :-----------------------------------: |
| ![Systray icon](https://raw.githubusercontent.com/babs/claude-quota/master/img/icon.png) | ![Hover tooltip](https://raw.githubusercontent.com/babs/claude-quota/master/img/hover-tooltip.png) | ![Context menu](https://raw.githubusercontent.com/babs/claude-quota/master/img/context-menu.png) |

### claude-watcher

https://github.com/claude-watcher

`claude-watcher` is a multi-frontend monitor for Claude Code sessions (GTK widget, TUI, and web UI) showing live working/waiting/idle status derived from transcripts, per-session topic lines, subagent counts, and worktree sessions. Co-maintained; I contribute across the [gtk](https://github.com/claude-watcher/gtk), [tui](https://github.com/claude-watcher/tui), and [webui](https://github.com/claude-watcher/webui) frontends.

### claude-code-sandbox

https://github.com/babs/claude-code-sandbox

`claude-code-sandbox` is a Docker-based sandbox for running Claude Code CLI in an isolated container with persistent credentials.

### skills

https://github.com/babs/skills

`skills` is my Claude Code skills collection, packaged to install two ways from the same repo: as a Claude Code plugin/marketplace (`claude plugin install babs@babs-skills`) and as [skills.sh](https://skills.sh) skills, usable from Cursor, Codex, and any agent reading the `SKILL.md` standard. 13 skills covering project scaffolding (`go-init`, `python-init`, `fullstack-init`, `dockerfile-init`), a layered review pipeline (`my-review`, `iterative-review`, `swarm-review`), and a spec → implement → ship workflow (`spec-feature`, `ship-feature`, `implement-loop`, `smart-commit`).

### grip-live-diff

https://github.com/babs/grip-live-diff

`grip-live-diff` is a single Go binary that renders a Markdown file with GitHub's look, reloads on every save, and highlights what changed, word by word, inside the rendered page. Three diff references (since open, last save, git `HEAD`), a VS Code style minimap, and annotations: select a passage, type what should change, and the comment lands in a JSON5 sidecar next to the file that an agent answers in place. Built for reading a spec while Claude Code rewrites it. Forked from [go-grip](https://github.com/chrishrb/go-grip).

### phototag

https://github.com/babs/phototag

`phototag` is a local, single-user photo-tagging and face-management tool. Scans a folder, tags every image with **RAM++** (~4500 open-vocabulary labels), embeds with **CLIP** for semantic search, clusters with **UMAP + HDBSCAN** to surface the corpus's natural taxonomy, and optionally detects + clusters faces via RetinaFace + ArcFace. CLI plus a single-page FastAPI UI. Runs offline — no telemetry, no cloud.

## Mobile

### aNag

https://play.google.com/store/apps/details?id=info.degois.damien.android.aNag

`aNag` is the unofficial [Nagios](https://www.nagios.org/) / [Icinga](https://icinga.com/) / [Thruk](https://www.thruk.org/) / [Naemon](https://www.naemon.io/) client for Android. Features custom notifications, passive check submission, enable/disable notifications, recheck, and downtime management. 100K+ installs, 4.7 stars on Google Play.

### aNag-backup-codec

https://github.com/babs/aNag-backup-codec

`aNag-backup-codec` converts aNag preference backups (`.bak`) to and from a hybrid JSON format, for inspection, diffing, bulk edits, and migration between installs.

## Networking & DNS

### multiping

https://github.com/babs/multiping

`multiping` is a CLI tool to monitor several targets at once using ICMP or TCP probing, with optional logging of state transitions to a file.

#### `multiping` demo
![Demo01](https://raw.githubusercontent.com/babs/multiping/master/_demo/demo-001.svg)

### ebpf4fun-ring

https://github.com/babs/ebpf4fun-ring

`ebpf4fun-ring` is an eBPF experimentation project for DNS packet capture using BPF ring buffers. Monitors network interfaces and captures DNS queries/responses for inspection.

### filtering-dns-reverseproxy

https://github.com/babs/filtering-dns-reverseproxy

`filtering-dns-reverseproxy` is a filtering DNS reverse proxy to expose part of some zones publicly (e.g. Let's Encrypt challenges, domain delegation) without leaking private records or falling into split-horizon DNS.

### phpipam2dns

https://github.com/babs/phpipam2dns

`phpipam2dns` applies phpIPAM changelog entries to DNS via dynamic updates (RFC 2136). Also my first Go project.

## Kubernetes & DevOps

### Cosanet

https://github.com/cosanet/cosanet

`cosanet` is a Prometheus exporter for collecting advanced network statistics from Linux hosts and Kubernetes pods. Deployed as a DaemonSet, it collects metrics from all container sandboxes (conntrack, /proc/net/snmp, netstat) without requiring instrumentation of individual pods.

### externalsecrets-refresh

https://github.com/babs/externalsecrets-refresh

`externalsecrets-refresh` is a container designed as a Kubernetes Job that triggers ExternalSecrets to refresh by patching their annotations and monitors completion. Built for Helm Charts and ArgoCD workflows.

### argocd-app-helm-version

https://github.com/babs/argocd-app-helm-version

`argocd-app-helm-version` checks and updates Helm chart versions in ArgoCD Application manifests. Recursively scans directories for YAML files and can auto-update outdated chart references.

### helm-charts

https://github.com/babs/helm-charts

Personal Helm charts repository.

```bash
helm repo add babs https://babs.github.io/helm-charts
```

* `babs/extra-objects` — a chart that instantiates objects from an `extraObjects` array. Useful when a primary Helm chart lacks this support.

### helm-registry-mirrors

https://github.com/babs/helm-registry-mirrors

Helm chart that deploys multiple OCI registry mirrors in one shot — `docker.io`, `quay.io`, `gcr.io`, `ghcr.io`, `public.ecr.aws` — with per-mirror storage and ingress configuration.

### k8s-ps1.sh

https://github.com/babs/k8s-ps1.sh

Bash shell extension that shows the current Kubernetes context in your prompt. Toggle with `Ctrl+T`.

```bash
source k8s-ps1.sh
PS1="${K8S_EXT}\001\e[1;34m\002[\t]\001\e[1;${USERCOLOR}m\002[\u@\h] \001\e[0;36m\002\w${GIT_EXT} ${CHAR}\001\e[0m\002 "
```

### pre-commit-hooks

https://github.com/babs/pre-commit-hooks (replaces https://github.com/babs/check-argocd-yaml)

* `check-argocd-yaml` — pre-commit hook to enforce readability and maintainability in ArgoCD Application manifests.

## CI/CD & Containers

### kaniko-build/builder

https://github.com/kaniko-build/builder

`kaniko-build/builder` builds and publishes OCI images from public Kaniko forks ([osscontainertools](https://github.com/osscontainertools/kaniko), [chainguard-forks](https://github.com/chainguard-forks/kaniko)) to GHCR, providing ready-to-use executor and warmer images.

### ecr-prime

https://github.com/babs/ecr-prime

`ecr-prime` is a write-first Amazon ECR create-on-push primer for cross-account pushes (IRSA / Pod Identity). Single static binary.

### ecr-repo-creator

https://github.com/babs/ecr-repo-creator

`ecr-repo-creator` creates AWS ECR repositories if missing, statically built with no dependencies. Can apply policies on newly created repos. Includes a [GitLab CI component example](https://github.com/babs/ecr-repo-creator/blob/master/glci-example).

### oci-toolbox

https://github.com/babs/oci-toolbox

`oci-toolbox` is an OCI image bundling tools for container image and Helm chart operations: skopeo, oras, helm, jq, yq, ecr-repo-creator, and more.

### pre-commit-image

https://github.com/babs/pre-commit-image

`pre-commit-image` tracks `pre-commit` releases and auto-builds a Debian bookworm slim Docker image, published to GHCR, Quay.io, and Docker Hub.

### skopeo-static

https://github.com/babs/skopeo-static

`skopeo-static` provides a static build of [skopeo](https://github.com/containers/skopeo) for environments where dynamic linking isn't practical.

## Libraries & Middleware

### h2r2h

https://github.com/h2r2h

`h2r2h` is an HTTP-to-RabbitMQ-to-HTTP async replay system:
* [`h2r`](https://github.com/h2r2h/h2r) — accepts HTTP requests and publishes them to RabbitMQ
* [`r2h`](https://github.com/h2r2h/r2h) — consumes messages and replays them as HTTP requests to a target service

### fastapi-structured-logging

https://github.com/babs/fastapi-structured-logging

`fastapi-structured-logging` is a Python module providing structured logging and access log middleware for FastAPI. Configures `structlog` for JSON or console output with OpenTelemetry trace/span enrichment.

### db_migrate

https://github.com/babs/db_migrate

`db_migrate` is a dbmate-style async PostgreSQL migration runner. Single-file, zero-framework, using asyncpg and structlog. Supports create, apply, status, and rollback.

### runstats

https://github.com/babs/runstats

`runstats` wraps any command and reports resource usage metrics (memory, CPU time, I/O, context switches) as JSON to stderr, while transparently passing through stdin/stdout/stderr.

### blibs

https://github.com/babs/blibs

Personal Python helpers — colored logging setup and other utilities.

```python
from blibs import init_root_logger
init_root_logger(level=10)
```

## Auth & Identity

### bifrons

https://github.com/bifrons-sh/bifrons

`bifrons` is a database access portal: auth-remapping proxies for MySQL, PostgreSQL and MongoDB fronted by a Go control plane. Users log in with OIDC, request access through a dual-gate approval workflow, and the proxy transparently remaps their identity to real database credentials. No shared passwords, full audit trail.

### mcp-auth-proxy

https://github.com/babs/mcp-auth-proxy

`mcp-auth-proxy` is an OAuth 2.1 authorization server that fronts any OIDC IdP, so MCP clients (Claude Desktop, Cursor, Claude Code, MCP Inspector) can talk to a private MCP server without writing any auth code. Strict OAuth 2.1 posture, replay protection, per-tool metrics with cardinality cap, configurable rate limits on `/.well-known/*`, security-headers middleware, and STRIDE-modeled threat coverage.

### Teams Notifier

https://github.com/teams-notifier — docs at [teams-notifier.github.io](https://teams-notifier.github.io/)

`Teams Notifier` replaces the retired MS Teams webhooks with a bot and a set of APIs to post, update and delete messages in channels and group chats, with a dedicated token per user and conversation for auditability. Core and add-ons:

* [`bf-directline-endpoint`](https://github.com/teams-notifier/bf-directline-endpoint) — Bot Framework endpoint: receives Teams events and issues a conversation token by private message when the bot is @mentioned.
* [`activity-api`](https://github.com/teams-notifier/activity-api) — send / update / delete messages against a conversation token; addresses each conversation at its own Teams service URL.
* [`gitlab-mr-api`](https://github.com/teams-notifier/gitlab-mr-api) — one card per merge request, updated through its lifecycle from GitLab webhooks, deleted on merge or close.
* [`jira-api`](https://github.com/teams-notifier/jira-api) — expandable issue cards from Jira webhooks or Jira Automation, HMAC-authenticated.

![Merge request card](https://teams-notifier.github.io/docs/deployment/addons/gitlab-mr-api/merge-request-card-example.png)

### observium-header-authentication

https://github.com/babs/observium-header-authentication

`observium-header-authentication` enables header-based authentication for [Observium](https://www.observium.org/), allowing OIDC via [oauth2-proxy](https://oauth2-proxy.github.io/oauth2-proxy/).

### oauth2-rp

https://github.com/babs/oauth2-rp

`oauth2-rp` is an OAuth2 reverse proxy for Keycloak with dedicated API route filtering (API key vs headers).

### keycloak-phpipam-is-admin-mapper

https://github.com/babs/keycloak-phpipam-is-admin-mapper

SAML2 Keycloak mapper for the phpIPAM admin attribute, with a multi-stage Docker build example.

## Fun & Creative

### trollvatar

https://github.com/babs/trollvatar

`trollvatar` adds a customizable LinkedIn-style "#OPENTOWORK" arc overlay on any avatar image. Runs entirely in the browser — no server, no dependencies.

**Try it:** [babs.github.io/trollvatar](https://babs.github.io/trollvatar/)

### ram-eater

https://github.com/babs/ram-eater

`ram-eater` is a small C tool that consumes RAM by the GB to test resource limitation behaviors. Also available as [beardedbabs/ram-eater](https://hub.docker.com/r/beardedbabs/ram-eater).

## Plugins & Browser Scripts

### phpipam-enhancer.user.js

https://github.com/babs/phpipam-enhancer.user.js

[Tampermonkey](https://www.tampermonkey.net/) script for [phpIPAM](https://phpipam.net/) that adds http/https links and clipboard copy next to IPs and hostnames.

#### Examples on demo.phpipam.net

![Example on subnet view](https://raw.githubusercontent.com/babs/phpipam-enhancer.user.js/main/img/demo.phpipam.net-subnetview.png)

![Example on search result](https://raw.githubusercontent.com/babs/phpipam-enhancer.user.js/main/img/demo.phpipam.net-search-result-dark.png)

### dokuwiki-plugin-stlviewer

https://github.com/babs/dokuwiki-plugin-stlviewer

DokuWiki plugin to embed STL 3D model renders using the ViewSTL library.

## Hardware & Makers

### opendeck-plugins-rotary-volume

https://github.com/babs/opendeck-plugins-rotary-volume

[OpenDeck](https://github.com/nekename/OpenDeck) plugin (Rust) to control audio volume via rotary encoder on Linux. Supports PipeWire and PulseAudio backends, configurable volume step, max volume cap, and a long-press shell command.

### opendeck-plugins-rotary-command

https://github.com/babs/opendeck-plugins-rotary-command

[OpenDeck](https://github.com/ninjadev64/OpenDeck) plugin (Rust) that maps rotary encoder actions (CW, CCW, press, long press) to custom shell commands. All four commands are configured per-instance via the property inspector.

### cnc-linuxcnc-nowforever_vfd

https://github.com/babs/cnc-linuxcnc-nowforever_vfd

LinuxCNC HAL userspace driver for Nowforever E100 VFD over RS485 Modbus RTU.

### marlin-config-tracking-build-script

https://github.com/babs/marlin-config-tracking-build-script

`marlin-config-tracking-build-script` tracks configuration changes between Marlin firmware builds on PlatformIO.

## Legacy

### pyrowl

https://github.com/babs/pyrowl

Python module for the Prowl/NotifyMyAndroid push notification API.

### amqp2mongo

https://github.com/babs/amqp2mongo

Dumps RabbitMQ messages into MongoDB with TTL-indexed collections for message tracking.

### SaltStack Formulas

SaltStack formulas: [formula-k8s](https://github.com/babs/formula-k8s) for Kubernetes cluster bootstrapping, [formula-autostate](https://github.com/babs/formula-autostate) for pillar-driven state application, and [formula-TEMPLATE](https://github.com/babs/formula-TEMPLATE) for formula scaffolding.

### android-customfonthtml

https://github.com/babs/android-customfonthtml

Android library for custom font rendering with an `Html.fromHtml`-like API.

### MuninNode.net

https://github.com/babs/MuninNode.net

A .NET reimplementation of MuninNode for Windows monitoring.
