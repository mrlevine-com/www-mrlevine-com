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
**An app that helps its user make a decision**, like what to eat for lunch or which video game to buy. You'll build it from scratch over three days by following the 12 steps in this lesson's assignment. Code.org calls these steps the Planning Guide, so when a level says something like "Step 4 in the Planning Guide," look at Step 4 in your Unit Journal.

| Day | Milestone           | Code.org Levels | Steps                | What you'll do                                                                 |
|-----|---------------------|-----------------|----------------------|--------------------------------------------------------------------------------|
| 1   | **Plan**            | 1–2             | 1–6                  | Explore the sample apps, then plan your app in your Unit Journal               |
| 2   | **Build**           | 3–6             | 7                    | Build your app in App Lab                                                      |
| 3   | **Test and Finish** | 7–8             | 8–12                 | Test, improve, record, and submit your app, then practice the Create PT written response |

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
Complete Steps 1–6 to plan how your app will make its decision. Label each step with its number, like "Step 4", because Code.org's levels tell you to look back at them.

1. Choose your app's decision:
    - **Step 1: Brainstorm App Ideas.** Write 3 decisions your app could help a classmate make. They can be small or big, like what to eat for lunch or where to apply for a job.
    - **Step 2: Choose One Idea.** Talk through your ideas with a classmate, then circle the one you're most interested in.
    - **Step 3: Survey Your Classmates.** Talk with 2 classmates about your decision for a couple of minutes, then fill in this table:

      | Name | What information is needed to make this decision? |
      |------|---------------------------------------------------|
      |      |                                                   |
      |      |                                                   |

2. Plan your app's logic:
    - **Step 4: Storing Information.** Fill in this table with a variable for each piece of information from Step 3. You need at least one number and one string.

      | Name    | Information Stored  | Type (string, number, or Boolean) |
      |---------|---------------------|-----------------------------------|
      | `age`   | The age of the user | number                            |
      |         |                     |                                   |

    - **Step 5: Flowchart.** Draw a flowchart of how your app will make its decision:
        - Write your question at the top, like "What kind of fish should I get?"
        - Draw a small rectangle listing your variables from Step 4.
        - Write each Boolean expression in a diamond. Use at least one logical operator: `&&`, `||`, or `!`.
        - Give each diamond exactly 2 arrows: one labeled `true` and one labeled `false`. Use plain arrows to connect steps that don't involve a decision.
        - End each path with a rectangle showing a result. You need at least 3 different results.

      Here's the flowchart from Conditionals Make as an example:

      ![A flowchart. A box labeled day, age, discountCode points to a diamond containing discountCode == "FREEFRIDAY" && day == "Friday". Its true arrow leads to price = 0. Its false arrow leads to a diamond containing day == "Saturday" || day == "Sunday", whose true arrow leads to price = 10. Its false arrow leads to a diamond containing age <= 18, whose true arrow leads to price = 5 and whose false arrow leads to price = 10.](/images/flowchart-museum-tickets.svg)

3. **Step 6: Design User Interface.** Sketch your app's screen. Draw every button, text box, and image the user will use, and label what each one does. You can use 1 screen or more; if you use more, draw arrows showing how they connect.

{{% instructions-code-org-update %}}

Complete Steps 7–11 to build, test, and submit your app:

1. **Step 7: Start Building Your App (Day 2).** Build your app, using your plan and the updateScreen pattern from Functions Make. It's OK to change your design as you go.

    | Level | What to do                                                                                                                      |
    |-------|---------------------------------------------------------------------------------------------------------------------------------|
    | 3     | Recreate your Step 6 sketch in Design Mode.                                                                                     |
    | 4     | Create a variable for each row of your Step 4 table, and give each one a starting value.                                        |
    | 5     | Declare `updateScreen()`. Inside it, turn your Step 5 flowchart into an if-else-if statement, and add a comment explaining its purpose (what it does) and functionality (how it works). |
    | 6     | Add an `onEvent()` for each input. Inside each one, update its variable, then call `updateScreen();`.                           |

    _Stuck? Describe what you expected and what actually happened, look for errors and the code you changed most recently, then try one small change at a time._

2. Test your app (Day 3):
    - **Step 8: Testing.** Watch at least 2 classmates use your app in Level 7, then ask what they'd improve. Fill in this table. It's OK if your app isn't finished; explain what it will do.

      | Name | Things that could be improved based on watching them use the app | Improvements this person recommends |
      |------|------------------------------------------------------------------|-------------------------------------|
      |      |                                                                  |                                     |
      |      |                                                                  |                                     |

    - **Step 9: Pick Improvements.** Write at least one improvement you'll make based on your Step 8 feedback. A second improvement is optional.

3. Finish and submit your app (Day 3):
    - **Step 10: Complete Your App.** Make your Step 9 improvements, then check that your app meets each item on this checklist:
        - [ ] Your Unit Journal has Steps 1–9 completed.
        - [ ] Your app is easy to navigate, it's clear how to use it, and all text is readable.
        - [ ] Your code runs with no warnings or errors, and at least one number and one string are each stored in a variable and used to make the decision.
        - [ ] `updateScreen()` is called at least twice and has a comment that clearly explains its purpose and functionality.
        - [ ] Inside `updateScreen()`, a conditional uses your variables and a logical operator (`&&`, `||`, or `!`) to display at least 3 different responses.
    - **Step 11: Record Video.** Screen-record your app running, showing its input, at least one thing it does, and its output. Keep it under 1 minute, with no voice narration. On Windows:
        1. Run your app in Code.org.
        2. Press <kbd>Windows</kbd> + <kbd>Shift</kbd> + <kbd>R</kbd>, then drag a box around your app.
        3. Make sure the microphone button is off, then click **Start**.
        4. Use your app, then click the red **Stop** button. Your video saves automatically to your **Videos > Screen Recordings** folder.
    - Submit your app in Level 8.

### Practice the Create PT Written Response (~20mins)
Complete Step 12 by answering these two Create PT practice questions about your app:

> **Question 1:** Your program includes a conditional statement that makes a decision based on certain criteria. Explain how the program determines which block of code to execute. What are the possible outcomes of this conditional statement, and how do they affect the program? (Approx 150 words)

> **Question 2:** Consider a procedure in your program that performs a specific task. Explain how this procedure helps manage the complexity of your program. Describe how using this procedure improves the organization of your code and makes it easier to modify or extend. (Approx 150 words)

A procedure is another name for a function, like `updateScreen()`.

1. Record both questions.
2. Circle each part of each question that you must answer.
3. Answer each question in about 150 words, writing at least one sentence for each part you circled.

_No working app? Write about the Where Should I Eat? sample app in Level 1 as if you built it._
