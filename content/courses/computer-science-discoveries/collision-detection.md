---
title: Collision Detection
units: [Interactive Animations and Games, Building Games]
summary: Detect when sprites touch, and see how one block can hide a lot of hard math.
weight: 480
---

{{% param summary %}}

## Today's Objectives
- Describe how abstractions help to manage the complexity of code.
- Detect when sprites are touching or overlapping, and change the program in response.

## Lesson Overview
### How could a computer tell whether two sprites are touching?
{{< collapse summary="Click here to reveal the answer." >}}

It uses math. A computer can't "see" your sprites the way you can. All it knows are their properties, like `x`, `y`, `width`, and `height`.

- In many games, sprites change when they touch: a player grabs a coin, or a car crashes.
- To make that happen, your program needs to check, every frame, whether the sprites are touching.
- Today, you'll try the math yourself, then learn a block that does it for you.

{{</ collapse >}}

### How do you use math to check whether two sprites are touching?
{{< collapse summary="Click here to reveal the answer." >}}

Compare the distance between their centers to their sizes. This works for 2 square sprites on the same line, where `x` is the center of each square:

| Sprite   | `x` | `width` |
|----------|-----|---------|
| sprite 1 | 5   | 4       |
| sprite 2 | 8   | 4       |

1. Subtract the `x` positions to find the distance between their centers: 8 - 5 = 3.
2. Divide each `width` by 2 to find the distance from each center to its edge, then add them: 2 + 2 = 4.
3. Compare the two numbers:
    - Distance is bigger than the sum: not touching.
    - Distance equals the sum: barely touching.
    - Distance is smaller than the sum: overlapping. Here, 3 is smaller than 4, so these sprites overlap.

That's just for sprites on the same line. Sprites that can move anywhere need the same math for `y` and `height` too, every frame.

{{</ collapse >}}

{{% define "Abstraction" %}}

### How do you detect collisions in Game Lab?
{{< collapse summary="Click here to reveal the answer." >}}

Use `sprite.isTouching(target)`. It's `true` when the sprites touch and `false` when they don't, so put it in an `if` statement.

This code makes 2 cars drive toward each other and stop when they crash:

```js {linenos=table}
var car1 = createSprite(50, 200);
car1.setAnimation("car1");
var car2 = createSprite(350, 200);
car2.setAnimation("car2");
car1.velocityX = 2;
car2.velocityX = -2;
function draw() {
  background("gray");
  if (car1.isTouching(car2)) {
    car1.velocityX = 0;
    car2.velocityX = 0;
  }
  drawSprites();
}
```

- Line 9 hides all the math from the last question inside one block. That's an abstraction: you think about "are they touching?" instead of the details.
- Want to see the box Game Lab uses to check for touching? Add `car1.debug = true;` before the draw loop.
- Collision happening too early? Your picture probably has empty space around it. In the Animation tab, click the crop icon to trim it.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: play the sample game, and watch what happens when the sprites touch.
2. Levels 2-5: follow the instructions on each level. Level 2's code looks overwhelming on purpose: it's the math that `isTouching` hides, so you don't need to understand every line. In Level 5, fix the bug in the Animation tab, not the code.
3. Level 6: fix code that won't detect a collision, improve collisions for round sprites, or make a mouse run away when it's touched.
4. Level 7: open the "Rubric" tab first to see how to prove you understand collision detection.
5. Level 8 (challenge): improve collisions for angled sprites, fix code that adds too many points, make an emoji happy or sad with an `if`-`else`, combine 2 foods into a new one when they touch, or animate your favorite sport.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Abstraction" %}}
{{% unit-journal-question-of-the-day question="How can programming help make complicated problems more simple?" hint="Draw a number line from 0 to 20 with 2 squares on it, and label each square's x and width. Show the math that tells whether they touch. Then explain what isTouching hides from you, and why that helps." %}}
