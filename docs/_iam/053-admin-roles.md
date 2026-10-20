---
title: Admin roles
kind: page
topic: building-identity-in-entra-id
order: 53
status: Planned
summary: Giving IT functions the least powerful roles that do the job, with just-in-time activation.
updated: 2026-10-20
permalink: /identity-before-detection/building-identity-in-entra-id/admin-roles/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Assigning Entra admin roles to the IT functions, and setting up Privileged Identity Management for just-in-time access.

## Why it matters for Via Wash

This is where least privilege becomes real. Getting it wrong means either too much power in too many hands, or admins who can’t do their jobs.

## What will be done

- Create separate admin accounts
- Assign the smallest suitable role to each IT function
- Make roles eligible through PIM rather than permanent
- Set up the emergency accounts

## How it will be checked

- An admin can activate their role, do the task and lose it again
- No everyday account holds a role
