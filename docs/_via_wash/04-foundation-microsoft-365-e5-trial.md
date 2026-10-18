---
title: Microsoft 365 E5 trial
headline: "The environment is ready. Nothing is configured yet."
short: E5 trial
order: 4
part: Foundation
part_intro: The groundwork laid before stage 1 — somewhere to build, a first look at device management, and a working domain and email identity.
status: Documented
status_note: Trial setup documented. Licensing and billing should be rechecked before any decision relies on them.
summary: How the Microsoft test environment was set up, what the evidence shows, and why a licence on its own proves nothing is configured.
updated: 2026-10-18
permalink: /via-wash/foundation/microsoft-365-e5-trial/
---

## Why this stage matters

Via Wash needs a controlled Microsoft environment where identity, device management and security controls can be explored against a realistic business. The Microsoft 365 E5 trial was started to make the relevant services available for hands-on learning and validation.

This is a test environment, not a production deployment.

## What was done

The trial was added through the Microsoft 365 admin centre on 17 October 2026. It didn’t go through first time: the “Try now” button on the checkout page was disabled to begin with. The trial was then added successfully, and the admin centre confirmed that Microsoft 365 E5 (Trial) had been added.

The trial runs for one month, ending on 16 November 2026. One licence was then assigned, so the environment could be explored from a licensed account.

## What it established

- A product view showed **Microsoft 365 E5 (Trial)** alongside **Microsoft Entra ID Free**.
- A licensing view showed **25 E5 trial licences**, with **one assigned and 24 available**.

{% include callout.html title="What this does not prove" text="A licence, or a service plan that is visible or selected, doesn’t show that a feature has been configured or tested. This chapter records that the environment exists. Each capability gets its own chapter, written only once real configuration and testing evidence exists." %}

{% include quote.html text="A licence and a working admin centre are where the work starts, not proof of it." %}

## Why it matters to Via Wash

Several of the [six build stages]({{ '/via-wash/what-are-we-building/' | relative_url }}) rely on services included in E5, so the trial is a dependency for much of the project rather than a piece of work in its own right. It also sets a time limit: anything that depends on E5 has to fit inside the trial period or wait for a licensing decision.

## Evidence

These are genuine captures from the setup. They will be added once each one has been reviewed and redacted. Tenant, user, subscription, billing and contact identifiers stay private.

{% include evidence.html title="Product list: E5 trial and Entra ID Free" shows="Microsoft 365 E5 (Trial) listed as active alongside Microsoft Entra ID Free." proves="The trial was added to the environment. It doesn’t prove that any service is configured." redact="Billing account and billing profile names. The capture is already partly redacted; check it again before use." where="Microsoft 365 admin centre · Your products" source="Screenshot 2026-10-17 133515.png" %}

{% include evidence.html title="Confirmation that the trial was added" shows="The admin centre message “You’ve added Microsoft 365 E5 (Trial)”." proves="The trial checkout completed after the earlier “Try now” problem." redact="Nothing sensitive expected; check before use." where="Microsoft 365 admin centre · Marketplace" source="Screenshot 2026-10-17 131018.png" %}

{% include evidence.html title="The disabled “Try now” button" optional=true shows="The trial checkout page with the “Try now” button greyed out." proves="Only that the button was unavailable at that point. It adds context to the troubleshooting step." redact="Account initials in the top bar, if preferred." where="Microsoft 365 admin centre · Checkout" source="Screenshot 2026-10-17 121801.png" %}

{% include evidence.html title="Licence assignment" shows="Microsoft 365 E5 selected for one account, with 24 of 25 licences still available." proves="One trial licence was assigned. It doesn’t prove the included services are in use." redact="The assigned user’s name and any account identifier." where="Microsoft 365 admin centre · Licences and apps" source="Screenshot 2026-10-18 112531.png" %}

## Limitations

- This chapter records the trial setup, not a completed security implementation.
- The screenshots date from 17–18 October 2026. Current licence status and billing terms should be checked directly in the admin centre before any decision relies on them.

## What comes next

With the environment in place, the first build stage is [identity and access]({{ '/via-wash/identity-and-access/' | relative_url }}). Devices, security policies and monitoring all depend on knowing who Via Wash’s users are and what they should be able to reach.
