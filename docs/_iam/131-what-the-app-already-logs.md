---
title: What the app already logs
kind: page
topic: application-security
order: 131
status: Needs validation
summary: The sign-in logging and failed-login detection already built into the app, recorded as an inventory.
updated: 2026-10-18
permalink: /identity-before-detection/application-security/what-the-app-already-logs/
headline: The app’s first security work, and what still needs checking.
---

## What already exists

The app is built with Next.js and Supabase. Earlier work added the following:

- an `auth_events` table, written to by a `logAuthEvent()` function on sign-up, successful login, failed login and logout
- forwarding of the `x-forwarded-for` header to Supabase, so the requester’s address can be recorded
- a `suspicious_login_activity` view, intended to flag three or more failed logins for one email address within ten minutes
- row-level security enabled on seven tables
- a trigger that creates a customer profile automatically on sign-up

{% include callout.html tone="warn" title="An inventory, not a security claim" text="These items are a starting inventory. They don’t yet show that the controls are secure. Several areas need a careful review first: who can read the detection view, who can insert events into the log, whether the forwarded IP header can be trusted, what happens if logging silently fails, and whether a ten-minute window is the right design." %}

## What comes next

1. Review the code and the current database policy definitions.
2. Set up safe tests in a non-production or isolated environment. Nothing will be tested against the live database without explicit approval.
3. Record the actual outcomes, fix any confirmed issues, and retest.

Test email addresses, user IDs, secrets and database credentials will never be published here.
