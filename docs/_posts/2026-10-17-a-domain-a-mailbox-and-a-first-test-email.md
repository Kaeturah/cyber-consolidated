---
title: A domain, a mailbox and a first test email
summary: cyber-consolidated.com now has business email. Outbound delivery works; DKIM turned out to need a closer look.
project: via-wash
tags: [Foundation, Email, DNS]
related: /via-wash/foundation/domain-and-business-email/
related_title: Domain and business email
---

The domain was already serving this site from GitHub Pages. Today it got an email identity too.

The domain purchase didn’t include email hosting, so I compared a few providers and chose Namecheap Private Email. Activating it meant adding the provider’s MX and SPF records at NameSilo, where the domain’s DNS lives, then creating the `franklin@` mailbox.

The first test message sent from it arrived in my personal inbox, and a later one sent from the Private Email platform landed in the inbox with the business name, not in spam.

Going back over the DNS later showed one thing still wrong: the DKIM record had been entered without the underscore in its name, so receiving servers won’t find it. Mail can still be delivered on SPF alone, which is why the tests passed. Fixing DKIM, then adding DMARC, is next on the list.
