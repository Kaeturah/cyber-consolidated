---
title: Building identity in Entra ID
headline: A new starter should not depend on guesswork
kind: topic
topic: building-identity-in-entra-id
order: 50
status: Planned
summary: Follow a Via Wash employee from the HR request through account creation, group-based access, authentication and the device they will use on their first day.
updated: 2026-10-28
permalink: /identity-before-detection/building-identity-in-entra-id/
short: Entra ID
---

## A first day at Via Wash

Imagine a new employee is joining the **Operations** team at one of Via Wash’s branches. HR has confirmed the start date. On the first day, the employee needs to sign in, see the information required for their job, and use a prepared device with the right applications.

That outcome depends on several decisions working together. IT needs to know which person the account represents, which department and role they belong to, what group membership should give them, and how their device and applications will be prepared. A user record on its own is only the first link in that chain.

This topic follows that employee through the identity part of the journey. It starts with a single account, then moves to groups and access, administrative roles, authentication, and checks from the user's point of view. Device enrolment and app installation follow from this identity foundation; they are not implied by creating the account.

## Why the work is split into steps

An account should not be created by copying whatever details happen to be available into a form. The account needs a consistent sign-in name and profile, and the organisation needs a clear rule for how department and job information will lead to access.

For example, an Operations employee may eventually join an Operations access group. That group could become the target for appropriate applications or device policies. For that to happen, the group, its membership rules, and the assignments must first be designed, configured, and tested. Entering “Operations” in a user’s profile does not do those things automatically.

The sequence therefore moves from the person, to the groups and controls around them, then to validation. Learn units that continue one subject will be explained together in the relevant step, while each unit’s learning progress remains separately recorded.

## What exists today

The first user-creation exercise was a Microsoft Learn practice exercise in a separate directory. It gave a chance to walk through the Entra form and see the resulting account in a user list. It did not create a Via Wash employee, assign Via Wash access, enrol a device, or install applications.

The pages below show where that exercise fits, and what must be built before the new-starter journey can be demonstrated in the Via Wash test environment.

