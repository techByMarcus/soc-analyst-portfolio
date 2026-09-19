# SOC Analyst Portfolio

Hands-on security investigations completed in controlled lab and training environments.

This repository documents how I approach common SOC alerts: establish the question, review the available evidence, analyze the pattern, make an assessment, note uncertainty, and recommend the next response step.

The work shown here is training and lab experience. It is not presented as production SOC employment.

## Published Case Studies

| Case | Focus | Tools / Concepts |
| --- | --- | --- |
| [Brute Force Authentication Investigation](./cases/brute-force-authentication/README.md) | Repeated failed logins, source analysis, authentication triage | Splunk, Windows Event Logs |
| [Suspicious Login / Potential Account Compromise](./cases/suspicious-login/README.md) | Unusual login timing and source, behavioral analysis | SIEM, log correlation, incident triage |
| [Phishing Email Investigation](./cases/phishing-email/README.md) | Sender validation, social engineering, link analysis | Email analysis, URL inspection, phishing response |

## Investigation Approach

Each case is written to show the analyst decision process rather than only list lab steps.

The case studies separate:

- what evidence was actually available in the lab
- what conclusion the evidence supported
- what remained uncertain
- what response I would recommend
- what additional telemetry I would review in a production environment

## Additional Security Work

My broader public portfolio includes network-security labs, IDS/SIEM work, incident-response exercises, vulnerability assessment, and GRC projects.

Portfolio: https://techbymarcus.github.io/aboutMarcus/

GitHub: https://github.com/techByMarcus
