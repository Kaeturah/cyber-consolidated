---
title: Meet Via Wash
kind: page
topic: start-here
order: 11
status: Documented
summary: Meet the business behind the project, and why its IT is being built carefully, in stages, before anything goes live.
updated: 2026-10-18
permalink: /identity-before-detection/start-here/meet-via-wash/
headline: A real business, with its IT still to build.
---

## The business behind the project

Via Wash collects people’s laundry and dry cleaning, cleans it, and brings it back. It is starting in London, with the aim of growing into more areas as it finds its feet.

Customers deal with Via Wash through an app. They sign up, save their pickup and delivery addresses, choose the services they need and place an order. I started building that app in September 2026, before this documentation project began, so Via Wash wasn’t invented for a lab exercise. It is a business that genuinely needs the IT this project builds.

{% include quote.html text="Via Wash isn’t a company invented for a lab exercise. It is a business that genuinely needs the IT this project builds." %}

## A business is more than its app

The app is the part customers see. Behind it, the company itself has to run, and that raises questions the app can’t answer:

- **Who works here, and what should they reach?** Six departments, each needing an account and only the access their job requires. Someone in Delivery has no reason to open payroll.
- **Which devices can be trusted?** Laptops and phones need setting up, keeping up to date and protecting.
- **Can people trust our email?** Customers and suppliers need to know a message really came from the business.
- **What happened, and when?** Records of who did what, so problems can be spotted and investigated.
- **Who helps when something breaks?** Someone staff can turn to when a password, a device or a system stops working.

Answering those questions is the IT environment this project builds, one decision at a time.

## Why I’m building it in stages

It is tempting to switch on every security feature at once. The usual result is a tangle of settings nobody fully understands, including the person who set them up.

So Via Wash grows in layers, each resting on the one before. Identity comes first, because devices, data and alerts only make sense once you know who the people are and what they should reach. Devices come next, then the protection around them, then the visibility to notice when something is wrong, and finally the practice of responding when it is.

## A test environment first

Nothing in this project is a live production system yet. I’m designing and testing Via Wash’s IT in a Microsoft test environment, where mistakes are cheap and every decision can be checked before real staff or customers depend on it.

That comes with one rule I hold myself to: a page only says something is done when there is evidence for it, and every screenshot is genuine and redacted before it is published.

## Where to go next

[What are we building?]({{ '/identity-before-detection/start-here/what-are-we-building/' | relative_url }}) sets out the plan, and why the work happens in the order it does.
