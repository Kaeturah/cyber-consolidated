---
title: Creating a user in Entra ID
headline: Sarah’s first day at Stratford
kind: page
topic: building-identity-in-entra-id
order: 51
status: Needs validation
summary: I created a Via Wash test user and followed the details from the HR scenario into Entra. The record is there; the onboarding process still needs work.
updated: 2026-10-29
permalink: /identity-before-detection/building-identity-in-entra-id/creating-a-user/
---

## The HR request

When a new person joins Via Wash, HR needs to tell IT who they are, what job they are doing and where they will work. IT turns that request into an account, then makes sure the account receives only the access and tools needed for that job.

I used **Sarah Eze** as a test identity for that scenario and created her account in the Via Wash test tenant. Sarah is a test user, not a production employee. The screenshots below follow the account through the actual Entra creation flow.

## The account I created

On the **Basics** page, I entered `sarah.eze` as the sign-in name and **Sarah Eze** as the display name. The tenant part of the UPN is redacted in the screenshot. The display name is what colleagues will see; the UPN is what Sarah will use to sign in. An email-shaped sign-in name does not prove that a mailbox exists. I left the mail nickname derived from the UPN, kept the account enabled and selected Entra’s auto-generated password option. The password itself is masked and is not recorded here.

{% include evidence.html title="Basics · Sarah’s sign-in and display names" where="Via Wash test tenant · Create new user · Basics" image="/assets/evidence/vw-entra-001-create-user-basics-2026-10-29.png" alt="Create new user Basics tab for test identity Sarah Eze. The UPN tenant domain is redacted and the generated password is masked." shows="The UPN begins sarah.eze, the display name is Sarah Eze, the password is auto-generated and the account is enabled." proves="The Basics details entered for this test user; it does not prove that Sarah signed in or that a mailbox exists." %}

On **Properties**, I set Sarah’s user type to **Member**, because she represents an internal Via Wash employee. Her job title is **Store Assistant**, the company name is **Via Wash**, the employee type is **Employee**, and the test employee ID is `VW-EMP-001`. I left the hire date and manager blank rather than making up HR details.

The branch is recorded as **London - Stratford Branch** under **Office location**. It is a place where Operations work happens, not another department. There is one value I need to fix: I entered **Store Operations** in the Department field, but the agreed business department is **Operations**. I have not changed the Entra account, so the screenshot records what was actually saved. I need to correct that value before using Sarah to test department-based group membership.

{% include evidence.html title="Properties · the employee record" where="Via Wash test tenant · Create new user · Properties" image="/assets/evidence/vw-entra-002-create-user-properties-2026-10-29.png" alt="Properties tab showing Sarah Eze as a Member and Employee, Store Assistant at Via Wash, department Store Operations, employee ID VW-EMP-001, and London - Stratford Branch as office location." shows="The workforce attributes entered for the test identity. The hire date and manager are blank." proves="These values were entered in the user profile; the department value needs to be corrected to Operations before group-rule testing." %}

## What happened to access?

The **Assignments** tab lets IT add a new account to existing groups or assign directory roles and administrative units. Sarah had none selected. That was the right result for this first pass: we have not designed and created the Via Wash groups yet, so there was no approved Operations group to assign.

The outcome also shows why filling in a department is not enough. Later, a membership rule or onboarding workflow can connect agreed employee attributes to the right groups. Until that rule exists and is tested, Sarah does not automatically receive department access just because her profile says Store Operations—or Operations.

{% include evidence.html title="Assignments · no groups or roles selected" where="Via Wash test tenant · Create new user · Assignments" image="/assets/evidence/vw-entra-003-create-user-assignments-2026-10-29.png" alt="Assignments tab states No assignments to display. Add administrative unit, Add group and Add role are available." shows="No group, directory role or administrative unit was selected during creation." proves="The creation workflow made no assignments on this screen; it does not test group rules or access elsewhere." %}

## Review, create, then check the result

I checked the values on **Review + create** and submitted the account. Entra confirmed that Sarah Eze was created, and the Users list then showed her as a Member. That proves the test account exists in the Via Wash tenant. I have not yet tested a sign-in, application access, group membership, device enrolment or app deployment for Sarah.

{% include evidence.html title="Review + create · the values before submission" where="Via Wash test tenant · Create new user · Review + create" image="/assets/evidence/vw-entra-004-create-user-review-2026-10-29.png" alt="Review + create page summarising Sarah Eze's UPN with the tenant portion redacted, Member account type, job title, company, department, employee ID and Stratford Branch location. No assignments are listed." shows="The final account details and empty assignment sections before selecting Create." proves="The form was ready for submission; the success notification below confirms creation." %}

{% include evidence.html title="Entra confirms that Sarah Eze was created" where="Via Wash test tenant · Create new user · confirmation notification" image="/assets/evidence/vw-entra-005-create-user-success-2026-10-29.png" alt="Microsoft Entra notification: Successfully created user. Successfully created user Sarah Eze." shows="A successful user-creation confirmation." proves="Entra accepted the create request; it does not demonstrate sign-in or access." %}

{% include evidence.html title="Sarah appears in All users" where="Via Wash test tenant · Users · All users" image="/assets/evidence/vw-entra-006-user-list-2026-10-29.png" alt="All users list with Sarah Eze shown as a Member; her UPN and another user's details are redacted." shows="Sarah Eze appears in the tenant’s user list as a Member." proves="The account object is present in the directory at capture time; no sign-in or application-access test is shown." %}

The supplied screenshots have the tenant domain, password and unrelated account details masked. I have kept those redactions intact. Sarah and `VW-EMP-001` are the test identity used for this Via Wash scenario.

## The next onboarding step

The immediate correction is to set Sarah’s Department to **Operations** in Entra and capture that corrected value. Then I can design the department and job groups, decide whether dynamic membership is appropriate, and test what Sarah receives. Only after identity and membership are right can I follow her through the next parts of the first-day scenario: authentication, a managed device, and the applications an Operations Store Assistant needs.

The walkthrough follows Microsoft Learn’s [Create a new user in Microsoft Entra ID](https://learn.microsoft.com/en-us/training/modules/manage-security-controls-identity-access/5-create-new-user) unit in the 51-unit **Manage security controls for identity and access** module. The next related unit is [Secure Microsoft Entra groups](https://learn.microsoft.com/en-us/training/modules/manage-security-controls-identity-access/6-secure-microsoft-entra-groups). I reviewed the user-creation concepts, but the module knowledge-check result is still unrecorded. The wider decisions belong in the [Via Wash identity and access design]({{ '/identity-before-detection/designing-identity-and-access/' | relative_url }}).

