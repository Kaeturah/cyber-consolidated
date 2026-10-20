---
title: Is Entra ID ready?
kind: page
topic: preparing-the-environment
order: 22
status: Planned
summary: Reviewing the tenant in the Entra admin centre before any identities are built inside it.
updated: 2026-10-20
permalink: /identity-before-detection/preparing-the-environment/entra-id-readiness/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

A review of Microsoft Entra ID, the identity service at the heart of the tenant, before anything is created in it. It records the tenant’s basic details, who already has administrative access, and whether the licensed identity features are visible.

## Why it matters for Via Wash

Every later topic builds on Entra ID. Knowing its starting state means any later change can be traced, and it catches problems early, like the wrong tenant, a missing licence feature, or an admin account with more access than intended.

## What will be done

- Open the Entra admin centre and confirm it is the Cyber Consolidated tenant
- Record the tenant’s overview: licence edition, domains and user count
- List existing users and who holds administrative roles
- Check that E5 identity features appear, such as Conditional Access and Privileged Identity Management
- Confirm sign-in logs and audit logs are being recorded

## How it will be checked

- The overview shows the expected tenant and licence edition
- Admin roles are held only by the intended account
- Sign-in and audit logs show recent activity

## Key terms

- **Tenant**: an organisation’s own space in Microsoft’s cloud
- **Entra ID**: Microsoft’s cloud identity service, formerly Azure Active Directory
- **Global Administrator**: the most powerful role in a tenant, to be used sparingly
