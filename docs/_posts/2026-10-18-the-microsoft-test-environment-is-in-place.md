---
title: The Microsoft test environment is in place
date: 2026-10-18 12:00:00 +0100
summary: A Microsoft 365 E5 trial is running, one licence is assigned, and a first look at Intune shows exactly where device management starts from.
project: identity-before-detection
tags: [Foundation, Microsoft 365, Intune]
related: /identity-before-detection/preparing-the-environment/tenant-and-e5-licence/
related_title: Microsoft 365 E5 trial
---

The Microsoft 365 E5 trial is now active. It didn’t go smoothly at first: the “Try now” button on the first checkout I tried stayed greyed out, and the trial only went through once I added Microsoft 365 E5 from the admin centre’s Marketplace instead. The trial runs until 16 November 2026, which puts a clear deadline on the stages that depend on it.

Today I assigned the first licence and opened the Intune admin centre to record its starting state before changing anything. The account is active, the service is healthy, and zero devices are enrolled on any platform. There is also a warning about firewall configuration for new Intune network endpoints, which I still need to look into.

None of this means anything is configured yet. A licence and a working admin centre are where the work starts, not proof of it. Identity and access with Entra ID comes next; it is on the [roadmap]({{ '/identity-before-detection/' | relative_url }}#roadmap-entra-id).
