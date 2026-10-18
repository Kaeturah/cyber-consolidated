---
title: What are we building?
headline: "Six stages, each one standing on the last."
short: The plan
order: 2
part: Introduction
status: Documented
status_note: This chapter describes the plan; each stage has its own status.
summary: The six build stages, what each one depends on, what it makes possible next, and the practical limits of the lab.
updated: 2026-10-18
permalink: /via-wash/what-are-we-building/
---

## The shape of the journey

The work follows one progression, and every stage passes through some part of it:

**Design → Implement → Validate → Monitor → Detect → Investigate → Respond**

Early stages spend most of their time on the first three steps: deciding what should exist, building it, and proving it behaves as intended. Later stages move to the right: watching the environment, recognising when something looks wrong, and dealing with it. By the time Via Wash reaches incident response, the alerts being investigated come from an environment that was designed and built here, step by step.

{% include quote.html text="By the time Via Wash reaches incident response, the alerts being investigated come from an environment that was designed and built here." %}

## Before stage 1: the foundation

Before anything can be built, there has to be somewhere to build it and a way to communicate. The foundation covers three things:

- a [Microsoft 365 E5 trial]({{ '/via-wash/foundation/microsoft-365-e5-trial/' | relative_url }}) that provides the test environment
- a [first look at Microsoft Intune]({{ '/via-wash/foundation/microsoft-intune/' | relative_url }}), to record its starting state
- a [domain and business email]({{ '/via-wash/foundation/domain-and-business-email/' | relative_url }}), so the project has a professional identity on the web and in email

## The six stages

### 1. Identity and access

**Why first:** every later decision refers back to a person. Which department are they in? What should they reach? Should this account have admin rights at all?

**Builds:** users and groups for Via Wash’s six departments in Microsoft Entra ID, least-privilege roles, sign-in protection, and the joiner, mover and leaver process.

**Makes possible:** device ownership, access policies, and a baseline of normal sign-in behaviour to compare against later.

### 2. Endpoint and device management

**Why next:** knowing the person isn’t enough. The device they use also has to be one the business can trust.

**Builds:** device enrolment with Microsoft Intune, configuration and compliance policies, and app deployment.

**Makes possible:** checking that a device meets the rules before it reaches company data, and protecting it in stage 3.

### 3. Endpoint and email security

**Why here:** once devices are managed, they can be protected and watched. Email is the other common way attacks arrive.

**Builds:** endpoint protection and email protection using the Microsoft Defender capabilities available in the licence, tested with safe, controlled scenarios.

**Makes possible:** real security signals, such as alerts, device risk and suspicious messages, for monitoring to pick up.

### 4. Hybrid identity and on-premises infrastructure

**Why it matters:** many organisations still run traditional servers alongside the cloud. Understanding how the two meet is part of understanding real environments.

**Builds:** a small test Active Directory domain on Windows Server and, if it proves feasible in the lab, synchronisation of identities to the cloud.

**Makes possible:** realistic scenarios that span both worlds for detection and investigation to work through.

### 5. Monitoring and detection

**Why now:** by this point the environment produces meaningful activity: sign-ins, device events, alerts.

**Builds:** chosen log sources, queries and detection rules, along with the tests that prove each detection fires when it should.

**Makes possible:** spotting suspicious behaviour quickly enough to act on it.

### 6. Security operations and incident response

**Why last:** this stage brings everything together. Investigating an incident properly means knowing the users, devices, access and controls involved, and every earlier stage provides one of those pieces.

**Builds:** triage, investigation, containment and recovery workflows, practised on safe simulated incidents and written up as runbooks and lessons learned.

## Across the whole business

Two workstreams run alongside the stages rather than after them:

- **IT support and operations.** Requests, account and device support, approvals, escalation and change records. Technology only works if people can be supported in using it.
- **Application security.** The Via Wash customer app has its own users, logs and risks, and it already has security work that needs reviewing and validating.

## Honest limits of the lab

Some constraints shape the order and scope of the work, and they are recorded here rather than hidden:

- **The E5 trial is time-limited.** Stages that depend on E5 services have to fit inside the trial or wait for a licensing decision.
- **Microsoft Sentinel is separate.** It runs on an Azure subscription and is billed by usage, so it isn’t simply switched on by the E5 trial. Monitoring may start with tools the licence already includes.
- **Device testing needs a suitable virtual machine.** The host computer runs Windows 11 Home, which can’t be enrolled the way a business device would be, so tests will use a Windows virtual machine.
- **The hybrid lab is limited by hardware.** Running a domain controller and a client side by side needs memory and storage, so stage 4 will be scoped to what the lab can realistically support.
