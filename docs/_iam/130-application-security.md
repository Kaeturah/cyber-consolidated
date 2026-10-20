---
title: Application security
headline: The customer app has its own security story
kind: topic
topic: application-security
order: 130
status: In progress
summary: The security work already built into the Via Wash customer app, and the review it needs before anything is claimed.
updated: 2026-10-20
permalink: /identity-before-detection/application-security/
short: App security
---

## Why the app has its own topic

The Via Wash customer app was in development before the rest of this project began. It has its own users, its own data and its own logs, separate from the company’s Microsoft environment. Customers sign in to the app, not to the workforce directory, and that separation is deliberate.

## How it connects to the rest of the project

- **Identity:** customer identity and workforce identity are different problems with different rules. This app is where the customer side lives.
- **Monitoring and detection:** the app’s own security log is a data source in its own right.
- **Incident response:** a burst of failed customer logins is a realistic scenario to investigate.
