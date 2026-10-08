---
title: Variables
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Use variables to label values so you can reuse them throughout your programs.
weight: 310
---

{{% param summary %}}

## Today's Objectives
- Identify a variable as a way to label and reference a value in a program.
- Use variables in a program to store a piece of information that is used multiple times.

## Lesson Overview
### Where do you see input, output, storage, and processing in Game Lab?
{{< collapse summary="Click here to reveal the answer." >}}

Everywhere. All computers do these four things, and Game Lab is no different:

- Input: the values you type into Game Lab, like the parameters of `rect`.
- Output: the shapes on the Game Lab screen.
- Storage: Game Lab remembering your code.
- Processing: Game Lab turning your code into pictures.

Today, you'll focus on storage. Variables are the most common way to store information in a program.

{{</ collapse >}}

### What is a variable?
{{< video title="Introduction to Variables" src="/videos/introduction-to-variables.mp4" poster="/images/video-poster-introduction-to-variables.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

A container that stores a value under a label. Type the label anywhere you need the value.

- Apps use variables to keep track of information that changes, like your score and the lives you have left in a game.
- Variables can hold numbers, text, and colors.
- The video also shows `console.log`, which is from a different tool. You won't need it today.

{{</ collapse >}}

{{% define "Variable" %}}

### How do you create and use a variable?
{{< collapse summary="Click here to reveal the answer." >}}

Create it with `var`, give it a value with `=`, then type its label wherever you need that value.

This code draws two circles that are both 100 wide and 100 tall:

```js {linenos=table}
var size = 100;
ellipse(100, 200, size, size);
ellipse(300, 200, size, size);
```

- Line 1 creates `size` and gives it its first value. This is called initializing.
- Read `=` as "gets": "`size` gets 100."
- The label goes on the left, and the value goes on the right. `100 = size` is an error.
- Lines 2 and 3 use `size` four times. Change line 1 to `50`, and both circles shrink at once.

{{</ collapse >}}

### How do you change a variable's value?
{{< collapse summary="Click here to reveal the answer." >}}

Use `=` again, without `var`. Use `var` only once per variable, when you create it.

This code draws a big circle on the left and a small one on the right:

```js {linenos=table}
var size = 100;
ellipse(100, 200, size, size);
size = 50;
ellipse(300, 200, size, size);
```

- Line 3 replaces 100 with 50. The old value is gone forever.
- Code runs top to bottom, so line 2 still uses 100, and line 4 uses 50.

{{</ collapse >}}

### How do you name a variable?
{{< collapse summary="Click here to reveal the answer." >}}

Pick a label that tells you what's inside, like `score` or `lives`. Labels like `number` or `a` don't help.

Break one of these rules, and you'll get an error:

1. No spaces: `width of rectangle` fails.
2. Don't start with a number: `4sides` and `2morrow` fail.
3. Match spelling and capitals exactly: `size`, `Size`, and `SIZE` are three different variables.

For labels with more than one word, use camelCase: start lowercase, then capitalize each new word, like `sizeOfRectangle`. Underscores, like `size_of_rectangle`, also work. Pick one style and stick with it so you always remember how you spelled your labels.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Levels 1-2: predict where the circle will be drawn and what will happen if you change the numbers on lines 1 and 2, then run the code to check. Use your new vocabulary, like "`xPosition` gets 300, so the circle will be on the right."
2. Levels 3-5: follow the instructions on each level. If level 5 gets stuck in text mode, fix the variable names marked with red error squares, then click "Block Mode" at the top right.
3. Level 6: change a variable's value, fix broken variable names, or use variables to make code easier to read. Check with your teacher before moving on.
4. Level 7: open the "Rubric" tab first to see how to prove you understand variables.
5. Level 8 (challenge): update variables, use variables for colors, or draw your own art or nature scene.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Variable" %}}
{{% unit-journal-question-of-the-day question="How can you use variables to store information in your programs?" hint="Draw a variable as a labeled box holding a value, like size holding 100. Then explain in your own words why variables are useful." %}}
