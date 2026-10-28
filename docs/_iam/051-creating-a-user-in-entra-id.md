---
title: Creating a user in Entra ID
headline: An account is more than a name and password
kind: page
topic: building-identity-in-entra-id
order: 51
status: Documented
summary: A Microsoft Learn exercise walked through the user-creation form, its profile fields and assignments, then confirmed that the new practice account appeared in the directory.
updated: 2026-10-28
permalink: /identity-before-detection/building-identity-in-entra-id/creating-a-user/
---

## Why this step matters

Every later identity decision starts with a user account. Entra needs a sign-in identifier, a display name, and enough profile information to distinguish the person and describe their place in the organisation. The account can also be assigned to groups, administrative roles or an administrative unit during creation.

For Via Wash, that information will eventually help IT give a new employee the right access and prepare the right device. The account fields alone do not grant department access: that only happens when a group or another access mechanism is configured to use them.

## What the form taught

- **User principal name (UPN):** the account's sign-in identifier. It commonly looks like an email address, but it is not automatically a working mailbox address. It must be unique in the directory.
- **Display name:** the readable name shown in Microsoft interfaces and applications.
- **Mail nickname:** a mail-related alias value. The form can derive it from the UPN, or the administrator can enter a distinct value.
- **Properties:** profile details such as a person's name, user type, job title, department and usage location. These make the directory understandable and can support later processes.
- **Assignments:** the administrator can add the user to existing groups or assign supported roles and administrative units. Those assignments determine access or administrative scope; merely filling in a department field does not.
- **User type:** a workforce employee is normally represented as a Member. Guest is generally used for an external identity invited to collaborate; the organisation's identity policy determines how contractors are represented.

The notes for this exercise identify **User Administrator** as the role needed to create a user. Use a role with sufficient permissions for the task, and avoid using a broad administrator role when a narrower one is enough.

## The practice exercise

The screenshots follow the Entra **Create new user** workflow through Basics, Properties, Assignments and Review + create. The Assignments page showed no assignments. The final capture then showed one user in the directory's user list.

This was a learning exercise in a separate practice directory. It is useful evidence of the form and the result of that exercise, but it is not a Via Wash account or a test of Via Wash access.

## What the evidence establishes

The final user-list capture supports that the account was created and appeared in the directory. The earlier captures show which fields were reviewed and that no groups or roles were assigned during this exercise.

It does not show that the account successfully signed in, received application access, or was governed by a joiner process. It also does not establish that the same configuration exists in the Via Wash test environment.

{% include evidence.html title="Basics tab in the Entra user-creation form" where="Microsoft Entra admin centre · Create new user · Basics" shows="The account identifier and initial account settings are entered in the first step." proves="The form was reached and the Basics step was reviewed; it does not establish a successful sign-in." %}

{% include evidence.html title="User profile properties" where="Microsoft Entra admin centre · Create new user · Properties" shows="The form's identity and job-information fields, including department and job title." proves="These are profile fields. They do not grant group membership or access by themselves." %}

{% include evidence.html title="Assignments before creation" where="Microsoft Entra admin centre · Create new user · Assignments" shows="No group, role or administrative-unit assignments were listed for this exercise." proves="The account was not assigned those items through this screen; it does not prove anything about access granted elsewhere." %}

{% include evidence.html title="Reviewing the new account before creation" where="Microsoft Entra admin centre · Create new user · Review + create" shows="The account details gathered across the earlier steps are reviewed before submission." proves="The review screen was reached; the following user-list capture is the evidence that creation completed." %}

{% include evidence.html title="The user appears in the directory" where="Microsoft Entra admin centre · Users · All users" shows="One user is listed after the creation workflow." proves="The account object appeared in the directory at capture time; it does not prove sign-in or access tests." %}

## Knowledge review

We reviewed the lesson together after looking at the screenshots. The main points were:

- The UPN identifies the sign-in account; the display name is the human-readable label.
- Department and job title belong in the user's properties, but those attributes need a configured rule or process before they affect group membership or access.
- The Assignments step can add a user to an existing group or assign a role. No assignments were present in this exercise.
- An internal Via Wash employee would normally be a Member. Guest is generally for an external collaborator, subject to the organisation's policy.
- The specific least-privilege administrative role in the notes is User Administrator.

This was a guided review of the concepts, not a recorded Microsoft Learn assessment result. The saved learning note does not identify the module name or confirm the official knowledge-check completion, so those details remain to be checked in Microsoft Learn.

## What comes next

This page records the user-creation lesson before moving on. The next connected work will be group design and creation: first deciding how Via Wash's departments and job responsibilities should be represented, then building and testing those groups in the Via Wash environment.

