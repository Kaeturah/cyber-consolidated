---
title: Monitoring and detection
headline: "Turning a stream of activity into signals."
short: Monitoring
order: 10
stage: 5
part: Build stages
status: Planned
summary: Choosing the logs that matter, writing detections, and proving they fire when they should.
updated: 2026-10-18
permalink: /identity-before-detection/monitoring-and-detection/
---

{% include callout.html title="Not started yet" text="No monitoring or detection is claimed for the Microsoft environment. This chapter will record the log sources, queries and detection tests actually used." %}

## Why this stage matters

By this point the environment produces a steady stream of activity: sign-ins, device events, security alerts. On its own that is just noise. Monitoring turns it into something useful by picking the sources that matter, defining what suspicious looks like, and making sure the right activity stands out.

## What it depends on

- Identities, devices and security services from stages 1 to 4, which generate the activity to monitor.
- The right tools for the budget. Microsoft Sentinel runs on a separate, usage-billed Azure subscription, so the first detections may be built with tools the licence already includes.

## What it will cover

- Available audit and security logs
- Detection use cases, such as repeated failed sign-ins or sign-ins from unusual places
- Query development and validation
- Alert review and investigation notes
- Coverage gaps, licensing and cost limits

## How it will be validated

Each detection will be triggered deliberately with a safe test, such as a burst of failed sign-ins on a test account, and the evidence will show both the activity and the detection catching it.

## What it makes possible

Alerts with enough context to investigate, which is where stage 6 begins.
