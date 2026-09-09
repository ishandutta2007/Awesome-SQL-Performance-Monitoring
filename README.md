# Awesome-SQL-Performance-Monitoring

## Top SQL Performance Monitoring Platforms Ecosystem
**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Query Analytics, Wait-Time Analysis, Index Advisors, Database Health, Explain Plans & Estate-Wide DBA Visibility*
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **SQL / Database Performance Monitoring**. These tools collect query statistics, wait events, plans, host metrics, and historical trends so DBAs and engineers can find slow queries, blocking, and configuration issues across PostgreSQL, SQL Server, MySQL, and other engines.

**Examples** include pganalyze, EverSQL, SolarWinds DPA, Redgate SQL Monitor, Quest Foglight, Datadog Database Monitoring, New Relic Database Monitoring, Percona PMM, DBmarlin, and SQL Diagnostic Manager (the category leaders).

**Open-source emphasis**: Database performance monitoring has excellent open options. **Percona PMM**, **pgwatch**, **pgHero**, **pgBadger**, Prometheus exporters + Grafana, and related projects deliver production-grade query analytics and dashboards. This section is heavily expanded with these tools.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms
- **[pganalyze](https://pganalyze.com/)**  
  Deep PostgreSQL-focused monitoring with query analysis, Index Advisor, VACUUM Advisor, auto_explain integration, and log correlation.

- **[EverSQL](https://www.eversql.com/)**  
  Automated SQL query optimization and indexing recommendations (often used alongside broader monitoring platforms).

- **[SolarWinds Database Performance Analyzer (DPA)](https://www.solarwinds.com/database-performance-analyzer)**  
  Wait-time based analysis across SQL Server, Oracle, PostgreSQL, and other platforms with historical trends and tuning guidance.

- **[Redgate SQL Monitor](https://www.red-gate.com/products/sql-monitor/)**  
  Estate-wide monitoring for SQL Server (and related) with strong plan-regression detection, blocking insight, and DBA-centric UX.

- **[Quest Foglight](https://www.quest.com/products/foglight/)**  
  Database and infrastructure performance monitoring with diagnostics for SQL Server and other platforms.

- **[Datadog Database Monitoring](https://www.datadoghq.com/product/database-monitoring/)**  
  Query metrics, explain plans, and wait analysis correlated with APM traces, infrastructure, and logs in the Datadog platform.

- **[New Relic Database Monitoring](https://newrelic.com/)**  
  Database query performance visibility linked to application traces and full-stack observability.

- **[DBmarlin](https://www.dbmarlin.com/)**  
  Cross-platform database performance monitoring with wait-based analysis and historical comparison.

- **[SQL Diagnostic Manager (Idera)](https://www.idera.com/)**  
  SQL Server monitoring with alerting, diagnostics, and performance analysis for DBA teams.

- **[Other commercial / cloud-native options](https://github.com/)**  
  Cloud provider consoles (AWS Performance Insights, Azure, GCP) and additional vendor tools often used alongside the platforms above.

## Open-Source GitHub Projects
- **[Percona Monitoring and Management (PMM)](https://github.com/percona/pmm)**  
  Leading open-source database monitoring and observability platform — Query Analytics (QAN), Prometheus + Grafana based, advisors, and support for MySQL, PostgreSQL, MongoDB, and more. Fully free to self-host.

- **[pgwatch / pgwatch2](https://github.com/cybertec-postgresql/pgwatch2)**  
  Self-hosted PostgreSQL metrics collector with flexible storage backends and ready-made Grafana dashboards.

- **[pgHero](https://github.com/ankane/pghero)**  
  Simple, actionable PostgreSQL performance dashboard — slow queries, index usage, space, connections, and more.

- **[pgBadger](https://github.com/darold/pgbadger)**  
  Fast PostgreSQL log analyzer that produces detailed HTML reports on queries, checkpoints, checkpoints, and errors.

- **[pg_stat_statements & pg_stat_monitor](https://www.postgresql.org/docs/current/pgstatstatements.html)**  
  Built-in and Percona-enhanced extensions that form the foundation of almost all PostgreSQL query monitoring.

- **[Prometheus + postgres_exporter / mysqld_exporter / sql_exporter](https://github.com/prometheus)**  
  Industry-standard metrics pipeline with official and community exporters for database engines, visualized in Grafana.

- **[Grafana database dashboards](https://grafana.com/grafana/dashboards/)**  
  Community and vendor dashboards for PostgreSQL, MySQL, SQL Server, and PMM that turn raw metrics into DBA views.

- **[DBA Dash and open SQL Server scripts](https://github.com/)**  
  Open-source and community tools focused on SQL Server wait stats, performance counters, and estate reporting.

- **[Netdata](https://github.com/netdata/netdata)**  
  Real-time, low-overhead monitoring with strong database charts and anomaly detection; can complement deeper query tools.

- **[Zabbix and other open monitoring platforms](https://www.zabbix.com/)**  
  General-purpose open monitoring that includes database templates and can be extended for SQL performance metrics.

### Additional Strong Open-Source Options
- Running **Percona PMM** as the central pane of glass for mixed MySQL/PostgreSQL/MongoDB fleets.
- Combining **pg_stat_statements / pg_stat_monitor** + **pgwatch** or **Prometheus** + **Grafana** for a fully open PostgreSQL stack.
- Using **pgHero** for quick, developer-friendly insight and **pgBadger** for deep log forensics.
- Exporting cloud database metrics (RDS, Cloud SQL, etc.) into Prometheus/PMM for consistent dashboards.
- Layering open wait-stat and index-usage scripts for SQL Server alongside commercial tools when needed.
- Preferring open stacks when data residency, cost at scale, or full control of retention matter most.

**Frameworks for building custom systems**: Enable native stats extensions → scrape with **PMM** or **Prometheus exporters** → store in Prometheus/Timescale → visualize and alert in **Grafana**. Add **pgBadger**/log analysis for historical depth. This stack is production-proven and free. Commercial platforms (pganalyze, Redgate, SolarWinds DPA, Datadog DBM, etc.) still lead in polished advisors, cross-engine correlation with APM, managed SaaS convenience, and specialized SQL Server estate features.

## How to Contribute
1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer
- This is a **community-curated** list — not exhaustive and not an endorsement.
- Database monitoring agents and extensions consume resources and can expose sensitive query text. Always review security, sampling rates, and data-retention policies. Open-source deployments require your own high-availability, backup, and upgrade practices. Performance advice from any tool should be validated in a non-production environment before changes are applied.
- This list is not DBA or production-support advice.

---
**Made for DBAs, SREs, and platform teams who need to see which queries are actually hurting the database.**
Let's keep performance data open, actionable, and under your control.
