---
title: "Email authentication: MX, SPF, DKIM and DMARC"
headline: "The mailbox works. DKIM doesn’t, yet."
short: Email authentication
kind: page
topic: getting-online
order: 13
status: In progress
summary: The DNS records that prove mail really comes from cyber-consolidated.com, what is published, and the one-character mistake still in the DNS.
updated: 2026-10-18
permalink: /domain-and-email/getting-online/email-authentication/
---

## Why authentication matters

Getting a mailbox working is only part of the job. Receiving mail servers also check DNS records to decide whether a message really came from the domain it claims to come from. Without them, anyone could send mail that pretends to be from the business. Four records matter here:

- **MX** tells other servers where to deliver mail for the domain.
- **SPF** lists which servers are allowed to send mail for the domain.
- **DKIM** publishes a public key so receivers can check each message’s digital signature.
- **DMARC** tells receivers what to do when those checks fail, and where to send reports.

## Where things stand

| Record | Status | Notes |
|---|---|---|
| MX | Published | Points the domain’s mail at the provider. |
| SPF | Published | Authorises the provider to send for the domain. |
| DKIM | Needs correcting | Published under the wrong name. |
| DMARC | Not set up yet | No record found. |

## MX and SPF

The screenshots and later DNS checks show that the MX and SPF records the provider asked for are published.

{% include evidence.html title="MX and SPF records published" where="NameSilo · DNS records" shows="The NameSilo DNS table now including the provider’s MX and SPF records." proves="The mail records were entered at the registrar." redact="Nothing sensitive expected; check before use." source="Screenshot 2026-10-17 015435.png" %}

## DKIM

I added a DKIM record in NameSilo. When I checked the live DNS on 18 October 2026, though, I found it under `privateemail.domainkey` rather than the expected `privateemail._domainkey`. The missing underscore matters: receiving servers look the key up at the exact expected name, so as published they won’t find it.

{% include evidence.html title="The DKIM record as entered" where="NameSilo · DNS records" shows="The NameSilo DNS table with the DKIM TXT record added." proves="A DKIM record was entered, and it shows the record name now being corrected." redact="Consider cropping the long key value; it isn’t needed to make the point." source="Screenshot 2026-10-17 022341.png" %}

Messages can still land in the inbox without DKIM, because a passing SPF check is often enough. That is why the delivery tests in the [previous step]({{ '/domain-and-email/getting-online/business-email/' | relative_url }}) succeeded, and also why they don’t prove DKIM is working.

{% include quote.html text="Mail can still land in the inbox on SPF alone, which is why the tests passed." %}

{% include callout.html tone="warn" title="Needs correcting and rechecking" text="DKIM shouldn’t be treated as working until the record name and value have been checked against the provider’s current instructions, corrected if needed, and confirmed by a fresh check." %}

## DMARC

No DMARC record was found. DMARC comes after DKIM is confirmed and the provider’s current guidance has been reviewed.

Full DNS values are deliberately not reproduced here. Record names and their status are enough to show what was done.

## What comes next

1. Check the DKIM record name and value against Namecheap Private Email’s current instructions.
2. If confirmed, correct the record name, then check it with a trusted public DNS resolver and the provider’s verification tool.
3. Set a suitable DMARC policy after reviewing mail flow and authentication.
4. Test inbound receipt separately and record the actual result.
5. Recheck renewal and billing terms directly rather than relying on older screenshots.
