# Brute Force Authentication Investigation

## Case Summary

This case documents a hands-on SOC lab investigation involving repeated failed authentication attempts observed in a Windows environment and reviewed through Splunk.

**Environment:** Controlled training lab  
**Tools:** Splunk, Windows Event Logs  
**Primary focus:** Authentication analysis, log correlation, incident triage

## Investigation Question

Was the authentication activity consistent with normal user behavior, or did the pattern indicate a brute-force attempt?

## Evidence Reviewed

The investigation focused on:

- Repeated failed login activity
- Source IP information
- Timestamps and frequency of attempts
- Affected user accounts
- Whether the pattern was isolated or repeated over a short period

## Analysis

I reviewed the authentication activity in Splunk and compared the timing and source of the failed login attempts.

The pattern showed repeated failures originating from the same source over a short period rather than a small number of isolated login mistakes. I correlated the timestamps to determine whether the activity was sustained and reviewed the affected accounts to understand the scope.

The concentration of failed attempts from a single source made ordinary user error less likely and was consistent with brute-force behavior.

## Analyst Assessment

**Assessment:** Activity consistent with a brute-force authentication attempt.

The available lab evidence supported escalation because the volume and repetition of failed logins did not resemble normal authentication behavior.

In a production SOC, I would also verify whether the source IP belonged to an approved scanner, VPN, service account, or other known infrastructure before finalizing the disposition.

## Recommended Response

- Block or restrict the suspicious source if confirmed unauthorized
- Review the affected accounts for successful logins after the failed attempts
- Enforce account lockout controls where appropriate
- Require multi-factor authentication
- Continue monitoring for repeated activity from the same source or against the same accounts

## What I Would Check Next in Production

If this were a live enterprise environment, I would expand the investigation by reviewing:

- Successful authentications following the failed attempts
- Additional source IP activity across other users or hosts
- VPN, firewall, and endpoint telemetry
- Whether the targeted accounts were privileged
- Any signs of lateral movement after authentication

## What This Case Demonstrates

This investigation reflects the way I approach authentication alerts: establish the pattern, compare it with expected behavior, determine scope, document uncertainty, and recommend the next response step based on the evidence available.
