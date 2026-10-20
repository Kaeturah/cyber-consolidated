---
title: Movers
kind: page
topic: joiners-movers-and-leavers
order: 42
status: Planned
summary: What happens when someone changes department or role, so old access doesn’t quietly stay behind.
updated: 2026-10-20
permalink: /identity-before-detection/joiners-movers-and-leavers/movers/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

The process for a role or department change: reviewing access, removing what is no longer needed, and adding what the new role needs.

## Why it matters for Via Wash

Movers are where access quietly builds up. Someone who moves from Finance to Operations shouldn’t keep Finance access just because nobody removed it.

## What will be done

- Change the department field and let group membership update
- Review anything granted outside the groups
- Remove old exceptions and confirm the new access

## How it will be checked

- A test mover loses their old department’s access and gains the new one’s
