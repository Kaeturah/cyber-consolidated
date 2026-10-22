---
title: Company profile
kind: page
topic: start-here
order: 13
status: In progress
summary: The departments, functions and locations that shape every access, device and security decision Via Wash makes.
updated: 2026-10-18
permalink: /identity-before-detection/start-here/company-profile/
headline: Six departments, and what each needs from IT.
status_note: Departments are defined. Named test identities will be created during the Entra ID build.
---

## Why the organisation comes first

Before I can decide who gets access to what, I need to know who Via Wash actually is: which departments it has, what each one does, and what each one handles that would hurt the business if the wrong person reached it. Every group, policy and permission later in the project traces back to this page.

## Six departments

Via Wash is organised into six business departments. I use these names everywhere, in the identity design, the documentation and this site, so a group or policy can always be traced back to a real part of the business.

| Department | What it does | What it will need from IT |
|---|---|---|
| Management | Runs the business and makes the decisions that affect all of it. | Broad visibility, but not administrative control of IT systems. |
| Finance | Handles payments, invoicing, payroll and financial records. | Access to financial data, kept separate from everyone else. |
| HR | Recruits, onboards and supports staff, and holds employee records. | Access to personal data, and a trigger for joiner, mover and leaver changes. |
| Operations | Runs day-to-day service: processing orders and running the branches. | Reliable shared devices and access to order systems, with no access to finance or HR data. |
| Delivery Team | Collects and returns customers’ orders. | Mobile access to collection and delivery details while on the move. |
| IT | Runs, secures and supports the technology for everyone else. | Administrative access, kept to the minimum each task needs. |

The right-hand column is the working design, not configuration. It is what I will turn into real groups, access rules and tests during the identity work, and this page will link to them as they exist.

The table already shows why one-size-fits-all access won’t work. Finance and HR both hold sensitive data, but different sensitive data, and neither should see the other’s. Operations needs order systems but nothing from either of them. That separation is the starting point for the identity design.

## Branches are places, not departments

As Via Wash grows it will operate from branches. A branch is a location, not a department: Operations staff at a branch still belong to Operations. Location still matters, for example for devices and for what a normal sign-in looks like, so I record it as an attribute of the person rather than inventing a seventh department.

## Functions inside IT

Security and cloud administration aren’t separate departments at Via Wash. They are functions within IT:

- IT Support
- Identity and Access Management
- Cloud and Microsoft 365 Administration
- Endpoint Management
- Endpoint and Email Security
- Hybrid Identity and On-Premises Infrastructure
- Security Monitoring and Incident Response
- Application Security

Splitting IT into functions matters for access. Admin roles can then be given one function at a time, so working in IT doesn’t automatically mean holding every permission. Someone doing IT Support, for example, shouldn’t need the rights to change security policies.

## Customers are a different kind of identity

Customers sign in to the Via Wash app, not to the company’s Microsoft environment. Their accounts are handled by the app’s own authentication and kept apart from staff identities. Staff and customers bring different risks and need different rules, so keeping them separate is a deliberate design decision rather than an accident of two systems.

## People we will follow

{% include callout.html title="Still to come" text="Named test identities for each department will be created during the identity work. They will be listed here once they exist in the test environment, along with the roles and access each one is meant to have." %}
