---
title: Deploying software by group
kind: page
topic: on-premises-it
order: 96
status: Planned
summary: Software that installs itself because the user or computer is in the right group.
updated: 2026-10-20
permalink: /identity-before-detection/on-premises-it/software-by-group/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Deploying an application to a department through Group Policy, so it installs automatically for members of that group.

## Why it matters for Via Wash

Installing software by hand doesn’t scale. Group-based deployment means a new starter gets the right apps just by being placed in the right group.

## What will be done

- Choose an application packaged as an MSI installer
- Deploy it to a department group or OU through Group Policy
- Restart the test client and watch it install

## How it will be checked

- The app installs for a member of the group and not for anyone else
