---
title: From departments to groups
kind: page
topic: designing-identity-and-access
order: 33
status: Planned
summary: Turning Via Wash’s six departments and the functions inside IT into the groups that will control access.
updated: 2026-10-20
permalink: /identity-before-detection/designing-identity-and-access/departments-into-groups/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

The group design: how Management, Finance, HR, Operations, Delivery Team and IT, and the functions inside IT, become groups in Entra ID.

## Why it matters for Via Wash

Granting access person by person doesn’t scale and is hard to review. Groups let access follow the job: put someone in the Finance group, and they get what Finance needs.

## What will be done

- Define one group per department
- Define role groups inside IT, such as IT Support and Endpoint Management
- Decide which groups use automatic (dynamic) membership based on the department field
- Write down what each group grants

## How it will be checked

- Every department and IT function maps to a group
- Each group’s purpose is written down

## Key terms

- **Security group**: a group used to grant access
- **Dynamic group**: a group whose members are added automatically by a rule, such as department equals Finance
