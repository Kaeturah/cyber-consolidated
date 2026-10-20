---
title: Hybrid identity
headline: Where the cloud meets the server room.
kind: topic
topic: hybrid-identity
order: 100
status: Planned
summary: Connecting the on-premises Active Directory domain to Entra ID, so one identity works in both places.
updated: 2026-10-20
permalink: /identity-before-detection/hybrid-identity/
short: Hybrid
---

{% include callout.html title="Not started yet" text="No on-premises infrastructure or synchronisation is claimed. This topic will record what the lab could realistically support, what was built, and what stayed as a documented design." %}

## Why this stage matters

Many organisations still run traditional servers, with user accounts managed in on-premises Active Directory, alongside their cloud services. Understanding how the two connect, and where that connection can go wrong, is part of understanding real environments rather than only cloud-only ones.

## What it depends on

- The identity design from [stage 1]({{ '/identity-before-detection/building-identity-in-entra-id/' | relative_url }}), so that on-premises accounts and groups mirror the same departments.
- The domain from [On-premises IT]({{ '/identity-before-detection/on-premises-it/' | relative_url }}).

## How it will be validated

Domain sign-ins, group membership and, if synchronisation is built, the same identity appearing correctly in the cloud, each shown with evidence from both sides.

## What it makes possible

Scenarios that cross the boundary between traditional and cloud infrastructure, for stages 5 and 6 to monitor and investigate.
