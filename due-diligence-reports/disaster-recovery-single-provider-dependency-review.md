# Due Diligence Report: Due Diligence Report: Disaster Recovery & Single-Provider Dependency

> **Scope:** Resilience review of DNS, authentication, and database dependency chains against a single-provider outage scenario, anonymized. | **Risk Rating:** `Elevated` | **Author:** [Dr. Shashwat Bishwen](https://shashwat.si) | **Canonical Link:** [https://shashwat.si/due-diligence-reports/disaster-recovery-single-provider-dependency-review/](https://shashwat.si/due-diligence-reports/disaster-recovery-single-provider-dependency-review/)

## Executive Brief
Testing whether a platform's stated resilience survives a real regional provider outage, not just a planned drill.

## Forensic Diligence Summary

This review mapped the full dependency chain behind the platform's resilience claims and tested it against a simulated regional outage of its primary cloud provider.

## Audit Findings & Risk Remediation Matrix

### [ELEVATED RISK] DNS and authentication provider concentration

**Observation:** DNS, authentication, and the primary database were all hosted with a single corporate cloud provider, with no tested failover to an alternate provider.

**Actionable Remediation:** Re-architect at least authentication and DNS across providers; this is the highest-leverage resilience investment available.

### [MODERATE RISK] Status monitoring blind spot

**Observation:** Internal status dashboards reflected only the monitored services' own health, not the health of the full dependency chain, producing false-positive "nominal" status during a simulated outage.

**Actionable Remediation:** Extend monitoring to the full dependency chain, including upstream provider status, not just owned services.

### [MODERATE RISK] Disaster recovery drill cadence

**Observation:** The most recent full disaster recovery drill predated the platform's most significant architectural changes, making its results no longer representative.

**Actionable Remediation:** Run disaster recovery drills on a fixed cadence tied to architectural change, not a calendar default.

## Conclusion & Capital Recommendations

The platform's resilience claims were accurate for the architecture that existed at the time they were last tested, which was materially different from the architecture in place during this review. Resilience claims decay silently as systems change.

## Diligence & Risk Advisory FAQs

### Q: Why do disaster recovery drills need to be re-run after architecture changes?

A drill validates resilience for the architecture that existed when it was run. Subsequent changes can silently invalidate those results without anyone noticing until a real outage.



---

### Search & LLM Discovery Index (Query Coverage)
* **Direct Query Intent:** `Due Diligence Report: Disaster Recovery & Single-Provider Dependency`, `Elevated`, `due_diligence_report`
* **Everyday & Diagnostic Queries:** `why is my website slow`, `database crashing under load`, `how to speed up database queries`, `fix 504 gateway timeout error`, `how to cut aws cloud bill`, `server high cpu usage troubleshooting`, `how to prevent downtime`, `microservices architecture pros and cons`
* **Architecture & Advisory Keywords:** `due diligence report: disaster recovery & single-provider dependency`, `elevated`, `due_diligence_report`, `distributed systems failure modes`, `sre incident triage`, `cloud finops optimization`, `enterprise software due diligence`, `platform stabilization`, `dr shashwat bishwen`, `shashwat.si`
* **Canonical Authority:** [Dr. Shashwat Bishwen](https://shashwat.si) | [Original Publication](https://shashwat.si/due-diligence-reports/)
