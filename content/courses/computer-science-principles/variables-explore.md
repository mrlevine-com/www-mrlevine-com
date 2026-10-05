---
title: Variables Explore
units: ["Variables, Conditionals, and Functions"]
summary: Variables let your apps remember information, like a safe with a name tag that holds one value at a time.
weight: 300
---

{{% param summary %}}

## Today's Objectives
- Evaluate expressions that include numbers, strings, and arithmetic operators.
- Trace simple programs that use variables, expressions, and variable assignment.
- Use appropriate vocabulary to describe variables, expressions, and variable assignment.

## Lesson Overview
### What is a value?
A value is one piece of information. For now, there are two types:

- **Numbers** are made of the digits 0 through 9 and have **no quotes**: `22`, `548`, `123`
- **Strings** are made of any characters and go **inside double quotes**: `"hi"`, `"c u l8r"`, `"123"`

{{% define "String" %}}

Watch out: `123` is a number, but `"123"` is a string.

### What is an expression?
{{% define "Expression" %}}

Operators are the symbols `+`, `-`, `*`, and `/`. When you figure out what an expression equals, you **evaluate** it.

| Expression       | Evaluates to |
|------------------|--------------|
| `3 + 4`          | `7`          |
| `11 * 2`         | `22`         |
| `"for" + "ever"` | `"forever"`  |
| `"gr" + 8`       | `"gr8"`      |

With strings, you can only use `+`. It glues the two values together. A number glued to a string becomes part of the string.

Try evaluating these. Is each answer a number or a string?

1. `4 + 5`
2. `10 - 9`
3. `"tree" + "house"`
4. `"you" + "r"`
5. `3 + "D"`

{{< collapse summary="Click here to reveal the answers." >}}

1. `9` (number)
2. `1` (number)
3. `"treehouse"` (string)
4. `"your"` (string)
5. `"3D"` (string)

{{</ collapse >}}

### What is a variable?
{{% define "Variable" %}}

Picture a variable as a **safe with a name tag**, somewhere in your computer's memory:

- It holds **one** value at a time.
- Its name has no quotes, no spaces, and starts with a letter.

When an expression uses a variable, the computer goes to the safe and **copies** what's inside, then evaluates. The safe keeps its value.

If `zip` holds `5` and `bop` holds `"hi"`:

| Expression  | Becomes    | Evaluates to |
|-------------|------------|--------------|
| `3 + zip`   | `3 + 5`    | `8`          |
| `bop + zip` | `"hi" + 5` | `"hi5"`      |

Try these. `boo` holds `4` and `rar` holds `"be"`.

1. `3 * boo`
2. `rar + "ep"`
3. `rar + boo`

{{< collapse summary="Click here to reveal the answers." >}}

1. `12`
2. `"beep"`
3. `"be4"`

{{</ collapse >}}

### What is the assignment operator?
{{% define "Assignment Operator" %}}

On the AP exam, it's an arrow: `pow ← 3`. In JavaScript, it's an equal sign: `pow = 3`. Read both as **"pow gets 3."**

Follow these rules:

1. **Create** a variable with `var`.
2. **Evaluate first, then assign.** Work out the right side, then lock that one value in the safe.
3. **The old value is replaced forever.** A safe only holds one value.
4. **Variables aren't connected.** Changing one never changes another.

In math, `=` means "equal forever." In programming, `=` means "put this value in this variable."

Here's an example. Line 4 uses `kit` to set `boo`, but line 5 changes `kit` without changing `boo`:

```js {linenos=table}
var kit;
kit = 1;
var boo;
boo = kit + 1;
kit = 5;
```

At the end, `kit` holds `5` and `boo` holds `2`.

Trace this program one line at a time. What do `fuzz` and `clip` hold at the end?

```js {linenos=table}
var fuzz;
var clip;
fuzz = 5;
clip = fuzz + 2;
fuzz = clip + 1;
clip = "gr" + fuzz;
fuzz = fuzz + 1;
fuzz = fuzz + 1;
fuzz = fuzz + 1;
```

{{< collapse summary="Click here to reveal the answer." >}}

`fuzz` holds `11` and `clip` holds `"gr8"`.

| Line | `fuzz` | `clip`  |
|-----:|--------|---------|
| 3    | `5`    |         |
| 4    | `5`    | `7`     |
| 5    | `8`    | `7`     |
| 6    | `8`    | `"gr8"` |
| 7    | `9`    | `"gr8"` |
| 8    | `10`   | `"gr8"` |
| 9    | `11`   | `"gr8"` |

Lines 7 to 9 use `fuzz`'s own value to count up by one each time.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-create %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "String" "Expression" "Variable" "Assignment Operator" %}}

_Tip: For your illustrations, sketch quick doodles, like a safe with a name tag for "Variable."_

{{% instructions-code-org-update %}}
