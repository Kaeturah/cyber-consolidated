---
title: Audit logs and Azure
kind: page
topic: preparing-the-environment
order: 25
status: Planned
summary: "The last checks: making sure activity is being recorded, and deciding whether an Azure subscription is needed for later stages."
updated: 2026-10-20
permalink: /identity-before-detection/preparing-the-environment/audit-logs-and-azure/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Two final checks. First, that audit logging is switched on, so changes made in the tenant are recorded. Second, whether an Azure subscription is needed. Some later tools, such as Microsoft Sentinel, run on Azure and are billed by use rather than included in the E5 licence.

## Why it matters for Via Wash

Monitoring and incident response can only use what was recorded. Switching audit logging on late means losing the history of how the environment was built. And knowing Azure’s cost early avoids a surprise in stage 5.

## What will be done

- Confirm audit logging is on in Microsoft Purview
- Run a test audit search and record the result
- Decide whether an Azure subscription is needed yet, and record the reasoning and any spending limit

## How it will be checked

- An audit search returns recent admin activity
- The Azure decision and any budget limit are written down

## Key terms

- **Audit log**: a record of who changed what in the tenant, and when
- **Microsoft Purview**: Microsoft’s compliance and data governance portal, which includes audit search
- **Microsoft Sentinel**: a cloud SIEM that collects and analyses security data, billed through Azure
