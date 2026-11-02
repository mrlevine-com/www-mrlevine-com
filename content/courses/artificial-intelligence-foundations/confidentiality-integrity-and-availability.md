---
title: Confidentiality, Integrity, and Availability
units: [AI-Powered Threats and Defenses]
summary: Every security failure exposes, changes, or blocks information.
weight: 480
---

{{% param summary %}}

## Today's Objectives
- Describe how a system vulnerability allowed a confidentiality, integrity, or availability failure and propose a user-centered fix.
- Identify cybersecurity failures based on their impact on confidentiality, integrity, or availability (CIA Triad).

## Lesson Overview
### What makes an app feel untrustworthy?
{{< collapse summary="Click here to reveal the answer." >}}

The fear of losing one of three things:

- **Privacy:** "What if someone sees my stuff?"
- **Accuracy:** "What if someone changes it or messes it up?"
- **Access:** "What if I can't use it when I need it?"

{{</ collapse >}}

### What is the CIA Triad?
![A triangle labeled CIA Triad. Its corners are Confidentiality: who can see it? Integrity: is it correct? Availability: can you get to it?](/images/cia-triad-triangle.svg)

{{< collapse summary="Click here to reveal the answer." >}}

The three goals of cybersecurity. Professionals use them to find what went wrong and how to protect people:

| Goal                | Question it asks    | Example failure                          |
|---------------------|---------------------|------------------------------------------|
| **Confidentiality** | Who can see it?     | A stranger reads your private messages.  |
| **Integrity**       | Is it correct?      | Someone changes your score without permission. |
| **Availability**    | Can you get to it?  | An app crashes on the day your work is due. |

{{</ collapse >}}

{{% define "CIA Triad" %}}
{{% define "Confidentiality" %}}
{{% define "Integrity" %}}
{{% define "Availability" %}}

### Which goal failed in each scenario?
1. The homework portal crashes the night before an assignment is due, so you miss the deadline.
2. A sign-up sheet with students' home addresses and phone numbers gets posted where the whole school can see it.
3. Someone edits your essay in a shared folder, so it's no longer what you wrote.
4. Someone logs into your music app, sees what you listen to, and changes your playlist.

{{< collapse summary="Click here to reveal the answers." >}}

| Scenario | Goal                          | Why                                                   |
|----------|-------------------------------|-------------------------------------------------------|
| **1**    | Availability                  | You couldn't get to the system when you needed it.    |
| **2**    | Confidentiality               | Private info was seen by people it wasn't meant for.  |
| **3**    | Integrity                     | The file was changed without permission.              |
| **4**    | Integrity and confidentiality | The playlist was changed, and your listening was seen. |

{{</ collapse >}}

### How do you attack and defend a system?
Find the failure as the attacker, then fix it as the defender. For example, an attacker logs into a student's account and reads their private messages:

| Attacker's target | Goal            | Why it matters                                  | Defender's fix                 | Tradeoff                     |
|-------------------|-----------------|-------------------------------------------------|--------------------------------|------------------------------|
| Private messages  | Confidentiality | The attacker could share them or pretend to be the student. | Add 2-step verification to prove it's really them. | Logging in takes longer. |

{{< collapse summary="Click here to reveal how to find the target." >}}

Ask what the attacker could do:

- **See** something they shouldn't? Confidentiality.
- **Change** or mess something up? Integrity.
- **Block** someone from using it? Availability.

Not every failure comes from a hacker. Sometimes a regular user causes harm because the system didn't protect against it.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1: skip the linked documents. Do "Attack and Defend a System" in your Unit Journal instead.
2. Level 2 (AI Chat): if you get stuck, ask which goal was affected, why it matters, or for possible fixes and tradeoffs.
3. Level 3: read about careers that protect the CIA Triad.
4. Level 4 (Check for Understanding): explain which career you think makes the biggest difference, and why. Connect it to confidentiality, integrity, or availability.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "CIA Triad" "Confidentiality" "Integrity" "Availability" %}}

_Tip: For "CIA Triad," sketch the triangle. For the other three, sketch a lock, a document with a checkmark, and an "Open" sign._

### Attack and Defend a System (~20mins)
Investigate the scenarios below with a partner:

| Scenario                     | What happened                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------|
| **1. Deleted Memories**      | A teen shares a family photo folder where every relative can view, upload, and delete. After someone reorganizes it, photos are missing. |
| **2. Locked Out on Launch Day** | On a game's release night, the login system can't handle the traffic. Correct logins fail, some people are blocked, and no one knows who got in. |
| **3. Calendar Chaos**        | A student adds personal notes to a school calendar, then finds out others could see it and someone changed a note. |
| **4. Science Fair Switch-Up** | Two groups share a folder. One group's project is replaced with something else, and the teacher can't tell who did it or when. |
| **5. Guest Wi-Fi Surprise**  | Maya gives a friend her guest Wi-Fi password. That night, her smart TV connects and her Netflix profile is renamed, with no one else home. |
| **6. Locked Grades**         | After an update, no one can log into the school's grade portal for two days, so a student can't check their GPA when they need it. |

1. Write C, I, or A (or more than one) next to each scenario number.
2. Draw a table with the columns from the example in the Lesson Overview. Fill in a row for three scenarios, one for each goal, taking turns as attacker and defender. Use these if you get stuck:

    | Fix type          | Fixes                                                                      |
    |-------------------|----------------------------------------------------------------------------|
    | **Check identity** | 2-step verification, stronger logins, unique accounts instead of shared ones |
    | **Limit access**  | Let only some people edit or delete, give view-only access, preview who can see it before sharing |
    | **Track changes** | Version history, change logs, alerts for logins or changes                  |
    | **Recover**       | Backups and auto-save                                                       |
    | **Handle traffic** | More system capacity for busy times and outages                            |

    Tradeoffs might be slower logins or extra steps, confused users or real users locked out, less flexibility for working together, or more cost and effort to manage.

3. Write one pattern you notice for each goal: what went wrong, and what kind of fix helped.

{{% instructions-code-org-update %}}
