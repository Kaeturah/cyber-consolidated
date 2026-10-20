---
title: Writing detections
kind: page
topic: monitoring-and-detection
order: 122
status: Planned
summary: Turning “this looks suspicious” into a query that finds it.
updated: 2026-10-20
permalink: /identity-before-detection/monitoring-and-detection/writing-detections/
---

{% include callout.html title="Not started yet" text="This step hasn’t been done yet. The page explains what it involves so you can follow along, and it will be rewritten with the real configuration and screenshots once the work happens." %}

## What this step is

Writing detection queries in KQL, the query language used across Microsoft’s security tools.

## Why it matters for Via Wash

A detection is a precise description of suspicious behaviour. Writing them builds the core skill of a SOC analyst.

## What will be done

- Start with a clear case, such as repeated failed sign-ins
- Write and refine the query
- Turn it into an alert rule

## How it will be checked

- The query returns the expected results on known test data

## Key terms

- **KQL (Kusto Query Language)**: the query language used in Microsoft Sentinel and Defender advanced hunting
