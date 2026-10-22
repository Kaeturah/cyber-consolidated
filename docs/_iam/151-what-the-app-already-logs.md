---
title: What the app already logs
kind: page
topic: application-security
order: 151
status: Needs validation
summary: The blank IP address I found in the app’s login logs, how I fixed it, and the failed-login detection it led to.
updated: 2026-10-18
permalink: /identity-before-detection/application-security/what-the-app-already-logs/
headline: The blind spot in the app’s own login logs
---

## How this started

While building sign-up and login for the Via Wash app, I created a few test accounts and then read the resulting authentication logs the way an analyst would: who signed in, when, and from where. Supabase, the backend the app uses, keeps its own Auth Audit Logs, so that was where I looked first.

## What I found

The `ip_address` field was empty on every authentication event. It wasn’t one bad row. It was blank every time.

That matters more than it sounds. Any rule like “flag a login from somewhere unusual” depends on knowing where the login came from. Built on those logs, it would have been blind from the start.

The cause was the way the app handles sign-in. Authentication runs inside Next.js Server Actions, which execute on the app’s own server. So Supabase sees the request arriving from the app’s server, not from the customer’s browser, and has no real visitor address to record.

## What I changed

I made two changes, both on 12 September 2026:

- **Forwarding the real address.** The app now passes the incoming `x-forwarded-for` header to Supabase on its server-side calls. Behind a real host in production, that header carries the customer’s address. On a local development machine nothing sets it, so it does nothing there, and that is expected.
- **Keeping its own log.** Rather than rely on another service’s logs alone, the app now writes its own `auth_events` table. A `logAuthEvent()` function records sign-up, successful login, failed login and logout, with the address and browser details taken straight from the request.

## What I tested

After the change, I signed in and out and checked the new table. The `login_success` and `logout` rows recorded `::1`, the IPv6 loopback address, which is correct for a test run on the same machine, along with the real browser details. Both rows belonged to the same user, a consistent actor rather than an anomaly.

## Turning the log into a detection

With trustworthy events in place, I added a `suspicious_login_activity` view. It flags any email address with three or more failed logins within ten minutes, the same shape as a SIEM detection rule: group the events, count them over a time window, and alert past a threshold. I triggered it with three deliberate wrong passwords on a test account, and the view returned exactly one flagged row.

## The rest of what exists

The app also has row-level security enabled on seven tables, which keeps each customer’s data scoped to that customer at the database level, and a trigger that creates a customer profile automatically on sign-up.

{% include callout.html tone="warn" title="Built and tested once, but not yet reviewed" text="These results come from my own development tests. They don’t yet show that the controls are secure. Several areas need a careful review: who can read the detection view, who can insert events into the log, whether the forwarded IP header can be trusted, what happens if logging silently fails, and whether a ten-minute window is the right design." %}

## Evidence

The work is recorded in the app’s code and commit history, and in a case-study write-up from 13 September 2026. Screenshots from that write-up need redacting before they appear here, because they show a test account’s email address and user ID.

## What comes next

1. Review the code and the current database policy definitions.
2. Set up safe tests in a non-production or isolated environment. Nothing will be tested against the live database without explicit approval.
3. Record the actual outcomes, fix any confirmed issues, and retest.

Test email addresses, user IDs, secrets and database credentials will never be published here.
