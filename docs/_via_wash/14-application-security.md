---
title: Application security
headline: "The app’s first security work, and what still needs checking."
short: Application security
order: 14
part: Across the business
status: Needs validation
status_note: Existing work recorded. Review and safe testing are needed before any of it is presented as secure.
summary: The security work already built into the Via Wash customer app, and the review it needs before anything is claimed.
updated: 2026-10-18
permalink: /via-wash/application-security/
---

## Why the app has its own chapter

The Via Wash customer app was in development before the rest of this project began. It has its own users, its own data and its own logs, separate from the company’s Microsoft environment. Customers sign in to the app, not to the workforce directory, and that separation is deliberate.

The app is also where some of the project’s first security work happened, so it deserves its own place in the story.

## What already exists

The app is built with Next.js and Supabase. Earlier work added the following:

- an `auth_events` table, written to by a `logAuthEvent()` function on sign-up, successful login, failed login and logout
- forwarding of the `x-forwarded-for` header to Supabase, so the requester’s address can be recorded
- a `suspicious_login_activity` view, intended to flag three or more failed logins for one email address within ten minutes
- row-level security enabled on seven tables
- a trigger that creates a customer profile automatically on sign-up

{% include callout.html tone="warn" title="An inventory, not a security claim" text="These items are a starting inventory. They don’t yet show that the controls are secure. Several areas need a careful review first: who can read the detection view, who can insert events into the log, whether the forwarded IP header can be trusted, what happens if logging silently fails, and whether a ten-minute window is the right design." %}

## How it connects to the rest of Via Wash

- **Identity:** customer identity and workforce identity are different problems with different rules. This app is where the customer side lives.
- **Monitoring and detection:** the app’s own security log is a data source in its own right, and the failed-login view is an early detection rule in the same shape as those planned for stage 5.
- **Incident response:** a burst of failed customer logins is a realistic scenario to investigate in stage 6.

## What comes next

1. Review the code and the current database policy definitions.
2. Set up safe tests in a non-production or isolated environment. Nothing will be tested against the live database without explicit approval.
3. Record the actual outcomes, fix any confirmed issues, and retest.

Test email addresses, user IDs, secrets and database credentials will never be published here.
