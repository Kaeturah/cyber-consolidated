---
title: Joining Windows 11 to the domain
kind: page
topic: on-premises-it
order: 93
status: Planned
summary: Making the test laptop part of the domain, so staff sign in with their domain account.
updated: 2026-10-20
permalink: /identity-before-detection/on-premises-it/joining-windows-11/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Joining the lab’s Windows 11 client to the Via Wash domain and signing in as a test user.

## Why it matters for Via Wash

This is the everyday reality in many offices: a staff member turns on a company laptop and signs in with their work account, and IT can manage the machine centrally.

## What will be done

- Point the client at the domain’s DNS
- Join it to the domain and move it to the right OU
- Sign in as a test user from one department

## How it will be checked

- The test user signs in and the computer appears in Active Directory
