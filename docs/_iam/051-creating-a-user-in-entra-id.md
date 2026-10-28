---
title: Creating a user in Entra ID
headline: The first step in getting a new colleague ready
kind: page
topic: building-identity-in-entra-id
order: 51
status: Documented
summary: What the practice user-creation exercise taught me about representing a Via Wash employee—and what still has to happen before that person can work.
updated: 2026-10-28
permalink: /identity-before-detection/building-identity-in-entra-id/creating-a-user/
---

## The day-one problem

An employee is joining Via Wash’s **Operations** department. HR knows who is starting and when; IT has to turn that information into a usable, appropriately limited work account. The employee will eventually need to sign in, use the applications their role requires, and work from a prepared device.

That sounds like one onboarding task, but it is a chain. First the identity must describe the right person. Then access needs to be tied to the person’s job, the device needs to be prepared, and the result needs to be checked from the employee’s point of view. This page records only the first learning step in that chain: understanding the new-user workflow. It does not say that Via Wash onboarding has been built.

## The exercise and the decisions I noticed

I followed Microsoft Learn’s **Create a new user in Microsoft Entra ID** unit in a separate practice directory. In the admin centre, the route was **Identity → Users → All users → New user → Create new user**. The wizard moved through **Basics → Properties → Assignments → Review + create**.

The first distinction that matters in the Via Wash design is between the **user principal name (UPN)** and **display name**. The UPN is the sign-in identifier; the display name is the human-readable name colleagues see. They serve different purposes, so both need a deliberate check before creation. An email-shaped UPN is not proof that a mailbox exists.

On **Properties**, the department and job title give the directory useful context. For our Operations starter, those values would describe the employee’s actual place in Via Wash. I learned not to treat those fields as access controls: entering “Operations” does not automatically add the account to a group. We will need to design and configure that connection, then test it.

The **Assignments** screen made that gap visible. It offered a way to attach existing groups and supported roles, but the practice account had no assignments. I had initially thought about groups and roles as part of creating the account; the exercise clarified that the choices only work when the right groups and role model already exist. That is why the group-design work belongs next, before we try to demonstrate role-based access for Via Wash.

For the employee scenario, the intended user type is **Member** because this is an internal workforce identity. An external collaborator is generally represented as a Guest, subject to the organisation’s policy. The notes for this exercise identify **User Administrator** as the role needed to create a user; this is a learning point, not evidence that I changed or assigned an administrative role in Via Wash.

## What the practice result establishes

The account appeared in the practice directory’s user list after the creation flow. The Assignments screenshot showed no group or role attached through that screen. Together, those captures support that the practice account was created and show what was selected in the wizard.

They do not show a Via Wash account, successful sign-in, access to an application, automatic group membership, device enrolment, or a completed joiner process. Those are separate outcomes we will need to implement and validate in the Via Wash test environment.

## Evidence from the exercise

The original screenshots contain personal account details. I have left a separate, labelled space for each one so the page does not present a tight block of images; approved, redacted copies can be added when available.

{% include evidence.html title="Basics: sign-in name and display name" where="Practice directory · Create new user · Basics" shows="The two identity labels and the initial account settings in the form." proves="The Basics step was reviewed; it does not establish that the account could sign in." %}

{% include evidence.html title="Properties: where the employee belongs" where="Practice directory · Create new user · Properties" shows="The profile fields for identity, department and job information." proves="These fields describe the user; they do not grant group membership or access by themselves." %}

{% include evidence.html title="Assignments: no access was attached here" where="Practice directory · Create new user · Assignments" shows="The assignment step with no groups or roles selected." proves="No assignment was made through this screen in the exercise." %}

{% include evidence.html title="Review + create: checking before submission" where="Practice directory · Create new user · Review + create" shows="The entered account details at the final review step." proves="The review step was reached; the user-list capture below supports that creation followed." %}

{% include evidence.html title="Result: the account appears in the directory" where="Practice directory · Users · All users" shows="The new practice account listed after creation." proves="The account object appeared in that practice directory at capture time, not that it signed in or received access." %}

## Learning reference

This exercise is the **“Create a new user in Microsoft Entra ID”** unit in Microsoft Learn’s [Manage security controls for identity and access](https://learn.microsoft.com/en-us/training/modules/manage-security-controls-identity-access/) module. That module contains 51 units. The walkthrough and our discussion helped me understand the form; the official module assessment result is not recorded, so I am not marking the knowledge check complete.

## The next link in the chain

Before creating Via Wash accounts, I need to settle what department and job information mean, which groups represent access, and who is allowed to administer those groups. The next connected topic is [designing identity and access]({{ '/identity-before-detection/designing-identity-and-access/' | relative_url }}); the user’s department-to-group relationship will be considered there before implementation. Later, we can follow the same Operations starter through group assignment, authentication, device preparation, app availability, and a real validation check.

