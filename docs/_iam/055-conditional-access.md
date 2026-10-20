---
title: Conditional Access
kind: page
topic: building-identity-in-entra-id
order: 55
status: Planned
summary: Rules that decide whether a sign-in is allowed, based on who, from where and from what.
updated: 2026-10-20
permalink: /identity-before-detection/building-identity-in-entra-id/conditional-access/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Building Conditional Access policies: rules that check each sign-in and decide whether to allow it, require more proof, or block it.

## Why it matters for Via Wash

Conditional Access is where Zero Trust becomes practical. It can require MFA, block risky sign-ins, and later require a compliant device.

## What will be done

- Start policies in report-only mode to see their effect safely
- Require MFA for all users and stronger checks for admins
- Exclude the emergency accounts so nobody gets locked out

## How it will be checked

- Sign-in logs show each policy applying as intended
- A blocked scenario is tested and recorded
