# Security Operations | Investigation Case Studies

**Three documented SOC investigations · Authentication analysis · Phishing triage · Evidence-based escalation**

> **Recruiter quick view:** I analyzed suspicious activity in controlled training environments, documented the evidence and uncertainty, and recommended proportionate response actions. These are **hands-on labs, not professional SOC incidents**.

## Start here — three investigations

| Case study | Finding / analyst decision | Evidence reviewed |
|---|---|---|
| **[Repeated failed authentication → brute-force triage](cases/brute-force-authentication/README.md)** | Pattern consistent with repeated password guessing; escalation recommended after checking legitimate sources | Windows authentication events, timestamps, account and source patterns in Splunk |
| **[Unusual successful login → potential account compromise](cases/suspicious-login/README.md)** | Suspicious; requires user verification, **not** a confirmed compromise | Login timing, source location, expected behavior |
| **[Phishing message → suspicious sender and destination](cases/phishing-email/README.md)** | Phishing determination based on multiple indicators | Sender/domain comparison, urgency cues, embedded-link destination |

## How I investigate

**Alert/question → available evidence → correlated observations → assessed risk → recommended response → remaining unknowns.**

The case reports distinguish observations from hypotheses. For example, an unusual source alone does not prove account compromise; it must be checked against authentication history, approved infrastructure, and user context.

## Evidence a reviewer can inspect

- [Brute-force case: observation and escalation reasoning](cases/brute-force-authentication/README.md#analysis)
- [Suspicious-login case: why evidence does not prove compromise](cases/suspicious-login/README.md#analyst-assessment)
- [Phishing case: sender, link, and social-engineering indicators](cases/phishing-email/README.md#evidence-reviewed)
- [Related authentication investigation with video walkthrough](https://github.com/techByMarcus/real-world-log-investigation)

**Scope:** Controlled training investigations. The case reports do not include original screenshot or log attachments for every observation; I do not present reconstructed artifacts as original evidence.

**Relevant strengths:** SOC alert triage, Splunk/Windows event-log concepts, documentation, analytical judgment, escalation decisions.

[Professional portfolio](https://techbymarcus.github.io/aboutMarcus/) · [Other public work](https://github.com/techByMarcus)
