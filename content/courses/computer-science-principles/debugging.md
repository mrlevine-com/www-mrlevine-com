---
title: Debugging
units: [Intro to App Design]
summary: Find and fix bugs in real apps, and build the patience and focus it takes to keep going when your code doesn't work the first time.
weight: 270
---

{{% param summary %}}

## Today's Objectives
- Debug simple sequential and event-driven programs.
- Use the debugging process and identify specific best practices for debugging programs.
- Use the speed slider, break points, and documentation as part of the debugging process.

## Lesson Overview
### What is debugging?
{{% define "Debugging" %}}

Your code won't always work the first time, and that's OK. Debugging takes patience, resilience, and focus. You get better at it by doing it.

When something breaks, work through these four steps:

1. **Describe the problem.** What do you expect the code to do? What does it actually do? Does it always happen?
2. **Hunt for bugs.** Are there warnings or errors? What did you change most recently? Look for the code related to the problem, and try explaining it out loud to a classmate.
3. **Try a solution.** Make one small change, then run your code again.
4. **Document as you go.** What have you learned? What strategies did you use? What questions do you still have?

### What are comments and documentation?
{{% define "Comment" %}}
{{% define "Documentation" %}}

For example, lines 1 and 2 below are comments. They explain the code, but the computer skips them:

```js {linenos=table}
// When the user clicks the cat button,
// play a meow sound.
onEvent("catButton", "click", function() {
  playSound("sound://category_animals/cat.mp3");
});
```

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Debugging" "Documentation" "Comment" %}}

{{% instructions-code-org-update %}}

### Log a Bug (~10mins)
Pick one bug you fixed during today's Code.org lesson.

Record your answers to the following questions:

1. What did you expect the code to do, and what did it actually do?
2. How did you find the bug, and how did you fix it?
3. When you felt stuck, what did you do to keep going?
