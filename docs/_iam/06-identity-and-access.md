---
title: Identity and access
headline: "Everything starts with who people are."
short: Identity and access
order: 6
stage: 1
current: true
part: Build stages
part_intro: Six stages, each built on the one before — from knowing who the users are to responding when something goes wrong.
status: Planned
status_note: Next up. This chapter will be written as the work happens.
summary: Deciding who Via Wash’s people are, what each of them should reach, and how access changes when people join, move and leave.
updated: 2026-10-18
permalink: /identity-before-detection/identity-and-access/
---

{% include callout.html title="Not started yet" text="This chapter sets out the plan for stage 1. It will be rewritten with real configuration, test results and evidence as the work happens." %}

## Why this stage comes first

Every security decision eventually comes back to a person. Should this account reach payroll data? Should it be able to change other people’s passwords? Is this sign-in from the person it claims to be?

None of those questions can be answered until the identities exist and are organised sensibly. Identity gives every later stage its context. Devices are assigned to users, policies target groups, and alerts are judged against what a user would normally do.

## What it depends on

- The [Microsoft 365 E5 test environment]({{ '/identity-before-detection/microsoft-365-e5-trial/' | relative_url }}), which provides Microsoft Entra ID.
- The [company profile]({{ '/identity-before-detection/company-profile/' | relative_url }}): six departments and the functions inside IT.

## What it will cover

- The directory and tenant context
- Users and groups mapped to Management, Finance, HR, Operations, Delivery Team and IT
- Least privilege and role assignment, including how administrative roles are handled
- Authentication and access policies
- Conditional Access and identity protection, where available and actually configured
- The joiner, mover and leaver lifecycle

## How it will be validated

Each control will be tested from the user’s side, not just from the settings page. That means signing in as test users from different departments and confirming they can reach what they should and can’t reach what they shouldn’t, then recording both results.

## What it makes possible

Once identities and groups exist, stage 2 can tie devices to their users, and later stages have a baseline of normal access to compare against.
