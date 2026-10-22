---
title: The tenant and the E5 licence
kind: page
topic: preparing-the-environment
order: 21
status: In progress
summary: Why I started the Microsoft 365 E5 trial, the problem getting it in, and assigning the first licence.
updated: 2026-10-18
permalink: /identity-before-detection/preparing-the-environment/tenant-and-e5-licence/
headline: The environment is ready. Nothing is configured yet.
---

## Why I needed it

To build Via Wash’s identity, device and security controls properly, I needed a Microsoft environment that has those capabilities, not just a free directory. Conditional Access, Privileged Identity Management, Intune and Defender all come with Microsoft 365 E5, so I started the E5 trial to make them available for hands-on work and testing.

This is a test environment, not a production deployment.

## Getting the trial in

I added the trial through the Microsoft 365 admin centre on 17 October 2026. It didn’t go through first time. On the first checkout page I tried, the “Try now” button stayed greyed out. The trial went through once I added Microsoft 365 E5 from the admin centre’s Marketplace instead, and the admin centre confirmed that Microsoft 365 E5 (Trial) had been added.

The trial runs for one month, ending on 16 November 2026. That date matters: any stage that depends on E5 has to fit inside it, or wait for a decision about paying for the licence.

## Giving it to an account

A licence sitting unassigned doesn’t let anyone use anything. I assigned one licence to the administrator account, so I could open and explore the licensed services from it.

The admin centre then showed:

- **Microsoft 365 E5 (Trial)** in the product list, alongside **Microsoft Entra ID Free**.
- **25 E5 trial licences**, with **one assigned and 24 available**.

The 24 spare licences matter later. When I create named test users for each department, I will only license the ones that need to sign in or enrol a device, rather than spending licences on accounts that don’t.

{% include callout.html title="What this does not prove" text="A licence, or a service plan that is visible or selected, doesn’t show that a feature has been configured or tested. This step records that the environment exists. Each service gets its own step, written only once real configuration and testing evidence exists." %}

{% include quote.html text="A licence and a working admin centre are where the work starts, not proof of it." %}

## Evidence

These are genuine captures from the setup. They will be added once each one has been reviewed and redacted. Tenant, user, subscription, billing and contact identifiers stay private.

{% include evidence.html title="Product list: E5 trial and Entra ID Free" shows="Microsoft 365 E5 (Trial) listed as active alongside Microsoft Entra ID Free." proves="The trial was added to the environment. It doesn’t prove that any service is configured." redact="Billing account and billing profile names. The capture is already partly redacted; check it again before use." where="Microsoft 365 admin centre · Your products" source="Screenshot 2026-10-17 133515.png" %}

{% include evidence.html title="Confirmation that the trial was added" shows="The admin centre message “You’ve added Microsoft 365 E5 (Trial)”." proves="The trial checkout completed after the earlier “Try now” problem." redact="Nothing sensitive expected; check before use." where="Microsoft 365 admin centre · Marketplace" source="Screenshot 2026-10-17 131018.png" %}

{% include evidence.html title="The disabled “Try now” button" optional=true shows="The trial checkout page with the “Try now” button greyed out." proves="Only that the button was unavailable at that point. It adds context to the troubleshooting step." redact="Account initials in the top bar, if preferred." where="Microsoft 365 admin centre · Checkout" source="Screenshot 2026-10-17 121801.png" %}

{% include evidence.html title="Licence assignment" shows="Microsoft 365 E5 selected for one account, with 24 of 25 licences still available." proves="One trial licence was assigned. It doesn’t prove the included services are in use." redact="The assigned user’s name and any account identifier." where="Microsoft 365 admin centre · Licences and apps" source="Screenshot 2026-10-18 112531.png" %}

## Limitations

- This step records the trial setup, not a completed security implementation.
- The screenshots date from 17–18 October 2026. Current licence status and billing terms should be checked directly in the admin centre before any decision relies on them.

## What comes next

With the licence in place, the next job is to check each service it includes. Intune is the first one I’ve documented, in [Microsoft Intune]({{ '/identity-before-detection/preparing-the-environment/intune-readiness/' | relative_url }}). Checking Entra ID, the identity service everything else in Via Wash depends on, is still to do and is on the [roadmap]({{ '/identity-before-detection/' | relative_url }}#roadmap-entra-id).
