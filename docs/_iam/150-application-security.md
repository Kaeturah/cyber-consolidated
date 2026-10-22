---
title: Application security
headline: The customer app has its own security story
kind: topic
topic: application-security
order: 150
status: In progress
summary: The security work already built into the Via Wash customer app, and the review it needs before anything is claimed.
updated: 2026-10-20
permalink: /identity-before-detection/application-security/
short: App security
---

## Why the app has its own topic

The Via Wash customer app was in development before the rest of this project began. It has its own users, its own data and its own logs, separate from the company’s Microsoft environment. Customers sign in to the app, not to the workforce directory, and that separation is deliberate.

The app is also where some of my earliest security work happened. While testing customer sign-in, I found that the login logs I was relying on had a blind spot, fixed it, and built a first detection on top. [What the app already logs]({{ '/identity-before-detection/application-security/what-the-app-already-logs/' | relative_url }}) tells that story. A safe review of it is still to do before any of it can be called secure, and is listed on the [roadmap]({{ '/identity-before-detection/' | relative_url }}#roadmap-app-security).

## How it connects to the rest of the project

- **Identity:** staff and customers are different kinds of identity with different rules. This app is where the customer side lives.
- **Monitoring and detection:** the app’s own security log is a data source in its own right, and its failed-login view has the same shape as the detections planned for the Microsoft environment.
- **Incident response:** a burst of failed customer logins is a realistic scenario to investigate.
