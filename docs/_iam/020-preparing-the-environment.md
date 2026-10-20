---
title: Preparing the Microsoft environment
headline: Preparing the Microsoft environment
kind: topic
topic: preparing-the-environment
order: 20
status: In progress
summary: Getting a tenant and the Microsoft 365 E5 licence, then checking that Entra ID, Intune, Defender and the rest are actually ready before building anything.
updated: 2026-10-20
permalink: /identity-before-detection/preparing-the-environment/
short: Environment
---

## Somewhere to build

Before Via Wash can have users, groups, devices or security policies, it needs a Microsoft environment of its own: a **tenant**. A tenant is an organisation’s own space in Microsoft’s cloud, with its own directory of users and its own settings, kept separate from anyone else’s.

## A licence is not the same as being ready

The Microsoft 365 E5 licence switches on a long list of capabilities: Entra ID features such as Conditional Access and Privileged Identity Management, Intune for devices, Defender for endpoints and email, and Purview for audit and compliance.

But having the licence only means those services are *available*. It doesn’t mean each one is reachable, set up correctly, or ready for the work ahead. So this topic has two halves:

1. **Get the tenant and the licence.**
2. **Check each service in turn:** open it, confirm it’s working, and record its starting state before changing anything.

{% include callout.html title="If you’re following along" text="Don’t stop at the licence. Open each service it includes, check it works, and screenshot its starting state before you change anything. That starting point is your evidence later, and it often shows problems early, like a warning or a missing permission." %}

## Where things stand

| Service | What gets checked | Status |
|---|---|---|
| Tenant and E5 licence | Licence active and assigned | Written |
| Entra ID | Tenant details, admin roles, sign-in and audit logs | Not started |
| Intune | Admin centre, devices, enrolment options | Written |
| Defender | Portals, onboarding options, alerts | Not started |
| Audit logs and Azure | Audit logging, Azure subscription for later stages | Not started |

## What it makes possible

Once every service is confirmed ready, the design and build work can start, knowing the environment supports everything the plan needs.
