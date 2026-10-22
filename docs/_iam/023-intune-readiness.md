---
title: Microsoft Intune
kind: page
topic: preparing-the-environment
order: 23
status: In progress
summary: "Checking Intune’s starting point, creating a controlled test group, and limiting automatic enrolment to that group. Device enrolment comes next."
updated: 2026-10-21
permalink: /identity-before-detection/preparing-the-environment/intune-readiness/
headline: Building the foundation for device management
---

## Why Via Wash needs it

As Via Wash grows, the company will need a way to manage and protect the computers used by its employees. Someone working in Finance may handle sensitive financial information, while the IT team may need access to administrative tools. Not every employee should have the same access, and devices should not be brought under management without a clear plan.

Microsoft Intune gives administrators a central place to manage devices, apply settings and security policies, and check whether devices meet the requirements that have been set. Before testing those capabilities, I first needed to understand the state of the Intune environment.

## Understanding the starting point

I opened the Microsoft Intune admin centre and reviewed the dashboard and device overview. The dashboard showed that no devices had been enrolled. It also reported no Intune enrolment failures in the previous seven days and no configuration policy errors or conflicts.

{% include evidence.html title="The Intune dashboard provided the initial view of enrolment and configuration status." where="Microsoft Intune admin centre · Dashboard" image="/assets/evidence/vw-intune-001-dashboard-2026-10-20.png" alt="Intune admin centre dashboard: device enrolment OK with no enrolment failures in the last 7 days, device configuration OK with no policies in error or conflict, and Intune enrolled devices showing 0 for Android, iOS/iPadOS, Linux, macOS, Windows and Windows Mobile." %}

This gave me a clear starting point: Intune was accessible, but I had not yet demonstrated device enrolment or management.

## Creating a controlled test group

Rather than enabling automatic enrolment for everyone in the tenant, I created a dedicated Microsoft Entra security group called `VW-Intune-Test-Devices`.

The group gives me a specific target for the Intune test. It means I can control which users are included in the enrolment exercise instead of applying the scope to every user. I set the membership type to **Assigned**, so membership can be managed deliberately, and added my test account to the group.

## Configuring automatic enrolment

Creating the group was only part of the work. Intune also needed to know which users should be included in automatic mobile device management (MDM) enrolment.

When I inspected the Automatic Enrolment settings, the MDM user scope was initially set to **None**. That meant no users were included through this scope. I changed it to **Some** and selected `VW-Intune-Test-Devices`, limiting the intended scope to that group rather than all users.

I left the Windows Information Protection (WIP) user scope set to **None**, because WIP is not part of this enrolment exercise. After saving, Microsoft Intune displayed a confirmation that the settings had been updated successfully.

{% include evidence.html title="I limited the MDM enrolment scope to the dedicated Via Wash test group and confirmed that Intune saved the settings successfully." where="Microsoft Intune admin centre · Automatic Enrolment" image="/assets/evidence/vw-intune-002-automatic-enrolment-scope-2026-10-20.png" alt="Intune Automatic Enrolment settings with MDM user scope set to Some and 1 group selected, WIP user scope set to None, and a confirmation message reading Successfully updated Microsoft Intune." %}

## Where the project stands

The initial Intune assessment, test-group creation, and Automatic Enrolment configuration are complete. The next stage is to check the suitability of a Windows test device and then determine the appropriate way to test enrolment.

My current computer runs Windows 11 Home, version 26H2. I have recorded this as part of the preparation, but I have not yet enrolled the device. I will only describe enrolment as successful after Intune confirms that a suitable test device has enrolled and appears in the admin centre.

{% include evidence.html title="The computer I recorded during preparation runs Windows 11 Home, version 26H2. It has not been enrolled." where="Windows · About Windows" image="/assets/evidence/vw-intune-003-windows-version-2026-10-20.png" alt="About Windows dialog showing Windows 11, version 26H2 (OS Build 26300.9711), Windows 11 Home." %}

{% include callout.html title="Current status" text="Initial configuration complete; device enrolment and policy testing remain outstanding." %}

| Work | Status |
|---|---|
| Intune dashboard and device overview inspected | Done |
| VW-Intune-Test-Devices security group created, test account added | Done |
| Automatic Enrolment MDM user scope set to Some, test group selected | Done |
| Settings saved and confirmed by Intune; WIP scope left at None | Done |
| Device enrolment | Not done yet |
| Configuration policy deployment and validation | Not done yet |
| Compliance policy testing | Not done yet |

The enrolment and policy work is next on the [roadmap]({{ '/identity-before-detection/' | relative_url }}#roadmap-intune).
