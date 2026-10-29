---
title: Joiners
kind: page
topic: identity-lifecycle
order: 41
status: In progress
summary: Follow Sarah, a Via Wash test identity, from the HR request through account, access, device and first sign-in.
updated: 2026-10-29
permalink: /identity-before-detection/identity-lifecycle/joiners/
---

{% include callout.html title="The first account exists; onboarding is not complete" text="Sarah Eze is now a test identity in the Via Wash tenant. Her account has no group assignments, and sign-in, application access and device setup have not been tested. This page will follow the remaining steps as I build and verify them." %}

## The problem

A new starter’s first day sets the tone. If their account, laptop and access aren’t ready, they sit waiting, and the temptation is to give them broad access “just to get them working”. That shortcut is how new accounts start out over-privileged.

## Sarah’s onboarding, one decision at a time

The [account creation page]({{ '/identity-before-detection/building-identity-in-entra-id/creating-a-user/' | relative_url }}) records Sarah’s Entra user and the details HR would provide: name, role, department and branch. It also records one correction to make before testing membership: Entra currently says **Store Operations**, while the agreed department name is **Operations**.

Next I need to agree what an Operations Store Assistant should be able to reach, create the appropriate groups, and decide how the HR details will add the right person to those groups. A department or job title in the profile does not grant access by itself. I’ll test the membership rule or onboarding workflow before relying on it.

From there, I can work through the rest of Sarah’s first day: assign only the licence she needs, prepare and enrol a test device, make the required applications available, and verify her first sign-in and access. None of those steps is established by the account-creation screenshots.

## How I’ll know it worked

- Sarah receives the agreed Operations access and no access to Finance or HR information.
- Her device enrols and receives only the policies and applications intended for her role.
- Sarah signs in and can use the tools needed for her work; the checks and screenshots show each result.
