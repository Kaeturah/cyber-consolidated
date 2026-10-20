---
title: Admin and emergency access
kind: page
topic: designing-identity-and-access
order: 35
status: Planned
summary: Keeping powerful access separate from everyday work, and planning for the day normal admin access fails.
updated: 2026-10-20
permalink: /identity-before-detection/designing-identity-and-access/admin-and-emergency-access/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

The plan for privileged access: separate admin accounts, the smallest role that does the job, and an emergency account for recovery.

## Why it matters for Via Wash

Admin accounts can change the environment itself, which makes them the most valuable target for an attacker. Keeping them separate, limited and closely watched reduces the damage if something goes wrong.

## What will be done

- Separate admin accounts from everyday accounts
- Map IT functions to the least powerful Entra roles that do the job
- Plan just-in-time admin access with Privileged Identity Management
- Plan and document two emergency (break-glass) accounts

## How it will be checked

- No everyday account holds an admin role
- Every admin role assignment has a written reason

## Key terms

- **Privileged Identity Management (PIM)**: lets someone activate an admin role only when needed, for a limited time
- **Just-in-time access**: admin rights that exist only while they are being used
