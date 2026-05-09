# Diogo Vilela

Senior Software Engineer / Tech Lead based in Switzerland. I build and ship Kubernetes platform tooling — operators, kubectl plugins, distribution channels — for the engineers who have to live with them.

The IC craft is the headline; the lead role is what happens when you stay close enough to the code to write the tools your team needs.

---

## What I work on professionally

Currently Tech Lead at [Nexthink](https://www.nexthink.com) in Lausanne, in the **Data Platform group** — leading a team of senior engineers responsible for the traffic in and out of the platform: endpoint ingestion, configuration distribution, and update delivery across **20M+ connected endpoints** globally. The work spans Kubernetes, Apache Kafka, and cloud-native Java microservices.

The platform operates at:
- **>1M messages/s** ingested from **19M+ devices**
- **>150K notifications/s** delivered back to those devices

Currently leading:
- **Dynamic configuration propagation** to the endpoint fleet
- **Refactoring the downstream communication channel** — the >150K notifications/s path from platform to endpoints

Previously led:
- **Observability improvements** across the platform
- The **autoscaling pilot using [KEDA](https://keda.sh)** for the ingestion path

Previously a software engineer in **Sky's Global Commerce department**, on the systems behind [NOW](https://www.nowtv.com/), [Peacock](https://www.peacocktv.com/), [SkyShowtime](https://www.skyshowtime.com/), and [Showmax](https://www.showmax.com/) — including:
- Part of **Peacock's exclusive AFC Wild Card Game stream** — the biggest live-streamed event in the U.S., consuming **30% of internet traffic** during the game
- Building a **Kubernetes controller** for cluster-wide audit logging of user actions
- **Launching 2 streaming services across 66 territories**
- Leading the introduction of **Chaos Engineering** in the department

---

## Featured open-source work

### projection — Kubernetes CRD for declarative resource mirroring
**[github.com/projection-operator/projection](https://github.com/projection-operator/projection)** · [docs.projection.sh](https://docs.projection.sh)

A kubebuilder-based CRD operator that mirrors arbitrary Kinds — ConfigMaps, Secrets, custom resources — across namespace boundaries. Declarative, conflict-safe, watch-driven. Built for the recurring multi-tenant cluster pattern where the same configuration needs to live in many namespaces and the alternatives (manual copies, init scripts, CI templates) all fail in ways that are hard to debug.

Ships under Apache-2.0 with its own docs domain so it can be adopted without friction.

### kubectl-xctx — multi-context kubectl execution
**[github.com/be0x74a/kubectl-xctx](https://github.com/be0x74a/kubectl-xctx)**

A kubectl plugin that runs commands across every context matching a regex — `kubectl xctx 'prod-.*' get pods` returns answers from fifteen clusters instead of one. Distributed via my own krew tap:

```sh
kubectl krew index add be0x74a https://github.com/be0x74a/krew-index.git
kubectl krew install be0x74a/xctx
```

Building the distribution channel — the krew index, the release pipeline, the install path — taught me as much as building the tool itself.

### github-pr-quick-approve — keystroke-to-approval browser extension
**[github.com/be0x74a/github-pr-quick-approve](https://github.com/be0x74a/github-pr-quick-approve)** · **[Chrome Web Store](https://chromewebstore.google.com/detail/github-pr-quick-approve/hoomepimalbnnnmighljohjfidjnemoo?authuser=0&hl=en)**

A Chromium extension that collapses GitHub's five-click PR approval flow into one keystroke. Built because I review a lot of PRs and the friction was eating real time. The kind of internal-developer tool that quietly compounds.

---

## Upstream open-source contributions

Contributions to projects in the Kubernetes ecosystem:
- **[Kubernetes Autoscaler](https://github.com/kubernetes/autoscaler)**
- **[KEDA](https://keda.sh)** (CNCF graduated)
- **[go-github](https://github.com/google/go-github)**

---

## What ties this work together

- **Multi-context, multi-tenant ergonomics.** The kubectl plugin and the CRD operator solve the same problem in different layers: making one engineer effective across many namespaces, or many clusters, without per-tenant exceptions.
- **Distribution is part of the design.** The krew tap, the [homebrew tap](https://github.com/be0x74a/homebrew-tap), the Apache-2.0 license, the docs domain — those are infra decisions made up-front because the barrier to adoption *is* the product.
- **Boring-by-design.** Watch-driven controllers, conflict-safe mirroring, declarative semantics — these projects are optimized for "stop being interesting after week one" rather than for cleverness.

---

## Currently exploring

- **CRD ergonomics beyond `projection`.** Stronger admission-time guarantees and a multi-cluster story are the next questions I'm chasing.
- **AI as a force-multiplier in platform work.** `buddy` is my exploration of running personal LLM workflows end-to-end (Android + self-hosted backend) — the question I'm chasing is what platform tooling looks like when an agentic helper is part of the design instead of a layer on top.

---

## Get in touch

- Email: [diogofsvilela@gmail.com](mailto:diogofsvilela@gmail.com)
- LinkedIn: [linkedin.com/in/diogofsvilela](https://www.linkedin.com/in/diogofsvilela)

Based in Switzerland. Open to platform / Kubernetes / cloud-infrastructure conversations.
