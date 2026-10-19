---
title: Functions Explore and Investigate
units: ["Variables, Conditionals, and Functions"]
summary: Functions give a group of commands a name, so you can write code once and run it anywhere by calling that name.
weight: 380
---

{{% param summary %}}

## Today's Objectives
- Describe the way a function call interrupts the normal flow of execution within a program.
- Modify programs that declare and call functions to adjust their functionality.
- Trace the flow of execution in programs that declare and call functions.
- Use appropriate vocabulary to describe the declaring and calling of functions.

## Lesson Overview
### What is a function?
{{< video title="Introduction to Functions" src="/videos/introduction-to-functions.mp4" poster="/images/video-poster-introduction-to-functions.jpg" >}}

{{% define "Function" %}}

Using one takes 2 steps:

1. **Declare it once** to give a group of commands a name:

    ```js {linenos=table}
    function sayHello() {
      console.log("Hello world!");
    }
    ```

2. **Call it** as many times as you want to run those commands:

    ```js {linenos=table}
    sayHello();
    ```

{{% define "Function Call" %}}

A function call interrupts the normal top-to-bottom order of your program:

1. The computer jumps to the function's declaration.
2. It runs every command inside the function.
3. It jumps back to the line after the call.

Trace this program. In what order do its lines run?

```js {linenos=table}
console.log("Starting my program!");
sayHello();
sayHello();
console.log("Ending my program!");

function sayHello() {
  console.log("Hello world!");
}
```

{{< collapse summary="Click here to reveal the answer." >}}

1, 2, 7, 3, 7, 4.

- Line 2 calls `sayHello()`, so the computer jumps to line 7, then comes back to line 3.
- Line 3 calls it again, so line 7 runs a second time before line 4.
- Line 6 only declares the function. It doesn't run anything by itself.

{{</ collapse >}}

### How do you make a function in App Lab?
{{< video title="Defining and Calling Functions" src="/videos/defining-and-calling-functions.mp4" poster="/images/video-poster-defining-and-calling-functions.jpg" >}}

Use the 2 blocks in the "Functions" tab of the toolbox: one declares a function, and one calls it.

- **Declaring alone does nothing.** Nothing runs until you call the function.
- **Order doesn't matter.** A call still works if it comes before the declaration.
- **Put declarations at the bottom** of your program to keep it organized.
- **Name it clearly**, like `updateScreen`, not `doStuff`, so anyone can tell what it does.

### How does a function make code easier to change?
Declare it once and call it everywhere. Then you only need to change or fix your code in one place.

Many apps use this updateScreen pattern. Each button changes a variable, then calls `updateScreen()` to show the change:

```js {linenos=table}
var count = 0;
updateScreen();

onEvent("upButton", "click", function() {
  count = count + 1;
  updateScreen();
});

onEvent("downButton", "click", function() {
  count = count - 1;
  updateScreen();
});

function updateScreen() {
  setText("countLabel", count);
  if (count > 20) {
    setProperty("countLabel", "text-color", "green");
  }
}
```

1. On what line is `updateScreen()` declared?
2. On what lines is it called?
3. You want `count` to turn red when it drops below 0. Where do you add that code?

{{< collapse summary="Click here to reveal the answers." >}}

1. Line 14.
2. Lines 2, 6, and 11.
3. Inside `updateScreen()`, after line 18. You write it once, and it works for both buttons and when the app starts.

{{</ collapse >}}

Without `updateScreen()`, you'd copy lines 15–18 into both buttons. Then every change or bug fix would need to happen in each copy.

## Assignment
{{% instructions-code-org-update %}}

Use these tips as you work:

- **Levels 1–2**: Add `singChorus();` wherever the comments say the chorus goes. Run it, and watch the code jump to the function and back.
- **Levels 3–5**: Make all of your changes inside `updateScreen()`.
- **Level 6**: Find the lines repeated in each `onEvent()`. Move one copy into a new `updateScreen()` function, then replace every copy with `updateScreen();`.

{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Function" "Function Call" %}}
