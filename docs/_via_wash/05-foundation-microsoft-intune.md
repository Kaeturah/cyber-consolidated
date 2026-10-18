---
title: Microsoft Intune — initial readiness
headline: "Intune is reachable. Zero devices are enrolled."
short: Intune readiness
order: 5
part: Foundation
status: Documented
status_note: Admin centre access documented. Enrolment and device management not yet demonstrated.
summary: A first look at device management before anything is enrolled or configured, recording exactly where it stands.
updated: 2026-10-18
permalink: /via-wash/foundation/microsoft-intune/
---

## Why Intune is part of Via Wash

Via Wash has staff across Management, Finance, HR, Operations, Delivery Team and IT. A realistic environment needs a way to decide how company devices are brought under management, which settings they must meet, and how they stay protected. In this project, that is Intune’s job.

Knowing who a user is isn’t enough on its own. The next question is whether the device they are using should be trusted, and Intune is where that question starts to be answered.

## What the evidence shows

Screenshots from 18 October 2026 show the Intune admin centre open and reachable. The dashboard showed an active account and a warning about firewall configuration for new Intune network endpoints. Whether that warning applies to this lab hasn’t been assessed.

The device overview showed **zero devices** on every platform listed. The Windows enrolment options page was also visible. That shows where enrolment will be set up, not that any enrolment setting has been chosen.

A licence screenshot showed several Intune-related service plans selected as part of E5.

{% include callout.html title="What this does not prove" text="A selected or available service plan doesn’t mean the capability has been configured, assigned or tested. A dashboard with no errors and no non-compliant devices isn’t evidence that policies work either, because no devices are enrolled for them to apply to." %}

{% include quote.html text="A dashboard with no errors isn’t evidence that policies work when there are no devices for them to apply to." %}

## Current state

| Capability | Status | Notes |
|---|---|---|
| Intune admin centre access | Documented | Dashboard opened and showed an active account. |
| Device enrolment | Not demonstrated | No device has been enrolled. |
| Managed devices | None shown | Zero devices in the captured overview. |
| Compliance policies and configuration profiles | Not yet evidenced | Nothing to validate until a device is enrolled. |
| Endpoint security policies | Not yet evidenced | Covered later under endpoint and email security. |
| Enrolment settings | Needs validation | Options page seen; current settings not yet reviewed. |

## Why this matters to Via Wash

Before any policy can be validated, three things need to be settled: how a device enters management, which user or group it belongs to, and what baseline settings it should meet. The second depends on the identity work. Devices are assigned to users and groups, so Via Wash’s departments need to exist in Entra ID before device management means much.

## Evidence

These are genuine screenshots from the readiness check. They will be added once each one has been inspected and approved for publication.

{% include evidence.html title="Intune admin centre dashboard" shows="The Intune home page with account status Active, service health and the firewall-endpoint warning." proves="The admin centre was reachable on 18 October 2026." redact="Tenant details, if visible." where="Microsoft Intune admin centre · Home" source="Screenshot 2026-10-18 113809.png" %}

{% include evidence.html title="Device overview showing zero devices" shows="Windows, Apple mobile, macOS, Android and Linux, each with 0 devices." proves="The starting point: nothing was enrolled at the time of capture." redact="Nothing sensitive expected; check before use." where="Microsoft Intune admin centre · Devices" source="Screenshot 2026-10-18 113903.png" %}

{% include evidence.html title="Windows enrolment options" shows="The Windows enrolment page listing options such as Automatic Enrollment and Windows Autopilot." proves="Where enrolment will be configured. It doesn’t show any setting being chosen." redact="Nothing sensitive expected; check before use." where="Microsoft Intune admin centre · Enrolment" source="Screenshot 2026-10-18 113932.png" %}

{% include evidence.html title="Intune service plans in the E5 licence" shows="Intune-related service plans selected in the licence details." proves="Only that the plans were selected, not that they are configured or working." redact="The account holder’s name and any account details." where="Microsoft 365 admin centre · Licences and apps" source="Screenshot 2026-10-18 112919.png" %}

## What comes next

1. Review the current enrolment settings and record them as they are.
2. Decide which test account and device scenario to use.
3. Enrol a suitable test device when ready, then record what actually happened.
4. Document compliance, configuration and endpoint-security work only after the settings have been applied and validated.

This work continues in stage 2, [endpoint and device management]({{ '/via-wash/endpoint-and-device-management/' | relative_url }}).
