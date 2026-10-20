---
title: Building the lab
headline: A small network on one computer
kind: topic
topic: building-the-lab
order: 60
status: Planned
summary: "Virtual machines and networking for the device and on-premises work: a Windows 11 test client, a Windows Server, and a network to join them."
updated: 2026-10-20
permalink: /identity-before-detection/building-the-lab/
short: Lab
---

{% include callout.html title="Not started yet" text="This topic sets out the lab plan. Each step will be written as the lab is built." %}

## Why a lab is needed

Some of this project can be done entirely in the cloud. But managing devices and running on-premises Active Directory need real machines. A lab of virtual machines gives Via Wash test computers and servers without buying hardware, and without risking a real computer.

## The constraints

- **The host computer runs Windows 11 Home.** Home edition doesn’t include Hyper-V, Microsoft’s built-in virtualisation, so the lab will use a separate hypervisor.
- **A test device must be an edition that can be enrolled.** Windows 11 Home can’t join Entra ID like a business device can, so the test client needs Windows 11 Pro or Enterprise.
- **Memory and storage are limited.** A domain controller and a client running side by side need enough of both, which may limit what runs at once.

## What the lab is for

The Windows 11 client supports [Managing devices with Intune]({{ '/identity-before-detection/managing-devices/' | relative_url }}) and [Protecting devices and email]({{ '/identity-before-detection/protecting-devices-and-email/' | relative_url }}). The Windows Server supports [On-premises IT]({{ '/identity-before-detection/on-premises-it/' | relative_url }}) and [Hybrid identity]({{ '/identity-before-detection/hybrid-identity/' | relative_url }}).
