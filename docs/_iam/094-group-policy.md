---
title: Group Policy
kind: page
topic: on-premises-it
order: 94
status: Planned
summary: Applying settings to every machine and user from one place.
updated: 2026-10-20
permalink: /identity-before-detection/on-premises-it/group-policy/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Creating Group Policy Objects (GPOs) that apply settings, such as a password policy, a desktop setting or a mapped drive, to the right OUs.

## Why it matters for Via Wash

Group Policy is how IT keeps hundreds of machines consistent without visiting each one. It is a core day-to-day admin skill.

## What will be done

- Create a GPO for a company-wide setting
- Create a GPO that applies only to one department
- Link them to the right OUs

## How it will be checked

- The settings appear on the test client after a policy refresh
- Policy results show which GPOs applied, and why

## Key terms

- **GPO (Group Policy Object)**: a set of settings applied to users or computers in an OU
