---
title: Conditionals Investigate
units: ["Variables, Conditionals, and Functions"]
summary: Conditional statements let apps make decisions, like ending a game when you run out of lives.
weight: 350
---

{{% param summary %}}

## Today's Objectives
- Explain the purpose of those programming patterns with boolean expressions and conditional statements both in terms of how they work and what they accomplish.
- Identify common programming patterns using boolean expressions and conditional statements.
- Modify apps that make use of common programming patterns with boolean expressions and conditional statements to adjust their functionality.

## Lesson Overview
### What's the difference between "when" and "if"?
"When" means the app responds to an event. "If" means the app checks a Boolean expression.

- **"when"**: There's an `onEvent` to respond to user input. The app does something "when" you click.
- **"if"**: There's a conditional statement that decides what code to run. The app does something "if" a Boolean expression evaluates to `true`.

For example, "when" you click a button, the app decides "if" the temperature can change.

### What is an if statement?
{{< video title="CSP: Conditionals pt 2A - if statements" src="/videos/if-statements.mp4" poster="/images/video-poster-if-statements.jpg" >}}

{{% define "Conditional Statement" %}}

The simplest one is an if statement. It runs code only if its Boolean expression is `true`:

```js {linenos=table}
if (age >= 13) {
  console.log("You can see a PG-13 movie alone.");
}
console.log("Done");
```

1. Line 1 evaluates `age >= 13`.
2. If it's `true`, line 2 runs. If it's `false`, the computer skips line 2.
3. Line 4 runs either way.

In Lemon Squeeze Part 1, the game keeps going when you have 0 lives. Say `lives` holds your lives. Which Boolean expression checks if the game should end?

{{< collapse summary="Click here to reveal the answer." >}}

`lives == 0`, or `lives <= 0` to also catch negative numbers. Put the code that ends the game inside an if statement with this Boolean expression.

{{</ collapse >}}

### What is an if-else statement?
{{< video title="CSP: Conditionals pt 2B - if/else statements" src="/videos/if-else-statements.mp4" poster="/images/video-poster-if-else-statements.jpg" >}}

It runs one block of code if its Boolean expression is `true`, and a different block if it's `false`:

```js {linenos=table}
if (age >= 13) {
  console.log("You can see a PG-13 movie alone.");
} else {
  console.log("You can see a G-rated movie.");
}
```

Exactly one of lines 2 and 4 runs, never both.

`age` holds `12`. What does this code print?

{{< collapse summary="Click here to reveal the answer." >}}

`You can see a G-rated movie.`, because `12 >= 13` is `false`.

{{</ collapse >}}

### What does MOD do?
MOD (`%`) gives the remainder after you divide one number by another.

It works like any other arithmetic operator:

| Operator | Example | Result |
|----------|---------|-------:|
| Add      | `3 + 2` | `5`    |
| Subtract | `3 - 2` | `1`    |
| Multiply | `3 * 2` | `6`    |
| Divide   | `3 / 2` | `1.5`  |
| MOD      | `3 % 2` | `1`    |

To evaluate `17 % 5`, use long division:

1. 5 goes into 17 three times: `3 * 5` is `15`.
2. `17 - 15` leaves a remainder of `2`, so `17 % 5` is `2`.

MOD is useful for checking:

- **Even or odd**: If `x % 2` is `0`, `x` is even.
- **Divisible**: If `x % y` is `0`, `x` divides evenly by `y`.

Lemon Squeeze Part 2 uses MOD to check if your score is even or odd:

```js {linenos=table}
// the MOD operator "%" - divides two numbers and returns the remainder
// in this case - if a number divided by two has a remainder of zero, it's an even number
if (score % 2 == 0) {
  setText("evenOddLabel", "You collected an EVEN number of lemons.");
} else {
  setText("evenOddLabel", "You collected an ODD number of lemons.");
}
```

What do these evaluate to?

1. `10 % 3`
2. `8 % 2`
3. `15 % 4`
4. `4 % 6`

{{< collapse summary="Click here to reveal the answers." >}}

1. `1`
2. `0`, so 8 is even
3. `3`
4. `4`, since 6 goes into 4 zero times

{{</ collapse >}}

### What is an if-else-if statement?
{{< video title="CSP: Conditionals pt 2C - if/else if statements" src="/videos/if-else-if-statements.mp4" poster="/images/video-poster-if-else-if-statements.jpg" >}}

It checks several Boolean expressions in order, then runs only the code for the **first** one that's `true`:

```js {linenos=table}
if (temperature > 100) {
  console.log("It's dangerously hot");
} else if (temperature > 90) {
  console.log("It's very hot");
} else if (temperature > 80) {
  console.log("It's hot");
} else if (temperature > 70) {
  console.log("It's warm");
} else {
  console.log("It's cool");
}
```

`temperature` holds `95`:

1. `95 > 100` is `false`, so skip to line 3.
2. `95 > 90` is `true`, so print `It's very hot`.
3. Skip everything else, even though `95 > 80` is also `true`.

Always put the most specific case first. What would print if line 1 checked `temperature > 70` instead?

{{< collapse summary="Click here to reveal the answer." >}}

`It's warm`, because `95 > 70` is the first `true` expression. Any temperature over 70 would print `It's warm`, so the hotter messages would never run.

{{</ collapse >}}

### How do logical operators work in conditionals?
{{< video title=`CS Principles: Conditionals - Part 3 "And & Or" Operators` src="/videos/and-or-operators.mp4" poster="/images/video-poster-and-or-operators.jpg" >}}

{{% define "Logical Operator" %}}

Use them to combine comparisons into one Boolean expression. For example, this checks for a discount day OR a teen age:

```js {linenos=table}
(day == "Tuesday" || day == "Thursday") || (age > 12 && age < 21)
```

`day` holds `"Monday"` and `age` holds `16`. Is this `true` or `false`?

{{< collapse summary="Click here to reveal the answer." >}}

`true`. Here's how:

1. `day == "Tuesday" || day == "Thursday"` becomes `false || false`, which is `false`.
2. `age > 12 && age < 21` becomes `true && true`, which is `true`.
3. `false || true` is `true`.

{{</ collapse >}}

### How are if, if-else, and if-else-if statements alike?
They all use Boolean expressions to decide which code to run.

| Statement  | What it does                                                               |
|------------|----------------------------------------------------------------------------|
| if         | Runs its code if one Boolean expression is `true`                          |
| if-else    | Also runs different code if that Boolean expression is `false`             |
| if-else-if | Checks several Boolean expressions, and runs code for the first `true` one |

After any of them, the program continues as normal.

## Assignment
{{% instructions-code-org-update %}}

_Tip: In Lemon Squeeze Part 4, use a fake password when you add a username and password. Never put real passwords directly in your code._

{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Conditional Statement" %}}

### Draw Lemon Squeeze Flowcharts (~15mins)
Draw flowcharts for the if-else-if statements added to Lemon Squeeze as you reach them on Code.org:

1. Draw a flowchart for Part 3's if-else-if statement, chaining a new diamond onto each `false` arrow.
2. Draw a flowchart for Part 4's if-else-if statement the same way.
3. Under one flowchart, describe in 2–3 sentences one result or side effect of changing a condition in it.
