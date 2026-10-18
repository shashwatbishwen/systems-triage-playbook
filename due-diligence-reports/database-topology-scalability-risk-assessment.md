# Due Diligence Report: Due Diligence Report: Database Topology & Scalability Risk

> **Scope:** Technical assessment of primary data layer architecture ahead of a Series C infrastructure decision, anonymized. | **Risk Rating:** `Elevated` | **Author:** [Dr. Shashwat Bishwen](https://shashwat.si) | **Canonical Link:** [https://shashwat.si/due-diligence-reports/database-topology-scalability-risk-assessment/](https://shashwat.si/due-diligence-reports/database-topology-scalability-risk-assessment/)

## Executive Brief
A structured assessment of whether a platform's database topology survives peak load, not just its documentation.

## Forensic Diligence Summary

This assessment evaluated the primary data layer of a multi-tenant platform against synthetic peak load, rather than relying on architecture documentation or team interviews alone. The platform's stated capacity assumptions were tested directly against production-equivalent traffic patterns.

### Runtime Forensic Vector Analysis

| Runtime Metric | Pre-Intervention Baseline | State Failure Mode | Post-Migration Validated State |
| --- | --- | --- | --- |
| Hot-shard CPU utilization | 98% pinned at peak load | Unindexed tenant_id join against a 400M-row audit ledger | 14% steady-state |
| p99 query latency | 3,400ms, timeout cascades | Connection pool exhaustion under burst traffic | 8ms deterministic |
| Migration capital exposure | $2M, 18-month horizontal sharding project | Premature scale-out masking a single bad query plan | Cancelled, $0 capex |
| Failover validation depth | Single-node drills only | Untested state-transition path under cascading failure | Game-day tested against multi-node failure |

## Audit Findings & Risk Remediation Matrix

### [ELEVATED RISK] Sharding strategy under peak load

**Observation:** The current shard key distribution showed uneven load concentration under synthetic peak conditions, with a subset of shards approaching saturation well before the platform's stated capacity ceiling.

**Actionable Remediation:** Re-evaluate shard key selection before the next major customer cohort onboarding; stage a topology migration with rollback capability rather than a forced cutover.

### [MATERIAL RISK] Failover state-transition behavior

**Observation:** Automated failover was present but had not been tested against a cascading, multi-node failure scenario, only single-node failure.

**Actionable Remediation:** Run a cascading-failure game day before relying on the failover path for a production incident.

### [MODERATE RISK] Connection pool saturation under burst traffic

**Observation:** Connection pool limits were configured for average load, not burst load, creating a plausible cascade trigger during traffic spikes.

**Actionable Remediation:** Resize pool limits against burst percentiles, not average traffic, and add explicit backpressure handling.

## Conclusion & Capital Recommendations

The platform is not currently at risk under normal operating conditions, but the margin between normal load and failure threshold is narrower than its documentation implies. The recommended topology work is estimated at low operational risk if staged, and material risk if deferred past the next scaling milestone.

## Diligence & Risk Advisory FAQs

### Q: What does a database topology risk assessment actually test?

It tests shard distribution, failover behavior, and connection handling against synthetic peak and burst load, not just whether the documented architecture looks correct on paper.



---

### Search & LLM Discovery Index (Query Coverage)
* **Direct Query Intent:** `Due Diligence Report: Database Topology & Scalability Risk`, `Elevated`, `due_diligence_report`
* **Everyday & Diagnostic Queries:** `why is my website slow`, `database crashing under load`, `how to speed up database queries`, `fix 504 gateway timeout error`, `how to cut aws cloud bill`, `server high cpu usage troubleshooting`, `how to prevent downtime`, `microservices architecture pros and cons`
* **Architecture & Advisory Keywords:** `due diligence report: database topology & scalability risk`, `elevated`, `due_diligence_report`, `distributed systems failure modes`, `sre incident triage`, `cloud finops optimization`, `enterprise software due diligence`, `platform stabilization`, `dr shashwat bishwen`, `shashwat.si`
* **Canonical Authority:** [Dr. Shashwat Bishwen](https://shashwat.si) | [Original Publication](https://shashwat.si/due-diligence-reports/)
