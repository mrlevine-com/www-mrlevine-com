---
title: Random Numbers
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Use random numbers to make your programs draw something different every time they run.
weight: 320
---

{{% param summary %}}

## Today's Objectives
- Generate and use random numbers in a program.
- Update a value stored in a variable.

## Lesson Overview
### When would you want a program to do something different each time it runs?
{{< collapse summary="Click here to reveal the answer." >}}

Whenever surprises make it better, like games. So far, your programs have done the same thing every time, and most surprises have been bugs.

- A die roll should land on a different number each time.
- An enemy in a game is more fun when you can't predict where it will appear.
- Today, you'll code random behavior into your programs so you get good surprises.

{{</ collapse >}}

### How do you make a random number?
{{< collapse summary="Click here to reveal the answer." >}}

Use `randomNumber(min, max)`. It picks a whole number from `min` to `max`, including both.

- Find it in the "Math" drawer of the toolbox.
- Use it anywhere you'd type a number.
- This is like rolling a die. It could be 1, 2, 3, 4, 5, or 6:

```js {linenos=table}
randomNumber(1, 6);
```

{{</ collapse >}}

### How do you make a random drawing?
{{< collapse summary="Click here to reveal the answer." >}}

Put `randomNumber` inside a drawing command as a parameter.

This code draws a circle at a random spot along a line across the middle:

```js {linenos=table}
ellipse(randomNumber(0, 400), 200);
```

- Run it 3 times, and you might get 3 different pictures.
- Each `randomNumber` is a new roll. This code picks a new `x` and a new `y`, so the circle can land anywhere:

```js {linenos=table}
ellipse(randomNumber(0, 400), randomNumber(0, 400));
```

{{</ collapse >}}

### How do you update a variable?
{{< collapse summary="Click here to reveal the answer." >}}

Use the variable's own value on the right side of `=`, like `x = x + 50`. Read it as "`x` gets `x` plus 50."

This code draws 3 circles in a row, each 50 to the right of the last:

```js {linenos=table}
var x = randomNumber(50, 200);
ellipse(x, 200);
x = x + 50;
ellipse(x, 200);
x = x + 50;
ellipse(x, 200);
```

- Line 1 rolls a random starting spot once.
- Lines 3 and 5 move `x` 50 to the right of wherever it already is.
- The whole row moves each run, but the circles always stay 50 apart.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: write down what you think `randomNumber` will do, then run the code a few times. Compare your screen with a neighbor's. Did you get the same thing?
2. Levels 2-5: follow the instructions on each level.
3. Level 6: give planets random sizes, keep randomly placed rectangles stacked, or randomize a scene.
4. Level 7: open the "Rubric" tab first to see how to prove you understand random numbers.
5. Level 8 (challenge): randomize colors, lines, or arcs, use math to keep a drawing symmetrical, or draw your favorite song or season so it changes every run.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Draw 3 Runs of a Random Program ~10mins
Hand-draw what this code could draw on 3 different runs:

```js {linenos=table}
var x = randomNumber(50, 300);
ellipse(x, 200);
x = x + 50;
ellipse(x, 200);
```

1. Draw 3 squares side by side, labeled "Run 1," "Run 2," and "Run 3."
2. In each square, pick a random `x`, write it down, and draw both circles.
3. Below the squares, write one thing that changes every run and one that never changes.

{{% unit-journal-question-of-the-day question="How can you make your programs behave differently each time they are run?" hint="Name the block that does it. Then list other things you'd like to be random in a program, besides numbers." %}}
