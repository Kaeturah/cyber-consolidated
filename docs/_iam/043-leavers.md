---
title: Leavers
kind: page
topic: identity-lifecycle
order: 43
status: Planned
summary: "Removing access properly when someone leaves: more than just disabling the account."
updated: 2026-10-20
permalink: /identity-before-detection/identity-lifecycle/leavers/
---

{% include callout.html title="Not started yet" text="I haven’t done this step yet. This page explains the problem it solves and what I plan to do, and it will be rewritten with the real decisions, configuration and screenshots once the work happens." %}

## The problem

Disabling an account feels like the end of the job, but it often isn’t. A session that was already signed in can keep working for a while. An admin account, an app permission or a device can all outlive the main account if nobody deals with them. A leaver’s access has to be removed properly, not just switched off.

## What I plan to do

- Disable the account and revoke any active sessions
- Remove group memberships, licences and any separate admin accounts
- Retire or wipe their device
- Hand ownership of their files and mailbox to the right person

## How I’ll know it worked

- A test leaver can no longer sign in anywhere
- Their device shows as retired
