---
title: Who needs an identity?
kind: page
topic: designing-identity-and-access
order: 31
status: Planned
summary: Staff are only part of it. Admin accounts, service accounts, devices and emergency accounts all need identities too.
updated: 2026-10-20
permalink: /identity-before-detection/designing-identity-and-access/who-needs-an-identity/
---

{% include callout.html title="Not started yet" text="I haven’t done this step yet. This page explains the problem it solves and what I plan to do, and it will be rewritten with the real decisions, configuration and screenshots once the work happens." %}

## The problem

When people think of identities, they think of staff accounts. But Via Wash will have more than that. There is my own administrator account. There will be emergency accounts for when normal admin access fails. Later there may be service accounts for automated jobs, the devices themselves, and possibly guests such as an outside accountant.

Each of these carries a different risk. An everyday staff account, an administrator account and an emergency account shouldn’t be protected or reviewed the same way. If I don’t define the types up front, the riskiest accounts end up treated like ordinary ones.

## What I plan to decide

- Which identity types Via Wash needs now (staff, administrators, emergency accounts) and which can wait (service accounts, guests)
- What each type is for, and who owns it
- How each type should be protected and reviewed

## How I’ll know it worked

- Every account I create later fits exactly one type
- Each type has an owner and a clear purpose written down

## Key terms

- **Break-glass account:** an emergency administrator account kept aside for when normal admin access fails
- **Service account:** an identity used by an application or automated process rather than a person
