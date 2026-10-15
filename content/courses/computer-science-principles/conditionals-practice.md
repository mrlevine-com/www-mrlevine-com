---
title: Conditionals Practice
units: ["Variables, Conditionals, and Functions"]
summary: Use conditionals to build a real-world app one milestone at a time, and debug your code when it doesn't work.
weight: 360
---

{{% param summary %}}

## Today's Objectives
- Debug programs that use boolean expressions and conditional statements.
- Write programs that use boolean expressions and conditional statements with the support of sample code.

## Lesson Overview
### How do you build an app today?
You pick one of three apps (MindEase, VeloCity, or Tix Finder) and finish it one milestone at a time. The apps are already designed. Your job is to add the conditionals that make them work.

Apps are built in three layers:

1. **User story**: what someone using the app needs, in their words. For example, "I would like to be able to save my favorite items."
2. **Milestone**: one feature that meets that need. For example, "Create the ability to save favorite items."
3. **Tasks**: the steps to build that feature. For example, "Make a favorite button," then "Save data into a variable when the user clicks it."

Each level is one milestone. Work through every level the same way:

1. **Read the user story.** Click the green "Analyzing User Stories" bar to open it.
2. **Complete the tasks.** Each level has 1 to 3. Click any task with a triangle (▶) to reveal more instructions and hints.
3. **Test your code.** Run the level's tests to check that your code works.

Try one. A task says: "For users who rated their happiness higher than a `5`, assign the variable `happinessLevel` a value of `"High"`. For others, assign `happinessLevel` a value of `"Low"`." Say `rating` holds the user's rating. Write the code.

{{< collapse summary="Click here to reveal the answer." >}}

```js {linenos=table}
if (rating > 5) {
  happinessLevel = "High";
} else {
  happinessLevel = "Low";
}
```

"Higher than" means `>`, not `>=`, so a rating of exactly `5` is `"Low"`.

{{</ collapse >}}

### How do you debug a conditional?
Find out whether it ran, then find out why. Use these strategies:

- **Trace**: Read your code in the order the computer runs it, evaluating each Boolean expression to `true` or `false`.
- **`console.log(...)`**: Put one inside an if statement. If it never prints, that code never ran.
- **Change starting values**: Set a variable to the value you want to test. For example, start `score` at `99` to test what happens at `100`.
- **Comment out code**: Turn off a section. If the bug goes away, it's in that section.

Change one small thing at a time, then test again. Big random changes add new bugs.

Riders get a discount if they're under 18 OR over 65. This code prints `10` for a 70-year-old instead of `5`. Find the bug.

```js {linenos=table}
var age = 70;
var price = 10;

if (age < 18 && age > 65) {
  price = 5;
}
console.log(price);
```

{{< collapse summary="Click here to reveal the answer." >}}

Line 4 uses `&&` instead of `||`:

1. `70 < 18 && 70 > 65` becomes `false && true`, which is `false`, so line 5 never runs.
2. No age is both under 18 and over 65, so no one ever gets the discount.

Fix line 4:

```js {linenos=table}
if (age < 18 || age > 65) {
```

{{</ collapse >}}

### Can you trace these conditionals?
These are like the questions at the end of today's Code.org lesson.

An if statement can go inside another one. The inner one only runs if the outer one sends the computer there.

1. What does this code print?

    ```js {linenos=table}
    var score = 4;
    var lives = 3;

    if (lives == 0) {
      console.log("You Lose!");
    } else {
      if (score >= 5 && lives == 3) {
        console.log("Perfect Game!");
      } else {
        console.log("You Win!");
      }
    }
    ```

2. `number` holds a number the user typed. What number makes this code print `COLD`?

    ```js {linenos=table}
    if (number >= 10) {
      if (number <= 20) {
        console.log("MEDIUM");
      } else {
        console.log("HOT");
      }
    } else {
      console.log("COLD");
    }
    ```

{{< collapse summary="Click here to reveal the answers." >}}

1. `You Win!`:
    1. `3 == 0` is `false`, so skip to line 7.
    2. `4 >= 5 && 3 == 3` becomes `false && true`, which is `false`.
    3. So line 10 runs.
2. Any number less than `10`, like `5`. Line 1 is `false`, so the computer skips to line 8.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}

_Tip: Pick one app and choose that **same** app at every choice level. Each level you finish completes one milestone of your app._

{{% instructions-unit-journal-update %}}

### Explain a Logical Operator (~10mins)
Explain what a logical operator does in your code, like you will on the AP Create Performance Task.

1. Paste a screenshot of code from today's Code.org lesson that uses `&&` or `||`.
2. Circle each logical operator, and write `true` or `false` above each side of it for one test value.
3. Answer in 2–3 sentences: "How would the outcome of this code segment differ if the logical operations were reversed (AND changed to OR and vice versa)?"

    _(Hint: In the first trace question above, changing `&&` to `||` makes `false || true`, which is `true`, so it prints `Perfect Game!` instead of `You Win!`.)_

### Log a Bug (~10mins)
Pick one bug you found during today's Code.org lesson.

1. Sketch what you expected the app to show next to what it actually showed. Note whether it always happened.
2. Write what caused the bug and how you found it.
3. Write what you changed to fix it.
