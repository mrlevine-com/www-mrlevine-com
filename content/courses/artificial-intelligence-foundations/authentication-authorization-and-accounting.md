---
title: Authentication, Authorization, and Accounting
units: [AI-Powered Threats and Defenses]
summary: Systems check who you are, then decide what you can do.
weight: 490
---

{{% param summary %}}

## Today's Objectives
- Apply authentication and access control models to real-world scenarios.
- Explain how systems verify identity and manage access to information.

## Lesson Overview
### What are AAA tools?
![Three boxes with arrows between them: Authentication asks who are you? Authorization asks what can you do? Accounting asks what did you do?](/images/aaa-tools-flow.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Three steps systems use to protect the CIA Triad, whether you're logging into a game, checking grades, or sharing a playlist:

1. **Authentication:** checks who you are.
2. **Authorization:** decides what you're allowed to do. It only works after authentication.
3. **Accounting:** tracks what you did. You'll learn more about it next lesson.

{{</ collapse >}}

{{% define "AAA Tools" %}}
{{% define "Authentication" %}}
{{% define "Authorization" %}}
{{% define "Accounting" %}}

### How do you prove you're you without showing your face?
{{< collapse summary="Click here to reveal the answer." >}}

With something you know, have, or are:

| Something you... | Examples                                                                  |
|------------------|---------------------------------------------------------------------------|
| **Know**         | Password, PIN code, security question, pattern lock                       |
| **Have**         | Code texted to your phone, hardware security key (like a YubiKey), authentication app (like Google Authenticator), access card or badge |
| **Are**          | Fingerprint scan, Face ID, voice recognition, iris scan                   |

AI can fool some of these. For example, it can fake your voice or face.

{{</ collapse >}}

### How do systems decide what you're allowed to do?
{{< collapse summary="Click here to reveal the answer." >}}

With an access control model. Each one writes rules like "If [conditions], then grant or deny access to [something]":

| Model                              | Who or what decides                 | Example                                          |
|------------------------------------|-------------------------------------|--------------------------------------------------|
| **Role-Based (RBAC)**              | Your role, like student or teacher  | If you're a teacher, then grant access to change grades. |
| **Discretionary (DAC)**            | The owner of the thing              | If you shared your doc with a friend, then grant them access to edit it. |
| **Attribute-Based (ABAC)**         | Details like device, location, or time | If you're on a school laptop, then grant access to the testing app. |

{{</ collapse >}}

### Is each statement accurate?
1. "Authentication decides which files you're allowed to edit."
2. "You choose who can comment on your posts, so that's role-based access control."
3. "A bank app blocks logins from a new country at 3 a.m. That's role-based access control."

{{< collapse summary="Click here to reveal the answers." >}}

None of them are accurate:

1. **Authorization** decides what you can edit. Authentication only checks who you are.
2. You own the posts and chose who can comment, so it's **discretionary**.
3. Location and time are attributes, so it's **attribute-based**.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1 (Check for Understanding): answer two questions about how systems check who you are and decide what you can access. Say *how* a login checks you, not just "you log in."

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "AAA Tools" "Authentication" "Authorization" "Accounting" %}}

_Tip: For "AAA Tools," sketch the three boxes from the Lesson Overview. For the other three, sketch a fingerprint, a door with a "Teachers Only" sign, and a list of logins._

### Sort Logins and Write Access Rules (~20mins)
Practice authentication and access control:

1. Draw three columns labeled Know, Have, and Are. Without looking, sort these into them, then check against the Lesson Overview: password, PIN code, security question, pattern lock, code texted to your phone, hardware security key, authentication app, access card, fingerprint scan, Face ID, voice recognition, iris scan.
2. Circle one method in each column that AI could fool, and write how. Then add one new method of your own to each column.
3. Pick two scenarios below. For each, write a rule ("If ..., then grant/deny access to ..."), label it RBAC, DAC, or ABAC, and write why that model fits.

| Where              | Scenarios                                                                                         |
|--------------------|---------------------------------------------------------------------------------------------------|
| **School**         | Only teachers can update final grades. Anyone can browse the online library, but only logged-in students can download eBooks. School Wi-Fi blocks gaming sites during school hours. You join a video call directly with a school email, or else wait in the lobby. |
| **Home & friends** | A friend gives you their Disney+ login. Your mom sets screen time limits on your sibling's iPad apps. You let only certain friends add songs to your playlist. You let a friend see your private photo album for 24 hours. Only parents can approve new events on the family calendar. |
| **Apps**           | A ride-sharing app shows the driver's exact location based on ride status and user role. An app blocks payments on public Wi-Fi. A smartwatch app shares your step count publicly but keeps your heart rate private. A bank app shows your balance but needs face recognition to transfer money. You enter a PIN sent to your email to reset your social media password. A messaging app shows your online status only to your contacts. An online store shows different prices to logged-in members. |
| **Groups**         | VIP ticket holders get the front section at a concert. Only registered members can vote on a club website. Moderators can delete offensive comments in an online art community. Gym trainers can update your fitness goals, but you can only view them. |

{{% instructions-code-org-update %}}
