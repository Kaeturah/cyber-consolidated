---
title: The domain and the website
headline: "An address of its own."
short: Domain and website
kind: page
topic: getting-online
order: 11
status: In progress
summary: Registering cyber-consolidated.com and pointing it at a website hosted on GitHub Pages.
updated: 2026-10-18
permalink: /domain-and-email/getting-online/the-domain-and-the-website/
---

## Why a domain first

A portfolio that lives at someone else’s address is easy to forget. I wanted Cyber Consolidated to have a name people can type, link to and trust, and the domain is the foundation for everything else in this project. The same domain carries the website and, in the next step, business email.

## Registering the domain

I registered `cyber-consolidated.com` through NameSilo in October 2026. NameSilo is the registrar, so it is also where the domain’s DNS records live: the public entries that tell the internet where the website and email for the domain can be found. Every later step in this project comes back to that DNS table.

## Hosting the website

I host the site on GitHub Pages, from the Cyber Consolidated repository on GitHub. Pages is free, needs no server to look after, and publishes straight from files kept in version control. Pages builds the site from the `docs` folder on the repository’s `master` branch, so publishing an update is a matter of committing to that folder.

{% include evidence.html title="GitHub Pages building the site from the docs folder" where="GitHub · Pages settings" shows="The repository’s Pages settings: deploy from a branch, using the /docs folder on master." proves="Where the website is built from. It doesn’t show the domain connection on its own." redact="Nothing sensitive expected; check before use." source="Screenshot 2026-10-17 204437.png" %}

## Connecting the two

Two pieces join the domain to the website, and it took both to make it work:

- **DNS records at NameSilo.** Four `A` records point the bare domain at GitHub Pages, and a `www` `CNAME` record points the `www` address at the GitHub account’s Pages host.
- **A `CNAME` file in the repository.** It tells GitHub Pages which custom domain the site answers to. I committed it on 15 October 2026, and I leave it untouched whenever the site changes, because removing it would disconnect the domain.

{% include evidence.html title="DNS records for the website" where="NameSilo · DNS records" shows="The NameSilo DNS table with the GitHub Pages A records and the www CNAME, before any email records were added." proves="The website records were in place at the registrar." redact="Nothing sensitive expected; check before use." source="Screenshot 2026-10-17 014701.png" %}

## What it established

`cyber-consolidated.com` now serves this site. The DNS table above is also the starting point for the next step: before any email records were added, the domain only knew about the website.

## What comes next

The domain purchase didn’t include email hosting. The [next step]({{ '/domain-and-email/getting-online/business-email/' | relative_url }}) covers choosing a provider and setting up the business mailbox.
