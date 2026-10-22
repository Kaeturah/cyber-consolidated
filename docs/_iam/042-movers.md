---
title: Movers
kind: page
topic: identity-lifecycle
order: 42
status: Planned
summary: What happens when someone changes department or role, so old access doesn’t quietly stay behind.
updated: 2026-10-20
permalink: /identity-before-detection/identity-lifecycle/movers/
---

{% include callout.html title="Not started yet" text="I haven’t done this step yet. This page explains the problem it solves and what I plan to do, and it will be rewritten with the real decisions, configuration and screenshots once the work happens." %}

## The problem

Movers are where access quietly builds up. When someone moves from Finance to Operations, giving them the Operations access is the easy part, because they will ask for it. Removing the Finance access is the part that gets forgotten, because nobody asks for it to be taken away.

## What I plan to do

- Change the department on the account and let group membership update automatically
- Review anything granted outside the groups, such as exceptions
- Remove what the old role needed and confirm the new access works

## How I’ll know it worked

- A test mover loses the old department’s access and gains the new department’s
