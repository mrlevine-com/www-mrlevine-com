---
title: Variables Practice
units: ["Variables, Conditionals, and Functions"]
summary: Practice writing and debugging programs with variables, and learn to spot the bug that happens when you create the same variable twice.
weight: 320
---

{{% param summary %}}

## Today's Objectives
- Debug programs that use variables and expressions.
- Write programs that use variables and expressions with the support of sample code.

## Lesson Overview
### Which debugging tools should you use today?
Three App Lab tools show you what your variables are doing:

- **Speed slider** (turtle to rabbit, above the Debug Console): slows your code down so you can watch it run one line at a time.
- **`console.log(...)`**: prints a value in the Debug Console.
- **Watch area** (right of the Debug Console): type a variable's name to see its value change as your code runs.

When you're stuck, use the four debugging steps: **Describe** the problem, **Hunt** for bugs, **Try** one small change, and **Document** what you learned.

What prints in the Debug Console when this code runs?

```js {linenos=table}
var myFavoriteNumber;
var myFavoriteFood;

myFavoriteNumber = 1;
myFavoriteFood = "pizza";

console.log("My favorite number is");
console.log(myFavoriteNumber);
console.log("My favorite food is");
console.log(myFavoriteFood);
```

{{< collapse summary="Click here to reveal the answer." >}}

```
"My favorite number is"
1
"My favorite food is"
"pizza"
```

Strings print with quotes. Numbers don't.

{{</ collapse >}}

### What does `\n` do?
`\n` is the new line character. Put it inside a string to start a new line.

For example, `setText("label", "Score: 5\nLives: 3");` shows:

```
Score: 5
Lives: 3
```

### Why does `var` inside an `onEvent()` cause a bug?
It creates a second variable with the same name. Watch how this breaks a clicker app:

{{< video title="Debugging Global vs Local Variables" src="/videos/debugging-global-vs-local-variables.mp4" poster="/images/video-poster-debugging-global-vs-local-variables.jpg" >}}

There are two types of variables:

| Type       | How it's created                | How it works                                                                         |
|------------|---------------------------------|--------------------------------------------------------------------------------------|
| **Global** | `var` used outside an `onEvent()` | Permanent. You can use it anywhere in your code.                                     |
| **Local**  | `var` used inside an `onEvent()`  | Temporary. You can only use it inside that `onEvent()`. Deleted once it's done running. |

So far, you've only needed global variables. Here's what the bug usually looks like:

```js {linenos=table}
var count = 0;

onEvent("button1", "click", function() {
  var count = count + 1;
});
```

It looks like one variable, but there are two named `count`: a global one (line 1) and a local one (line 4). Changing one never changes the other.

How would you fix line 4?

{{< collapse summary="Click here to reveal the answer." >}}

Delete `var`, so the button updates the global `count`:

```js {linenos=table}
count = count + 1;
```

{{</ collapse >}}

To avoid this bug, create your variables:

1. **Once.** Use `var` only once per variable.
2. **At the top of your program.** Your code stays organized and easier to read.
3. **Outside any `function` or `onEvent()` blocks.**

## Assignment
{{% instructions-code-org-update %}}

| Levels | What you'll practice                    |
|-------:|-----------------------------------------|
| 1–2    | Assigning numbers and strings           |
| 3–7    | Variables and operators                 |
| 8–9    | Debugging scope issues                  |
| 10     | Putting it together (pick one)          |
| 11–12  | Check your understanding                |

{{% instructions-unit-journal-update %}}

### Explain a Variable's Purpose (~10mins)
Explain why a program uses a variable, like you will on the AP Create Performance Task.

1. Paste a screenshot of code from today's Code.org lesson that uses a variable. For example:

    ```js {linenos=table}
    var dollars = 0;

    onEvent("addFiveButton", "click", function() {
      dollars = dollars + 5;
      setProperty("dollarsLabel", "text", "$" + dollars);
      playSound("sound://category_digital/ring_1.mp3");
    });
    ```

2. Circle where the variable is created, and draw an arrow to every line that updates or uses it.
3. Answer in 1–2 sentences: "What is the purpose of using a variable in the code that you have provided here?"

    _(Hint: Fill in the blanks: "The variable [name] keeps track of [what], so that [why].")_

{{% unit-journal-question-of-the-day question="What aspects of working with variables do you feel like clicked today? What do you still feel like you have trouble with?" %}}
