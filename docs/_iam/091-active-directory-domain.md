---
title: The Active Directory domain
kind: page
topic: hybrid-identity
order: 91
status: Planned
summary: Turning the lab server into a domain controller for Via Wash.
updated: 2026-10-20
permalink: /identity-before-detection/hybrid-identity/active-directory-domain/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Installing Active Directory Domain Services on the lab server and creating Via Wash’s on-premises domain.

## Why it matters for Via Wash

Active Directory is still how many organisations manage identities on their own servers. Building one shows how it works and how it differs from Entra ID.

## What will be done

- Install the AD DS role and promote the server to a domain controller
- Join the test client to the domain, if the design calls for it

## How it will be checked

- The domain is running and the client can find it
