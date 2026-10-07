---
title: Variables Make
units: ["Variables, Conditionals, and Functions"]
summary: Build the Photo Liker App from a blank screen using variables, event handlers, and comments.
weight: 330
---

{{% param summary %}}

## Today's Objectives
- Implement programming patterns with variables to develop a functioning app.
- Recognize the need for programming patterns with variables as part of developing a functioning app.
- Use debugging skills as part of developing an app.
- Write comments to clearly explain both the purpose and function of different segments of code within an app.

## Lesson Overview
### What will you make today?
The Photo Liker App. Its screen is already designed; you write all of its code, starting from a blank screen.

- The thumbs up and thumbs down buttons change the number of likes.
- Typing a comment and clicking the speech bubble button adds it under the photo.

Try the working app in Level 1 on Code.org. Then think about:

1. What are the app's inputs?
2. What are its outputs?
3. What's one piece of information that might be stored in a variable?

{{< collapse summary="Click here to reveal the answers." >}}

1. The thumbs up and thumbs down buttons, the text box for a new comment, and the button to add the comment.
2. The number of likes and the list of comments shown on the screen.
3. The number of likes, or all of the comments added so far.

{{</ collapse >}}

### Which programming patterns will you use?
The two patterns from Variables Investigate:

**Counter Pattern with Event:** updates a variable every time something happens, like a click.

```js {linenos=table}
var myVar = 0;
onEvent("id", "click", function() {
  myVar = myVar + 1;
});
```

**Variable with String Concatenation Pattern:** stores glued-together strings in a variable.

```js {linenos=table}
var myString = "rock";
var myOtherString = "roll";
var myStory = myString + " and " + myOtherString;
```

Which pattern does each button need?

{{< collapse summary="Click here to reveal the answer." >}}

| Button          | Pattern                                                                       |
|-----------------|-------------------------------------------------------------------------------|
| `upButton`      | Counter Pattern with Event (adds 1)                                           |
| `downButton`    | Counter Pattern with Event (subtracts 1)                                      |
| `commentButton` | Variable with String Concatenation (glues the new comment onto all the others) |

_Tip: Put `"\n"` between comments so each one starts on a new line._

{{</ collapse >}}

### What should you do when your code doesn't work?
Try these debugging tools, one at a time:

- **Speed slider:** drag it toward the turtle to watch your code run one line at a time.
- **Watch area:** type a variable's name to see its value change as your code runs.
- **`console.log(...)`:** prints a value in the Debug Console.
- **Explain your code to a friend:** saying it out loud often reveals the bug.
- **Read line by line:** decide which line is causing the error.

### What makes a good code comment?
It explains both the **purpose** (why the code exists) and the **function** (what it does).

For example, from the Thermostat App:

```js {linenos=table}
// Lowers the temperature by 1 degree F and updates the
// screen, so the user can make the room cooler.
onEvent("downButton", "click", function() {
```

## Assignment
{{% instructions-unit-journal-update %}}

### Plan the Photo Liker App (~10mins)
Sketch the Photo Liker App's screen and label what each part of your code will do.

1. Sketch the screen and label each element with its ID:

    | ID                  | Element                       |
    |---------------------|-------------------------------|
    | `upButton`          | Thumbs up button              |
    | `downButton`        | Thumbs down button            |
    | `likeCounterOutput` | "Likes: 0" text               |
    | `newCommentInput`   | Text box for a new comment    |
    | `commentButton`     | Speech bubble button          |
    | `allCommentsOutput` | Box that shows every comment  |

2. Next to each button, write what its event handler will do when clicked: which variable changes, what text updates on the screen, and which sound plays.
3. Under your sketch, list each variable you'll need and what it stores.

{{% instructions-code-org-update %}}

Build the app in Level 2, using your plan:

1. Create your variables at the top of your program and give them starting values with `=`.
2. Make one button work at a time: add its `onEvent()`, write its code, and click it to test. Start with `upButton`: "Likes" should go up by 1 every click.
3. Add a comment above each `onEvent()` explaining its purpose and function.

Before you submit, check that:

- [ ] Every button has an `onEvent()`.
- [ ] Clearly named variables store the likes and the comments, and they're updated inside the `onEvent()`s.
- [ ] The screen shows the likes and all comments, and each button plays a sound.
- [ ] Your code runs with no errors.
- [ ] Every `onEvent()` has a comment explaining its purpose and function.

_Done early? Clear the text box after a comment is added: `setText("newCommentInput", "");`_

### Explain a User Interface Feature (~10mins)
Explain how your app's design helps people use it, like you will on the AP Create Performance Task.

1. Pick one feature of your app's user interface, like the `upButton`. (If your app isn't finished, use the working app in Level 1.)
2. Answer in 3–5 sentences: "Explain how the design of your program's user interface supports its functionality. In your response, describe one feature of the interface and how it helps users interact with the program."

    _(Hint: Use or modify these sentence starters:_
    - _One feature of my program's user interface that supports its functionality is \_\_\_\_\_._
    - _This feature allows the user to \_\_\_\_\_._
    - _For example, when the user interacts with \_\_\_\_\_, it \_\_\_\_\_._
    - _This makes it easier for users to \_\_\_\_\_._
    - _Additionally, the program provides feedback by \_\_\_\_\_.)_
