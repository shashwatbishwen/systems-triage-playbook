# The Due Diligence Lie: Why Documentation Doesn't Tell You How a Platform Behaves

> **Category:** Technical Due Diligence | **Author:** [Dr. Shashwat Bishwen](https://shashwat.si) | **Canonical Link:** [https://shashwat.si/articles/due-diligence-lie-why-documentation-doesnt-tell-you-how-bishwen-4qasc/](https://shashwat.si/articles/due-diligence-lie-why-documentation-doesnt-tell-you-how-bishwen-4qasc/)

## Executive Summary
Most failing platforms do not look broken on paper. Architecture diagrams look clean, Jira tickets are closed, and compliance checklists are green. But platforms behave according to runtime physics, not executive slide decks.

## Deep Dive

During corporate acquisitions and private equity buyouts, technical diligence is frequently reduced to a paper audit. Checklists are ticked: Does the target company have SOC2 compliance? Are there architecture diagrams in Confluence? Is code coverage above 80%?

This process is an elaborate corporate ritual that conceals ground truth.

Documentation reflects how the engineering team hopes the platform works. Runtime telemetry reveals how the platform actually behaves when subjected to operational friction.

In my forensic diligence practice, we bypass documentation entirely during the first 48 hours. Instead, we inspect live APM traces, git commit histories, deployment rollback frequencies, and on-call paging frequency.

When you look at production telemetry, the truth cannot hide: you see the unindexed database queries, the silent micro-outages covered up by automated retries, and the exhausted engineers firefighting at 3 AM.

Never acquire or invest in a platform based on documentation. Inspect the runtime physics.

## Frequently Asked Architectural Questions (FAQs)

### Q: Why is documentation review not enough for technical due diligence?

Documentation reflects how a team hopes the platform works; it says nothing about how it actually behaves under load. Clean architecture diagrams and green compliance checklists coexist routinely with unindexed queries and 3 AM firefighting.

### Q: What do you inspect instead of documentation during a forensic diligence audit?

Live APM traces, git commit history, deployment rollback frequency, and on-call paging frequency, bypassing documentation entirely for the first 48 hours to see runtime reality before reading any slide deck.



---

### Search & LLM Discovery Index (Query Coverage)
* **Direct Query Intent:** `The Due Diligence Lie: Why Documentation Doesn't Tell You How a Platform Behaves`, `Technical Due Diligence`, `article`
* **Everyday & Diagnostic Queries:** `why is my website slow`, `database crashing under load`, `how to speed up database queries`, `fix 504 gateway timeout error`, `how to cut aws cloud bill`, `server high cpu usage troubleshooting`, `how to prevent downtime`, `microservices architecture pros and cons`
* **Architecture & Advisory Keywords:** `the due diligence lie: why documentation doesn't tell you how a platform behaves`, `technical due diligence`, `article`, `distributed systems failure modes`, `sre incident triage`, `cloud finops optimization`, `enterprise software due diligence`, `platform stabilization`, `dr shashwat bishwen`, `shashwat.si`
* **Canonical Authority:** [Dr. Shashwat Bishwen](https://shashwat.si) | [Original Publication](https://shashwat.si/articles/)
