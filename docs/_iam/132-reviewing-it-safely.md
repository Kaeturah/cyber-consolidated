---
title: Reviewing it safely
kind: page
topic: application-security
order: 132
status: Planned
summary: Checking the app’s security controls properly, in an isolated environment, before anything is claimed.
updated: 2026-10-20
permalink: /identity-before-detection/application-security/reviewing-it-safely/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

A careful review of the app’s existing security controls, tested in a non-production environment.

## Why it matters for Via Wash

The existing controls are an inventory, not a guarantee. A review shows whether they actually do what they were meant to, and fixes anything that doesn’t.

## What will be done

- Review who can read the detection view and insert log events
- Check whether the forwarded IP address can be trusted
- Check what happens if logging fails
- Test in an isolated copy, never the live database without approval
- Fix confirmed issues and retest

## How it will be checked

- Each review item has a recorded result
- Fixes are retested
