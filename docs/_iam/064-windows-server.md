---
title: Windows Server
kind: page
topic: building-the-lab
order: 64
status: Planned
summary: The server that will run Via Wash’s on-premises Active Directory.
updated: 2026-10-20
permalink: /identity-before-detection/building-the-lab/windows-server/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Building a Windows Server virtual machine, ready to become a domain controller in the hybrid identity topic.

## Why it matters for Via Wash

On-premises Active Directory needs a server. Building it here keeps the lab work in one place.

## What will be done

- Create the server virtual machine using an evaluation licence
- Give it a fixed IP address and a sensible name
- Take a snapshot before installing any roles

## How it will be checked

- The server is reachable from the client on the lab network
