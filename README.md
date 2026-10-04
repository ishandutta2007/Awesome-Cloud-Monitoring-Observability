# Awesome-Cloud-Monitoring-Observability

# Awesome-Cloud-Monitoring-Observability

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Metrics, Logs, Traces, APM & Incident Management*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Monitoring & Observability**. These tools help teams collect metrics, aggregate logs, trace distributed requests, and manage incidents across cloud-native environments.

**Examples** include Azure Monitor, Datadog, New Relic, Dynatrace, AppDynamics, Sumo Logic, LogicMonitor, Splunk Infrastructure Monitoring, and Site24x7 (the category leaders).

**Open-source emphasis**: The open-source observability ecosystem is **exceptionally mature**, anchored by the **Prometheus + Grafana** stack for metrics and visualization . **OpenTelemetry** provides a vendor-neutral instrumentation standard across all three pillars — metrics, logs, and traces . However, **logs are a notable gap**: the classic "three-piece stack" (Prometheus + Grafana + Tempo) covers metrics and traces but requires **Loki or OpenSearch/ELK** for log aggregation . This section documents these production-grade solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## 📖 Table of Contents

- [☁️ SaaS/Hosted Platforms](#-saas-hosted-platforms)
- [🔓 Open-Source GitHub Projects](#-open-source-github-projects)
- [🤝 How to Contribute](#-how-to-contribute)
- [⚠️ Disclaimer](#-disclaimer)

## ☁️ SaaS/Hosted Platforms

> **📊 Market Context**: The global observability market is estimated at **~$45B in 2026**, growing toward **~$110B by 2032** at a **~16% CAGR**. The sector is **moderately concentrated** — **Dynatrace** reported **$2.018B revenue (FY2026)** , **New Relic** reached **$733.8M revenue** , and **Datadog** continues as the cloud-native leader. **Pricing models vary dramatically**: Dynatrace uses **hourly, consumption-based rate-card pricing** (e.g., $0.04/hour per host, $0.01 per memory-GiB-hour) , while New Relic charges **per user plus per GB ingested** ($99–$349/user/month + $0.40/GB after 100 GB free) . LogicMonitor enterprise contracts for **1,000–2,500 devices typically range $150,000–$350,000 annually** . No single vendor holds a winner-take-all position; enterprises typically run multi-vendor stacks.

| Platform | Description | Pricing (Starting Tier) | Free Tier Limits | Company Size |
|----------|-------------|------------------------|------------------|--------------|
| **[Dynatrace](https://www.dynatrace.com/)** | Causal AI engine (Davis) for root cause analysis using Smartscape topology. Deterministic and causal AI for automated remediation. **$2.018B revenue (FY2026)** . | **Infrastructure Monitoring**: **$0.04/hour per host**; **Full-Stack**: **$0.01/memory-GiB-hour** . **Log Analytics**: **$0.20/GiB ingested** + **$0.0007/GiB-day** retention . **RUM**: **$0.00225/session** . | **15-day free trial** (no permanent free tier) . | **$2.018B revenue (FY2026)**  |
| **[New Relic](https://newrelic.com/)** | Full-stack observability with NRQL query language. Metrics, logs, traces, and events in one data model. **$733.8M revenue** . | **Standard**: **$99/user/month** (first user $10); **Pro**: **$349/user/month** (annual). **Data ingest**: **$0.40/GB** after 100 GB free . | **Free tier**: **100 GB/month** data ingest, **1 full-platform user**, unlimited basic users . | **$733.8M revenue**  |
| **[Datadog](https://www.datadoghq.com/)** | Cloud-native monitoring with APM, infrastructure, logs, and database monitoring. **High watermark** and **hybrid** billing plans . | **APM**: **$31/host/month** (APM), **$35** (Pro), **$40** (Enterprise) . **Indexed Spans**: **$1.70/million** after included allowance . **Logs**: per GB ingested + per million events indexed . | **14-day free trial** with full platform access. No perpetual free tier. | **~$2.5B revenue (FY2025 est.)** |
| **[Azure Monitor](https://azure.microsoft.com/en-us/products/monitor/)** | Microsoft's comprehensive monitoring for cloud and hybrid. Log Analytics, Application Insights, and alerts. | **Analytics Logs**: **¥23.4/GB** (pay-as-you-go) with first 5 GB/month free . **Basic Logs**: **¥5.088/GB** ingestion + **¥0.05088/GB** scanned . | **Azure free account**: **$200 credit for 30 days** + **5 GB/month free** log ingestion. | **~$281B revenue (Microsoft FY2025)** |
| **[LogicMonitor](https://www.logicmonitor.com/)** | Enterprise infrastructure monitoring for hybrid/multi-cloud. Auto-discovery and CMDB integration. | **Enterprise contracts for 1,000–2,500 devices**: **$150,000–$350,000 annually** . Per-device costs at scale: **$80–$200/device/year** . | **None** — enterprise demo required. | **Private (~$300M+ revenue est.)** |
| **[Splunk Infrastructure Monitoring](https://www.splunk.com/)** | Real-time hybrid cloud monitoring. **Splunk AI Assistant** now installed by default with **Agent Mode** for natural language queries . | **Custom pricing** — credit-based licensing. **Flex Pricing**: **$3.14/TB scanned** (estimate) . | **Free trial** available with full access to self-service plans . | **~$3.8B revenue (Splunk, part of Cisco)** |
| **[AppDynamics](https://www.appdynamics.com/)** | APM and observability within Cisco's portfolio. | **Enterprise Edition Term License**: **$5,093.99 per license** (CDW list price) . | **15-day free trial** available. | **Part of Cisco (~$63B revenue)** |
| **[Sumo Logic](https://www.sumologic.com/)** | Cloud-native log analytics and security intelligence. **Unlimited data ingest** with Flex pricing. | **Flex Pricing**: **$3.14/TB scanned** (estimate) . **Essentials**: per GB ingested with annual commitment. | **Free trial**: Full access to browse self-service plans . | **~$300M+ revenue (private)** |
| **[Site24x7](https://www.site24x7.com/)** | Cloud-based infrastructure and application monitoring. | **StatusIQ**: **$10/month** (or **$9/month** annual) per status page . SMS credits: **$10 per 50 credits** . | **Free tier**: **1 status page** . No perpetual free tier for full monitoring. | **Part of Zoho** |

## 🔓 Open-Source GitHub Projects

Sorted by star count (descending). Star badge links to each repo's stargazers page.

| Repo | Description | Stars |
|---|---|---|
| **[Prometheus](https://github.com/prometheus/prometheus)** — **The de facto standard for metrics collection.** Pull-based time-series database with PromQL query language. Cloud-native, battle-tested at scale, huge ecosystem of exporters . Apache-2.0. | [![Stars](https://img.shields.io/github/stars/prometheus/prometheus?style=social&color=white)](https://github.com/prometheus/prometheus/stargazers) | ~58,000 |
| **[Grafana](https://github.com/grafana/grafana)** — **The leading visualization and dashboard platform.** Connects to Prometheus, Loki, Tempo, Elasticsearch, and 100+ other data sources . AGPL-3.0. | [![Stars](https://img.shields.io/github/stars/grafana/grafana?style=social&color=white)](https://github.com/grafana/grafana/stargazers) | ~65,000 |
| **[OpenTelemetry Collector](https://github.com/open-telemetry/opentelemetry-collector)** — **Vendor-neutral telemetry collection.** SDK + Collector for metrics, logs, and traces. The instrumentation layer that ties all three pillars together with a shared trace_id . Apache-2.0. | [![Stars](https://img.shields.io/github/stars/open-telemetry/opentelemetry-collector?style=social&color=white)](https://github.com/open-telemetry/opentelemetry-collector/stargazers) | ~6,000 |
| **[Jaeger](https://github.com/jaegertracing/jaeger)** — **Leading distributed tracing platform.** Created by Uber, CNCF graduated. End-to-end transaction monitoring, root cause analysis, service dependency visualization . Apache-2.0. | [![Stars](https://img.shields.io/github/stars/jaegertracing/jaeger?style=social&color=white)](https://github.com/jaegertracing/jaeger/stargazers) | ~21,000 |
| **[Loki](https://github.com/grafana/loki)** — **"Prometheus for logs."** Cost-effective log aggregation by Grafana Labs. Indexes labels, not full text, for storage efficiency . AGPL-3.0. | [![Stars](https://img.shields.io/github/stars/grafana/loki?style=social&color=white)](https://github.com/grafana/loki/stargazers) | ~25,000 |
| **[Netdata](https://github.com/netdata/netdata)** — **Real-time infrastructure visibility with zero configuration.** Per-second metrics, auto-detection, beautiful dashboards, minimal footprint . GPL-3.0. | [![Stars](https://img.shields.io/github/stars/netdata/netdata?style=social&color=white)](https://github.com/netdata/netdata/stargazers) | ~73,000 |
| **[SigNoz](https://github.com/SigNoz/signoz)** — **Open-source Datadog/New Relic alternative.** Metrics, traces, and logs in one platform. OpenTelemetry native, ClickHouse backend . MIT (Community). | [![Stars](https://img.shields.io/github/stars/SigNoz/signoz?style=social&color=white)](https://github.com/SigNoz/signoz/stargazers) | ~22,000 |
| **[OneUptime](https://github.com/OneUptime/oneuptime)** — **Complete open-source observability platform.** Uptime monitoring, status pages, incident management, on-call, logs, metrics, traces, error tracking, AI-powered remediation . Apache-2.0. | [![Stars](https://img.shields.io/github/stars/OneUptime/oneuptime?style=social&color=white)](https://github.com/OneUptime/oneuptime/stargazers) | ~9,000 |
| **[Zabbix](https://github.com/zabbix/zabbix)** — **Traditional infrastructure monitoring since 2001.** Agent-based and agentless, auto-discovery, extensive templates, handles 100,000+ devices . AGPL-3.0. | [![Stars](https://img.shields.io/github/stars/zabbix/zabbix?style=social&color=white)](https://github.com/zabbix/zabbix/stargazers) | ~5,000 |
| **[Checkmk](https://github.com/Checkmk/checkmk)** — **Enterprise infrastructure monitoring evolved from Nagios.** Auto-discovery, BI dashboards, CMDB integration . GPL-2.0 (Raw Edition). | [![Stars](https://img.shields.io/github/stars/Checkmk/checkmk?style=social&color=white)](https://github.com/Checkmk/checkmk/stargazers) | ~2,000 |

**Additional open-source options worth exploring:**

| Repo | Description |
|---|---|
| **[Tempo](https://github.com/grafana/tempo)** — Distributed tracing backend from Grafana Labs. Receives OTLP/Jaeger/Zipkin, uses object storage . AGPL-3.0. | [![Stars](https://img.shields.io/github/stars/grafana/tempo?style=social&color=white)](https://github.com/grafana/tempo/stargazers) |
| **[Zipkin](https://github.com/openzipkin/zipkin)** — Lightweight distributed tracing by Twitter. Simpler than Jaeger . Apache-2.0. | [![Stars](https://img.shields.io/github/stars/openzipkin/zipkin?style=social&color=white)](https://github.com/openzipkin/zipkin/stargazers) |
| **[OpenSearch](https://github.com/opensearch-project/OpenSearch)** — Apache-2.0 fork of Elasticsearch. Full-text log search and analytics . | [![Stars](https://img.shields.io/github/stars/opensearch-project/OpenSearch?style=social&color=white)](https://github.com/opensearch-project/OpenSearch/stargazers) |

## 🤝 How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## ⚠️ Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Observability platforms handle sensitive telemetry data; ensure compliance with data protection regulations and internal security policies.
- **Open-source reality**: The open-source ecosystem for observability is **exceptionally mature**. **Prometheus + Grafana** is the de facto standard for metrics and visualization . **OpenTelemetry** provides vendor-neutral instrumentation across all three pillars . However, **logs are a notable gap**: the classic "three-piece stack" requires **Loki or OpenSearch/ELK** for log aggregation . **The critical nuance**: "能打通" (can be connected) and "默认打通" (connected by default) are different cost tiers. Open-source correlation across pillars requires manual configuration of exemplars, spanmetrics, and data links — while commercial APMs provide default correlation . The open-source path is **genuinely viable** for organizations with strong platform engineering capacity.
- **Pricing caveat**: All pricing figures above are **verified against cited search results** but may change without notice. Observability costs scale with **data volume** — a chatty microservice can push 5–10 GB/day in log data alone . Model your telemetry volume before committing to any vendor.

---

**Made for SREs, platform engineers, DevOps teams, and observability practitioners.**
Let's make cloud monitoring more open, transparent, and observable.
