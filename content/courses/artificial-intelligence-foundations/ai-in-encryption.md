---
title: AI in Encryption
units: [AI-Powered Threats and Defenses]
summary: AI can find ways around encryption, but it can also help protect it.
weight: 520
---

{{% param summary %}}

## Today's Objectives
- Analyze a tradeoff introduced by AI’s role in encryption.
- Identify ways AI can both weaken and strengthen encryption.
- Model how AI and computational power influence the effectiveness of encryption systems.

## Lesson Overview
### How can AI help and hurt an encrypted app?
You just built a messaging app, and its encryption is solid. Then someone warns you, "With AI, you might still be in trouble."

{{< collapse summary="Click here to reveal the answer." >}}

It can do both. AI finds ways around encryption, and it helps block them.

| Side     | What AI does                                                     |
|----------|------------------------------------------------------------------|
| **Hurt** | Finds weak passwords and vulnerable settings                     |
| **Help** | Creates strong passwords, detects unusual activity, and blocks threats |

{{</ collapse >}}

### How does AI crack passwords?
![Two ways to guess a password. Brute force tries every combination in order, like aaaaaa, aaaaab, aaaaac, so it needs a huge number of tries. AI guessing learns from Leo's posts about soccer and being born in 2009, so it tries likely guesses first, like Soccer2009! and GoalKing09.](/images/brute-force-vs-ai-guessing.svg)

{{< collapse summary="Click here to reveal the answer." >}}

By spotting patterns, not by guessing randomly.

- **Training:** AI learns from huge collections of leaked passwords and public info, like social media posts.
- **Prediction:** it guesses what a person is most likely to choose. It doesn't read private messages or store anyone's actual password.
- **Power:** computers try guesses incredibly fast, and AI makes each guess smarter, so weak passwords fall even sooner.
- **Defense:** the same skill can warn you that your password is weak or showed up in a leak.

{{</ collapse >}}

### What can AI learn from encrypted messages?
![An encrypted message in a locked envelope, labeled "What you said: hidden." Next to it, its metadata is visible: who (Sam to Riley), when (8:02 PM), how often (6 messages in 13 minutes), and how long (195 characters). AI can still find patterns in it.](/images/encrypted-message-metadata.svg)

{{< collapse summary="Click here to reveal the answer." >}}

A lot, without reading a word. Apps like Signal, WhatsApp, and iMessage encrypt what you say, so no one, not even the app, can read it.

- **Metadata:** who you messaged, when, how often, and how long your messages were can still be visible.
- **Guesses:** AI finds patterns in that [metadata](/glossary/metadata/) to guess what kind of conversation you're having.
- **Tradeoff:** that can protect you, like by flagging bullying or spam, but it can also flag the wrong person or invade your privacy.

{{</ collapse >}}

### Should a school use AI to watch its encrypted messages?
{{< collapse summary="Click here to reveal the answer." >}}

It's a tradeoff between safety, privacy, and control. To decide, ask:

| Question                 | Examples                                               |
|--------------------------|--------------------------------------------------------|
| **Who uses it?**         | A hacker, a school IT team, or a big tech company      |
| **How?**                 | To guess passwords, monitor security, or help users    |
| **What could go wrong?** | It flags the wrong person, gets misused, or invades privacy |

Also ask who benefits, and who might be overlooked.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1: answer a quick check about how AI guesses passwords. Think patterns.
2. Level 2: ask AI Chat to guess Maya's next password. Compare its guesses with yours: what's similar, what's different, and what stands out?
3. Level 3: ask AI Chat to analyze one chat's metadata. Decide what it got right and what it might get wrong.
4. Level 4: choose a solution for the school's encrypted messaging app. Explain your choice with at least one benefit and one tradeoff from the level's table.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Think Like a Password-Cracking AI (~10mins)
Predict Maya's next password from her leaked ones:

**DogMom2006, Swiftie2025!, VolleyballGirl09, PizzaQueen99, GoVolleys_08, TSnaps_2009, PawsAreLife22, RedCard_7x**

1. Copy Maya's passwords, circle the things she cares about, and underline the numbers and symbols.
2. Write the rule she seems to follow, and two passwords she might make next.
3. Write one way AI could use this skill to harm Maya, and one way it could protect her.

### Think Like a Metadata AI (~15mins)
Decide how your school's messaging AI would treat two of these chats:

| Chat | Time     | From → To      | Length (characters) |
|------|----------|----------------|--------------------:|
| 1    | 8:02 PM  | Sam → Riley    | 195                 |
| 1    | 8:03 PM  | Riley → Sam    | 6                   |
| 1    | 8:04 PM  | Sam → Riley    | 220                 |
| 1    | 8:06 PM  | Riley → Sam    | 9                   |
| 1    | 8:10 PM  | Sam → Riley    | 180                 |
| 1    | 8:15 PM  | Riley → Sam    | 5                   |
| 2    | 10:28 AM | Jamie → Alex   | 14                  |
| 2    | 10:29 AM | Alex → Jamie   | 18                  |
| 2    | 10:30 AM | Jamie → Alex   | 20                  |
| 2    | 10:45 AM | Alex → Jamie   | 16                  |
| 2    | 10:46 AM | Jamie → Alex   | 15                  |
| 3    | 4:12 PM  | Casey → Morgan | 6                   |
| 3    | 4:13 PM  | Casey → Morgan | 8                   |
| 3    | 4:14 PM  | Casey → Morgan | 5                   |
| 3    | 4:15 PM  | Casey → Morgan | 7                   |
| 3    | 4:16 PM  | Casey → Morgan | 9                   |
| 3    | 4:18 PM  | Casey → Morgan | 6                   |

1. Draw each chat as a row of message bubbles, making longer messages bigger bubbles.
2. Write what you think is happening in each chat, and whether the AI would flag it for bullying, spam, or off-task chatting in class.
3. Write whether you think each chat should be flagged, and why.

{{% instructions-code-org-update %}}
