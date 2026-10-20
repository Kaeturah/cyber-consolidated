---
title: A new starter’s first day
headline: From an HR request to a ready laptop
kind: topic
topic: a-new-starters-first-day
order: 110
status: Planned
summary: "One new Via Wash employee, followed from the HR request to their first sign-in: the account, the access, the laptop and the apps that install themselves."
updated: 2026-10-20
permalink: /identity-before-detection/a-new-starters-first-day/
short: First day
---

{% include callout.html title="Not started yet" text="This scenario will be run once identity, devices and on-premises IT are in place. Each step will record what actually happened." %}

## Why follow one person

The earlier topics build the pieces one at a time. This one puts them together and asks a simple question: when someone new joins Via Wash, does it all just work?

We will follow one new starter, joining the Operations team, through their first day. The aim is that IT creates the account and puts it in the right group, and almost everything else happens automatically.

## The journey

{% include flow.html label="A new starter’s first day" steps="HR request|Account created|Access through groups|Laptop ready|Apps install|First sign-in" notes="HR tells IT who is joining and in which role.|One account, with the department filled in.|Group membership brings licences, files and app access.|The device is prepared and enrolled.|Software arrives because of the group, not by hand.|MFA registered, everything checked." %}

## What this shows

- **Groups do the work.** Nobody installs apps or grants folders one by one.
- **The cloud and on-premises routes side by side.** In the cloud, Intune deploys the apps. On-premises, Group Policy does. Both are shown.
- **Proof, not assumption.** Every step is checked from the new starter’s point of view.

## What it depends on

[Building identity in Entra ID]({{ '/identity-before-detection/building-identity-in-entra-id/' | relative_url }}), [Managing devices with Intune]({{ '/identity-before-detection/managing-devices/' | relative_url }}) and [On-premises IT]({{ '/identity-before-detection/on-premises-it/' | relative_url }}). The process design comes from [Identity lifecycle]({{ '/identity-before-detection/identity-lifecycle/' | relative_url }}).
