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

{% include callout.html title="Not started yet" text="This topic sets out the design questions I need to answer. Each step will be written up as I make the decisions." %}

## The problem with creating accounts first

It would be quick to open Entra ID and start creating accounts for Via Wash. But accounts created without a plan tend to collect permissions nobody can explain. Six months later, nobody remembers why someone in Operations can see payroll, or why an old test account still has admin rights.

Via Wash makes the risk concrete. Finance holds payments and payroll. HR holds employee records. Operations runs the orders and branches. Delivery staff work from phones on the road. Each department needs different things, and some of what Finance and HR hold would cause real harm in the wrong hands. If I don’t design access first, I will end up granting it person by person, and that is exactly how permissions drift.

## The principles I’m designing to

- **Least privilege.** Every identity gets only the access its job needs. A Delivery driver needs collection and delivery details, not financial records.
- **Role-based access.** Access follows the job, through groups, rather than being granted to individuals. When someone joins Finance, they get what Finance needs because they are in Finance.
- **Separation of duties.** No single person should be able to complete something sensitive end to end on their own, such as both approving and paying an invoice.
- **Zero Trust.** Being signed in once, or being on the office network, doesn’t earn trust. Each request is judged on who is asking, from what device, and how risky it looks.

## What this topic will produce

Each step answers one design question and records the decision with its reasoning. The [Entra ID build]({{ '/identity-before-detection/building-identity-in-entra-id/' | relative_url }}) will follow those decisions. If the build ever needs to break the design, I will update the design first, so the documentation always explains why the environment looks the way it does.
