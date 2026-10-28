---
title: Creating a user in Entra ID
headline: The first step in getting a new colleague ready
kind: page
topic: building-identity-in-entra-id
order: 51
status: Needs validation
summary: I worked through Entra’s new-user flow and used it to see what needs deciding before I create a Via Wash employee account.
updated: 2026-10-28
permalink: /identity-before-detection/building-identity-in-entra-id/creating-a-user/
---

## An Operations starter is waiting for access

Imagine HR tells IT that someone is joining Via Wash’s **Operations** department at a London branch. On their first shift, they’ll need to sign in, use the systems their role requires and work from a prepared device.

That starts before anyone opens Entra. HR has to tell IT who the employee is and what they’ll do. IT has to turn that into an account people can recognise, then connect the person to the right access. A name in a directory is not the same thing as a ready employee.

I haven’t built this onboarding process in Via Wash yet. I used a separate practice directory to work through the Entra form and find out which decisions I need to make before I do.

## Give the account the right name

In Entra, the sign-in name and the display name do different jobs. The **user principal name (UPN)** is how the person signs in. The **display name** is the person’s name colleagues should see. I need both to be right, and I must not assume that an email-shaped UPN means a mailbox is working.

For Via Wash, I still need to confirm the sign-in naming rule and domain for staff accounts. The Cyber Consolidated business email belongs to the portfolio project; it isn’t a Via Wash employee account.

{% include evidence.html title="Basics · choose the sign-in name and display name" where="Practice directory · Create new user · Basics" shows="The sign-in name, display name and account settings in the form." proves="I reached and reviewed the Basics step; it does not show a successful sign-in." %}

## Put the employee in the right part of Via Wash

The **Properties** page is where the directory records details such as department and job title. For this starter, the department is Operations. The job title should describe the actual job, using the wording Via Wash agrees to use consistently.

That consistency will matter when I build group rules. If a future rule matches a department or title, a different spelling or an unapproved title could leave the employee out. The rules don’t exist yet, so the profile fields won’t grant access by themselves.

This is an internal Via Wash employee, so the intended account type is **Member**. **Guest** is generally used for an external collaborator. The administrator creating the account needs the **User Administrator** role; that permission belongs to IT, not to the new employee.

{% include evidence.html title="Properties · record the employee’s department and job" where="Practice directory · Create new user · Properties" shows="The identity and job-information fields available for a new user." proves="These fields describe an account; they do not create access rules or add the person to a group." %}

## Access comes from groups we have designed

On the **Assignments** page, an administrator can add the new account to existing groups or assign a directory role. My practice account had no assignments. That was useful to see: Entra can attach a group here, but it can’t choose the right Via Wash group until we have designed one.

You’ve said that the future process should use the employee’s department and job to put them in the right groups. That can be built with an agreed membership rule or another onboarding workflow; filling in the profile alone won’t do it. We need to decide what an Operations employee should reach, create the groups, and test that the membership and access are correct before we rely on it.

{% include evidence.html title="Assignments · no group or role selected" where="Practice directory · Create new user · Assignments" shows="The assignment choices before the practice account was created; none were selected." proves="No group or role was added through this step for that practice account." %}

## Check what was created

The **Review + create** page let me look over the account details before submitting them. After creation, the account appeared in the practice directory’s user list. That confirms the practice account object was created there. It doesn’t show a successful sign-in or prove access to an application.

{% include evidence.html title="Review + create · check the details before submission" where="Practice directory · Create new user · Review + create" shows="The final review of the account details." proves="I reached the review step; the user list below is the evidence that creation followed." %}

{% include evidence.html title="The account appears in the practice directory" where="Practice directory · Users · All users" shows="The new account listed after the creation flow." proves="The account object appeared in the separate practice directory; it is not a Via Wash account or sign-in test." %}

The screenshots are from the practice directory and contain personal account details. I haven’t put the unredacted originals on the public site. I’ll replace these labelled spaces with the genuine screenshots after they’ve been redacted.

## What I’m learning, and what I’ll do next

I worked through Microsoft Learn’s [Create a new user in Microsoft Entra ID](https://learn.microsoft.com/en-us/training/modules/manage-security-controls-identity-access/5-create-new-user) unit. It is part of the 51-unit **Manage security controls for identity and access** module. We reviewed the concepts together, but I haven’t recorded the module knowledge-check result as complete.

The next business question is what an Operations employee should be able to use on day one. I’ll work through [Secure Microsoft Entra groups](https://learn.microsoft.com/en-us/training/modules/manage-security-controls-identity-access/6-secure-microsoft-entra-groups) alongside the [Via Wash identity and access design]({{ '/identity-before-detection/designing-identity-and-access/' | relative_url }}). Once the group model is clear, I can create it, add a test user, and check whether access follows the job as intended.

