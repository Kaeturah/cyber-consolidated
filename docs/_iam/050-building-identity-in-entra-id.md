---
title: Building identity in Entra ID
headline: Everything starts with who people are.
kind: topic
topic: building-identity-in-entra-id
order: 50
status: Planned
summary: "Stage 1: turning the identity design into real users, groups, roles and sign-in controls in Microsoft Entra ID."
updated: 2026-10-20
permalink: /identity-before-detection/building-identity-in-entra-id/
short: Entra ID
---

{% include callout.html title="Not started yet" text="This topic sets out the plan for stage 1. It will be rewritten with real configuration, test results and evidence as the work happens." %}

## Why this stage comes first

Every security decision eventually comes back to a person. Should this account reach payroll data? Should it be able to change other people’s passwords? Is this sign-in from the person it claims to be?

None of those questions can be answered until the identities exist and are organised sensibly. Identity gives every later stage its context. Devices are assigned to users, policies target groups, and alerts are judged against what a user would normally do.

## What it depends on

- The [Microsoft 365 E5 test environment]({{ '/identity-before-detection/preparing-the-environment/tenant-and-e5-licence/' | relative_url }}), which provides Microsoft Entra ID.
- The [company profile]({{ '/identity-before-detection/start-here/company-profile/' | relative_url }}): six departments and the functions inside IT.

## How it will be validated

Each control will be tested from the user’s side, not just from the settings page. That means signing in as test users from different departments and confirming they can reach what they should and can’t reach what they shouldn’t, then recording both results.

## What it makes possible

Once identities and groups exist, stage 2 can tie devices to their users, and later stages have a baseline of normal access to compare against.
