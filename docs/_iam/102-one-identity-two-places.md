---
title: One identity, two places
kind: page
topic: hybrid-identity
order: 102
status: Planned
summary: Checking a synced user can sign in on-premises and in the cloud, and what happens when something changes.
updated: 2026-10-20
permalink: /identity-before-detection/hybrid-identity/one-identity-two-places/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Testing a synced account end to end: signing in on-premises and to cloud services, then changing something on-premises and watching it reach the cloud.

## Why it matters for Via Wash

Sync isn’t proven by a user appearing in a list. It is proven when the same person can work in both places, and when changes and leavers flow through correctly.

## What will be done

- Sign in as a synced user on the domain-joined client and to Microsoft 365
- Change a department on-premises and check it syncs
- Disable an account on-premises and check access stops in the cloud

## How it will be checked

- Each change appears in Entra ID after a sync
- A disabled on-premises account can no longer sign in to the cloud
