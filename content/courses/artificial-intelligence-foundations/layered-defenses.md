---
title: Layered Defenses
units: [AI-Powered Threats and Defenses]
summary: Small defenses, stacked together, keep an app safe and easy to use.
weight: 540
---

{{% param summary %}}

## Today's Objectives
- Apply computational thinking to analyze cyberattacks, identify system vulnerabilities, and reason through defense strategies.
- Design a layered defense that balances protection, usability, and constraints.
- Evaluate design choices in system features that balance security and usability, including those enhanced by AI.

## Lesson Overview
### Why do you need more than one security feature?
List as many security features you use as you can in 1 minute, like Face ID on your phone or the key to your front door.

{{< collapse summary="Click here to reveal the answer." >}}

Because any one defense can fail.

- **Different jobs:** each defense stops different attacks.
- **Backup:** if one layer fails, another can still protect you.
- **Balance:** more isn't always better. Each layer costs money to build and adds hassle for users.

{{</ collapse >}}

{{% define "Layered Defense" %}}

### Where can an app be attacked?
![Three boxes connected by arrows. User input, like logins and forms, defended by CAPTCHA. Data storage, like saved profiles, defended by hashed passwords. Data transfer, like sharing and email, defended by encryption (HTTPS).](/images/app-attack-points.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Anywhere data enters, sits, or leaves:

| Place             | Shade it | Examples                   |
|-------------------|----------|----------------------------|
| **User input**    | Green    | Login, forms               |
| **Data storage**  | Blue     | Dashboard, saved profile   |
| **Data transfer** | Yellow   | Cloud sync, email, sharing |

{{</ collapse >}}

### Which pillar does a vulnerability hurt?
| Pillar              | What it protects                                              |
|---------------------|---------------------------------------------------------------|
| **Confidentiality** | Only the right people can see information.                   |
| **Integrity**       | Information stays correct and isn't changed without permission. |
| **Availability**    | People can get to information when they need it.            |
| **Authentication**  | The system checks that you are who you say you are.          |
| **Authorization**   | Rules decide what you can view, edit, or share once you're logged in. |
| **Accounting**      | The system records who did what, and when.                   |

{{< collapse summary="Click here to reveal two examples." >}}

- **Unlimited login guesses:** an attacker can keep guessing passwords. This hurts Authentication.
- **A share link that never expires:** a stranger could open it months later. This hurts Confidentiality.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1: pick one app and click through every screen. Then do steps 1–2 of "Defend Your App" in your Unit Journal.

    | App             | What it does                                       |
    |-----------------|----------------------------------------------------|
    | **LunchCrunch** | Lets students vote on what the cafeteria serves    |
    | **FutureForm**  | Suggests careers based on your interests and data  |
    | **ScoreStack**  | Shows and shares your high scores in popular games |
    | **SocialStar**  | Helps you build a profile and grow your reach as an influencer |

2. Level 2: pick user input, data storage, or data transfer. Describe one vulnerability there and the pillar it hurts, like this:
    - "One vulnerability in the ___ category is ___ because ___."
    - "This impacts the ___ pillar since ___."

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Layered Defense" %}}

_Tip: For your illustration, sketch your phone with two or more defenses stacked in front of it, like a passcode and Face ID._

### Defend Your App (~30mins)
Find the weak spots in your Level 1 app, then choose layered defenses for them:

1. Screenshot each screen of your app into your Unit Journal, or sketch it. Shade where the user enters information green, where the app saves or shows it blue, and where the app sends it out yellow.
2. Fill in this table with one vulnerability for each color and the pillar it hurts:

    | Place         | Vulnerability | Pillar | Why |
    |---------------|---------------|--------|-----|
    | User input    |               |        |     |
    | Data storage  |               |        |     |
    | Data transfer |               |        |     |

3. Choose 2–3 defenses from the Defense Menu below that fix your vulnerabilities. Spend at most 5 cost points and 5 friction points, and fill in this table:

    | Defense   | Why you chose it | Cost | Friction |
    |-----------|------------------|-----:|---------:|
    |           |                  |      |          |
    |           |                  |      |          |
    | **Total** |                  |      |          |

    For example, CAPTCHA (cost 1, friction 1) plus Hashed Passwords (cost 2, friction 0) adds up to cost 3, friction 1.

**Defense Menu:** _cost_ is how much a defense takes to build and run, and _friction_ is how much hassle it adds for users, each from 0 to 3.

**User Input**

| Defense                         | What it does                                             | Cost | Friction | Pillar helped                    |
|---------------------------------|----------------------------------------------------------|-----:|---------:|----------------------------------|
| **MFA (Multi-Factor Authentication)** | Requires a second method, like a code or app, to log in | 2 | 2 | Confidentiality, Authentication |
| **CAPTCHA**                     | Blocks bots by asking you to prove you're human          | 1    | 1        | Confidentiality, Authentication  |
| **Login Rate Limiting**         | Limits how many times someone can try to log in quickly  | 1    | 1        | Availability, Authorization      |
| **Device Fingerprinting**       | Tracks the device used to log in for suspicious patterns | 2    | 0        | Authentication, Accounting       |
| **Security Questions**          | Adds an extra question only the real user can answer     | 1    | 2        | Authentication                   |
| **Input Validation**            | Checks for missing, duplicate, or dangerous inputs       | 1    | 1        | Integrity, Confidentiality       |
| **Character Limits**            | Stops super-long or harmful inputs                       | 1    | 1        | Availability, Integrity          |

**Data Storage**

| Defense                   | What it does                                          | Cost | Friction | Pillar helped                |
|---------------------------|-------------------------------------------------------|-----:|---------:|------------------------------|
| **Hashed Passwords**      | Stores only scrambled versions of passwords           | 2    | 0        | Confidentiality              |
| **Sanitization**          | Cleans data before storing it, like removing scripts or emojis | 1 | 0 | Integrity                 |
| **Unique Username Check** | Stops users from choosing someone else's name         | 1    | 1        | Integrity                    |
| **Data Expiry (TTL)**     | Auto-deletes data after a set time                    | 2    | 1        | Confidentiality, Availability |
| **Version Control**       | Tracks changes to data and lets you roll back         | 3    | 0        | Integrity, Accounting        |
| **Visibility Controls**   | Lets users decide what's private and what's public    | 2    | 1        | Confidentiality              |

**Data Transfer**

| Defense                    | What it does                                        | Cost | Friction | Pillar helped                 |
|----------------------------|-----------------------------------------------------|-----:|---------:|-------------------------------|
| **Encryption (HTTPS)**     | Scrambles data while it travels across the internet | 2    | 0        | Confidentiality               |
| **Rate Limiting on Share** | Stops users from spamming "Send" buttons            | 1    | 1        | Availability                  |
| **Confirmation Dialogs**   | Asks "Are you sure?" before you post or send        | 1    | 2        | Integrity                     |
| **Anonymization**          | Removes personal details from shared data           | 1    | 0        | Confidentiality               |
| **Share Expiry**           | Makes shared links stop working after a while       | 1    | 3        | Confidentiality, Availability |
| **Audit Logging**          | Tracks what was shared, when, and by whom           | 3    | 0        | Accounting                    |

_AI can power some of these defenses. For example, Device Fingerprinting can learn which devices you usually use and flag a login that doesn't fit._

{{% instructions-code-org-update %}}
