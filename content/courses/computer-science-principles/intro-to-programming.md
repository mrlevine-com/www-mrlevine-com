---
title: Intro to Programming
units: [Intro to App Design]
summary: Investigate a series of simple apps to see how programs run one command at a time, and discover the difference between sequential and event-driven programming.
weight: 260
---

{{% param summary %}}

## Today's Objectives
- Define a program as a sequence of commands that are executed or run by a computer.
- Define comments as notes or documentation into a program that do not affect how the program executes.
- Explain the differences between how sequential and event-driven programs execute.

## Lesson Overview
### What is a program?
{{% define "Program Statement" %}}
{{% define "Program" %}}

For example, this program has two program statements:

```js {linenos=table}
console.log("Starting my program!");
console.log("Hi!");
```

### What are comments?
{{< collapse summary="Click here to reveal the answer." >}}

A comment is a note added to a program to explain what it does. Comments don't affect how the program runs; they're just there to help you (or anyone else reading the code) understand it. In App Lab, any line that starts with `//` is a comment:

```js {linenos=table}
// This line is a comment and won't run.
console.log("This line runs.");
```

{{</ collapse >}}

### How do sequential and event-driven programs differ?
There are two ways a program can run:

{{% define "Sequential Programming" %}}
{{% define "Event Driven Programming" %}}

You can make part of a program event-driven by wrapping it in `onEvent()`. Code outside of an `onEvent()` runs right away, while code inside only runs once the event happens, even if it appears earlier in the program:

```js {linenos=table}
console.log("This runs first, right away.");

onEvent("bigButton", "click", function() {
  console.log("This only runs when the button is clicked.");
});
```

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Program Statement" "Program" "Sequential Programming" "Event Driven Programming" %}}

{{% instructions-code-org-update %}}

### Explain Your Code (~10mins)
Find an example of either sequential or event-driven programming from today's Code.org investigation.

1. Record the example code, including any variables it uses.
2. Record your answer: What is the function of this code, and how does it work when it runs?
