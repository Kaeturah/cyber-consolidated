---
title: Getting Cyber Consolidated online
headline: "Getting Cyber Consolidated online"
kind: topic
topic: getting-online
order: 10
status: In progress
summary: Three steps, in order. Register the domain and point it at the website, set up business email, then publish the records that let mail servers trust it.
updated: 2026-10-20
permalink: /domain-and-email/getting-online/
---

## Why this came first

This site needed an address before it could document anything, and the business needed an email identity to go with it. Neither is complicated on its own, but each depends on the one before. The website needs the domain, the mailbox needs the domain’s DNS, and email authentication needs the mailbox to be working first.

## The three steps

1. **The domain and the website.** Register cyber-consolidated.com and point it at GitHub Pages.
2. **Business email.** Choose a provider, activate it for the domain, create the mailbox and test it.
3. **Email authentication.** Publish the DNS records that let other mail servers trust mail from the domain.

{% include callout.html title="If you’re following along" text="Write down every DNS record you add, and check each one with a public DNS lookup after adding it. A single wrong character in a record name, like a missing underscore, can silently stop it from working." %}
