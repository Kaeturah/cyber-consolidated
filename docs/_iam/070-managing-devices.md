---
title: Managing devices with Intune
headline: Knowing the user isn’t enough. The device matters too.
kind: topic
topic: managing-devices
order: 70
status: In progress
summary: Bringing Via Wash’s devices under management, so the business knows which devices exist and whether they can be trusted.
updated: 2026-10-20
permalink: /identity-before-detection/managing-devices/
short: Intune
status_note: Initial Intune readiness is documented. Enrolment hasn’t started.
---

{% include callout.html title="Only the readiness check is done" text="The starting state of Intune is documented in the Intune readiness step. No device has been enrolled and no policy has been applied yet. This topic will grow as that work happens." %}

## Why this stage comes next

Once Via Wash knows who its people are, the next question is what they are using. A trusted person on an unmanaged, out-of-date laptop is still a risk. Device management gives the business a list of its devices, a standard they must meet, and a way to fix them, or lock them, when they don’t.

## What it depends on

- [Identity and access]({{ '/identity-before-detection/building-identity-in-entra-id/' | relative_url }}): devices are enrolled by users and policies target groups.
- The [Intune readiness check]({{ '/identity-before-detection/preparing-the-environment/intune-readiness/' | relative_url }}), which recorded the starting point.
- A Windows test device from [Building the lab]({{ '/identity-before-detection/building-the-lab/' | relative_url }}).

## How it will be validated

Enrolment will be shown from the device itself and from the admin centre. Each policy will be checked on the device, so the evidence shows both that a setting was applied and that it had the intended effect.

## What it makes possible

Managed devices can be protected and monitored in stage 3, and Via Wash can start requiring a compliant device before granting access.
