---
title: "Project: Decision Maker App"
units: ["Variables, Conditionals, and Functions"]
summary: Plan, build, and test an app that helps its user make a decision, then write about your code like you will on the Create PT.
weight: 410
days: 4
---

{{% param summary %}}

## Today's Objectives
- Plan an app's decision-making process with a flowchart and a sketch of its user interface.
- Build an app that uses variables, a conditional statement with a logical operator, and a function that updates the screen to make a decision.
- Write comments that explain the purpose and functionality of each function.
- Test an app with classmates and use their feedback to improve it.
- Explain how a conditional statement and a procedure work in a program.

## Lesson Overview
### What will you build?
**An app that helps its user make a decision**, like what to eat for lunch or which video game to buy. You'll build it from scratch over three days:

| Day | Milestone                         | What you'll do                                                                       |
|-----|-----------------------------------|--------------------------------------------------------------------------------------|
| 1   | **Plan** (Levels 1–2)             | Explore the sample apps, then plan your app in your Unit Journal                     |
| 2   | **Build** (Levels 3–6)            | Build your app in App Lab                                                            |
| 3   | **Test and Finish** (Levels 7–8)  | Test your app with 2 classmates, improve and submit it, then practice the Create PT written response |

Your app must:

1. Use at least one number and one string to make and report a decision with a conditional statement.
2. Use at least one logical operator (`&&`, `||`, or `!`) in that conditional statement.
3. Have at least 3 different possible outputs, like "Yes, you can adopt a cat!", "No, you can't adopt a cat.", and "Congratulations, you can adopt a kitten!"
4. Update the screen with a function that's called at least twice. Every function needs a comment explaining its purpose (what it does) and functionality (how it works).
5. Have a clear, easy-to-navigate user interface and cleanly written code with no errors.

### What does a Decision Maker App look like?
Try the sample app **Where Should I Eat?** in Level 1 on Code.org. Then think about:

1. What does it do, and who would use it?
2. What are its inputs and outputs?
3. What variables does it need?
4. What conditional logic does it need?
5. How could a function be used in it?

{{< collapse summary="Click here to reveal the answers." >}}

1. It recommends a restaurant to someone looking for a place to eat.
2. Inputs: a text box for your name, a dropdown for the type of restaurant, and up and down buttons for how many dollars you want to spend. Outputs: a text box showing the recommendation, and a sound that plays when you use the app.
3. Your name, the type of restaurant, the dollar amount, and the output text.
4. It recommends different restaurants for different types and dollar amounts. For example, if the type is `"Chinese"` **and** the dollars are more than 20, it recommends Din Tai Fung.
5. A function can update the screen every time you change an input.

{{</ collapse >}}

The **Activity Finder** sample app in Level 2 works the same way: it uses the time of day and activity level you choose to recommend an activity.

## Assignment
{{% instructions-unit-journal-update %}}

### Plan Your Decision Maker App (~40mins)
Plan how your app will make its decision before you build it.

1. Brainstorm 3 decisions your app could help with, talk them through with a classmate, and circle the one you'll build.
2. Draw a flowchart of how your app will make that decision:
    - Write your question at the top, like "What kind of fish should I get?"
    - Ask 2 classmates what information they'd need to decide. Draw a box for each piece of information, labeled with its variable name and type, like `waterType` (string) and `tankSize` (number). You need at least one number and one string.
    - Write each Boolean expression in a diamond. Use at least one logical operator: `&&`, `||`, or `!`.
    - Give each diamond exactly 2 arrows: one labeled `true` and one labeled `false`.
    - End each path with a rectangle showing a result. You need at least 3 different results.

    Here's the flowchart from Conditionals Make as an example:

    ![A flowchart. A box labeled day, age, discountCode points to a diamond containing discountCode == "FREEFRIDAY" && day == "Friday". Its true arrow leads to price = 0. Its false arrow leads to a diamond containing day == "Saturday" || day == "Sunday", whose true arrow leads to price = 10. Its false arrow leads to a diamond containing age <= 18, whose true arrow leads to price = 5 and whose false arrow leads to price = 10.](/images/flowchart-museum-tickets.svg)

3. Sketch your app's screen. Draw every button, text box, and image the user will use, and label what each one does. If you use more than one screen, draw arrows showing how they connect.

{{% instructions-code-org-update %}}

Build, test, and submit your app:

1. **Day 2:** Build your app, using your plan and the updateScreen pattern from Functions Make:

    | Level | What to do                                                                                                                      |
    |-------|---------------------------------------------------------------------------------------------------------------------------------|
    | 3     | Recreate your screen sketch in Design Mode.                                                                                     |
    | 4     | Create a variable for each box in your flowchart, and give each one a starting value.                                           |
    | 5     | Declare `updateScreen()`. Inside it, turn your flowchart into an if-else-if statement, and add a comment explaining its purpose and functionality. |
    | 6     | Add an `onEvent()` for each input. Inside each one, update its variable, then call `updateScreen();`.                           |

    _Stuck? Describe what you expected and what actually happened, look for errors and the code you changed most recently, then try one small change at a time._

2. **Day 3:** Watch at least 2 classmates use your app in Level 7, and record what you notice in your Unit Journal. It's OK if your app isn't finished; explain what it will do.

    | Name | What confused them or broke | What they'd improve |
    |------|-----------------------------|---------------------|
    |      |                             |                     |
    |      |                             |                     |

3. **Day 3:** Make at least one improvement from your testing, then submit your app in Level 8 once it meets the rubric:

    - [ ] Your Unit Journal has your decision, flowchart, screen sketch, and testing feedback.
    - [ ] Your app is easy to navigate, it's clear how to use it, and all text is readable.
    - [ ] Your code runs with no warnings or errors, and at least one number and one string are each stored in a variable and used to make the decision.
    - [ ] `updateScreen()` is called at least twice and has a comment that clearly explains its purpose and functionality.
    - [ ] Inside `updateScreen()`, a conditional uses your variables and a logical operator (`&&`, `||`, or `!`) to display at least 3 different responses.

### Practice the Create PT Written Response (~20mins)
Answer these two Create PT practice questions about your app:

> **Question 1:** Your program includes a conditional statement that makes a decision based on certain criteria. Explain how the program determines which block of code to execute. What are the possible outcomes of this conditional statement, and how do they affect the program? (Approx 150 words)

> **Question 2:** Consider a procedure in your program that performs a specific task. Explain how this procedure helps manage the complexity of your program. Describe how using this procedure improves the organization of your code and makes it easier to modify or extend. (Approx 150 words)

A procedure is another name for a function, like `updateScreen()`.

1. Record both questions.
2. Circle each part of each question that you must answer.
3. Answer each question in about 150 words, writing at least one sentence for each part you circled.

_No working app? Write about the Where Should I Eat? sample app in Level 1 as if you built it._
