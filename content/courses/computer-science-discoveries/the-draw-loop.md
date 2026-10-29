---
title: The Draw Loop
units: [Interactive Animations and Games, Animation and Interaction]
summary: Use the draw loop to turn still drawings into animations.
weight: 390
---

{{% param summary %}}

## Today's Objectives
- Explain how the draw loop allows for the creation of animations in Game Lab.
- Use the draw loop in combination with the randomNumber() command, shapes, and sprites to make simple animations.

## Lesson Overview
### How does a flipbook trick your eyes into seeing motion?
{{< collapse summary="Click here to reveal the answer." >}}

It shows you many pictures in a row, each a little different from the last. Flip fast enough, and your eyes blur them into smooth motion.

- Each page of the flipbook is one picture in the animation.
- Movies, cartoons, and GIFs work the same way.
- So far, your programs have drawn one still picture. Today, you'll make them draw many.

{{</ collapse >}}

{{% define "Frame" %}}

### How do you animate your drawings in Game Lab?
{{< video title="Introduction to the Draw Loop" src="/videos/introduction-to-the-draw-loop.mp4" poster="/images/video-poster-introduction-to-the-draw-loop.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Put your drawing code inside the `draw` function. Game Lab runs it over and over, which is why it's called the "draw loop."

```js {linenos=table}
function draw() {
  ellipse(randomNumber(0, 400), randomNumber(0, 400));
}
```

- Each time `draw` runs, Game Lab draws a new frame, like turning a page in a flipbook.
- It runs 30 times a second. `World.frameRate` stores that speed, and you can set it from 1 to 60.
- You never call `draw()` yourself. Game Lab calls it for you.
- Use only one `draw` function per program.

{{</ collapse >}}

### Which code goes inside the draw loop, and which goes outside?
{{< collapse summary="Click here to reveal the answer." >}}

Outside sets up how your program starts. Inside is for things that change while it runs.

This code draws teal dots in random spots forever:

```js {linenos=table}
noStroke();
fill("teal");
function draw() {
  ellipse(randomNumber(0, 400), randomNumber(0, 400));
}
```

1. Lines 1-2 run first, one time, to set the color.
2. Lines 3-5 run next, over and over, forever. Each frame adds one new dot.

The draw loop always runs after all your other code, no matter where it sits in your program.

{{</ collapse >}}

### How do you animate a sprite?
{{< collapse summary="Click here to reveal the answer." >}}

Change a sprite property inside the draw loop, then draw a background and the sprite again.

This code makes an alien shake back and forth:

```js {linenos=table}
var sprite = createSprite(100, 200);
sprite.setAnimation("greenAlien");
function draw() {
  background("orange");
  sprite.x = randomNumber(200, 220);
  drawSprites();
}
```

- Lines 1-2 create the sprite once, outside the draw loop.
- Line 5 gives the sprite a new random `x` every frame, so it jumps around between 200 and 220.
- Line 4 covers up the last frame. Each frame is like a see-through sheet laid on top of the last one. Skip the background, and you'll see a blurry trail of every old sprite.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Levels 1-3 (shapes): predict what each program will draw, then run it. In Level 2, add orange circles next to the green ones.
2. Levels 4-5 (sprites): change the numbers in `randomNumber`, then make the second sprite shake like the first.
3. Level 6: make two aliens dance using `rotation`, fix a blurry sprite, or fix a sprite that won't move.
4. Level 7: open the "Rubric" tab first to see how to prove you understand the draw loop.
5. Level 8 (challenge): animate animals jumping on a couch, a rainbow snake, your favorite animal, a food pun, or your scene from last lesson.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-create %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Frame" %}}
{{% unit-journal-question-of-the-day question="How can you animate your images in Game Lab?" hint="Draw 3 frames of the shaking alien above, side by side, with the alien in a slightly different spot in each. Then explain how the draw loop turns frames like these into an animation." %}}
