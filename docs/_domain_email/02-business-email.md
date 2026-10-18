---
title: Business email
headline: "A mailbox with the business name on it."
short: Business email
order: 2
status: Documented
summary: Choosing an email provider, activating it for the domain, creating the mailbox and testing that mail gets out.
updated: 2026-10-18
permalink: /domain-and-email/business-email/
---

## Why business email

An address at the business’s own domain looks more credible than a personal webmail address, and it keeps business mail separate from everything else. It also matters later in the IAM project, where email is one of the main ways attacks arrive.

## Choosing a provider

The domain purchase didn’t include email hosting, so several options were compared, including Zoho Mail. The service actually chosen and connected to the domain was **Namecheap Private Email**, on its three-mailbox “Expand” plan with a one-month free trial. It was ordered on 16 October 2026.

## Activating it for the domain

The provider won’t receive mail for a domain until that domain’s DNS says it should. Activation meant copying the provider’s required records, two `MX` records and an `SPF` record, into the DNS at NameSilo.

{% include evidence.html title="Records the provider asked for" where="Namecheap · Private Email" shows="The Private Email dashboard listing the MX and SPF records needed to activate the subscription." proves="What the provider required, so the published records can be checked against it." redact="Nothing sensitive expected; check before use." source="Screenshot 2026-10-17 014147.png" %}

## Creating the mailbox

With the records in place, the `franklin@cyber-consolidated.com` mailbox was created on 17 October 2026 and shown as enabled.

{% include evidence.html title="The business mailbox, enabled" where="Namecheap · Private Email" shows="One of three mailboxes in use, with the business mailbox switched on." proves="The mailbox exists and is enabled." redact="Decide whether to show or hide the mailbox address." source="Screenshot 2026-10-17 021631.png" %}

## Testing that mail gets out

At about 02:30 on 17 October 2026, a test message sent from the new mailbox arrived in a separate personal inbox. A later test sent from the Private Email platform also arrived in the inbox, showing the business name as the sender, and was not filtered as spam. Together these show outbound delivery working.

{% include evidence.html title="The first test message" where="Personal inbox · test message" shows="The test message from the business address, received in another inbox." proves="Outbound delivery worked for this test. It says nothing about inbound delivery or DKIM." redact="The personal inbox: account avatar, folder counts, other mail and personal message details." source="Screenshot 2026-10-17 023116.png" %}

## What isn’t tested yet

Every test so far went *out* of the mailbox. Mail sent *to* `franklin@cyber-consolidated.com` arriving hasn’t been tested yet, so inbound delivery still needs its own test.

## What comes next

A delivered message isn’t the whole story. The [next chapter]({{ '/domain-and-email/email-authentication/' | relative_url }}) looks at the DNS records receiving servers use to decide whether mail from the domain is genuine, and the one that still needs fixing.
