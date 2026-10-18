---
title: Domain and business email
headline: "The mailbox works. DKIM doesn’t, yet."
short: Domain and email
order: 6
part: Foundation
status: In progress
status_note: Domain and mailbox set up, outbound mail tested. DKIM and DMARC still need attention.
summary: How cyber-consolidated.com was set up for the website and for business email, what has been tested, and what still needs fixing.
updated: 2026-10-18
permalink: /via-wash/foundation/domain-and-business-email/
---

## Why this setup matters

A portfolio and a realistic business scenario both need a proper domain and an email identity to go with it. The `cyber-consolidated.com` domain was set up for the Cyber Consolidated portfolio, and the `franklin@cyber-consolidated.com` mailbox was created for business use.

These are foundation services for the portfolio. They aren’t evidence that Via Wash has a production email environment.

## At a glance

| Item | Status | Notes |
|---|---|---|
| Domain registration | Documented | Registered through NameSilo. |
| Website | Documented | The domain serves this site from GitHub Pages. |
| Mailbox | Documented | Created and shown as enabled. |
| Outbound delivery | Documented | Test messages delivered to the inbox, not spam. |
| Inbound delivery | Not yet tested | No evidence yet of mail being received. |
| MX and SPF records | Documented | Published. |
| DKIM | Needs validation | Record published under the wrong name. |
| DMARC | Planned | No record found. |

## Domain and website

The domain was bought through NameSilo. Website DNS records point it at GitHub Pages, which hosts this site from the Cyber Consolidated repository on GitHub. That configuration, including the repository’s `CNAME` file, is what keeps `cyber-consolidated.com` serving the site, so it stays untouched whenever new pages are added.

## Email provider and mailbox

The domain purchase didn’t include email hosting, so a separate provider was needed. Zoho Mail was considered, but **Namecheap Private Email** was the service actually chosen and connected to the domain.

The `franklin@` mailbox was created and shown as enabled. On 17 October 2026, a test message sent from it arrived in a separate personal inbox. A later test sent from the Private Email platform also arrived in the inbox, showing the business name as the sender, and was not filtered as spam. Together these show outbound delivery working.

What hasn’t been shown yet is mail sent *to* the business mailbox arriving, so inbound delivery still needs its own test.

## DNS authentication

Getting a mailbox working is only part of the job. Receiving mail servers also check DNS records to decide whether a message really came from the domain it claims to come from. Four records matter here:

- **MX** tells other servers where to deliver mail for the domain.
- **SPF** lists which servers are allowed to send mail for the domain.
- **DKIM** publishes a public key so receivers can check each message’s digital signature.
- **DMARC** tells receivers what to do when those checks fail, and where to send reports.

### MX and SPF

The screenshots and later DNS checks show that the MX and SPF records the provider asked for are published.

### DKIM

A DKIM record was added in NameSilo. A live DNS check on 18 October 2026, however, found it under `privateemail.domainkey` rather than the expected `privateemail._domainkey`. The missing underscore matters: receiving servers look the key up at the exact expected name, so as published they won’t find it.

Messages can still land in the inbox without DKIM, because a passing SPF check is often enough. That is why the delivery tests succeeded, and also why they don’t prove DKIM is working.

{% include callout.html tone="warn" title="Configuration issue: needs correction and revalidation" text="DKIM shouldn’t be treated as working until the record name and value have been checked against the provider’s current instructions, corrected if needed, and confirmed by a fresh check." %}

{% include quote.html text="Mail can still land in the inbox on SPF alone, which is why the tests passed." %}

### DMARC

No DMARC record was found. DMARC is a follow-up, to be set once DKIM is confirmed and the provider’s current guidance has been reviewed.

Full DNS values are deliberately not reproduced here. Record names and their status are enough to show what was done.

## Evidence

These genuine screenshots trace the setup step by step. Each one will be added once it has been inspected, approved and redacted where needed.

{% include evidence.html title="DNS before the mail records were added" shows="The NameSilo DNS table with only the website records for GitHub Pages." proves="The starting point before any email configuration." redact="Nothing sensitive expected; check before use." where="NameSilo · DNS records" source="Screenshot 2026-10-17 014701.png" %}

{% include evidence.html title="Records required by the email provider" shows="The Private Email page listing the MX and SPF records needed to activate the service." proves="What the provider asked for, so the published records can be compared against it." redact="Nothing sensitive expected; check before use." where="Namecheap · Private Email" source="Screenshot 2026-10-17 014147.png" %}

{% include evidence.html title="DNS after MX and SPF were added" shows="The NameSilo DNS table now including the MX and SPF records." proves="The mail records were entered at the registrar." redact="Nothing sensitive expected; check before use." where="NameSilo · DNS records" source="Screenshot 2026-10-17 015435.png" %}

{% include evidence.html title="Mailbox enabled" shows="One of three mailboxes in use, with the business mailbox shown as on." proves="The mailbox was created and enabled." redact="Decide whether to show or hide the mailbox address." where="Namecheap · Private Email" source="Screenshot 2026-10-17 021631.png" %}

{% include evidence.html title="DKIM record entry" shows="The NameSilo DNS table with the DKIM TXT record added." proves="A DKIM record was entered. It also shows the record name now under review." redact="Consider cropping the long key value; it isn’t needed to make the point." where="NameSilo · DNS records" source="Screenshot 2026-10-17 022341.png" %}

{% include evidence.html title="Successful outbound test email" shows="The test message from the business address, received in another inbox." proves="Outbound delivery worked for this test. It says nothing about inbound delivery or DKIM." redact="The personal inbox: account avatar, folder counts, other mail and personal message details." where="Personal inbox · test message" source="Screenshot 2026-10-17 023116.png" %}

## What comes next

1. Check the DKIM record name and value against Namecheap Private Email’s current instructions.
2. If confirmed, correct the record name, then check it with a trusted public DNS resolver and the provider’s verification tool.
3. Set a suitable DMARC policy after reviewing mail flow and authentication.
4. Test inbound receipt separately and record the actual result.
5. Recheck renewal and billing terms directly rather than relying on older screenshots.

Email security comes back in stage 3, [endpoint and email security]({{ '/via-wash/endpoint-and-email-security/' | relative_url }}).
