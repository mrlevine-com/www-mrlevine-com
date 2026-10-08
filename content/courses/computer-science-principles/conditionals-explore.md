---
title: Conditionals Explore
units: ["Variables, Conditionals, and Functions"]
summary: Computers make decisions by evaluating a question to true or false, then following the matching path.
weight: 340
---

{{% param summary %}}

## Today's Objectives
- Evaluate expressions that include Boolean values, comparison operators, and logical operators.
- Trace simple programs that use Boolean expressions and conditional statements.
- Use appropriate vocabulary to describe Boolean expressions and conditional statements.

## Lesson Overview
### What is a Boolean value?
{{% define "Boolean Value" %}}

Booleans are a third type of value, after numbers and strings:

- They're written `true` and `false`, with **no quotes**.
- Computers use them to make decisions: if something is `true`, do this; if it's `false`, do that.

### What is a comparison operator?
{{< video title="CS Principles: Conditionals - Part 1 Boolean Expressions" src="/videos/boolean-expressions.mp4" poster="/images/video-poster-boolean-expressions.jpg" >}}

{{% define "Comparison Operator" %}}

When you see one, stop and evaluate to `true` or `false`. For example, `3 < 8` evaluates to `true`.

| Operator | Meaning                  |
|----------|--------------------------|
| `<`      | less than                |
| `>`      | greater than             |
| `<=`     | less than or equal to    |
| `>=`     | greater than or equal to |
| `==`     | equal to                 |
| `!=`     | not equal to             |

Watch out: `==` asks "are these equal?" A single `=` is the assignment operator, which puts a value in a variable.

Any expression that evaluates to `true` or `false` is a **Boolean expression**. To evaluate one:

1. Reduce each side of the operator to one value. Do parentheses first.
2. Compare the two values.

For example, `3 + 6 < 8` becomes `9 < 8`, which evaluates to `false`.

Try these. Is each one `true` or `false`?

1. `6 - 3 < 4 + 1`
2. `12 / 6 > 3 - 0`
3. `(7 - 3) * 3 <= 10`
4. `9 + 5 == 4 + 10`
5. `lives + 4 < score - 1`, when `lives` holds `5` and `score` holds `10`

{{< collapse summary="Click here to reveal the answers." >}}

1. `3 < 5` is `true`
2. `2 > 3` is `false`
3. `12 <= 10` is `false`
4. `14 == 14` is `true`
5. `9 < 9` is `false`

{{</ collapse >}}

### How does a computer make a decision?
It follows a **flowchart**: a picture of the steps for making a decision with a Boolean expression.

Take this question: "Can you go to the movies? You can if it's before 8 o'clock."

![A flowchart. A box labeled time points to a diamond containing time < 8. The true arrow leads to "You can go!" and the false arrow leads to "You can't go."](/images/flowchart-movies.svg)

1. **Variables** go in boxes at the top. Here, `time` holds the hour.
2. **The Boolean expression** goes in the diamond.
3. **Arrows** labeled `true` and `false` lead to each result.

It's 9 o'clock. Assign `9` to `time`. Then `9 < 8` is `false`, so follow the `false` arrow: you can't go.

Trace this one: "You win the game if `score * lives > 10`." What happens with each set of values?

1. `score` holds `3` and `lives` holds `3`
2. `score` holds `1` and `lives` holds `10`
3. `score` holds `-5` and `lives` holds `2`

{{< collapse summary="Click here to reveal the answers." >}}

You haven't won the game yet in all three:

1. `9 > 10` is `false`
2. `10 > 10` is `false`, since 10 isn't greater than itself
3. `-10 > 10` is `false`

{{</ collapse >}}

Challenge: "Is your dog older than you in human years? One dog year equals seven human years." What variables and Boolean expression do you need?

{{< collapse summary="Click here to reveal the answer." >}}

Use two variables, `dogAge` and `myAge`, and the Boolean expression `dogAge * 7 > myAge`.

- `true`: your dog is older than you.
- `false`: you're older than your dog.

{{</ collapse >}}

### What is a logical operator?
{{% define "Logical Operator" %}}

Use them to combine or flip Boolean values:

| Operator | Name | Rule                                     |
|----------|------|------------------------------------------|
| `&&`     | AND  | `true` only if **both** sides are `true` |
| `\|\|`   | OR   | `true` if **either** side is `true`      |
| `!`      | NOT  | Flips the value: `!true` is `false`      |

These are truth tables. They show every combination of `true` and `false`:

| `a`     | `b`     | `a && b` | `a \|\| b` |
|---------|---------|----------|------------|
| `true`  | `true`  | `true`   | `true`     |
| `true`  | `false` | `false`  | `true`     |
| `false` | `true`  | `false`  | `true`     |
| `false` | `false` | `false`  | `false`    |

To evaluate, reduce each side of the logical operator to one Boolean value, then use the truth table.

For example, "You can adopt a cat if you have 40 dollars AND you're over 14 years old" becomes:

```js {linenos=table}
money == 40 && age > 14
```

You're 17 and have $39. Is this `true` or `false`?

{{< collapse summary="Click here to reveal the answer." >}}

`false`. Here's how:

1. `money == 40` becomes `39 == 40`, which is `false`.
2. `age > 14` becomes `17 > 14`, which is `true`.
3. `false && true` is `false`, so you can't adopt a cat.

`==` checks for **exactly** 40. With $41, you still couldn't adopt one.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Boolean Value" "Comparison Operator" "Logical Operator" %}}

_Tip: For your illustrations, sketch quick doodles, like a `3 < 8` arrow pointing to `true`._

### Draw a Decision Flowchart (~10mins)
Draw a flowchart that decides what to wear to an event:

1. Draw boxes at the top for two variables you need to decide, like `temperature` and `chanceOfRain`.
2. Draw a diamond with a Boolean expression that uses those variables, then draw `true` and `false` arrows to two outfits.
3. Test it with a partner's values, and circle the path it takes.

_Challenge: Combine two comparisons in your diamond with `&&`, `||`, or `!`._

{{% instructions-code-org-update %}}
