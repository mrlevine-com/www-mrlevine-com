---
title: AAA and AI
units: [AI-Powered Threats and Defenses]
summary: AI learns what's normal for you, so it can spot what isn't.
weight: 500
---

{{% param summary %}}

## Today's Objectives
- Analyze how AI supports security features like fraud detection, anomaly detection, and adaptive authentication.
- Explain how AI is used in threat detection to identify suspicious patterns.

## Lesson Overview
### What makes something an anomaly?
![A timeline of five logins. Four are at 7:30 AM from home on your phone. One, on Thursday at 3:00 AM from a new city and a new device, sticks out as an anomaly.](/images/anomaly-login-timeline.svg)

{{< collapse summary="Click here to reveal the answer." >}}

It breaks a pattern. An anomaly is data that doesn't match what usually happens.

- **Clues:** late-night activity, unexpected places, or sudden changes, like strange card purchases.
- **Bias:** what looks suspicious to you depends on your own experience and background.

{{</ collapse >}}

### How does Accounting help catch fraud?
{{< collapse summary="Click here to reveal the answer." >}}

It keeps a record of what users do, so you can look back for anomalies. Accounting, also called auditing, is the third A in AAA:

| AAA                | Question it answers          |
|--------------------|------------------------------|
| **Authentication** | Who are you?                 |
| **Authorization**  | What are you allowed to do?  |
| **Accounting**     | What did you do?             |

- **Example:** a Google Doc's version history shows who changed what, and when.
- **Logs:** today you'll investigate three kinds: logins, locations, and purchases.

{{</ collapse >}}

{{% define "Accounting" %}}

### How does AI detect fraud?
{{< collapse summary="Click here to reveal the answer." >}}

It learns what "normal" looks like, then flags what doesn't fit.

- **Training:** people label many examples "suspicious" or "normal," and the AI finds the patterns in them.
- **Speed:** it scans huge logs fast and catches small, repeated patterns that tired humans miss. Banks use it to flag strange card purchases.
- **Context:** unusual isn't always fraud. A 3 AM login can be normal for someone who works nights.
- **Blind spots:** AI trained on limited data can misjudge people from different communities, lifestyles, or tech habits.

{{</ collapse >}}

### What is adaptive authentication?
![Three boxes. Low risk, like your usual phone at home, needs a password. Medium risk, like your usual phone on new Wi-Fi at 11 PM, needs a password and a code. High risk, like a new phone in a new city at 3 AM after failed tries, needs a password, Face ID, and a code.](/images/adaptive-authentication-levels.svg)

{{< collapse summary="Click here to reveal the answer." >}}

A login that gets stricter as risk goes up. AI scores each login's risk in real time.

- **Combinations:** one odd factor, like a late time, usually isn't enough. A new device + an odd time + an unfamiliar place is.
- **Response:** the higher the risk, the more proof you need, like a code or Face ID.

{{</ collapse >}}

### Whose logs will you investigate?
Pick one user. Each has a profile, a week of logs, and four login scenarios for your assignment.

{{< collapse summary="Click here for Jordan P.'s logs." >}}

**Profile**

- **Life:** 17, lives in Sacramento, CA, with their aunt and younger sibling. Likes fitness, drawing, and volunteering at an animal shelter. Has never left California and doesn't drive yet.
- **Schedule:** school from 8:30 AM–3:30 PM, and a part-time evening job at a smoothie shop.
- **Devices:** iPhone 14 and a school Chromebook. Logs in only from home or school Wi-Fi, never from public computers.
- **Spending:** Apple Pay or a debit card, usually at local shops and food places. Rarely shops online.
- **Security:** uses Face ID and MFA, but has used the same password on every account for 5+ years.

**Logs**

| When                 | Log      | What happened                                       | Where                         |
|----------------------|----------|-----------------------------------------------------|-------------------------------|
| Sep 10, 6:45 PM      | Purchase | Jamba Juice, $6.85, Apple Pay                       | Sacramento, CA                |
| Sep 10, 7:00 PM      | Location | Wi-Fi ping                                          | Home, Sacramento, CA          |
| Sep 10, 7:43 PM      | Login    | Success, iPhone 14 (iOS, Safari)                    | Sacramento, CA                |
| Sep 11, 7:15 AM      | Location | Wi-Fi ping                                          | School, Sacramento, CA        |
| Sep 11, 7:21 AM      | Login    | Success, Chromebook (ChromeOS, Chrome)              | Sacramento, CA                |
| Sep 11, 12:30 PM     | Purchase | School Cafeteria, $4.00, debit                      | Sacramento, CA                |
| Sep 11, 6:00 PM      | Location | Cell tower ping                                     | Smoothie shop, Sacramento, CA |
| Sep 11, 11:46 PM     | Login    | Success, iPhone 14 (iOS, Safari)                    | Sacramento, CA                |
| Sep 12, 1:00 AM      | Login    | Success, iPhone 14 (iOS, Safari)                    | Sacramento, CA                |
| Sep 12, 3:15 AM      | Purchase | Trendy Apparel, $13.80, debit                       | Online                        |
| Sep 12, 3:40 AM      | Location | No ping                                             | —                             |
| Sep 12, 3:48 AM      | Login    | Failed, "iPhone" (Linux Kernel, unknown browser)    | Reno, NV                      |
| Sep 12, 3:51–4:03 AM | Login    | 4 successes, same "iPhone"                          | Reno, NV                      |
| Sep 12, 3:55 AM      | Location | Wi-Fi ping                                          | Sacramento, CA                |
| Sep 12, 4:00 AM      | Purchase | Khan Academy Premium, $15.00, debit                 | Online                        |
| Sep 12, 4:05 AM      | Login    | Success, iPhone 14 (iOS, Safari)                    | Sacramento, CA                |
| Sep 12, 4:10 AM      | Purchase | Gift Cards Unlimited, $250.00, debit                | Online                        |
| Sep 12, 4:10 AM      | Location | Wi-Fi ping                                          | Reno, NV                      |
| Sep 12, 4:18 AM      | Purchase | Discord Nitro Subscription, $9.99, debit            | Online                        |
| Sep 12, 4:35 AM      | Purchase | AutoZone, $84.76, debit                             | Reno, NV                      |
| Sep 13, 9:10 AM      | Location | Wi-Fi ping                                          | Home, Sacramento, CA          |
| Sep 13, 9:16 AM      | Login    | Success, iPhone 14 (iOS, Safari)                    | Sacramento, CA                |
| Sep 13, 12:15 PM     | Purchase | Local Art Supply Store, $23.50, Apple Pay           | Sacramento, CA                |

**Login scenarios**

1. Jordan logs in at 11:55 PM from their iPhone on café Wi-Fi near the smoothie shop.
2. Jordan logs in at 7:20 AM from their Chromebook on school Wi-Fi.
3. Someone tries to log in at 2:42 AM from a new iPhone in Reno, NV, after 2 failed attempts.
4. Jordan logs in at 6:35 PM from a new Chromebook on school Wi-Fi.

{{</ collapse >}}

{{< collapse summary="Click here for Sana R.'s logs." >}}

**Profile**

- **Life:** 16, a first-generation Lebanese-American in Dearborn, MI, who lives with her parents and three younger siblings. Likes drawing, journaling, cooking with her mom, and helping her siblings with school. Often visits cousins in Windsor, Ontario (Canada).
- **Schedule:** a private Islamic high school, from 7:45 AM–2:30 PM.
- **Devices:** Samsung Galaxy S22 (uses WhatsApp, YouTube, and Chrome) and a school Windows laptop. Logs in from home or school.
- **Spending:** a family debit card that her mom monitors. Shops at halal-certified stores, avoids gambling content and streaming ads, and doesn't eat pork.
- **Security:** uses fingerprint ID, and doesn't sync to the cloud or save passwords in browsers.

**Logs**

| When                 | Log      | What happened                                  | Where                |
|----------------------|----------|------------------------------------------------|----------------------|
| Sep 6, 6:45 PM       | Location | Wi-Fi ping                                     | Home, Dearborn, MI   |
| Sep 6, 6:50 PM       | Login    | Success, Samsung Galaxy S22 (Android, Chrome)  | Dearborn, MI         |
| Sep 6, 6:55 PM       | Purchase | Al Medina Market, $17.32, debit                | Dearborn, MI         |
| Sep 7, 7:25 AM       | Location | Wi-Fi ping                                     | School, Dearborn, MI |
| Sep 7, 7:30 AM       | Login    | Success, Windows laptop (Windows, Edge)        | Dearborn, MI         |
| Sep 7, 12:20 PM      | Purchase | School Cafeteria, $3.50, debit                 | Dearborn, MI         |
| Sep 8, 8:45 PM       | Location | Cell tower ping                                | Windsor, ON (Canada) |
| Sep 8, 9:12 PM       | Login    | Success, Samsung Galaxy S22 (Android, Chrome)  | Windsor, ON          |
| Sep 8, 9:15 PM       | Purchase | HalalCart Canada, $22.10, debit                | Windsor, ON          |
| Sep 9, 3:20 AM       | Location | No ping                                        | —                    |
| Sep 9, 3:22 AM       | Login    | Failed, "iPhone" (iOS, unknown browser)        | Toledo, OH           |
| Sep 9, 3:26–3:34 AM  | Login    | 4 successes, same "iPhone"                     | Toledo, OH           |
| Sep 9, 3:30 AM       | Location | Wi-Fi ping                                     | Toledo, OH           |
| Sep 9, 3:33 AM       | Purchase | Crypto Wallet Setup Fee, $49.99, debit         | Toledo, OH           |
| Sep 9, 3:38 AM       | Purchase | BetZone Sports App, $24.99, debit              | Toledo, OH           |
| Sep 9, 3:40 AM       | Purchase | Grocery Express, $83.45, debit                 | Toledo, OH           |
| Sep 9, 8:10 AM       | Location | Wi-Fi ping                                     | Home, Dearborn, MI   |
| Sep 9, 8:15 AM       | Login    | Success, Samsung Galaxy S22 (Android, Chrome)  | Dearborn, MI         |
| Sep 9, 8:16 AM       | Purchase | Zaytuna Cafe, $6.70, debit                     | Dearborn, MI         |
| Sep 10, 10:00 AM     | Location | Wi-Fi ping                                     | School, Dearborn, MI |
| Sep 10, 10:12 AM     | Login    | Success, Windows laptop (Windows, Edge)        | Dearborn, MI         |
| Sep 10, 10:15 AM     | Purchase | Online Quran Reader, $11.99, debit             | Online               |

**Login scenarios**

1. Sana logs in at 9:10 PM from her Android phone at her cousin's house in Windsor, ON.
2. Sana logs in at 12:45 PM from her school Chromebook on school Wi-Fi.
3. Someone tries to log in at 3:18 AM from a new iPhone in Chicago, IL, after 3 failed attempts.
4. Sana logs in at 6:20 PM from her Android phone on public library Wi-Fi in Dearborn.

{{</ collapse >}}

{{< collapse summary="Click here for Amara T.'s logs." >}}

**Profile**

- **Life:** 17, a bilingual (Spanish and English) Mexican-American in El Paso, TX, who lives with her dad and younger brother. Plays soccer, makes music in GarageBand, and hangs out at the community rec center. Often visits family in Juárez, Mexico.
- **Schedule:** a public high school, plus dual-enrollment classes at a community college.
- **Devices:** iPhone SE, a school Chromebook, and an Xbox Series S. A heavy gamer (FIFA, Fortnite) who's active on Discord, Twitch, and Instagram, and often uses public Wi-Fi at the rec center.
- **Spending:** prepaid Visa gift cards. Buys game credits and skins.
- **Security:** uses fingerprint ID, reuses passwords, and sometimes forgets to log out of shared or public devices.

**Logs**

| When                 | Log      | What happened                                         | Where                   |
|----------------------|----------|-------------------------------------------------------|-------------------------|
| Sep 12, 9:10 PM      | Location | Wi-Fi ping                                            | Home, El Paso, TX       |
| Sep 12, 9:15 PM      | Login    | Success, iPhone SE (iOS, Safari)                      | El Paso, TX             |
| Sep 12, 9:20 PM      | Purchase | Taco Zone, $7.80, Visa gift card                      | El Paso, TX             |
| Sep 13, 10:30 AM     | Location | Wi-Fi ping                                            | School, El Paso, TX     |
| Sep 13, 10:35 AM     | Login    | Success, Chromebook (ChromeOS, Chrome)                | El Paso, TX             |
| Sep 13, 4:45 PM      | Location | Cell tower ping                                       | Rec center, El Paso, TX |
| Sep 13, 4:50 PM      | Login    | Success, iPhone SE (iOS, Safari)                      | El Paso, TX             |
| Sep 13, 5:00 PM      | Purchase | Xbox Game Store, $19.99, Visa gift card               | Online                  |
| Sep 14, 2:00 AM      | Location | No ping                                               | —                       |
| Sep 14, 2:05 AM      | Login    | Failed, Xbox console (Xbox OS, unknown browser)       | Houston, TX             |
| Sep 14, 2:09–2:15 AM | Login    | 3 successes, same Xbox console                        | Houston, TX             |
| Sep 14, 2:10 AM      | Location | Wi-Fi ping                                            | Houston, TX             |
| Sep 14, 2:12 AM      | Purchase | Crypto Mining App Subscription, $59.99, Visa gift card | Houston, TX            |
| Sep 14, 2:16 AM      | Purchase | DarkEdge VPN Pro, $12.49, Visa gift card              | Houston, TX             |
| Sep 14, 2:22 AM      | Location | Wi-Fi ping                                            | Home, El Paso, TX       |
| Sep 14, 2:22 AM      | Login    | Success, iPhone SE (iOS, Safari)                      | El Paso, TX             |
| Sep 14, 7:40 AM      | Location | Wi-Fi ping                                            | School, El Paso, TX     |
| Sep 14, 7:45 AM      | Login    | Success, Chromebook (ChromeOS, Chrome)                | El Paso, TX             |
| Sep 14, 7:47 AM      | Purchase | Coffee Cactus, $4.50, Visa gift card                  | El Paso, TX             |

**Login scenarios**

1. Amara logs in at 9:35 PM from her Xbox on public Wi-Fi at the rec center.
2. Amara logs in at 7:50 AM from her Chromebook on school Wi-Fi.
3. Someone tries to log in at 1:42 AM from a new iPhone in Houston, TX, after multiple failed attempts.
4. Amara logs in at 6:10 PM from her Xbox on hotel Wi-Fi in Juárez, Mexico.

{{</ collapse >}}

{{< collapse summary="Click here for Omar M.'s logs." >}}

**Profile**

- **Life:** 18, a Somali-American in Minneapolis, MN, who lives with his parents and grandmother. Likes henna art, baking, photo editing on his phone, and journaling. Went to Toronto once for a family wedding last summer, but otherwise stays in his neighborhood.
- **Schedule:** a public high school senior who works part-time as a receptionist at a dentist's office.
- **Devices:** a Motorola Android phone, a school Chromebook, and a shared family desktop. Uses Signal and WhatsApp, avoids video calls, clears his history often, and never saves passwords.
- **Spending:** reloadable debit cards. Rarely shops online, and prefers in-person stores for cultural groceries and clothing.
- **Security:** private and cautious: no biometrics, long passcodes, and guards his phone closely.

**Logs**

| When                 | Log      | What happened                                           | Where                   |
|----------------------|----------|---------------------------------------------------------|-------------------------|
| Sep 15, 4:30 PM      | Location | Wi-Fi ping                                              | Home, Minneapolis, MN   |
| Sep 15, 4:40 PM      | Login    | Success, Motorola Android (Android, Firefox Focus)      | Minneapolis, MN         |
| Sep 15, 4:50 PM      | Purchase | Halal Market, $12.60, reloadable debit                  | Minneapolis, MN         |
| Sep 16, 8:00 AM      | Location | Wi-Fi ping                                              | School, Minneapolis, MN |
| Sep 16, 8:10 AM      | Login    | Success, Chromebook (ChromeOS, Chrome)                  | Minneapolis, MN         |
| Sep 16, 12:15 PM     | Purchase | School Cafeteria, $3.75, reloadable debit               | Minneapolis, MN         |
| Sep 17, 8:00 PM      | Location | Wi-Fi ping                                              | Home, Minneapolis, MN   |
| Sep 17, 8:05 PM      | Login    | Success, Motorola Android (Android, Firefox Focus)      | Minneapolis, MN         |
| Sep 17, 8:10 PM      | Purchase | Photo Editor Pro (Upgrade), $4.99, reloadable debit     | Online                  |
| Sep 18, 2:25 AM      | Location | No ping                                                 | —                       |
| Sep 18, 2:28 AM      | Login    | Failed, Windows PC (Windows, Edge)                      | Toronto, ON             |
| Sep 18, 2:34–2:37 AM | Login    | 2 successes, same Windows PC                            | Toronto, ON             |
| Sep 18, 2:35 AM      | Location | Wi-Fi ping                                              | Toronto, ON             |
| Sep 18, 2:36 AM      | Purchase | Proxy IP Rotation Service, $29.00, reloadable debit     | Toronto, ON             |
| Sep 18, 2:40 AM      | Purchase | SecureNotes (Subscription), $6.99, reloadable debit     | Toronto, ON             |
| Sep 18, 2:41 AM      | Location | Wi-Fi ping                                              | Home, Minneapolis, MN   |
| Sep 18, 2:41 AM      | Login    | Success, Motorola Android (Android, Firefox Focus)      | Minneapolis, MN         |
| Sep 18, 8:00 AM      | Location | Wi-Fi ping                                              | School, Minneapolis, MN |
| Sep 18, 8:05 AM      | Login    | Success, Chromebook (ChromeOS, Chrome)                  | Minneapolis, MN         |
| Sep 18, 8:07 AM      | Purchase | Corner Bakery, $5.40, reloadable debit                  | Minneapolis, MN         |

**Login scenarios**

1. Omar logs in at 4:30 PM from his Android phone on mobile data at work.
2. Omar logs in at 8:10 AM from his Chromebook on school Wi-Fi.
3. Someone tries to log in at 2:27 AM from a new Windows laptop in Toronto, ON, after 2 failed attempts.
4. Omar logs in at 6:50 PM from the family desktop on home Wi-Fi.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1: pick the same user as above. Skip the linked documents, and use the logs in the Lesson Overview instead.
2. Level 2: answer a quick check on spotting suspicious activity. Activity is suspicious only if it doesn't fit the user's profile.
3. Level 3: attach your user's logs, and ask the AI to flag suspicious activity. Compare its list with yours.
4. Level 4: attach your user's login scenarios, and ask the AI for each one's risk level and login method, plus a fraud rule. Compare them with your predictions.
5. Level 5: answer a check for understanding about what makes a login risky. Look for combinations of factors.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Investigate Your User's Logs (~15mins)
Find the suspicious activity in your user's logs from the Lesson Overview:

1. Draw a timeline of your user's strangest night, and circle each event that doesn't fit their profile.
2. Next to each circle, write why it's suspicious for this user, and one innocent explanation for it.
3. Write one thing the AI flagged in Level 3 that you missed, or one thing you caught that it missed, and why.

_Tip: Look across all three logs. A login, a location ping, and a purchase at the same time can tell different stories._

### Predict the AI's Risk Levels (~15mins)
Predict how adaptive authentication would handle your user's four login scenarios:

1. Draw a table with columns for Scenario, Risk (Low, Medium, or High), Login (Password, Password + code, or Password + Face ID + code), and Reason. Fill in a row for each scenario.
2. Write a fraud rule an AI could follow: "If [a combination of behaviors], then [flag the login or require more authentication]."
3. Write one way the AI's risk levels or fraud rule in Level 4 differed from yours.

_Tip: For example, "If the login is from a new device in a different city at night, then require Face ID and a code."_

{{% instructions-code-org-update %}}
