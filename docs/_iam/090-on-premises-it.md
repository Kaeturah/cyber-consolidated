---
title: On-premises IT
headline: Everyday IT, on servers the business owns
kind: topic
topic: on-premises-it
order: 90
status: Planned
summary: "The day-to-day IT most companies still run on their own servers: Active Directory, Windows 11 joined to a domain, Group Policy, file shares and software deployed by group."
updated: 2026-10-20
permalink: /identity-before-detection/on-premises-it/
short: On-premises
---

{% include callout.html title="Not started yet" text="This topic sets out the on-premises build. Each step will be written as the lab work happens." %}

## Why on-premises still matters

Plenty of companies don’t run everything in the cloud. Their staff sign in to Windows with an Active Directory account, their settings come from Group Policy, their files sit on a shared drive, and their software is pushed out by IT. That everyday IT is what many IT support and system administration roles look after, so Via Wash will run it too, in the lab.

## What this topic builds

{% include flow.html label="On-premises build order" steps="Domain|Users and groups|Windows 11 joins|Group Policy|File shares|Software by group" notes="A domain controller for Via Wash.|Departments as OUs and groups.|The test client joins the domain.|Settings applied centrally.|Department folders with the right permissions.|Apps install because of group membership." %}

## The principle running through it

Access and software follow **groups**, not individuals. Put a new starter in the Finance group, and they get the Finance folder, the Finance settings and the Finance software, without IT touching their machine one item at a time.

## What it depends on

- The Windows Server and Windows 11 machines from [Building the lab]({{ '/identity-before-detection/building-the-lab/' | relative_url }}).
- The groups and naming from [Designing identity and access]({{ '/identity-before-detection/designing-identity-and-access/' | relative_url }}), so on-premises matches the cloud design.

## What it makes possible

[Hybrid identity]({{ '/identity-before-detection/hybrid-identity/' | relative_url }}) connects this domain to Entra ID, and [A new starter’s first day]({{ '/identity-before-detection/a-new-starters-first-day/' | relative_url }}) uses it to show onboarding from start to finish.
