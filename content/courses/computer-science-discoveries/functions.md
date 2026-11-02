---
title: Functions
units: [Interactive Animations and Games, Building Games]
summary: Create your own blocks with functions to organize your code and stop repeating yourself.
weight: 530
---

{{% param summary %}}

## Today's Objectives
- Create and use functions for blocks of code that perform a single high-level task within a program.
- Explain how functions allow programmers to reason about a program at a higher level.
- Explain the advantages of using functions in a program.

## Lesson Overview
### What new block would you add to Game Lab?
{{< collapse summary="Click here to reveal the answer." >}}

Whatever you want. Today, you'll learn to make your own blocks.

- Blocks like `velocityX`, `isTouching`, and `displace` are built from blocks you already knew, like the counter pattern and `if` statements.
- Someone else wrote those blocks. Now, you'll write yours.

{{</ collapse >}}

{{% define "Function" %}}

### How do you make your own blocks?
{{< video title="Functions" src="/videos/functions.mp4" poster="/images/video-poster-functions.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Use 2 steps: **define** a function to give a chunk of code a name, then **call** the function by its name to run that code.

This code draws a starry background and 2 planets:

```js {linenos=table}
drawBackground();
drawPlanet();
drawPlanet();
function drawBackground() {
  background("black");
  drawStar();
  drawStar();
  drawStar();
}
function drawStar() {
  fill("white");
  ellipse(randomNumber(0, 400), randomNumber(0, 400), 5, 5);
}
function drawPlanet() {
  fill(rgb(randomNumber(0, 255), randomNumber(0, 255), randomNumber(0, 255)));
  ellipse(randomNumber(50, 350), randomNumber(50, 350), 80, 80);
}
```

- Lines 4-17 define 3 functions. Defining a function doesn't run it.
- Lines 1-3 call functions. That's when the code inside actually runs.
- Line 3 calls `drawPlanet` a second time, so you get 2 planets in different spots and colors.
- Lines 6-8 call `drawStar` from inside `drawBackground`, since stars are part of the background.
- Name each function with a short description of what it does, like `drawPlanet`.

{{</ collapse >}}

### Why use functions?
{{< collapse summary="Click here to reveal the answer." >}}

They let you think about what your code does, not every detail of how it does it. That makes each function an abstraction.

This draw loop reads like a to-do list:

```js {linenos=table}
function draw() {
  drawBackground();
  movePlayer();
  checkCoin();
  drawSprites();
}
```

- **Organize your code:** move long chunks out of the draw loop into functions with clear names.
- **Stop repeating yourself:** write the code once, then call it as many times as you need.
- **Change code in one place:** fix or change a function once, and every call to it changes too.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: predict what the program will draw, then run it to check. Look for which functions get called, and how many times.
2. Levels 2-4: follow the instructions on each level. In Level 4, predict what happens when functions are defined in a different order.
3. Level 5: call a function in the draw loop, make a flyer reappear on the right side, change `setFlyer()` so the flyer starts at a random `y` and speed, or add code to `drawNight()` to draw a night scene. Then, in Level 6, answer the question in your own words.
4. Levels 7-9: use functions to build a collector game.
5. Level 10 (challenge): draw 2 scenes with 2 functions, build a paddle game, or draw one item in a function and call it many times to build a scene.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Function" %}}
{{% unit-journal-question-of-the-day question="How can programmers use functions to create their own abstractions?" hint="Draw a block labeled drawPlanet(), and write the code it hides inside. Then explain why a function counts as an abstraction." %}}
