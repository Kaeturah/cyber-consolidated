---
title: Lab networking
kind: page
topic: building-the-lab
order: 63
status: Planned
summary: Connecting the virtual machines to each other and to the internet, safely.
updated: 2026-10-20
permalink: /identity-before-detection/building-the-lab/lab-networking/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Designing the lab network: how the virtual machines reach each other, the internet, and the cloud services they need.

## Why it matters for Via Wash

Devices need internet access to reach Intune and Entra ID, and a domain controller needs the client to find it by name. Getting the network right avoids hours of confusing failures later.

## What will be done

- Choose the network mode, such as NAT or an internal network
- Plan IP addresses and DNS for the domain
- Check internet access from each machine

## How it will be checked

- Machines can reach each other and the internet as planned
