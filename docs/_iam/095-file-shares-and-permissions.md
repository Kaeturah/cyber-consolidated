---
title: File shares and permissions
kind: page
topic: on-premises-it
order: 95
status: Planned
summary: Department folders that only the right people can open.
updated: 2026-10-20
permalink: /identity-before-detection/on-premises-it/file-shares-and-permissions/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Creating shared folders for each department, with permissions granted to groups rather than individuals.

## Why it matters for Via Wash

Shared drives are where a lot of sensitive business data lives. Getting permissions right, and keeping them group-based, is a common real-world support and security task.

## What will be done

- Create a share for each department
- Grant access to department groups only
- Map the drive automatically with Group Policy

## How it will be checked

- A Finance user can open the Finance folder and not the HR folder

## Key terms

- **NTFS permissions**: the file-system permissions that control who can read or change files
