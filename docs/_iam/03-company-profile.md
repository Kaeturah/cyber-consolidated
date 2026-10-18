---
title: Company profile
headline: "Six departments, and what each needs from IT."
short: Company profile
order: 3
part: Introduction
status: In progress
status_note: Departments are defined. Named test identities will be created in stage 1.
summary: The departments, functions and locations that shape every access, device and security decision Via Wash makes.
updated: 2026-10-18
permalink: /identity-before-detection/company-profile/
---

## Six departments

Via Wash is organised into six business departments. These names are used consistently across the identity design, the documentation and this site.

| Department | What it does | What it will need from IT |
|---|---|---|
| Management | Runs the business and makes the decisions that affect all of it. | Broad visibility, but not administrative control of IT systems. |
| Finance | Handles payments, invoicing, payroll and financial records. | Access to financial data, kept separate from everyone else. |
| HR | Recruits, onboards and supports staff, and holds employee records. | Access to personal data, and a trigger for joiner, mover and leaver changes. |
| Operations | Runs day-to-day service: processing orders and running the branches. | Reliable shared devices and access to order systems, with no access to finance or HR data. |
| Delivery Team | Collects and returns customers’ orders. | Mobile access to collection and delivery details while on the move. |
| IT | Runs, secures and supports the technology for everyone else. | Administrative access, kept to the minimum each task needs. |

The descriptions above are the working design. As the identity work progresses, each one will be turned into real groups, access rules and tests, and this page will link to them.

## Branches are places, not departments

Via Wash will operate from branches as it grows. A branch is a location, not a department. Operations staff at a branch still belong to Operations. The location matters for things like devices and sign-in patterns, and it is recorded as an attribute rather than as a separate department.

## Functions inside IT

Security and cloud administration are not separate departments at Via Wash. They are functions within IT:

- IT Support
- Identity and Access Management
- Cloud and Microsoft 365 Administration
- Endpoint Management
- Endpoint and Email Security
- Hybrid Identity and On-Premises Infrastructure
- Security Monitoring and Incident Response
- Application Security

Keeping these as functions rather than departments matters for access. IT roles can be assigned one function at a time, so nobody in IT holds every permission just because they work in IT.

## Customers are a different kind of identity

Customers sign in to the Via Wash app, not to the company’s Microsoft environment. Their accounts are handled by the app’s own authentication, kept apart from staff identities. Workforce identity and customer identity have different risks and different rules, and keeping them separate is a deliberate design decision.

## People we will follow

{% include callout.html title="Still to come" text="Named test identities for each department will be created in stage 1, identity and access. They will be listed here once they exist in the test environment, along with the roles and access each one is meant to have." %}
