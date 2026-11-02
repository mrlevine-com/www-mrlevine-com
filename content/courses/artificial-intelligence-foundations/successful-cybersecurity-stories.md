---
title: Successful Cybersecurity Stories
units: [AI-Powered Threats and Defenses]
summary: The best defenses stop threats before you even notice.
weight: 470
---

{{% param summary %}}

## Today's Objectives
- Evaluate different defenses to determine what made them effective.
- Explain how system design, human behavior, and AI can work together to prevent a cyber threat.

## Lesson Overview
### Why do CAPTCHAs and one-time passcodes matter?
{{< collapse summary="Click here to reveal the answer." >}}

They quietly protect you, even when they feel annoying:

- **CAPTCHA:** checks that you're a person, not a bot, to stop fake signups and spam attacks.
- **One-time passcode:** adds a code to your login, so a stolen password isn't enough to get in.

{{</ collapse >}}

Protections like these are **defense mechanisms**. They can be built into a system, powered by AI, or come from people noticing something's wrong.

### How were these five threats stopped?
| Case                  | What happened                                                                     |
|-----------------------|-----------------------------------------------------------------------------------|
| **Faked voice**       | A caller used a faked voice of a long-time customer to get into their account.    |
| **Livestream trolls** | Trolls flooded the chat of a youth talent show's livestream with offensive messages. |
| **Lost game**         | Leo's game froze while saving, and his 3-hour battle arena build vanished.        |
| **Strange login**     | Someone in another state logged into Ava's YouTube channel from a Windows PC she doesn't own. |
| **Deepfake**          | A meme account posted a fake video of Jules, a student athlete, with her face and voice. |

{{< collapse summary="Click here to reveal the defenses." >}}

| Case                  | What stopped it                                                                                                         | Type of defense   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------|
| **Faked voice**       | AI noticed the voice's tone and timing were slightly off and asked for extra verification. The caller hung up, and the security team alerted the real customer. | AI, system, people |
| **Livestream trolls** | AI hid offensive comments in many languages and flagged accounts. Maya, the moderator, judged slang the AI wasn't sure about. | AI, people        |
| **Lost game**         | Cloud auto-save backed up the game every 15 minutes, so support restored it. Engineers patched the bug for everyone.   | System, people    |
| **Strange login**     | A login alert warned Ava, and two-factor authentication (2FA) blocked the intruder. Ava reset her password and limited which apps could access her account. | System, people    |
| **Deepfake**          | AI spotted mismatches in face movement and voice, and human reviewers confirmed it was fake. The video was removed within 30 minutes. | AI, people        |

{{</ collapse >}}

### What do successful defenses have in common?
![A threat arrow slips through a gap in the AI tool layer but is stopped by the system design layer. The three layers, AI tool, system design, and people, each have a gap in a different spot.](/images/layered-defense-threat.svg)

{{< collapse summary="Click here to reveal the answer." >}}

More than one layer. Every layer has gaps, so the next layer catches what the last one missed:

- **AI:** spots patterns people would miss, like a voice that's slightly off.
- **System design:** sets rules, backups, and extra login steps.
- **People:** notice, double-check, and act fast, like Maya judging slang the AI wasn't sure about.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1: skip the linked documents. Do "Analyze a Defense" in your Unit Journal instead.
2. Level 2 (Check for Understanding): explain how system design, human behavior, and AI worked together to stop a threat, and why the defense worked.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Analyze a Defense (~15mins)
Analyze one case from the Lesson Overview:

1. Write what the attacker tried to do and what the defense protected: "Someone tried to... This defense protected..."
2. Draw the defense as layers, like the diagram above. Label each layer AI, system, or people, and write what it did.
3. Write which job below could have helped set up or respond to the defense, and why.

| Job                      | What they do                                                  |
|--------------------------|---------------------------------------------------------------|
| **Security Analyst**     | Monitors systems, investigates unusual activity, and responds to alerts |
| **IT Support Specialist**| Troubleshoots problems and teaches people to use tech safely  |
| **Network Admin**        | Sets rules for how devices and users connect to the internet  |
| **AI Security Engineer** | Builds AI tools that detect suspicious patterns and flag risks |
| **UX Designer**          | Designs systems that are both safe and easy to use            |

### Compare Two Defenses (~10mins)
Compare your case with a classmate who chose a different one:

1. Share your drawings, and write one question you have about their case, like "Can you explain more about...?"
2. Write one way the two cases are similar and one way they're different.
3. Pick the layer that mattered most in each case, and write what could have gone wrong without it.

{{% instructions-code-org-update %}}
