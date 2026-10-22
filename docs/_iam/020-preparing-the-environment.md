---
title: Preparing the Microsoft environment
headline: Preparing the Microsoft environment
kind: topic
topic: preparing-the-environment
order: 20
status: In progress
summary: Getting a tenant and the Microsoft 365 E5 licence, then checking each service before building on it. The licence is in place and Intune has been checked; the other services haven’t been checked yet.
updated: 2026-10-20
permalink: /identity-before-detection/preparing-the-environment/
short: Environment
current: true
---

## Somewhere to build

Before Via Wash can have users, groups, devices or security policies, it needs a Microsoft environment of its own: a **tenant**. A tenant is an organisation’s own space in Microsoft’s cloud, with its own directory of users and its own settings, kept separate from anyone else’s. For this project it is the Cyber Consolidated tenant.

## Why a licence isn’t the same as being ready

The Microsoft 365 E5 licence switches on a long list of capabilities: Entra ID features such as Conditional Access and Privileged Identity Management, Intune for devices, Defender for endpoints and email, and Purview for audit and compliance.

When I added the licence, it was tempting to treat the environment as ready. But a licence only makes those services *available*. It doesn’t tell me whether each one opens, whether it is healthy, or what state it starts in. I’ve already seen the gap between the two. The Intune dashboard looked healthy, but it also showed zero enrolled devices and an MDM user scope set to None. Nothing was wrong, but nothing was ready either.

So this topic has two halves:

1. **Get the tenant and the licence.**
2. **Check each service in turn.** Open it, confirm it works, and record its starting state before changing anything.

{% include callout.html title="If you’re following along" text="Don’t stop at the licence. Open each service it includes, check it works, and screenshot its starting state before you change anything. That starting point is your evidence later, and it often shows problems early, like a warning or a setting that isn’t what you expected." %}

## Where things stand

| Service | What gets checked | Status |
|---|---|---|
| Tenant and E5 licence | Licence active and assigned | Written |
| Entra ID | Tenant details, admin roles, sign-in and audit logs | Not started |
| Intune | Starting point, test group, automatic enrolment scope | Under way |
| Defender | Portals, onboarding options, alerts | Not started |
| Audit logs and Azure | Audit logging, Azure subscription for later stages | Not started |

## What it makes possible

So far only Intune has been checked, and its device enrolment is still to do. The other services will be checked before any work depends on them, so the build starts on solid ground.
