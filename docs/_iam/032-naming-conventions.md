---
title: Naming things consistently
kind: page
topic: designing-identity-and-access
order: 32
status: Planned
summary: A simple naming pattern for users, admin accounts, groups and devices, so anything can be recognised at a glance.
updated: 2026-10-20
permalink: /identity-before-detection/designing-identity-and-access/naming-conventions/
---

{% include callout.html title="Not started yet" text="I haven’t done this step yet. This page explains the problem it solves and what I plan to do, and it will be rewritten with the real decisions, configuration and screenshots once the work happens." %}

## The problem

Names turn up everywhere: in the admin centres, in sign-in logs and in alerts. When an alert says an account did something unusual, I want the name alone to tell me whether it’s an everyday account or an admin account, and which department it belongs to. Without a convention, every investigation starts with “what is this?”.

## What I plan to decide

- A pattern for everyday staff accounts
- A separate, obvious pattern for administrator accounts, so an admin account can never be mistaken for an everyday one
- A pattern for groups that shows the department or IT function they belong to
- A pattern for devices that shows what kind of device it is

I will write each pattern down with an example, and keep using it in the on-premises work too, so names match in both places.

## How I’ll know it worked

- Every object I create later can be named using the patterns
- Reading a name in a log is enough to know roughly what the object is
