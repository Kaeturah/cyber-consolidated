---
title: Identity lifecycle
headline: Access has to change when people do
kind: topic
topic: identity-lifecycle
order: 40
status: Planned
summary: "Joiners, movers and leavers: how access is given when someone starts, adjusted when their role changes, and removed when they leave."
updated: 2026-10-20
permalink: /identity-before-detection/identity-lifecycle/
short: Lifecycle
---

{% include callout.html title="Not started yet" text="This topic sets out the lifecycle design. Each step will be written once the design is agreed and tested." %}

## Why the lifecycle matters

Getting access right on someone’s first day is only the start. People change roles, take on extra responsibilities and eventually leave, and access that was right six months ago can be wrong today.

The most common access problems aren’t dramatic hacks. They are a mover who kept their old permissions, or a leaver whose account was never switched off.

## The three moments

{% include flow.html label="The identity lifecycle" steps="Joiner|Mover|Leaver" notes="Account created, access given through groups, device prepared, sign-in methods registered.|Old access removed, new access added, exceptions reviewed.|Account disabled, sessions revoked, access and licences removed, device retired." %}

| Moment | The question it answers |
|---|---|
| Joiner | What does this person need on day one? |
| Mover | What should change when their role or department changes? |
| Leaver | What must be removed when they leave? |

The rule underneath all three: access should match what someone does **now**, not everything they have ever done.

## How it connects

HR starts each change, IT carries it out, and the groups from the [design]({{ '/identity-before-detection/designing-identity-and-access/' | relative_url }}) do most of the work automatically. To see the joiner process from start to finish, with a real new starter, account, laptop and apps, follow [A new starter’s first day]({{ '/identity-before-detection/a-new-starters-first-day/' | relative_url }}).
