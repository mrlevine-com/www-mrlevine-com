---
title: Automating Data Decisions
units: [Data and Society, Solving Data Problems]
summary: Design an algorithm that recommends a vacation spot, then test it on your classmates.
weight: 220
---

{{% param summary %}}

## Today's Objectives
- Design and implement an algorithm for making decisions using data as inputs.
- Explain the benefits and drawbacks of using computers for automated decision making.
- Interpret collected data to identify patterns.

## Lesson Overview
### What is today's scenario?
You're going to create an algorithm that will help your classmates choose a good vacation spot based on data collected about their preferences. You can suggest the beach, an amusement park, a national park, or a big city. After you create your algorithm, you'll try it out on two of your classmates.

### What does a computer need in order to make a decision?
{{< collapse summary="Click here to reveal the answer." >}}

For a computer to make a decision, it needs data as input and an algorithm to process that data. This is the same input, output, store, and process model you've already learned about.

Imagine you programmed a computer to pick out your clothes every morning. It would need input, like the temperature, the weather, and what events you have that day. It would also need rules to process that input, like "if the temperature is less than 60 degrees, pick out a jacket" or "if it's sunny, pick out sunglasses." Without both the data and the rules, the computer has nothing to decide with.

{{</ collapse >}}

### Why does a computer need you to write the rules?
{{< collapse summary="Click here to reveal the answer." >}}

A computer doesn't know what "the beach" or "the big city" is, and it doesn't have an opinion of its own. All it can see is which answer someone chose, not what that answer means. It needs a person to tell it how to turn those answer choices into a recommendation.

That's what makes today's work an algorithm: you're writing the exact steps that turn someone's answers into a decision, so the computer can make that decision automatically.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Survey Results
Someone gave a survey and put the results in the cross tabulation tables below. Use this information to decide what rules you want for your algorithm. A dash means nobody chose that combination.

**Vacation and Food**

| | Beach | Amusement Park | Big City | National Park |
|---|---|---|---|---|
| Ice Cream | 5 | 2 | 1 | - |
| Pizza | 1 | 2 | 2 | 1 |
| Salad | - | - | 1 | 5 |
| Sandwiches | 2 | - | - | 3 |

**Vacation and Superpower**

| | Beach | Amusement Park | Big City | National Park |
|---|---|---|---|---|
| Flying | 3 | 1 | - | 4 |
| Invisibility | - | - | 3 | 3 |
| Super Strength | - | 1 | - | 2 |
| Teleport | 5 | 2 | 1 | - |

**Vacation and Animal**

| | Beach | Amusement Park | Big City | National Park |
|---|---|---|---|---|
| Wolf | 2 | 1 | - | 3 |
| Whale | 2 | - | - | 2 |
| Mouse | - | 3 | 2 | - |
| Dog | 4 | - | 2 | 4 |

### Your Algorithm
Your algorithm will use the answers that a user gives to assign points to different types of vacation. For each possible answer to a question, you decide how many points each location gets. The location with the most points after all three questions is where your user should go on vacation.

The first rule has been written for you:

| Answer | Instructions |
|---|---|
| Ice cream | Add 2 points to beach. Add 1 point to amusement park. |

First, record your answers to the following questions:
- Based on what you see in the cross tabulation tables, why do you think someone created this as the first rule of the algorithm?
- Can you think of a different rule that would also fit the data?

Then write the rest of your rules. For each possible answer choice, add points to at least one of the four options of beach, amusement park, national park, or big city. You can change the first rule if you disagree with it.

Record your completed rules:

**What is your favorite food?**

| Answer | Instructions |
|---|---|
| Ice cream | Add 2 points to beach. Add 1 point to amusement park. |
| Pizza | |
| Salad | |
| Sandwiches | |

**Which is the best superpower?**

| Answer | Instructions |
|---|---|
| Flying | |
| Invisibility | |
| Super Strength | |
| Teleport | |

**Which animal do you like the best?**

| Answer | Instructions |
|---|---|
| Wolf | |
| Whale | |
| Mouse | |
| Dog | |

### Test Your Algorithm
Ask two of your classmates the three questions from the survey and record their answers. Then use your rules to add up their points and find the vacation spot your algorithm recommends.

**Classmate 1**

- Favorite food:
- Best superpower:
- Favorite animal:

| Beach Points | Amusement Park Points | National Park Points | Big City Points |
|---|---|---|---|
| | | | |

Recommended spot:

**Classmate 2**

- Favorite food:
- Best superpower:
- Favorite animal:

| Beach Points | Amusement Park Points | National Park Points | Big City Points |
|---|---|---|---|
| | | | |

Recommended spot:

If two locations tie, record the tie instead of picking a winner yourself. A tie is a real result of your algorithm, and it tells you something about your rules.

### Reflect
Record your answers to the following questions:
- Did you agree with the suggestions that your algorithm made? Why or why not?
- How could you improve this algorithm so that it could make better recommendations?
- What is a disadvantage of a computer making a decision automatically?
- What's a type of decision that you would not want a computer to make automatically? Why?
- What's a type of decision you would want a computer to make automatically? Why?

{{% unit-journal-question-of-the-day question="How can computers help us make decisions about data?" %}}
