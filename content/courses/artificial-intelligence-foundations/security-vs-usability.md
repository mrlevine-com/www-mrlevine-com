---
title: Security vs Usability
units: [AI-Powered Threats and Defenses]
summary: A system isn't truly secure if people can't use it.
weight: 530
---

{{% param summary %}}

## Today's Objectives
- Describe how a security feature might unintentionally create a barrier for users.
- Redesign a security feature to better balance security and usability.

## Lesson Overview
### What happens when password rules pile up?
Write one password that follows rule 1. Then change it to follow each next rule, keeping all the earlier ones:

1. At least 8 characters.
2. At least one special character, like `!` or `#`.
3. The name of a month.
4. Digits that add up to 25.
5. A two-letter element symbol, like `Na` or `He`.

{{< collapse summary="Click here to reveal the answer." >}}

Your password got more secure, but much harder to make and remember.

- **Workarounds:** when rules get too hard, people write passwords down, reuse them, or give up.
- **Big idea:** a system isn't truly secure if people can't use it.

{{</ collapse >}}

### Who gets blocked by these security features?
| Feature         | It's meant to                               | But it can                                                         |
|-----------------|---------------------------------------------|--------------------------------------------------------------------|
| Auto-logout     | Protect your info if you walk away          | Log you out mid-test if you work slowly or pause to think          |
| Account lockout | Stop someone from guessing your password    | Lock you out if your keyboard breaks, you need assistive tech, or you're stressed |

{{< collapse summary="Click here to reveal the answer." >}}

People whose needs the designer didn't plan for.

- **Intended benefit:** keep attackers out.
- **Unintended consequence:** keep real users out, too.
- **Ask:** what user situation might the designer not have pictured?

{{</ collapse >}}

### How do you rate a security feature?
![A 2-by-2 grid with security across the bottom and usability up the side. Good usability and low security: convenient but risky, like auto-login on a shared device. Good usability and high security: the sweet spot, like a password manager that autofills. Bad usability and low security: frustrating and dangerous, like a new complex password every 2 weeks. Bad usability and high security: over-secured, like two-factor login every single time.](/images/security-usability-matrix.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Place it in one box of the Security vs Usability Matrix above.

| Box                           | What happens                               |
|-------------------------------|--------------------------------------------|
| **Convenient but risky**      | It's easy for attackers to get in.         |
| **The sweet spot**            | Good behavior is the easy choice.          |
| **Frustrating and dangerous** | People write passwords down or reuse them. |
| **Over-secured**              | Users find ways around it.                 |

There's often more than one right box. What matters is your reason.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1: decide if a classmate's claim about auto-logout is accurate. Hint: does a more secure feature work for everyone?
2. Level 2: pick one user and follow their day. Then do "Map Your User's Security Features" in your Unit Journal.

| User       | Who they are                                      | What gets in their way    |
|------------|---------------------------------------------------|---------------------------|
| **Riley**  | An artist who uses a tablet for everything        | A tremor makes touch-based security tricky |
| **Amira**  | Uses a screen reader and high-contrast tools      | Security tools not designed for low vision |
| **Elijah** | Makes music and videos in a busy, shared home     | Voice-based security in noisy rooms |
| **Mei**    | Wears a mask and glasses every day for health reasons | Facial recognition and other biometric logins |

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Map Your User's Security Features (~15mins)
Place each security feature your Level 2 user runs into on the Security vs Usability Matrix:

1. Draw the matrix from the Lesson Overview, and write your user's name above it.
2. Draw a dot for each of the 3 features in the box where it fits, and label it with the feature's name.
3. Next to each dot, write whether it worked well, partly worked, or didn't work for your user, and why.

| Rate its     | Ask yourself                                                                     |
|--------------|----------------------------------------------------------------------------------|
| **Usability** | Could your user finish on the first try? Did it block or frustrate them?        |
| **Security**  | Would it stop someone who shouldn't get in? Could someone trick or bypass it?   |

### Redesign One Feature (~20mins)
Redesign the feature that worked worst for your user, ideally one in the "Frustrating and dangerous" box, so it's easier to use and still safe:

1. Sketch your user using your redesigned feature, with a speech bubble saying how it feels, like "Finally, I can log in with my fingerprint!"

    | Fix idea               | Example                  |
    |------------------------|--------------------------|
    | **Add a backup**       | Voice login plus a text code |
    | **Simplify the input** | Swap a swipe pattern for a PIN |
    | **Change the sensor**  | Swap face for fingerprint |
    | **Watch behavior**     | Spot unusual patterns instead of asking for a password |
    | **Add a cue**          | A sound or visual signal that shows what to do |

2. Explain your fix under your sketch by finishing these sentences:
    - "Instead of ___, we could try ___ because…"
    - "This fix would help users who…"
    - "It still keeps people safe by…"
    - "A tradeoff might be…, but it's worth it because…"
3. Show your redesign to a classmate who picked the same user, and write their answers to: Will this help the user more? Is it still secure? How could it be even better?

{{% instructions-code-org-update %}}
