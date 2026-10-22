---
title: Business email
headline: "A mailbox with the business name on it."
short: Business email
kind: page
topic: getting-online
order: 12
status: In progress
summary: Choosing an email provider, activating it for the domain, creating the mailbox and testing that mail gets out.
updated: 2026-10-18
permalink: /domain-and-email/getting-online/business-email/
---

## Why business email

I wanted an address at the business’s own domain rather than a personal webmail address. It looks more credible to anyone I contact, and it keeps business mail separate from everything else. It also matters later in the Identity Before Detection project, where email is one of the main ways attacks arrive.

## Choosing a provider

The domain purchase didn’t include email hosting, so I compared several options, including Zoho Mail. I chose **Namecheap Private Email**, on its three-mailbox “Expand” plan with a one-month free trial, and ordered it on 16 October 2026.

## Activating it for the domain

Ordering the plan wasn’t enough on its own. The provider won’t receive mail for a domain until that domain’s DNS says it should. So I copied the provider’s required records, two `MX` records and an `SPF` record, into the DNS at NameSilo.

{% include evidence.html title="Records the provider asked for" where="Namecheap · Private Email" shows="The Private Email dashboard listing the MX and SPF records needed to activate the subscription." proves="What the provider required, so the published records can be checked against it." redact="Nothing sensitive expected; check before use." source="Screenshot 2026-10-17 014147.png" %}

## Creating the mailbox

With the records in place, I created the `franklin@cyber-consolidated.com` mailbox on 17 October 2026, and the dashboard showed it as enabled.

{% include evidence.html title="The business mailbox, enabled" where="Namecheap · Private Email" shows="One of three mailboxes in use, with the business mailbox switched on." proves="The mailbox exists and is enabled." redact="Decide whether to show or hide the mailbox address." source="Screenshot 2026-10-17 021631.png" %}

## Testing that mail gets out

At about 02:30 on 17 October 2026, I sent a test message from the new mailbox to a separate personal inbox, and it arrived. A later test I sent from the Private Email platform also arrived in the inbox, showing the business name as the sender, and wasn’t filtered as spam. Together these show outbound delivery working.

{% include evidence.html title="The first test message" where="Personal inbox · test message" shows="The test message from the business address, received in another inbox." proves="Outbound delivery worked for this test. It says nothing about inbound delivery or DKIM." redact="The personal inbox: account avatar, folder counts, other mail and personal message details." source="Screenshot 2026-10-17 023116.png" %}

## What isn’t tested yet

Every test I’ve run so far went *out* of the mailbox. I haven’t yet tested mail sent *to* `franklin@cyber-consolidated.com`, so inbound delivery still needs its own test.

## What comes next

A delivered message isn’t the whole story. The [next step]({{ '/domain-and-email/getting-online/email-authentication/' | relative_url }}) looks at the DNS records receiving servers use to decide whether mail from the domain is genuine, and the one that still needs fixing.
