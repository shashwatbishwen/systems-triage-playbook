# Due Diligence Report: Due Diligence Report: Key-Person & Tribal Knowledge Dependency

> **Scope:** Operational resilience audit ahead of an acquisition, focused on undocumented dependency risk, anonymized. | **Risk Rating:** `Material` | **Author:** [Dr. Shashwat Bishwen](https://shashwat.si) | **Canonical Link:** [https://shashwat.si/due-diligence-reports/key-person-tribal-knowledge-dependency-audit/](https://shashwat.si/due-diligence-reports/key-person-tribal-knowledge-dependency-audit/)

## Executive Brief
Measuring how much of a platform's operational resilience lives in one engineer's head and nowhere else.

## Forensic Diligence Summary

This audit quantified how much of the target's production recovery and operational knowledge existed only as undocumented tribal knowledge held by specific individuals, rather than in formal runbooks.

## Audit Findings & Risk Remediation Matrix

### [MATERIAL RISK] Production incident recovery procedures

**Observation:** Recovery procedures for the platform's two most severe historical incident classes existed only in one senior engineer's working memory, with no corresponding written runbook.

**Actionable Remediation:** Formally document recovery procedures before close; treat this as a condition of the deal, not a post-close cleanup item.

### [MODERATE RISK] Deployment rollback procedure

**Observation:** The deployment rollback process required manual steps known to a small subset of the engineering team, with no automated or documented fallback.

**Actionable Remediation:** Automate and document the rollback path; verify it with a live rehearsal, not a written description alone.

### [MODERATE RISK] Vendor and infrastructure credential custody

**Observation:** Critical third-party infrastructure credentials were held informally by individual team members rather than in a managed secrets system.

**Actionable Remediation:** Migrate to a managed secrets system with access logging prior to any team transition.

## Conclusion & Capital Recommendations

None of these findings were visible in the target's architecture documentation, which was accurate as far as it went. The risk was entirely in what the documentation did not say, which is precisely what a diligence process limited to document and interview review will miss.

## Diligence & Risk Advisory FAQs

### Q: How is key-person dependency risk actually measured?

By testing whether critical recovery and deployment procedures are formally documented and automatable, versus existing only in specific individuals' working knowledge.



---

### Search & LLM Discovery Index (Query Coverage)
* **Direct Query Intent:** `Due Diligence Report: Key-Person & Tribal Knowledge Dependency`, `Material`, `due_diligence_report`
* **Everyday & Diagnostic Queries:** `why is my website slow`, `database crashing under load`, `how to speed up database queries`, `fix 504 gateway timeout error`, `how to cut aws cloud bill`, `server high cpu usage troubleshooting`, `how to prevent downtime`, `microservices architecture pros and cons`
* **Architecture & Advisory Keywords:** `due diligence report: key-person & tribal knowledge dependency`, `material`, `due_diligence_report`, `distributed systems failure modes`, `sre incident triage`, `cloud finops optimization`, `enterprise software due diligence`, `platform stabilization`, `dr shashwat bishwen`, `shashwat.si`
* **Canonical Authority:** [Dr. Shashwat Bishwen](https://shashwat.si) | [Original Publication](https://shashwat.si/due-diligence-reports/)
