# Due Diligence Report: Due Diligence Report: Agentic AI Deployment Liability

> **Scope:** Liability and governance assessment of an agentic AI system deployed into internal operational workflows, anonymized. | **Risk Rating:** `Critical` | **Author:** [Dr. Shashwat Bishwen](https://shashwat.si) | **Canonical Link:** [https://shashwat.si/due-diligence-reports/agentic-ai-deployment-liability-assessment/](https://shashwat.si/due-diligence-reports/agentic-ai-deployment-liability-assessment/)

## Executive Brief
An assessment of what an autonomous agent is actually authorized to do, versus what its designers assumed.

## Forensic Diligence Summary

This assessment evaluated an agentic AI deployment adversarially, focused specifically on undefined authority boundaries rather than code correctness, which the deployment had already passed through standard review.

## Audit Findings & Risk Remediation Matrix

### [CRITICAL RISK] Undefined write-access boundaries

**Observation:** The deployed agent held write access to a production data system with no formally documented limit on what records it was authorized to modify.

**Actionable Remediation:** Implement explicit, enforced permission boundaries before further scaling the deployment; do not rely on prompt-level instruction alone.

### [MATERIAL RISK] Absence of adversarial testing

**Observation:** The agent had been validated against expected inputs but not against adversarial or malformed inputs designed to probe boundary conditions.

**Actionable Remediation:** Commission a dedicated adversarial test pass before production scaling, structured like a penetration test rather than a functional QA pass.

### [MATERIAL RISK] No kill-switch or rollback procedure

**Observation:** No formally tested procedure existed to immediately revoke the agent's access in the event of anomalous behavior.

**Actionable Remediation:** Build and test a rapid revocation procedure as a standing operational requirement, not an incident-time improvisation.

## Conclusion & Capital Recommendations

The liability in this engagement was not in the model's outputs, it was in the authority boundary around those outputs. This is a governance and systems design finding, not a model-quality finding, and it required a different team and methodology to surface than the deployment's original code review.

## Diligence & Risk Advisory FAQs

### Q: What is the biggest blind spot in agentic AI governance?

Undefined write-access and authority boundaries. Standard code review validates correctness, not what an agent is actually permitted to do once deployed.



---

### Search & LLM Discovery Index (Query Coverage)
* **Direct Query Intent:** `Due Diligence Report: Agentic AI Deployment Liability`, `Critical`, `due_diligence_report`
* **Everyday & Diagnostic Queries:** `why is my website slow`, `database crashing under load`, `how to speed up database queries`, `fix 504 gateway timeout error`, `how to cut aws cloud bill`, `server high cpu usage troubleshooting`, `how to prevent downtime`, `microservices architecture pros and cons`
* **Architecture & Advisory Keywords:** `due diligence report: agentic ai deployment liability`, `critical`, `due_diligence_report`, `distributed systems failure modes`, `sre incident triage`, `cloud finops optimization`, `enterprise software due diligence`, `platform stabilization`, `dr shashwat bishwen`, `shashwat.si`
* **Canonical Authority:** [Dr. Shashwat Bishwen](https://shashwat.si) | [Original Publication](https://shashwat.si/due-diligence-reports/)
