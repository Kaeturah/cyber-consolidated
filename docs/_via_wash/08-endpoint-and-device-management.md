---
title: Endpoint and device management
headline: "Knowing the user isn’t enough. The device matters too."
short: Devices
order: 8
stage: 2
part: Build stages
status: In progress
status_note: Initial Intune readiness is documented. Enrolment hasn’t started.
summary: Bringing Via Wash’s devices under management, so the business knows which devices exist and whether they can be trusted.
updated: 2026-10-18
permalink: /via-wash/endpoint-and-device-management/
---

{% include callout.html title="Only the readiness check is done" text="The starting state of Intune is documented in the foundation chapter. No device has been enrolled and no policy has been applied yet. This chapter will grow as that work happens." %}

## Why this stage comes next

Once Via Wash knows who its people are, the next question is what they are using. A trusted person on an unmanaged, out-of-date laptop is still a risk. Device management gives the business a list of its devices, a standard they must meet, and a way to fix them, or lock them, when they don’t.

## What it depends on

- [Identity and access]({{ '/via-wash/identity-and-access/' | relative_url }}): devices are enrolled by users and policies target groups.
- The [Intune readiness check]({{ '/via-wash/foundation/microsoft-intune/' | relative_url }}), which recorded the starting point.
- A suitable Windows test device. The host computer runs Windows 11 Home, so testing will use a virtual machine running an edition that can be enrolled.

## What it will cover

- Device enrolment and inventory
- Compliance policies and configuration profiles
- Application deployment
- The device lifecycle, from setup to retirement, and the IT support procedures around it

## How it will be validated

Enrolment will be shown from the device itself and from the admin centre. Each policy will be checked on the device, so the evidence shows both that a setting was applied and that it had the intended effect.

## What it makes possible

Managed devices can be protected and monitored in stage 3, and Via Wash can start requiring a compliant device before granting access.
