---
title: "Project: Make a Recommendation Part 1"
units: [Data and Society, Solving Data Problems]
summary: Survey your classmates with a partner, turn their answers into a recommendation algorithm, test it, get peer feedback, then present your work to the class.
weight: 250
days: 2
---

{{% param summary %}}

## Today's Objectives
- Apply the data problem solving process to a personally relevant topic.
- Determine appropriate sources of data needed to solve a problem.

## Lesson Overview
### What will you do in this project?
In this unit, you've seen how data can be used to solve all kinds of problems. Now it's your turn to use data to help someone by making a recommendation to a classmate. You will:

1. Work with a partner.
2. Define a problem that a recommendation could solve.
3. Identify the data you need and create a survey to collect it.
4. Interpret the data to find relationships between survey answers.
5. Create an algorithm that makes a recommendation based on the data.
6. Test your algorithm.
7. Present your work to your classmates.

### Where should your algorithm's rules come from?
{{< collapse summary="Click here to reveal the answer." >}}

Your rules should come from the survey data you collect and interpret, **not** from what you already believe about the world.

For example, you might assume that people who love ice cream want to go to the beach. If your survey shows that most ice cream fans picked the amusement park, your rule should add points to the amusement park.

{{</ collapse >}}

### What if your idea is too big?
{{< collapse summary="Click here to reveal the answer." >}}

Don't throw your idea away. Shrink it instead:

| Step     | What it looks like                                 |
|----------|----------------------------------------------------|
| **Run**  | Your full idea.                                    |
| **Walk** | A smaller version you can finish in this project. |
| **Crawl** | An even smaller version, if "Walk" is still too big. |

For example, "Recommend any movie ever made" could shrink to "Recommend one of four movies playing this weekend."

{{</ collapse >}}

### How will your project be graded?
| Criteria             | Full credit looks like                                                                                                                                                      |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Defining the Problem | Your problem is well-defined, including a question that your recommender will answer. Every step of your process clearly and consistently relates back to the problem. |
| Data Analysis        | You analyze your data using cross tabulation, and you draw at least five relevant conclusions from each relationship between the types of data.                          |
| Your Algorithm       | Your algorithm includes at least five rules that clearly and consistently relate back to the results and conclusions from your cross tabulation.                         |
| Data                 | You clearly identify at least four types of data to collect, you design a survey to collect it, and you justify your data collection choices in your presentation.       |
| Feedback             | You test your algorithm at least three times, consider all feedback from your users, and explain why the feedback should or should not change your algorithm.            |

## Assignment
{{% instructions-unit-journal-update %}}

### Day 1: Warm Up (~5mins)
Record a list of as many problems from this unit as you can remember that involved making a recommendation. For example, you used survey data to decide what pizza to order.

### Day 1: Look at a Sample Recommender (~10mins)
In [Automating Data Decisions]({{< relref "automating-data-decisions.md" >}}), you built an algorithm that recommends a vacation spot. It asked three questions:

- What is your favorite food?
- Which is the best superpower?
- Which animal do you like the best?

Record your answers to the following questions about that recommender:

1. What choice does it help the user make?
2. What data does it use to make that recommendation?
3. How do you think its creators decided on the algorithm they used to make the choice?

### Day 1: Step 1 - Define Your Problem (~5mins)
With your partner, decide what problem your recommender will solve. Record:

1. The question your recommender will answer for the user (e.g. "Where should you go on vacation?").
2. The four possible recommendations it will choose from.

### Day 1: Step 2 - Decide What Data You Need (~10mins)
The vacation recommender used data about a user's food, superpower, and animal preferences. Decide what data would help you make your recommendation, and record it in a table like this:

| Type of Data (the kind of information you want to collect) | Possible Questions and Answers (what you might put in a survey) |
|------------------------------------------------------------|-----------------------------------------------------------------|
|                                                            |                                                                 |
|                                                            |                                                                 |
|                                                            |                                                                 |

### Day 1: Step 3 - Create Your Survey (~10mins)
Use the data from Step 2 to record your survey:

1. Three questions, each with four answer choices.
2. One **preference question** that asks which of your four recommendations the person likes best, with those four recommendations as the answer choices.

You need the preference question to figure out how the answers to your first three questions relate to what you want to recommend.

Before tomorrow, you may start collecting survey data from people outside of class.

### Day 2: Step 4 - Collect Your Survey Data (~20mins)
Give your survey to at least 20 different people. Record their answers in a table like this:

| #   | Answer 1 | Answer 2 | Answer 3 | Preference |
|-----|----------|----------|----------|------------|
| 1   |          |          |          |            |
| 2   |          |          |          |            |
| ... |          |          |          |            |
| 20  |          |          |          |            |

### Day 2: Step 5 - Interpret Your Data (~15mins)
Use cross tabulation to find out how the answers to each of your three questions relate to the preference you want to recommend.

1. Record one cross tabulation table for each question. Put the answer choices down the side and the four recommendations across the top.
2. Fill in each table by counting how many people chose each combination.
3. Under each table, record the relationships that could help you make a rule.

For example, a table for the vacation recommender's food question could look like this:

|            | Beach | Amusement Park | Big City | National Park |
|------------|-------|----------------|----------|---------------|
| Ice Cream  | 5     | 2              | 1        | 0             |
| Pizza      | 1     | 2              | 2        | 1             |
| Salad      | 0     | 0              | 1        | 5             |
| Sandwiches | 2     | 0              | 0        | 3             |

One relationship: most people who like salad prefer the national park.

### Day 2: Step 6 - Define Your Algorithm (~10mins)
Use the relationships from Step 5 to create your algorithm. For each answer choice to each question, record instructions for adding points to one or more recommendations, like this:

| Question   | Answer    | Instructions                                            |
|------------|-----------|---------------------------------------------------------|
| Question 1 | Ice Cream | Add 2 points to beach. Add 1 point to amusement park. |
| Question 1 |           |                                                         |
| ...        |           |                                                         |

Remember: base your rules on your survey data, not on what you believe to be true.

### Day 3: Step 7 - Try Out Your Algorithm (~15mins)
Test your algorithm on three classmates who did **not** take your original survey. For each classmate:

1. Record their answers to your three questions.
2. Use your rules to tally the points for each recommendation in a table like this:
    | Recommendation |   |   |   |   |
    |----------------|---|---|---|---|
    | **Points**     |   |   |   |   |
3. Record which recommendation your algorithm makes. If two recommendations tie, record the tie instead of picking a winner yourself.

Then record your answers to the following questions:

- Did your users agree with the recommendations you made? Explain.
- Are there any changes you think you should make to your algorithm?

### Day 3: Step 8 - Peer Review (~20mins)
Trade projects with another team and review each other's work. The goal is to come up with new ideas for improving your recommendation.

1. Before you trade, record one thing you want feedback on.
2. As the other team reviews your project, record their feedback in a table like this:
    | Types of Evidence | Evidence I Found | Ideas for More |
    |-------------------|------------------|----------------|
    | The problem is well-defined, including a question that the recommender will answer. Steps of the process clearly relate back to the problem. | | |
    | The data is analyzed using the cross tabulation tables, and at least five relevant conclusions are drawn from each relationship between the types of data. | | |
    | The algorithm includes at least five rules that clearly relate back to the results and conclusions drawn from the cross tabulation tables. | | |
    | At least four types of data to be collected are clearly identified, a survey is designed to collect the needed data, and choices around the data collection process are explained in the presentation. | | |
    | The algorithm is tested at least three times, and any feedback from the users is taken into consideration, with an explanation of why it should or should not result in changes to the algorithm. | | |
3. Record the other team's answers to these sentence starters:
    - I like...
    - I wish...
    - What if...

{{< collapse summary="Click here for an example of good feedback." >}}

For a project that recommends a trip:

| Evidence I Found | Ideas for More |
|------------------|----------------|
| One conclusion is found for each survey question, which is useful. | More conclusions can be drawn from the survey results to help decide the recommendation. |
| Rules are found for what should happen for each answer. | The rules don't always follow the conclusions. More conclusions would help your rules. |

- **I like** the questions you asked. They are really fun, so people will like taking the quiz.
- **I wish** there were more conclusions drawn from the data. That could help your rules.
- **What if** you went back to your tables to find more conclusions, then changed your rules based on what you found?

{{</ collapse >}}

### Day 3: Creator's Reflection (~10mins)
Look over the feedback you received and record your answers to the following questions:

1. What piece of feedback was most helpful to you? Why?
2. What piece of feedback surprised you the most? Why?
3. Based on the feedback, what changes will you make to your project?

Then make those changes to your project.

### Day 4: Step 9 - Finalize Your Project (~40mins)
1. Based on your peer feedback, make any changes you need to how you defined your problem, the data you collect, or how you analyze it.
2. Check your project against the rubric in the Lesson Overview.
3. Create a presentation of your project, such as slides, a poster, or a paper. You can find everything you need in your Unit Journal. Your presentation must include:
    - What choice you are helping the user make.
    - The types of data you collect to help the user make that choice.
    - The relationships you found when interpreting your survey data.
    - How you used those relationships to create your recommendation algorithm.
    - The results of testing your algorithm on users.

### Day 5: Present Your Project (~30mins)
Present your project to the class with your partner.

### Day 5: Reflect on Your Growth (~5mins)
Record a table like this. For each practice, describe how you've grown and how you want to grow:

| How I've Grown | Practice        | How I Want to Grow |
|----------------|-----------------|--------------------|
|                | Problem Solving |                    |
|                | Persistence     |                    |
|                | Creativity      |                    |
|                | Collaboration   |                    |
|                | Communication   |                    |

{{% unit-journal-question-of-the-day question="How can I use data to make my own recommendations?" %}}

## Upcoming Quiz
To prepare for your upcoming quiz, look over your Unit Journal and make sure you can explain each of these terms:

- **Raw data**, **cleaning data**, and **irrelevant data** from [Structuring Data]({{< relref "structuring-data.md" >}})
- **Cross tabulation** from [Interpreting Data]({{< relref "interpreting-data.md" >}})
- **Algorithm** from [Automating Data Decisions]({{< relref "automating-data-decisions.md" >}})
