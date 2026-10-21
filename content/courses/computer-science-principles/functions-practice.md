---
title: Functions Practice
units: ["Variables, Conditionals, and Functions"]
summary: Practice replacing repeated code with functions, and learn to spot the bug that happens when you create a variable inside a function.
weight: 390
---

{{% param summary %}}

## Today's Objectives
- Debug programs that use functions.
- Identify opportunities to use functions to reduce repeated code within a program.
- Write programs that use functions with the support of sample code.

## Lesson Overview
### How do you replace repeated code with a function?
Move one copy into a function, then call it everywhere the code used to be:

1. **Find** the lines that repeat.
2. **Declare** a function, and move one copy of those lines inside it.
3. **Replace** every copy with a call to the function.

Which lines repeat in this program?

```js {linenos=table}
var score = 0;

onEvent("addOneButton", "click", function() {
  score = score + 1;
  setText("scoreLabel", "Score: " + score);
  playSound("sound://category_digital/ring_1.mp3");
});

onEvent("addFiveButton", "click", function() {
  score = score + 5;
  setText("scoreLabel", "Score: " + score);
  playSound("sound://category_digital/ring_1.mp3");
});
```

{{< collapse summary="Click here to reveal the answer." >}}

Lines 5–6 and 11–12. Move them into `updateScreen()`, then call it in both buttons:

```js {linenos=table}
var score = 0;

onEvent("addOneButton", "click", function() {
  score = score + 1;
  updateScreen();
});

onEvent("addFiveButton", "click", function() {
  score = score + 5;
  updateScreen();
});

function updateScreen() {
  setText("scoreLabel", "Score: " + score);
  playSound("sound://category_digital/ring_1.mp3");
}
```

{{</ collapse >}}

### Why does `var` inside a function cause a bug?
It creates a second variable with the same name, so changing one never changes the other:

{{< video title="Debugging Variable Scope: Functions" src="/videos/debugging-variable-scope-functions.mp4" poster="/images/video-poster-debugging-variable-scope-functions.jpg" >}}

| Type       | How it's created                                 | How it works                                     |
|------------|--------------------------------------------------|--------------------------------------------------|
| **Global** | `var` used outside any `function` or `onEvent()` | Permanent. You can use it anywhere.              |
| **Local**  | `var` used inside a `function` or `onEvent()`    | Temporary. Deleted once that block is done running. |

To avoid this bug, create each variable once, at the top of your program, outside any `function` or `onEvent()`.

### When should you make a function?
As early as you can:

| When       | What you do                                                     |
|------------|-----------------------------------------------------------------|
| **Never**  | Copy and paste the same code everywhere.                        |
| **After**  | Notice code you wrote twice, then move it into a function.      |
| **During** | Notice you'll need code again, and make a function right then.  |
| **Before** | Plan your functions before you write any code.                  |

Today, "after" is fine. In the next lesson's project, try "during" or "before."

## Assignment
{{% instructions-code-org-update %}}

| Levels | What you'll practice                          |
|-------:|-----------------------------------------------|
| 1–5    | Calling functions and replacing repeated code |
| 6–7    | Debugging variable scope                      |
| 8      | Putting it together (pick one app)            |
| 9      | Deciding when to make a function              |
| 10     | Check your understanding                      |

_Tip for Level 10: In AP pseudocode, `PROCEDURE` declares a function, and `DISPLAY` works like `console.log`._

_Stuck? Hover over a block to read its documentation, check the Help & Tips tab, or ask your partner or the group next to you._
