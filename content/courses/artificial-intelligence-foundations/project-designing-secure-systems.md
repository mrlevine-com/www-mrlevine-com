---
title: "Project: Designing Secure Systems"
units: [AI-Powered Threats and Defenses]
summary: Redesign an app so it's safer and easier to use for real people.
weight: 550
days: 3
---

{{% param summary %}}

## Today's Objectives
- Design secure system improvements that balance protection with usability, using trade-off reasoning.
- Explain how solutions work and how they help real users.
- Identify security and usability issues in a digital system by analyzing user needs and risks.

## Lesson Overview
### What will you do?
**Redesign a real app to make it safer and easier to use.** You'll find two issues the app causes for its users, then draw a Before artifact showing them and an After artifact showing your fixes.

| Day | Milestone       | Code.org Levels | What you'll do                                               |
|-----|-----------------|-----------------|--------------------------------------------------------------|
| 1   | **Investigate** | 1               | Choose an app, find two issues, and draw your Before artifact |
| 2   | **Design**      | 2–3             | Choose fixes, draw your After artifact, and trade feedback    |
| 3   | **Share**       | None            | Polish your After artifact, join a gallery walk, and reflect  |

### What do Before and After artifacts look like?
![Two comic panels. Before: a person's chat message says "Alarm code: 7142," labeled "Saved forever. Anyone can scroll back." After: a smiling shield named Data Expiry says "I delete codes when the sit ends!"](/images/secure-systems-before-after.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Two drawings of the same app, like comic strips or storyboards:

- **Before:** your user runs into both issues. Show what's happening, what goes wrong, and how it affects them.
- **After:** your fixes in action. Personify each security feature as a character that says what it does and why it helps.

{{</ collapse >}}

### How will you be graded?
Full credit looks like this:

| Criteria                         | Full credit                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------|
| **User-Centered Analysis**       | You identify security shortcomings based on a specific user's needs and concerns, with thoughtful, specific reasons. |
| **Security Solutions**           | Your security features fix the issues your users face, and you explain the tradeoffs between security and usability. |
| **Before Artifact**              | It clearly shows at least two different types of security issues in the app's current design.   |
| **After Artifact**               | It shows two different personified security solutions and how they reduce risk, protect users, or prevent human error. |
| **Communication and Creativity** | Your ideas are clear, and your artifacts are creative, thoughtful, and help explain the issues and solutions. |

### How do you get through the levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1 (Day 1): choose an app and open its slide deck. Read its screens and both users' empathy maps, which show what each user says, thinks, feels, and does.

    | App                | Users                | One worry                                                   |
    |--------------------|----------------------|-------------------------------------------------------------|
    | **Pet Sitting**    | Pet owner, pet sitter | The owner wants the sitter to have the alarm code only during the sit. |
    | **Transportation** | Driver, passenger    | The passenger wants to know the driver is verified.          |
    | **Mental Health**  | Client, therapist    | The client wonders if their mood log is saved forever.       |
    | **Mutual Aid**     | Requester, volunteer | The requester wonders if it's safe to share their address.   |

2. Level 2 (optional): upload your app's file, name your user, and describe an issue and your ideas to fix it. Then ask the AI chat a question, like "How would this user react to this solution?"
3. Level 3 (optional): ask the AI chat for help planning your After artifact, like "How do I personify Multi-Factor Authentication in my comic strip?"

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Investigate Your App (Day 1) (~30mins)
Find two issues your Level 1 app causes for its users, and show them in a Before artifact:

1. Fill in this table for both users:

    | User | Needs and concerns |
    |------|--------------------|
    |      |                    |
    |      |                    |

2. Pick two issues from different places in the app: user input, data storage, or data transfer. Fill in this table:

    | Issue | Security, usability, or both? | Why it matters to your user |
    |-------|-------------------------------|-----------------------------|
    |       |                               |                             |
    |       |                               |                             |

3. Draw your Before artifact showing your user running into both issues. Include any important messages, actions, or design flaws.

### Design and Share Your Fixes (Days 2–3) (~75mins)
Fix both issues, show your fixes in an After artifact, and reflect on your choices:

1. Choose at least one security feature for each issue, from the list below or your own idea, and fill in this table:

    |                                              | Issue 1 | Issue 2 |
    |----------------------------------------------|---------|---------|
    | **The issue is…**                            |         |         |
    | **Your solution**                            |         |         |
    | **How does it improve security?**            |         |         |
    | **Is it easy to use? Explain.**              |         |         |
    | **How does it balance security and usability?** |      |         |

    | Place             | Security features                                                                                          |
    |-------------------|------------------------------------------------------------------------------------------------------------|
    | **User input**    | MFA, CAPTCHA, Login Rate Limiting, Device Fingerprinting, Security Questions, Input Validation, Character Limits |
    | **Data storage**  | Hashed Passwords, Sanitization, Unique Username Check, Data Expiry, Version Control, Visibility Controls   |
    | **Data transfer** | Encryption (HTTPS), Rate Limiting on Share, Confirmation Dialogs, Anonymization, Share Expiry, Audit Logging |

    _Forgot what one does? Check the Defense Menu in [Layered Defenses](/courses/artificial-intelligence-foundations/layered-defenses/#defend-your-app-30mins)._

2. Draw your After artifact. Personify each security feature as a character that says what it does and how it helps, like MFA as a bouncer asking for a second ID.

    _When your teacher says to, trade artifacts and tables with another group. Write answers to "Will their solutions fix the issues?" and "Do they make the app easier or harder to use? Why?" Then use their feedback to improve your After artifact._

3. After the Day 3 gallery walk, answer these questions:
    - **Balance:** Which was harder, protecting your users or keeping the app easy to use? How did your fixes balance both?
    - **Pride:** What's one decision in your redesign you're proud of, and why?
    - **Change:** How did this project change the way you think about cybersecurity and secure system design?

_Before you submit, check your work against the grading table above._

{{% instructions-code-org-update %}}
