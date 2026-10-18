---
title: Endpoint and email security
headline: "Where attacks usually arrive: devices and email."
short: Endpoint and email security
order: 9
stage: 3
part: Build stages
status: Planned
summary: Protecting managed devices and the mailbox, and proving the protection works with safe, controlled tests.
updated: 2026-10-18
permalink: /via-wash/endpoint-and-email-security/
---

{% include callout.html title="Not started yet" text="No Defender or email-security service is claimed as configured. This chapter will document what is actually available in the licence, what was configured, and how it was tested." %}

## Why this stage matters

Devices and email are where most attacks against a small business begin: a malicious attachment, a convincing phishing message, a file that shouldn’t run. With devices managed in stage 2, they can now be protected, and they can report back what they see.

## What it depends on

- Enrolled, managed devices from [stage 2]({{ '/via-wash/endpoint-and-device-management/' | relative_url }}).
- Mailboxes and correct email authentication. The [domain and email chapter]({{ '/via-wash/foundation/domain-and-business-email/' | relative_url }}) records what is still outstanding.

## What it will cover

- A review of which security services are available in the licence
- Endpoint protection configuration
- Email protection and domain authentication
- Alert review using safe test scenarios, never real malware
- Findings, fixes and retesting

## How it will be validated

Every protection will be tested with a scenario designed to be safe, such as an industry-standard test file or a simulated phishing message, and the resulting alert or block will be recorded alongside what triggered it.

## What it makes possible

Real security signals, such as alerts, device risk and suspicious messages, for monitoring and detection to work with in stage 5.
