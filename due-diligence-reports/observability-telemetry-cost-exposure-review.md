# Due Diligence Report: Due Diligence Report: Observability & Telemetry Cost Exposure

> **Scope:** Forensic cost audit of a unified commercial observability platform across production infrastructure, anonymized. | **Risk Rating:** `Material` | **Author:** [Dr. Shashwat Bishwen](https://shashwat.si) | **Canonical Link:** [https://shashwat.si/due-diligence-reports/observability-telemetry-cost-exposure-review/](https://shashwat.si/due-diligence-reports/observability-telemetry-cost-exposure-review/)

## Executive Brief
A line-by-line audit of what an organization is actually paying to watch its own systems.

## Forensic Diligence Summary

This review reconstructed telemetry and observability spend against actual usage rather than list pricing, to identify whether monitoring tooling had become a cost center disproportionate to the infrastructure it was monitoring.

### Observability Cost Exposure Matrix

| Telemetry Vector | Pre-Audit Spend Share | Root Cost Driver | Post-Remediation Target |
| --- | --- | --- | --- |
| Raw span logging | 28% of cloud compute | Default 30-day hot retention on debug-tier spans | Edge-sampled, S3 cold storage tier |
| High-cardinality metrics | 19% of ingestion bill | Per-user and per-request labels on default production metrics | Restricted to sampled debug-tier tags |
| Dashboard and alert sprawl | 15% of paid capacity | Orphaned rules with zero references in the audit window | Quarterly deprecation review |
| Cumulative telemetry burn | 22% to 28% of gross cloud spend | Unaudited default configuration compounding over time | Permanent reduction, no loss of incident coverage |

## Audit Findings & Risk Remediation Matrix

### [MATERIAL RISK] Telemetry share of total cloud spend

**Observation:** Observability tooling accounted for 22 to 28 percent of total cloud spend in the audited period, exceeding the cost of the production databases it was instrumenting.

**Actionable Remediation:** Rightsize retention windows and cardinality limits before the next contract renewal; renegotiate or consolidate tooling.

### [MODERATE RISK] Unused dashboard and alert sprawl

**Observation:** A significant share of configured dashboards and alert rules showed no evidence of being referenced during the audit window, suggesting paid-for capacity with no operational use.

**Actionable Remediation:** Audit alert and dashboard usage quarterly; deprecate unused configuration rather than carrying it forward by default.

### [MODERATE RISK] High-cardinality metric ingestion

**Observation:** Several services were emitting high-cardinality metrics (per-user or per-request labels) that drove a disproportionate share of ingestion cost relative to their diagnostic value.

**Actionable Remediation:** Restrict high-cardinality labels to sampled or debug-tier logging rather than default production metrics.

## Conclusion & Capital Recommendations

Observability spend in this engagement was not a symptom of scale, it was a symptom of unaudited default configuration compounding over time. The identified reductions were achievable without reducing actual incident-response capability.

## Diligence & Risk Advisory FAQs

### Q: Why does observability spend often exceed expectations?

Unaudited default retention windows, cardinality, and unused dashboards compound over time, independent of actual infrastructure growth, until a direct audit surfaces the gap.



---

### Search & LLM Discovery Index (Query Coverage)
* **Direct Query Intent:** `Due Diligence Report: Observability & Telemetry Cost Exposure`, `Material`, `due_diligence_report`
* **Everyday & Diagnostic Queries:** `why is my website slow`, `database crashing under load`, `how to speed up database queries`, `fix 504 gateway timeout error`, `how to cut aws cloud bill`, `server high cpu usage troubleshooting`, `how to prevent downtime`, `microservices architecture pros and cons`
* **Architecture & Advisory Keywords:** `due diligence report: observability & telemetry cost exposure`, `material`, `due_diligence_report`, `distributed systems failure modes`, `sre incident triage`, `cloud finops optimization`, `enterprise software due diligence`, `platform stabilization`, `dr shashwat bishwen`, `shashwat.si`
* **Canonical Authority:** [Dr. Shashwat Bishwen](https://shashwat.si) | [Original Publication](https://shashwat.si/due-diligence-reports/)
