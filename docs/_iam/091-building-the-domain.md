---
title: Building the domain
kind: page
topic: on-premises-it
order: 91
status: Planned
summary: Turning the lab server into Via Wash’s domain controller, with DNS.
updated: 2026-10-20
permalink: /identity-before-detection/on-premises-it/building-the-domain/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Installing Active Directory Domain Services on the lab server, creating the Via Wash domain, and setting up the DNS that domain-joined machines rely on.

## Why it matters for Via Wash

The domain is the centre of on-premises IT. Every account, computer and policy in this topic lives inside it.

## What will be done

- Install the AD DS role and promote the server to a domain controller
- Choose and record the domain name
- Check DNS is working for the domain

## How it will be checked

- The domain controller is running and answering DNS queries

## Key terms

- **Active Directory Domain Services (AD DS)**: the on-premises directory of users, computers and groups
- **Domain controller**: the server that runs AD DS and checks sign-ins
