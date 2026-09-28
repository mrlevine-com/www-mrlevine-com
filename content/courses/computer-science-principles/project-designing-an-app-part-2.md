---
title: "Project: Designing an App Part 2"
units: [Intro to App Design]
summary: Program your app with a partner using pair programming, test it with classmates to collect feedback, then submit it and practice writing about it for the AP Create performance task.
weight: 280
days: 2
---

{{% param summary %}}

## Today's Objectives
- Create the code and user interface of an app based on a program specification.
- Effectively use pair programming while designing the features of an app.
- Iteratively improve an app based on feedback.
- Provide effective feedback on the functionality or usability of an app.
- Reflect on the value of different stages of a development process in creating an app.
- Test an app's functionality by attempting to use features and behavior described in a program specification.

## Lesson Overview
### What makes a good partner?
{{< collapse summary="Click here to reveal the answer." >}}

A good partner:

- Listens.
- Contributes.
- Shares the work evenly.

{{</ collapse >}}

### What is pair programming?
{{% define "Pair Programming" %}}

When you pair program, you and your partner share one computer and take turns in two roles:

| Role          | What you do                                               |
|---------------|-----------------------------------------------------------|
| **Driver**    | Control the keyboard and the mouse.                       |
| **Navigator** | Keep track of the big picture and guide toward the goal. |

You will swap roles every 3 minutes. The partner sitting on the left starts as the driver.

### How does pair programming help, especially with debugging?
{{< collapse summary="Click here to reveal the answer." >}}

- Talking through your code with another person helps you figure out what to do.
- When you get stuck, someone is there to help brainstorm a solution.
- Two sets of eyes find more bugs than one.
- Different partners bring different perspectives to a project.

{{</ collapse >}}

### What makes feedback good or bad?
{{< collapse summary="Click here to reveal the answer." >}}

Good feedback:

- Gives specific information beyond "it's great."
- Explains why something needs work.

Bad feedback:

- Is overly negative without being constructive.
- Does not go into enough detail.

{{</ collapse >}}

### Why get feedback before your app is finished?
{{< collapse summary="Click here to reveal the answer." >}}

- Another person may find a bug you have been overlooking.
- Something that seems obvious to you may not be obvious to your users.
- Even if your app isn't finished, feedback can help guide your next steps.

Feedback and testing make sure your app actually works the way you designed it, and they help you make gradual improvements.

{{</ collapse >}}

### What is a development process?
{{% define "Development Process" %}}

Over this project, you and your partner go through a full development process: you investigate your users, design a prototype, build your app, and test it with classmates. On Day 5, you finish the process by making your final improvements and writing about your work.

### How will your project be graded?
| Criteria                   | Full credit looks like                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------|
| User Interface Screens     | Your user interface includes at least three screens.                                                  |
| User Interface Navigation  | Users can easily navigate between all screens.                                                        |
| User Interface Elements    | Your app includes at least one example each of text, images, and audio.                              |
| Code                       | Your code runs without errors.                                                                        |
| Element IDs                | Every screen element uses a meaningful ID.                                                            |
| App Topic                  | Your topic is clearly communicated and explained.                                                     |
| Unit Journal               | Your project work in your Unit Journal is fully completed.                                            |
| Written Response 1         | Your response accurately describes the purpose, functionality, and inputs and outputs of your app.   |
| Written Response 2         | Your response fully describes an idea or recommendation from your partner or a classmate, and how it improved your app. |

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Pair Programming" "Development Process" %}}

{{% instructions-code-org-update %}}

### Day 3: List Your Event Handlers (~10mins)
Look at the specification you sketched in your Unit Journal. Record a table listing every event handler your app needs, like this:

| Element ID    | Action    | What happens?                                                          |
|---------------|-----------|------------------------------------------------------------------------|
| `"dogButton"` | `"click"` | A picture of a dog appears. The background of the screen turns green. |
|               |           |                                                                        |
|               |           |                                                                        |

Each row becomes one `onEvent` block in your code. For example, the row above could become:

```js {linenos=table}
onEvent("dogButton", "click", function() {
  showElement("dogImage");
  setProperty("homeScreen", "background-color", "green");
});
```

### Day 3: Pair Program Your App (~25mins)
Complete Level 1 ("Add Code") on Code.org with your partner, using pair programming:

1. The partner on the left starts as the driver. The partner on the right starts as the navigator.
2. Add one event handler from your table at a time, then run your app to test it.
3. Swap roles every 3 minutes.

When something breaks, use the debugging process from the previous lesson, and record each bug you find and how you fixed it.

### Day 4: Keep Pair Programming (~20mins)
Complete Level 2 ("Add More Code") on Code.org with your partner, still swapping driver and navigator every 3 minutes.

### Day 4: Test and Get Feedback (~10mins)
Pair up with another group, called **Group B** here. It's OK if your app isn't finished yet.

1. Let Group B use your app. Watch them, and record anything that could be improved.
2. Ask Group B what specific improvements they recommend, and record them.
3. Swap: test Group B's app while they watch you.
4. Pair up with a new group and repeat steps 1 to 3.

Record your feedback in a table like this:

| Name | Things that could be improved based on watching them use the app | Improvements this person recommends |
|------|--------------------------------------------------------------------|-------------------------------------|
|      |                                                                    |                                     |
|      |                                                                    |                                     |

### Day 4: Pick Improvements (~5mins)
Return to your partner. Using the feedback you collected, record at least one improvement you plan to make to your app. A second improvement is optional.

### Day 4: Create PT Practice: Development Process (~10mins)
1. Record the following prompt:
    > Describe the process you used to develop your program. Include any goals that you set, challenges or setbacks that you encountered, and solutions that worked for your team.
2. Circle any keywords or ideas that describe what you must write about.
3. Record a response that addresses all of the keywords you identified.
4. Record a brief reflection on where you had trouble, what questions you still have, and what you did well.

### Day 5: Finish and Submit Your App (~30mins)
Complete Level 3 ("Submit Your App") on Code.org:

1. With your partner, make the improvements you picked on Day 4.
2. Check your app against the rubric in the Lesson Overview.
3. Click "Submit" to turn in your app.

### Day 5: Create PT Practice: Written Response 1 (~5mins)
Record a response of about 150 words that describes:

- The overall purpose of your program.
- The functionality of your app.
- The inputs and outputs of your app.

{{< collapse summary="Click here for sentence starters." >}}

You may use or change any of these sentence starters:

- The overall purpose of my program is to ___.
- The app functions by ___.
- My app includes key features like ___.
- The app allows users to ___ by ___.
- It takes ___ as input and provides ___ as output.

{{</ collapse >}}

### Day 5: Create PT Practice: Written Response 2 (~5mins)
Your project used a development process that included your partner's ideas and your classmates' feedback. Record a response of about 150 words that describes one part of your app that was improved by input from your partner **or** a classmate. Include:

- Who specifically gave the idea or recommendation.
- What their idea or recommendation was.
- The specific change you made to your app's user interface or functionality in response.
- How you believe this change improved your app for your expected users.

{{< collapse summary="Click here for sentence starters." >}}

You may use or change any of these sentence starters:

- One part of my app that was improved through feedback came from my partner, ___.
- They recommended that I ___ to enhance the ___ of the app.
- In response, I made a specific change to the app's [user interface/functionality] by ___.
- I believe this change improved the app for my expected users because ___.

{{</ collapse >}}

For example, a classmate might recommend adding sound effects, improving navigation, or changing the design. Your change might make your app more engaging, easier to use, more interactive, or more accessible.
