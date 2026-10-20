---
title: Designing identity and access
headline: Deciding who gets access to what
kind: topic
topic: designing-identity-and-access
order: 30
status: Planned
summary: "Before any account is created: the principles, identity types, naming, groups and access levels that the Entra ID build will follow."
updated: 2026-10-20
permalink: /identity-before-detection/designing-identity-and-access/
short: Design
---

{% include callout.html title="Not started yet" text="This topic sets out the design questions. Each step will be written as the design decisions are made." %}

## Why design comes first

It would be quick to open Entra ID and start creating accounts. But accounts created without a plan tend to collect permissions nobody can explain. Six months later, nobody remembers why someone in Operations can see payroll.

Designing first means every account, group and permission has a reason that can be written down, checked and defended.

## The principles behind the design

- **Least privilege.** Every identity gets only the access its job needs, and no more.
- **Role-based access.** Access follows the job, through groups, rather than being granted person by person.
- **Separation of duties.** No single person should be able to do something sensitive end to end on their own, such as both approving and paying an invoice.
- **Zero Trust.** Being inside the network or signed in once doesn’t earn trust. Every request is checked against who is asking, from what device, and how risky it looks.

## How the design connects to the build

Each step in this topic produces a decision that the [Entra ID build]({{ '/identity-before-detection/building-identity-in-entra-id/' | relative_url }}) will follow. If the build ever needs to break the design, the design gets updated first.
