---
title: Welcome to Via Wash
headline: "A real business, with its IT still to build."
short: Welcome
order: 1
part: Introduction
part_intro: Who Via Wash is, what is being built, and the business all of it has to serve.
status: Documented
summary: Meet the business behind the project, and why its IT is being built carefully, in stages, before anything goes live.
updated: 2026-10-18
permalink: /via-wash/welcome/
---

## Meet Via Wash

Via Wash collects people’s laundry and dry cleaning, cleans it, and brings it back. It is starting in London, with the aim of growing across more areas as it finds its feet.

Customers deal with Via Wash through an app. They sign up, save their pickup and delivery addresses, choose the services they need and place an order. That app has been in development since September 2026, well before this documentation project began. Via Wash isn’t a company invented for a lab exercise. It is a business that genuinely needs the IT described in this series.

{% include quote.html text="Via Wash isn’t a company invented for a lab exercise. It is a business that genuinely needs the IT described in this series." %}

## A business is more than its app

The customer app is the part people see. Behind it sits everything that keeps the company running:

- people across six departments who need accounts, and only the access their job requires
- laptops and phones that need setting up, keeping up to date and protecting
- business email that customers and suppliers can trust
- records that show who did what, so problems can be spotted and investigated
- someone people can turn to when a password, a device or a system stops working

That is the IT environment this series builds and documents, step by step.

## Why build it in stages

It is tempting to switch on every security feature at once. The result is usually a tangle of settings that nobody fully understands.

Via Wash will grow in layers instead, each one resting on the one before. Identities come first, because devices, data and alerts all make sense only once you know who the people are and what they should be able to reach. Devices come next, then the protection around them, then the visibility to notice when something is wrong, and finally the practice of responding when it is.

[What are we building?]({{ '/via-wash/what-are-we-building/' | relative_url }}) walks through those stages and how they depend on each other.

## A test environment first

Nothing in this series is a live production system yet. The IT environment is being designed and tested in a Microsoft test environment, so mistakes are cheap and every decision can be checked before real staff or customers depend on it.

That brings one rule with it. A page only says something is done when there is evidence for it. Each chapter carries a status, and each screenshot is genuine and redacted before it is published:

| Status | What it means |
|---|---|
| Documented | The available evidence supports the statement. |
| In progress | Work has started but isn’t finished. |
| Needs validation | Something exists but needs another check or test. |
| Planned | Future work. No implementation is claimed. |

## Where to go next

Read the chapters in order to follow the build, or start with the [project overview]({{ '/via-wash/' | relative_url }}) to see every chapter at once.
