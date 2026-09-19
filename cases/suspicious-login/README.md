# Suspicious Login / Potential Account Compromise

## Case Summary

This case documents a SOC lab investigation involving unusual login activity that occurred outside expected operating patterns and originated from an unfamiliar location.

**Environment:** Controlled training lab  
**Tools:** SIEM/log analysis environment  
**Primary focus:** Behavioral analysis, authentication review, incident triage

## Investigation Question

Did the login activity represent legitimate user behavior, or was there enough evidence to treat it as a potential account compromise?

## Evidence Reviewed

The investigation focused on:

- Login timestamps
- Source IP and location information
- Normal user activity patterns
- Whether the access occurred during expected working hours
- Whether the source was previously associated with the user

## Analysis

I reviewed the login activity against the user's expected behavior rather than relying on a single indicator.

The access occurred at an unusual time and originated from a location that was not consistent with the user's normal pattern. I compared the event with the available baseline information and treated the combination of unusual timing and unfamiliar source as more significant than either factor alone.

The evidence was suspicious, but by itself it was not enough to prove that the account had been compromised.

## Analyst Assessment

**Assessment:** Suspicious authentication activity requiring user validation and additional review.

I would not classify this as a confirmed compromise without more context. In a production SOC, the next step would be to validate the activity with the user and review additional telemetry before closing or escalating the incident.

## Recommended Response

- Confirm whether the user recognizes the login
- Require a password reset if the activity cannot be validated
- Enforce multi-factor authentication
- Review recent authentication history for additional anomalies
- Monitor the account for repeated suspicious activity

## What I Would Check Next in Production

Additional investigation would include:

- Successful and failed logins before and after the event
- VPN and geolocation context
- Device identity and endpoint telemetry
- Impossible-travel or concurrent-session indicators
- Privilege changes or unusual activity after authentication
- Whether the source IP appeared in other alerts

## What This Case Demonstrates

This case shows the importance of separating suspicious behavior from confirmed compromise. The goal is not to overstate the evidence, but to identify what is unusual, document why it matters, and determine what information is still needed before making a final incident decision.
