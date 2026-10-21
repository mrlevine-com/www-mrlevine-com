---
title: Functions Make
units: ["Variables, Conditionals, and Functions"]
summary: Build the Quote Maker App from a blank screen using variables, an if-else-if statement, and an updateScreen() function.
weight: 400
---

{{% param summary %}}

## Today's Objectives
- Implement a function using programming patterns while developing a functional app.
- Recognize the need for a function to reduce repeated code while developing a functional app.
- Use debugging skills as part of developing an app.
- Write comments to clearly explain both the purpose and function of different segments of code within an app.

## Lesson Overview
### What will you make today?
The Quote Maker App. Its screen is already designed; you write all of its code, starting from a blank screen.

- You type a quote and pick its font, background color, and font size.
- The app shows your styled quote and a feedback message about your design.

Try the working app in Level 1 on Code.org. Choose lavender and Lucida Sans, then choose lightgreen and move the slider until the feedback changes. Then think about:

1. What are the app's inputs?
2. What are its outputs?
3. When does the screen update?
4. How could a function be used in this app?

{{< collapse summary="Click here to reveal the answers." >}}

1. The quote text box, the font family and background color dropdowns, and the font size slider.
2. The styled quote and the feedback message.
3. Every time you change any input, even one letter of the quote.
4. One function can update the whole screen, including the feedback message. Every input calls it, so you write that code only once.

{{</ collapse >}}

### Which programming pattern will you use?
The updateScreen pattern: each `onEvent()` changes a variable, then calls one function that updates the whole screen.

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

Today, plan your function **before** you write any code, instead of noticing repeated code after.

Should the if-else-if statement that picks the feedback message go inside `updateScreen()`? Why?

{{< collapse summary="Click here to reveal the answer." >}}

Yes. The feedback must be checked every time any input changes. Inside `updateScreen()`, you write the if-else-if statement once, and all 4 inputs use it. Otherwise, you'd copy it into all 4 `onEvent()`s.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Plan the Quote Maker App (~10mins)
Sketch the Quote Maker App's screen and plan your `updateScreen()` function.

1. Sketch the screen and label each element with its ID. Next to each input, write the event its `onEvent()` will use:

    | ID                | Element                    | Event      |
    |-------------------|----------------------------|------------|
    | `quoteInput`      | Quote text box             | `"input"`  |
    | `fontFamilyInput` | Font family dropdown       | `"change"` |
    | `colorInput`      | Background color dropdown  | `"change"` |
    | `fontSizeInput`   | Font size slider           | `"input"`  |
    | `quoteOutput`     | Quote text                 |            |
    | `colorOutput`     | Box behind the quote       |            |
    | `feedbackOutput`  | Feedback message           |            |

2. Under your sketch, list each variable and what it stores, like `color`: the background color the user selects. You'll need 4.
3. Write the if-else-if statement for your feedback, filling in the blanks with your own combinations and messages:

    ```js {linenos=table}
    if (color == ____ && fontFamily == ____) {
      setText("feedbackOutput", ____);
    } else if (____ == ____ && ____ == ____) {
      setText("feedbackOutput", ____);
    } else {
      setText("feedbackOutput", ____);
    }
    ```

{{% instructions-code-org-update %}}

Build the app in Level 2, using your plan:

1. Create your 4 variables at the top of your program and give them starting values with `=`.
2. Declare `updateScreen()` at the bottom. Inside it, update every output, then add your if-else-if statement:

    | Output           | Code                                                      |
    |------------------|-----------------------------------------------------------|
    | Quote text       | `setText("quoteOutput", quote);`                          |
    | Background color | `setProperty("colorOutput", "background-color", color);`  |
    | Font family      | `setProperty("quoteOutput", "font-family", fontFamily);`  |
    | Font size        | `setProperty("quoteOutput", "font-size", fontSize);`      |

3. Add an `onEvent()` for each input. Inside each one, store the input's value in its variable, then call `updateScreen();`. Test each input as you add it.

    _Tip: Use `getText(...)` for the text box and dropdowns, and `getNumber("fontSizeInput")` for the slider. Stuck? Drag the speed slider toward the turtle, type a variable's name in the Watch area, or explain your code to a friend._

Before you submit, check that:

- [ ] Every input has an `onEvent()` that calls `updateScreen()`.
- [ ] Variables store the quote, font family, color, and font size.
- [ ] `updateScreen()` updates every output and uses an if-else-if statement to show the feedback.
- [ ] Your code runs with no errors.
- [ ] Every `onEvent()` and function has a comment explaining its purpose and function.

_For extra credit, add a dropdown of image names and use it to decorate your quote._

## Upcoming Quiz
To prepare for your upcoming quiz, study all of the terms and definitions that you have written in your Unit Journal. You can find all ten terms [here](/units/variables-conditionals-and-functions/) listed in alphabetical order after the lessons.
