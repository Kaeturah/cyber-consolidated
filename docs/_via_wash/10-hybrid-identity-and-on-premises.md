---
title: Hybrid identity and on-premises infrastructure
headline: "Where the cloud meets the server room."
short: Hybrid identity
order: 10
stage: 4
part: Build stages
status: Planned
summary: A small test Active Directory domain, and how traditional infrastructure and cloud identity meet.
updated: 2026-10-18
permalink: /via-wash/hybrid-identity-and-on-premises/
---

{% include callout.html title="Not started yet" text="No on-premises infrastructure or synchronisation is claimed. This chapter will record what the lab could realistically support, what was built, and what stayed as a documented design." %}

## Why this stage matters

Many organisations still run traditional servers, with user accounts managed in on-premises Active Directory, alongside their cloud services. Understanding how the two connect, and where that connection can go wrong, is part of understanding real environments rather than only cloud-only ones.

## What it depends on

- The identity design from [stage 1]({{ '/via-wash/identity-and-access/' | relative_url }}), so that on-premises accounts and groups mirror the same departments.
- Enough lab capacity to run a Windows Server virtual machine, ideally alongside a client machine.

## What it will cover

- Lab requirements and constraints
- An Active Directory Domain Services design
- Users, groups and organisational units
- An identity synchronisation approach, if it proves feasible
- Validation and troubleshooting
- A clear line between what a lab can show and what a production environment would need

## How it will be validated

Domain sign-ins, group membership and, if synchronisation is built, the same identity appearing correctly in the cloud, each shown with evidence from both sides.

## What it makes possible

Scenarios that cross the boundary between traditional and cloud infrastructure, for stages 5 and 6 to monitor and investigate.
