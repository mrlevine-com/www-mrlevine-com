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

Three checks every app runs, from games to grades:

| Step               | Asks                                    |
|--------------------|-----------------------------------------|
| **Authentication** | Who are you?                            |
| **Authorization**  | What can you do? (only after step 1)    |
| **Accounting**     | What did you do? (more on this next lesson) |

{{</ collapse >}}

{{% define "AAA Tools" %}}
{{% define "Authentication" %}}
{{% define "Authorization" %}}
{{% define "Accounting" %}}

### How do you prove you're you?
{{< collapse summary="Click here to reveal the answer." >}}

Show something you know, have, or are:

| Something you... | Examples                               |
|------------------|----------------------------------------|
| **Know**         | Password, PIN                          |
| **Have**         | Code texted to your phone, school ID   |
| **Are**          | Face ID, fingerprint                   |

AI can fake some of these, like your voice or face.

{{</ collapse >}}

### How do apps decide what you can do?
{{< collapse summary="Click here to reveal the answer." >}}

With an access control model: a rule like "If ..., then grant or deny access to ...":

| Model                      | Who decides            | Example                                   |
|----------------------------|------------------------|-------------------------------------------|
| **Role-Based (RBAC)**      | Your role              | If you're a teacher, then you can change grades. |
| **Discretionary (DAC)**    | The owner              | If you share your doc with a friend, then they can edit it. |
| **Attribute-Based (ABAC)** | Details like place or time | If it's class time, then school Wi-Fi blocks games. |

{{</ collapse >}}

### Can you spot the mistake in each?
Guess first, then check. Score 1 point for each one you get.

1. "Authentication decides which files you can edit."
2. "You choose who can comment on your posts. That's role-based."
3. "A bank app blocks logins from a new country at 3 a.m. That's role-based."

{{< collapse summary="Click here to reveal the answers." >}}

1. **Authorization** decides what you can edit. Authentication only checks who you are.
2. You own the posts, so it's **discretionary**.
3. Place and time are details, so it's **attribute-based**.

Got 3/3? You're ready for Code.org.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1 (Check for Understanding): answer two questions about how systems check who you are and decide what you can do. Say *how* a login checks you, not just "you log in."

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "AAA Tools" "Authentication" "Authorization" "Accounting" %}}

_Tip: For "AAA Tools," sketch the three boxes from the Lesson Overview._

### Design the Security for Your Own App (~15mins)
Draw the login and access rules for an app you'd want to build, like a game, a playlist app, or a club site:

1. **Login:** Sketch its login screen with two ways to prove it's you, and label each Know, Have, or Are.
2. **Rules:** Write two rules, like "If you're an admin, then you can ban players," and label each RBAC, DAC, or ABAC.
3. **Hack it:** Circle one login method AI could fake, and write how.

✅ Done when your app has 2 labeled logins, 2 labeled rules, and 1 weak spot circled.

{{% instructions-code-org-update %}}
