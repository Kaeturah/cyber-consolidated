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

{% include callout.html title="Not started yet" text="I haven’t done this step yet. This page explains the problem it solves and what I plan to do, and it will be rewritten with the real decisions, configuration and screenshots once the work happens." %}

## The problem

Via Wash has six departments, and the IT department has several functions inside it. If I grant access to each person individually, every new starter becomes a list of manual tasks, and every leaver becomes a list of things that might be forgotten. Groups solve that: access is granted to the group once, and people inherit it by being in the group.

The hard part is deciding the groups well. Too few, and people get access they don’t need. Too many, and nobody can tell what each one is for.

## What I plan to decide

- One group per department: Management, Finance, HR, Operations, Delivery Team and IT
- Role groups inside IT, such as IT Support and Endpoint Management, so IT access can be split by function rather than given to everyone in IT
- Which groups should fill themselves automatically (dynamic membership based on the department recorded on each account) and which should be managed by hand (assigned membership)
- What each group is allowed to reach, written down next to it

I already used an assigned group once, for the Intune test: `VW-Intune-Test-Devices`, so I could choose exactly who was in scope. That was a deliberate choice for a test. This step decides the permanent department structure.

## How I’ll know it worked

- Every department and IT function maps to a group with a written purpose
- Changing a test user’s department moves them into the right group

## Key terms

- **Security group:** a group used to grant access
- **Dynamic group:** a group whose members are added automatically by a rule, such as “department equals Finance”
