---
title: What are we building?
kind: page
topic: start-here
order: 12
status: Documented
summary: The order the work happens in, what each part depends on, what it makes possible next, and the practical limits of the lab.
updated: 2026-10-18
permalink: /identity-before-detection/start-here/what-are-we-building/
headline: Six stages, each one standing on the last.
status_note: This chapter describes the plan; each stage has its own status.
---

## The shape of the journey

I’m not building Via Wash’s environment all at once. Each part gives the next something to stand on, and the whole project follows one progression:

**Design → Implement → Validate → Monitor → Detect → Investigate → Respond**

The early work sits on the left: deciding what should exist, building it, and proving it behaves as intended. The later work moves to the right: watching the environment, noticing when something looks wrong, and dealing with it. By the time Via Wash reaches incident response, the alerts I investigate will come from an environment I designed and built myself, so every finding can be traced back to a decision made earlier.

{% include quote.html text="By the time Via Wash reaches incident response, the alerts I investigate will come from an environment I designed and built myself." %}

## Where it starts

Before anything can be built, there has to be somewhere to build it. [Preparing the Microsoft environment]({{ '/identity-before-detection/preparing-the-environment/' | relative_url }}) gets the tenant and the E5 licence in place, then checks that each service the licence includes is actually ready, because a licence makes a service available but doesn’t make it ready. So far I have documented the E5 licence and the Intune groundwork.

## Identity comes first

Every later decision refers back to a person. Which department are they in? What should they reach? Should this account have admin rights at all? That is why the thinking starts with [Designing identity and access]({{ '/identity-before-detection/designing-identity-and-access/' | relative_url }}) and [Identity lifecycle]({{ '/identity-before-detection/identity-lifecycle/' | relative_url }}): who should have access to what, and how that access changes when people join, move and leave. The build in [Entra ID]({{ '/identity-before-detection/' | relative_url }}#roadmap-entra-id) follows from those decisions.

## Then everything that rests on identity

Once Via Wash’s people and their access exist, the rest can be built on top:

- **Devices**, because knowing the person isn’t enough: the device they use must be trustworthy too. See [Intune and device management]({{ '/identity-before-detection/' | relative_url }}#roadmap-intune), [Windows configuration]({{ '/identity-before-detection/' | relative_url }}#roadmap-windows) and [Defender and endpoint security]({{ '/identity-before-detection/' | relative_url }}#roadmap-defender).
- **On-premises IT**, because many companies still run their own servers alongside the cloud. See [On-premises Active Directory]({{ '/identity-before-detection/' | relative_url }}#roadmap-on-premises) and [Hybrid identity]({{ '/identity-before-detection/' | relative_url }}#roadmap-hybrid).
- **A new starter, end to end**, the test of everything before it: if groups and policies are designed well, almost everything should happen automatically. See [the roadmap]({{ '/identity-before-detection/' | relative_url }}#roadmap-onboarding).
- **Watching and responding**, once the environment produces meaningful activity. See [Monitoring and detection]({{ '/identity-before-detection/' | relative_url }}#roadmap-monitoring) and [Incident response]({{ '/identity-before-detection/' | relative_url }}#roadmap-incident-response).

Two areas run alongside the rest: [IT Support & Operations]({{ '/identity-before-detection/' | relative_url }}#roadmap-it-support), a distinct workstream within IT, and [Application security]({{ '/identity-before-detection/application-security/' | relative_url }}) for the Via Wash customer app.

These future areas are a direction, not a fixed structure. Each gets its own pages only once I have done the work, and the grouping may change as the project and my learning progress.

## Honest limits of the lab

Some constraints shape the order and scope of the work. I’d rather record them here than hide them:

- **The E5 trial is time-limited.** It ends on 16 November 2026, so work that depends on E5 services has to fit inside it or wait for a licensing decision.
- **Microsoft Sentinel is separate.** It runs on an Azure subscription and is billed by usage, so it isn’t switched on by the E5 trial. Monitoring may start with tools the licence already includes.
- **Device testing needs a suitable machine.** My own computer runs Windows 11 Home, version 26H2, which isn’t a business edition. Checking its suitability is the next Intune step, and device tests are likely to use a Windows virtual machine.
- **The lab is limited by hardware.** Running a domain controller and a client side by side needs memory and storage, so the on-premises work will be scoped to what the lab can realistically support.
