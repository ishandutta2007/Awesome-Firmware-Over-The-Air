# Awesome-Firmware-Over-The-Air

# Top Website Monitoring Tools Ecosystem
**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Uptime Checks, Synthetic Monitoring, Status Pages, Alerting & Performance Observability*
**Last updated: August 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Website Monitoring / Uptime Monitoring**. These tools continuously probe websites, APIs, ports, SSL certificates, and services from global locations, detect downtime or degradation, send multi-channel alerts, and often provide public status pages and historical reporting.

**Examples** include Pingdom, UptimeRobot, Better Stack, Uptime.com, StatusCake, Site24x7, Freshping, HetrixTools, Hyperping, Montastic (the category leaders and popular options).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, full data ownership, unlimited monitors, config-as-code, and integration with existing observability stacks — ideal for developers, SREs, homelabbers, and companies building transparent, cost-controlled monitoring solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites / GitHub repos.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms
- **[Pingdom](https://www.pingdom.com/)**  
  Established SolarWinds tool for uptime, page-speed waterfalls, multi-step transaction monitoring, and real-user monitoring from 100+ global locations.
- **[UptimeRobot](https://uptimerobot.com/)**  
  Popular budget-friendly uptime monitor with a generous free tier (50 monitors), keyword checks, status pages, and broad alerting integrations.
- **[Better Stack](https://betterstack.com/)** (formerly Better Uptime)  
  Modern platform combining uptime monitoring, logs, on-call scheduling, incident management, and beautiful status pages.
- **[Uptime.com](https://uptime.com/)**  
  Enterprise-oriented monitoring with strong SLA reporting, synthetic checks, and multi-location coverage.
- **[StatusCake](https://www.statuscake.com/)**  
  Feature-rich monitoring supporting HTTP, TCP, DNS, SMTP, SSH, page-speed, domain, and SSL checks with status pages.
- **[Site24x7](https://www.site24x7.com/)**  
  Comprehensive Zoho/ManageEngine all-in-one suite covering website, synthetic, RUM, server, network, and cloud monitoring.
- **[Freshping](https://www.freshworks.com/)**  
  Simple Free-tier focused uptime monitoring (historically popular for 50 free monitors; check current availability).
- **[HetrixTools](https://hetrixtools.com/)**  
  Affordable uptime + IP/domain blacklist monitoring with free tier and useful server-oriented features.
- **[Hyperping](https://hyperping.com/)**  
  Clean all-in-one monitoring with fast check intervals, on-call, and polished status pages.
- **[Montastic](https://www.montastic.com/)**  
  Straightforward website uptime monitoring service focused on simplicity and reliability alerts.
- **[Checkly](https://www.checklyhq.com/)**  
  Developer-centric synthetic monitoring and API checks with Playwright, monitoring-as-code, and CI integration.
- **[Pulsetic](https://pulsetic.com/)**  
  Modern tool emphasizing beautiful status pages and multi-channel alerting.
- **[Oh Dear](https://ohdear.app/)**  
  Developer-friendly monitoring with consistent feature sets across plans and strong alerting.

## Open-Source GitHub Projects
- **[Uptime Kuma](https://github.com/louislam/uptime-kuma)**  
  The most popular self-hosted uptime monitor (90k+ stars). Beautiful reactive UI, 20+ monitor types (HTTP, TCP, Ping, DNS, Docker, etc.), 90+ notification channels, status pages, certificate monitoring, and easy Docker deployment.
- **[Gatus](https://github.com/TwiN/gatus)**  
  Lightweight, developer-oriented health dashboard written in Go. YAML config-as-code, advanced conditions (status, body, JSONPath, cert expiry), multi-protocol checks, badges, and very low resource usage.
- **[Upptime](https://github.com/upptime/upptime)**  
  Completely free uptime monitor and status page powered purely by GitHub Actions, Issues, and Pages — zero infrastructure required beyond a GitHub repo.
- **[OpenStatus](https://github.com/openstatusHQ/openstatus)**  
  Open-source status page + uptime/API monitoring platform with multi-region checks, monitoring-as-code (YAML/Terraform), and self-hostable architecture (AGPL).
- **[OneUptime](https://github.com/OneUptime/oneuptime)**  
  Full open-source observability platform replacing multiple SaaS tools: uptime monitoring, status pages, on-call, incident management, logs, traces, metrics, and APM (Apache 2.0).
- **[Kuvasz](https://github.com/kuvasz-uptime/kuvasz)**  
  Modern self-hosted uptime & SSL monitoring with status pages, YAML IaC support, full REST API, Prometheus/OpenTelemetry exporters, multi-user, and maintenance windows.
- **[Statping-ng](https://github.com/statping-ng/statping-ng)**  
  Actively maintained fork of Statping — single Go binary for HTTP/TCP/UDP/ICMP/gRPC monitoring, beautiful customizable status pages, graphs, and many notifiers.
- **[Healthchecks](https://github.com/healthchecks/healthchecks)**  
  Open-source cron job and “dead man’s switch” monitoring (Python/Django). Ideal for scheduled tasks, backups, and background jobs; also self-hostable with a rich dashboard and integrations.
- **[Prometheus + Blackbox Exporter](https://github.com/prometheus/blackbox_exporter)**  
  Industry-standard combination for probing HTTP, HTTPS, DNS, TCP, ICMP endpoints and feeding metrics into Prometheus + Alertmanager + Grafana dashboards.
- **[Cachet](https://github.com/cachethq/cachet)**  
  Classic open-source status page system focused on clear public communication of service status and incidents.
- **[Peekaping](https://peekaping.com/)** (open-source)  
  Modern Go + React self-hosted uptime monitor supporting HTTP, TCP, Ping, DNS, databases, Docker, gRPC, and branded status pages.
- **[Overcheck](https://github.com/overcheck/overcheck)**  
  API-first, config-as-code, multi-user self-hosted uptime monitor designed for teams that outgrow single-user tools (Postgres-backed).

### Additional Strong Open-Source Options
- **[Checkmate](https://github.com/bluewave-labs/checkmate)** — Modern UI with status pages and optional agent-based monitoring.
- **[HertzBeat](https://github.com/apache/hertzbeat)** — Apache project for comprehensive monitoring including websites, databases, and network devices.
- **[Netdata](https://github.com/netdata/netdata)** — Real-time metrics with some endpoint checking capabilities.
- **[Zabbix](https://github.com/zabbix/zabbix)** / **[Icinga](https://github.com/Icinga/icinga2)** / **[LibreNMS](https://github.com/librenms/librenms)** — Enterprise-grade open-source monitoring platforms that include website/service checks.
- Community tools built around **InfluxDB + Grafana**, **Node-RED**, or simple scripts using **curl + cron + notification webhooks**.

**Frameworks for building custom systems**: Combine **Uptime Kuma** or **Gatus** with **Prometheus + Grafana**, **Alertmanager**, **n8n/Node-RED** for workflows, and self-hosted status pages for fully owned, unlimited, transparent website monitoring stacks.

## How to Contribute
1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer
- This is a **community-curated** list — not exhaustive and not an endorsement.
- Website monitoring tools should be evaluated for false-positive rates, check frequency, data retention, and alerting reliability.
- Self-hosted open-source solutions require proper security hardening, high availability of the monitoring instance itself, and backup of historical data.
---
**Made for developers, SREs, DevOps engineers, agency owners, and anyone who wants reliable, transparent website & service monitoring.**
Let's make uptime monitoring more open, self-hostable, and developer-friendly.
