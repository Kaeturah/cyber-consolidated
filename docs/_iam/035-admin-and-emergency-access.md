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

{% include callout.html title="Not started yet" text="I haven’t done this step yet. This page explains the problem it solves and what I plan to do, and it will be rewritten with the real decisions, configuration and screenshots once the work happens." %}

## The problem

Administrator accounts can change the environment itself. That makes them the most valuable target an attacker can take, and the most damaging account to get wrong.

Right now I do all my work from one administrator account, because someone has to set the environment up. That is a sensible starting point, but it isn’t where I want to stay. As Via Wash’s IT grows into separate functions, broad admin rights in one everyday account become a single point of failure.

## What I plan to decide

- Separate admin accounts from everyday accounts, so browsing and email never happen with admin rights
- The least powerful Entra role for each IT function. IT Support, for example, may only need to reset passwords, not change security policy.
- Just-in-time admin access with Privileged Identity Management, so admin roles are switched on only when needed and expire afterwards
- Two emergency (break-glass) accounts, protected and documented, so a mistake in sign-in policies can never lock everyone out

## How I’ll know it worked

- No everyday account holds an admin role
- Every admin role assignment has a written reason

## Key terms

- **Privileged Identity Management (PIM):** lets someone activate an admin role only when needed, for a limited time
- **Just-in-time access:** admin rights that exist only while they are being used
