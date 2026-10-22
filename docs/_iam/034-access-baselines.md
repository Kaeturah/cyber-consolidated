---
title: Access baselines
kind: page
topic: designing-identity-and-access
order: 34
status: Planned
summary: What every employee gets, what each department adds on top, and how exceptions are approved.
updated: 2026-10-20
permalink: /identity-before-detection/designing-identity-and-access/access-baselines/
---

{% include callout.html title="Not started yet" text="I haven’t done this step yet. This page explains the problem it solves and what I plan to do, and it will be rewritten with the real decisions, configuration and screenshots once the work happens." %}

## The problem

Not all access is about departments. Everyone at Via Wash will need some things, such as email and company-wide information. Each department needs more on top. And now and then someone will need something unusual for a short time.

If those three kinds of access are mixed together, nobody can explain why a person has what they have. Layering them keeps it explainable.

## What I plan to decide

- **The company baseline:** what every employee gets on day one
- **The department layer:** what each of the six departments adds, for example order systems for Operations or financial records for Finance
- **Exceptions:** how one-off access is requested, who approves it, and when it ends

## How I’ll know it worked

- Any test user’s access can be explained layer by layer
- Every exception has an owner and an end date
