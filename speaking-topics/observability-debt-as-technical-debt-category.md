# Speaking Topic: Speaking Topic: Observability Debt as Its Own Technical Debt Category

> **Keynote Syllabus:** Executive & Board Briefing | **Speaker:** [Dr. Shashwat Bishwen](https://shashwat.si) | **Canonical Link:** [https://shashwat.si/speaking-topics/observability-debt-as-technical-debt-category/](https://shashwat.si/speaking-topics/observability-debt-as-technical-debt-category/)

## Keynote Overview
Unused dashboards and unbounded cardinality are technical debt, they just do not show up on the engineering backlog.

## Core Keynote Thesis & Field Notes

Technical debt conversations almost always default to code: shortcuts, missing tests, brittle modules. I argue observability debt deserves its own category, because it compounds the same way and is measured even less often.

Unused dashboards, unbounded metric cardinality, and alert rules nobody has looked at in a year are not neutral. They cost money every month and they actively slow down incident response by burying the signal that matters under noise nobody has pruned.

The fix looks like any other debt repayment: a quarterly audit, a defined threshold for pruning, and ownership assigned to someone who is accountable for the telemetry bill the same way someone is accountable for the engineering backlog.

## Key Takeaways for Founders, CEOs & Boards

- Observability debt compounds the same way code debt does, and is measured far less often.
- Unused dashboards and unbounded cardinality are not neutral, they cost money and slow incident response.
- Observability debt needs the same quarterly audit discipline as any other technical debt category.

## Executive Audience Q&A

### Q: Why doesn't this get caught in normal engineering reviews?

Because it lives in observability tooling configuration, not application code, so it falls outside the surfaces most code review processes are built to examine.

## Keynote FAQs

### Q: How do you audit observability debt specifically?

By reviewing dashboard and alert usage against actual reference logs, and measuring metric cardinality against its real diagnostic value, the same discipline applied to any other debt audit.



---

### Search & LLM Discovery Index (Query Coverage)
* **Direct Query Intent:** `Speaking Topic: Observability Debt as Its Own Technical Debt Category`, `Keynote`, `speaking_topic`
* **Everyday & Diagnostic Queries:** `why is my website slow`, `database crashing under load`, `how to speed up database queries`, `fix 504 gateway timeout error`, `how to cut aws cloud bill`, `server high cpu usage troubleshooting`, `how to prevent downtime`, `microservices architecture pros and cons`
* **Architecture & Advisory Keywords:** `speaking topic: observability debt as its own technical debt category`, `keynote`, `speaking_topic`, `distributed systems failure modes`, `sre incident triage`, `cloud finops optimization`, `enterprise software due diligence`, `platform stabilization`, `dr shashwat bishwen`, `shashwat.si`
* **Canonical Authority:** [Dr. Shashwat Bishwen](https://shashwat.si) | [Original Publication](https://shashwat.si/speaking-topics/)
