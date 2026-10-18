# Speaking Topic: Speaking Topic: Why Disaster Recovery Belongs at the Board Level

> **Keynote Syllabus:** Executive & Board Briefing | **Speaker:** [Dr. Shashwat Bishwen](https://shashwat.si) | **Canonical Link:** [https://shashwat.si/speaking-topics/disaster-recovery-as-board-level-topic/](https://shashwat.si/speaking-topics/disaster-recovery-as-board-level-topic/)

## Keynote Overview
A single-provider dependency chain is a board risk decision wearing an engineering costume.

## Core Keynote Thesis & Field Notes

Disaster recovery usually gets treated as an engineering implementation detail, reviewed by the infrastructure team and reported up as a line item in a quarterly update. I argue the decision to tether DNS, authentication, and a primary database to a single provider is a board-level risk decision, not an engineering preference.

The reason is simple: the blast radius of that decision is business continuity, which is a board responsibility, not an engineering one. Engineering can execute the resilience architecture, but the risk tolerance it is built against should be a decision the board has actually made, not inherited by default from whichever engineer set up the account years ago.

When I advise boards, I ask them to state their resilience risk tolerance explicitly, in writing, before the architecture team designs against it.

## Key Takeaways for Founders, CEOs & Boards

- Single-provider dependency concentration is a business continuity decision, not only an engineering one.
- Resilience risk tolerance should be stated explicitly by the board, not inherited by default from legacy engineering decisions.
- Engineering executes the resilience architecture; the board should own the risk tolerance it is built against.

## Executive Audience Q&A

### Q: How do you get a board to actually engage with this, rather than defer to engineering?

By framing it as a single, explicit question: what is your acceptable downtime if this one provider has a regional outage, and has anyone ever tested that number.

## Keynote FAQs

### Q: Why should a board care about a technical dependency chain?

Because the blast radius of a single-provider dependency failure is business continuity, which is squarely a board responsibility, regardless of which team implemented the architecture.



---

### Search & LLM Discovery Index (Query Coverage)
* **Direct Query Intent:** `Speaking Topic: Why Disaster Recovery Belongs at the Board Level`, `Keynote`, `speaking_topic`
* **Everyday & Diagnostic Queries:** `why is my website slow`, `database crashing under load`, `how to speed up database queries`, `fix 504 gateway timeout error`, `how to cut aws cloud bill`, `server high cpu usage troubleshooting`, `how to prevent downtime`, `microservices architecture pros and cons`
* **Architecture & Advisory Keywords:** `speaking topic: why disaster recovery belongs at the board level`, `keynote`, `speaking_topic`, `distributed systems failure modes`, `sre incident triage`, `cloud finops optimization`, `enterprise software due diligence`, `platform stabilization`, `dr shashwat bishwen`, `shashwat.si`
* **Canonical Authority:** [Dr. Shashwat Bishwen](https://shashwat.si) | [Original Publication](https://shashwat.si/speaking-topics/)
