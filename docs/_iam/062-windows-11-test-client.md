---
title: The Windows 11 test client
kind: page
topic: building-the-lab
order: 62
status: Planned
summary: A virtual Windows 11 machine that can be enrolled and managed like a real company laptop.
updated: 2026-10-20
permalink: /identity-before-detection/building-the-lab/windows-11-test-client/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Building a Windows 11 virtual machine that will act as a Via Wash company device.

## Why it matters for Via Wash

Device management and endpoint protection can only be tested on a device. This machine stands in for a real staff laptop.

## What will be done

- Create the virtual machine with enough memory and disk
- Install a Windows 11 edition that can join Entra ID, such as an Enterprise evaluation
- Take a snapshot before enrolling, so it can be reset

## How it will be checked

- The machine boots and is ready to enrol
- A clean snapshot exists
