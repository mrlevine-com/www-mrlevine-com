---
title: Encryption
units: [AI-Powered Threats and Defenses]
summary: Encryption scrambles your data so only the right key can unlock it.
weight: 510
---

{{% param summary %}}

## Today's Objectives
- Apply encryption concepts to different data states (at rest, in transit, in use).
- Describe how encryption helps protect data.
- Differentiate between symmetric and asymmetric encryption.

## Lesson Overview
### Can you read this secret message?
**WKLV PHVVDJH LV VHFUHW**

Try to decode it before you open the hint.

{{< collapse summary="Click here for a hint." >}}

Shift each letter back 3. For example, W becomes T.

![Two rows of the alphabet. The top row, plain, is A to Z. The bottom row, secret, starts at D and wraps around to A, B, C. Each plain letter points to the letter 3 places after it.](/images/caesar-cipher-shift-3.svg)

{{</ collapse >}}

{{< collapse summary="Click here to reveal the answer." >}}

"This message is secret." It's a Caesar cipher, one of the oldest ways to encrypt.

- **Method:** shift each letter by the same number of places.
- **Key:** that number. With a key of 2, A becomes C. Both people need the key.
- **Without them:** the message looks like nonsense.

{{</ collapse >}}

### What do encryption and decryption do?
{{< collapse summary="Click here to reveal the answer." >}}

Encryption scrambles data so no one can read it without the key. Decryption uses the key to unscramble it.

- **Encryption:** happens when you send a text or store a password.
- **Decryption:** happens when you unlock your phone or read a secure message, using a key your device already knows.

{{</ collapse >}}

{{% define "Encryption" %}}

{{% define "Decryption" %}}

### What does every encryption method need?
{{< collapse summary="Click here to reveal the answer." >}}

A rule you can reverse, and a key kept separate from the message.

- **Rule:** encryption isn't random. If you scramble without a rule, no one can decrypt it, not even you.
- **Key:** the key isn't part of the message. It's a secret you share separately.

{{</ collapse >}}

### What makes encryption strong?
{{< collapse summary="Click here to reveal the answer." >}}

It's hard to crack without the key, but still easy to use with it.

- **Strength:** hidden patterns, extra layers, and lots of possible keys. A Caesar cipher has only 25 keys, so a computer can try them all instantly.
- **Usability:** if a method is too hard, even you can't decode it. A quick text to a friend needs speed more than strength.
- **Real world:** AES protects stored data because it's fast. RSA lets computers share keys safely.

{{</ collapse >}}

### What's the difference between symmetric and asymmetric encryption?
![Two rows. Symmetric: "Hey!" is locked with a key into "Khb!", and the same key unlocks it. Asymmetric: "Hey!" is locked with a public key that anyone can have, and only a different private key unlocks it.](/images/symmetric-vs-asymmetric-encryption.svg)

{{< collapse summary="Click here to reveal the answer." >}}

The number of keys.

| Type           | Keys                                           | Good for                                        |
|----------------|------------------------------------------------|-------------------------------------------------|
| **Symmetric**  | One shared key locks and unlocks               | Speed, if both people already have the key      |
| **Asymmetric** | A public key locks, and only a private key unlocks | Sending secrets to someone you've never met |

It's like a mailbox: anyone can drop a letter through the slot (public key), but only the owner's key opens it (private key).

{{</ collapse >}}

{{% define "Symmetric Encryption" %}}

{{% define "Asymmetric Encryption" %}}

### How does encryption protect data at rest, in transit, and in use?
![Three stages of a message on your phone. At rest, saved on your phone, uses symmetric encryption because it's fast. In transit, sent over the internet, uses asymmetric encryption to connect, then symmetric. In use, opened to read or edit, it's decrypted so apps can read it.](/images/data-states-encryption.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Differently at each stage, like a message on your phone:

| State          | When                     | Protection                                                                  |
|----------------|--------------------------|-----------------------------------------------------------------------------|
| **At rest**    | Saved on your device     | Symmetric, because it's fast and efficient                                  |
| **In transit** | Sent across a network    | Asymmetric sets up a secure connection, even on public internet. Then symmetric protects the message. |
| **In use**     | Opened to read or edit   | Usually decrypted, so apps can read it                                      |

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1: answer three questions about the method you invent in your Unit Journal: how its key works, whether it's symmetric or asymmetric, and which data state it suits best, and why.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Encryption" "Decryption" "Symmetric Encryption" "Asymmetric Encryption" %}}

_Tip: For "Encryption" and "Decryption," encrypt and then decrypt your first name with a key of 3. For the two types, sketch their keys and locks._

### Invent Your Own Encryption Method (~20mins)
Design a method that scrambles a message so only someone with your key can decode it:

1. Pick a short message, and draw how your rule changes a letter, a number, and a symbol.
2. Encrypt your message, and write decryption steps that start with "To decode my message, you need to…"
3. Swap with a classmate, decrypt each other's messages, and write how easy it was and whether someone could crack it without the key.

_Need ideas? Try one of these, or mix two:_

| Idea       | How it works                                                     |
|------------|------------------------------------------------------------------|
| **Symbols**| Swap each letter for an emoji, shape, or color.                  |
| **Grid**   | Map each letter to a spot in a grid.                             |
| **Math**   | Turn each letter into a number, then do math, like adding 5.     |
| **Order**  | Reverse the letters, words, or sentences.                        |
| **Layers** | Stack two rules, or change the scramble based on a password, time, or place. |

{{% instructions-code-org-update %}}
