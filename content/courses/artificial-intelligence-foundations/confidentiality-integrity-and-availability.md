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
Attack and defend three of these systems with a partner:

| Scenario              | What happened                                                              |
|-----------------------|----------------------------------------------------------------------------|
| **1. Photo Folder**   | Every relative can delete from a shared family folder. Photos go missing.  |
| **2. Game Launch**    | Logins fail on release night, and no one knows who got in.                 |
| **3. School Calendar** | Others can see a student's personal notes, and someone changed one.       |
| **4. Science Fair**   | A group's project in a shared folder is replaced. No one knows by whom.    |
| **5. Guest Wi-Fi**    | A friend uses Maya's Wi-Fi password, then renames her Netflix profile.     |
| **6. Grade Portal**   | After an update, no one can log in for two days.                           |

1. Write C, I, or A next to each scenario number (some get more than one).
2. Draw a table with columns **Attacker's target**, **Goal**, **Why it matters**, **Defender's fix**, and **Tradeoff**. Fill in one row each for a C, an I, and an A scenario. Take turns as attacker and defender. Stuck? Pick a fix:

    | Fix type           | Examples                            | Tradeoff                      |
    |--------------------|-------------------------------------|-------------------------------|
    | **Check identity** | 2-step verification, own accounts   | Slower logins, users locked out |
    | **Limit access**   | View-only, only some can delete     | Harder to work together       |
    | **Track changes**  | Version history, change alerts      | More to manage                |
    | **Recover**        | Backups, auto-save                  | More cost                     |
    | **Handle traffic** | More capacity for busy times        | More cost                     |

3. Under your table, write what kind of fix worked for each goal.

{{% instructions-code-org-update %}}
