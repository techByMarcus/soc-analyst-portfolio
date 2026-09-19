# Phishing Email Investigation

## Case Summary

This case documents a hands-on phishing investigation performed in a controlled training environment.

**Environment:** Controlled training lab  
**Tools:** Email header review, URL inspection, threat-analysis techniques  
**Primary focus:** Phishing detection, sender validation, link analysis, incident response

## Investigation Question

Was the reported message a legitimate account-verification request, or did the sender, content, and embedded link indicate phishing?

## Evidence Reviewed

The investigation focused on:

- Sender address and domain
- Message wording and urgency
- Embedded link destination
- Whether the visible sender information matched the expected organization
- Signs of social engineering

## Analysis

I reviewed the sender information first to determine whether the message originated from the organization it claimed to represent.

The sender address did not match the legitimate domain. The message also used urgent language designed to pressure the recipient into taking immediate action. I then inspected the embedded link and found that it redirected to a non-legitimate destination.

No single indicator was used by itself. The combination of sender mismatch, social-engineering language, and suspicious link behavior supported a phishing determination.

## Analyst Assessment

**Assessment:** Phishing email.

The message contained multiple indicators that were inconsistent with a legitimate account-verification request.

## Recommended Response

- Do not interact with the embedded link
- Report and quarantine the message
- Block the malicious sender/domain if confirmed
- Review whether other users received the same message
- Reinforce phishing-awareness guidance where appropriate

## What I Would Check Next in Production

In a production environment, I would also review:

- Full email headers
- SPF, DKIM, and DMARC results
- URL and domain reputation
- Attachment hashes, if attachments were present
- Whether the domain or indicators appeared in threat-intelligence sources
- Mail-gateway logs to determine the scope of delivery

## What This Case Demonstrates

This investigation shows how I combine sender validation, content analysis, and link inspection rather than relying on one obvious phishing indicator. It also separates the evidence actually reviewed in the lab from the additional steps I would take in a production SOC.
