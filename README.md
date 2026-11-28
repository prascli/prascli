<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark-v2.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/banner-light-v2.svg">
  <img src="assets/banner-dark-v2.svg" alt="Indra Prasetya, Senior Software Engineer, backend and platform engineering">
</picture>

# Indra Prasetya <img align="right" src="https://komarev.com/ghpvc/?username=prascli&style=flat-square&color=gray&label=views" alt="profile views">

### Senior Software Engineer | Backend and Platform Engineering

I am a software engineer working on backend and platform systems. I have been
building software professionally since 2012, most of it in enterprise
environments: data migrations at telecommunications scale, database-heavy
services, and the delivery and monitoring work that keeps them running.

Day to day I work in Go, TypeScript and Python on PostgreSQL. At
[Qansa Solusi Indonesia](https://www.qansa.id) I build systems for clients and
maintain our open-source tooling. The rest of my time goes to developer tools
that remove a measurable cost, which is how
[agentdiet](https://github.com/qansaid/agentdiet) started.

[Email](mailto:indra@qansa.id) |
[LinkedIn](https://www.linkedin.com/in/prascli/) |
[GitHub](https://github.com/prascli) |
[qansa.id](https://www.qansa.id) |
[agentdiet.qansa.web.id](https://agentdiet.qansa.web.id)

---

## Engineering profile

- **Enterprise backend.** Service and data layers for systems where a wrong
  number matters, including customer data migration work for Telkomsel, one of
  Indonesia's largest telecommunications operators.
- **Databases and data movement.** PostgreSQL schema design, migrations,
  reconciliation, and the batch jobs around them.
- **Platform and delivery.** Containerised deployment with Docker and Compose,
  NGINX routing and caching, GitHub Actions pipelines, and release automation.
- **Observability.** Metrics, logs and alerting with Prometheus, Loki, Promtail
  and Grafana, including broker health checks that alert when a Kafka cluster
  degrades.
- **Open source.** Maintaining [qansaid](https://github.com/qansaid), where
  agentdiet and Qansa's tooling live, plus merged fixes to third-party projects
  listed below.

---

## Expertise

**Core.** Go, TypeScript and Node.js, Python, SQL and PostgreSQL, Bash.

**Platform and operations.** Docker and Compose, NGINX, GitHub Actions, Linux,
Git, Kafka with TLS and SASL-SCRAM, Prometheus, Loki, Grafana.

**Working knowledge.** Java and Spring Boot, from reviewed and tested changes
to a Spring Boot ERP codebase (pull requests in review upstream).

**Currently exploring.** Kubernetes, infrastructure as code, distributed
systems patterns, and tooling for AI coding agents.

---

## Flagship projects

### [agentdiet](https://github.com/qansaid/agentdiet)

Every AI coding agent loads its instruction files before it reads your request:
`AGENTS.md`, `CLAUDE.md`, `.cursorrules`, `copilot-instructions.md`. Those files
are paid for on every call, and most repositories never measure them.

agentdiet is a single static Go binary that measures that cost, keeps always-on
context separate from on-demand material, detects verbatim and near-duplicate
guidance, and fails CI when the always-on figure grows. On a simulated
repository it measured 6,770 always-on tokens at grade C and 711 at grade A, an
89.5 percent reduction. No account, no API key, no network call.

Stack: Go, GitHub Actions, Next.js product site. MIT licensed.
[source](https://github.com/qansaid/agentdiet) |
[site](https://agentdiet.qansa.web.id) |
`go install github.com/qansaid/agentdiet@latest`

### [gha-bill](https://github.com/prascli/gha-bill)

CI bills arrive after the cost is committed. gha-bill reads the workflow files
already in a repository and reports cost per workflow, per month, before the
invoice exists.

The interesting part is modelling what GitHub actually charges: per-job minute
rounding, operating system multipliers, and matrix expansion, computed from
triggers and schedules with no API token. Python CLI with a test suite, and a
CI workflow that runs it.

Stack: Python, GitHub Actions, CodeQL.

### [consistency-nginx](https://github.com/prascli/consistency-nginx)

A cache cluster only works when the same key lands on the same node, or the hit
rate collapses. This project builds a working demonstration: an NGINX router
using consistent hashing in front of two cache nodes and a backend, with a
script that proves routing is stable across requests.

Stack: NGINX, Docker Compose, Makefile, Shell.

### Repository status

Facts about each flagship repository, refreshed from the GitHub API.

<!-- PROJECTS:START -->
| Project | Release | Commit | License |
| --- | --- | --- | --- |
| [agentdiet](https://github.com/qansaid/agentdiet) | v0.1.8 | 12 days ago | MIT |
| [gha-bill](https://github.com/prascli/gha-bill) | none | 22 days ago | MIT |
| [consistency-nginx](https://github.com/prascli/consistency-nginx) | none | 18 days ago | MIT |
<!-- PROJECTS:END -->

---

## Other repositories

[kafka-security-ssl-sasl](https://github.com/prascli/kafka-security-ssl-sasl)
and [kafka-monitoring](https://github.com/prascli/kafka-monitoring):
operating a Kafka cluster is two problems, proving a broker is healthy and
seeing what it is doing. The first is a health checker for brokers behind TLS
and SASL-SCRAM, with retries and webhook alerts when a broker fails. The second
is a Compose stack that collects metrics and logs with Prometheus, Loki and
Promtail and visualises them in Grafana. Both are complete and stable rather
than under active development.

[backend-wis-mulai-hidup](https://github.com/prascli/backend-wis-mulai-hidup):
backend for a wedding invitation platform, with invitation and theme modules,
wedding media, transactional email and Prisma migrations on PostgreSQL.
Node.js, Express, TypeScript.

---

## Open source contributions

Merged pull requests into repositories I do not own.

Most of the merged work so far is in an open-source bug-bounty toolkit: fixes to
its installer, its HackerOne MCP integration and its documentation, each one made
after reproducing the failure.

<!-- CONTRIBUTIONS:START -->
- **[erkamyaman/unslop-anything](https://github.com/erkamyaman/unslop-anything)**: 1 merged pull request, latest 2026-11-27
  - fix(detect): flag Quasar and Element Plus images without alt ([#256](https://github.com/erkamyaman/unslop-anything/pull/256), merged 2026-11-27)
- **[coherera/quelor](https://github.com/coherera/quelor)**: 1 merged pull request, latest 2026-11-27
  - classify: add Docker Hub pull rate limit classifier ([#72](https://github.com/coherera/quelor/pull/72), merged 2026-11-27)
- **[getsentry/sentry-dotnet](https://github.com/getsentry/sentry-dotnet)**: 1 merged pull request, latest 2026-11-26
  - fix(profiling): link Android troubleshooting docs from build error ([#6025](https://github.com/getsentry/sentry-dotnet/pull/6025), merged 2026-11-26)
- **[viktorstrate/mactrix](https://github.com/viktorstrate/mactrix)**: 1 merged pull request, latest 2026-11-26
  - fix(tui): enable create room when a window is focused ([#146](https://github.com/viktorstrate/mactrix/pull/146), merged 2026-11-26)
- **[ClickHouse/loom](https://github.com/ClickHouse/loom)**: 1 merged pull request, latest 2026-11-26
  - fix(hooks): keep error text on failure events ([#1499](https://github.com/ClickHouse/loom/pull/1499), merged 2026-11-26)
- **[pyrite-wiki/pyrite](https://github.com/pyrite-wiki/pyrite)**: 1 merged pull request, latest 2026-11-25
  - fix(search): drop stop words from keyword fallback ([#1882](https://github.com/pyrite-wiki/pyrite/pull/1882), merged 2026-11-25)
- **[CurvineIO/curvine](https://github.com/CurvineIO/curvine)**: 1 merged pull request, latest 2026-11-25
  - fix(python-sdk): accept fsspec mode in CurvineFileSystem.open (#2317) ([#2547](https://github.com/CurvineIO/curvine/pull/2547), merged 2026-11-25)
- **[Kolgrim33/broom](https://github.com/Kolgrim33/broom)**: 1 merged pull request, latest 2026-11-24
  - feat(ecosystems): add marker-verified Bazel artifact rules ([#6](https://github.com/Kolgrim33/broom/pull/6), merged 2026-11-24)
<!-- CONTRIBUTIONS:END -->

Also credited: [garrytan/gstack#4085](https://github.com/garrytan/gstack/pull/4085),
merged 2026-11-06, where my work appears as a `Co-authored-by` trailer on commit
[5e2964d](https://github.com/garrytan/gstack/commit/5e2964d). The pull request
belongs to the maintainer, so it does not appear in the generated list.

---

## Engineering practice

- **Measure the cost before optimising it.** Token budgets, CI spend and broker
  health all start as numbers nobody looked at.
- **Keep failures visible.** Services that report staleness, truncation and
  partial results are easier to operate than services that only report success.
- **Automate the repeatable part.** Migrations, releases and health checks
  should behave the same at 03:00 as they do on a laptop.
- **Write the documentation with the change.** A tool nobody can install is not
  shipped, which is why each repository above carries run and verify steps.
- **Prefer the smallest design that survives production.** Fewer moving parts
  means fewer things to get paged about.

---

## Current focus

- Kubernetes and infrastructure as code, moving from Compose-based deployment
  toward declarative platforms.
- Tooling for AI coding agents, starting with context cost in agentdiet.
- Observability at the level of individual services, not only host metrics.
- Distributed systems patterns, currently consistent hashing and cache routing.

---

## Activity

<!-- STATS:START -->
| Metric | Value |
| --- | --- |
| Contributions, last 12 months | 928 |
| Commits, last 12 months | 367 |
| Pull requests opened, last 12 months | 221 |
| Private contributions, last 12 months | 225 |
| Merged pull requests authored, all time | 152 in 53 repositories |
| Merged upstream, all time | 66 in 44 repositories |

_Refreshed 2026-11-28 from the GitHub API._
<!-- STATS:END -->

<a href="https://github.com/prascli">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=prascli&theme=dark&hide_border=true&short_numbers=true">
    <source media="(prefers-color-scheme: light)" srcset="https://streak-stats.demolab.com?user=prascli&theme=default&hide_border=true&short_numbers=true">
    <img src="https://streak-stats.demolab.com?user=prascli&theme=dark&hide_border=true&short_numbers=true" alt="GitHub streak: total contributions, current streak and longest streak">
  </picture>
</a>

---

## Contact

- Email: [indra@qansa.id](mailto:indra@qansa.id)
- LinkedIn: [Indra Prasetya](https://www.linkedin.com/in/prascli/)
- GitHub: [@prascli](https://github.com/prascli)
- Company: [Qansa Solusi Indonesia](https://www.qansa.id)
- Product: [agentdiet.qansa.web.id](https://agentdiet.qansa.web.id)

Open to remote backend and platform engineering work.
