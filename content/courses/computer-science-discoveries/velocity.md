---
title: Velocity
units: [Interactive Animations and Games, Building Games]
summary: Use velocity blocks to move sprites without writing the counter pattern yourself.
weight: 470
---

{{% param summary %}}

## Today's Objectives
- Describe the advantages of simplifying code by using higher level blocks.
- Use the velocity and rotationSpeed blocks to create and change sprite movements.

## Lesson Overview
### How would you simplify these instructions: "Step forward 1. Step forward 1. Step forward 1..."?
{{< collapse summary="Click here to reveal the answer." >}}

Say it once: "Keep stepping forward by 1." Nobody gives the same instruction over and over in real life.

- The counter pattern is like those repeated steps. Every frame, you tell the sprite to move again.
- Programming languages can hide repeated patterns like this inside a single block.
- Today, you'll use blocks in Game Lab that do the counter pattern for you.

{{</ collapse >}}

### How can one block replace the counter pattern?
{{< video title="Velocity" src="/videos/velocity.mp4" poster="/images/video-poster-velocity.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Set the sprite's `velocityX` once. Game Lab adds it to the sprite's `x` every frame for you.

These two programs move the alien the same way:

```js {linenos=table}
var sprite = createSprite(0, 200);
sprite.setAnimation("greenAlien");
function draw() {
  background("orange");
  sprite.x = sprite.x + 2;
  drawSprites();
}
```

```js {linenos=table}
var sprite = createSprite(0, 200);
sprite.setAnimation("greenAlien");
sprite.velocityX = 2;
function draw() {
  background("orange");
  drawSprites();
}
```

- In the second program, the counter pattern is still there. It's hidden inside `velocityX`.
- Line 3 runs just once, outside the draw loop, but the sprite keeps moving.
- Velocity is how fast a sprite moves in a direction. Bigger numbers move it faster.

{{</ collapse >}}

### Which velocity property should you use?
{{< collapse summary="Click here to reveal the answer." >}}

Pick the movement, then use a positive or negative number.

| Property                 | Positive number    | Negative number         |
|--------------------------|--------------------|-------------------------|
| `sprite.velocityX`       | Moves right        | Moves left              |
| `sprite.velocityY`       | Moves down         | Moves up                |
| `sprite.rotationSpeed`   | Spins clockwise    | Spins counterclockwise  |

Set `velocityX` and `velocityY` together to move diagonally. Set a property to 0 to stop that movement.

{{</ collapse >}}

### When does velocity go inside the draw loop?
{{< collapse summary="Click here to reveal the answer." >}}

When you want the movement to change while the program runs. Outside the draw loop sets how the sprite starts. Inside, usually in a conditional, changes it.

This code makes a robot take off once you press the space bar:

```js {linenos=table}
var robot = createSprite(200, 350);
robot.setAnimation("robot");
function draw() {
  background("skyblue");
  if (keyDown("space")) {
    robot.velocityY = -3;
  }
  drawSprites();
}
```

- Line 6 only runs while space is held, but the robot keeps flying after you let go. Its velocity stays at -3 until something changes it.
- With `robot.y = robot.y - 3;` on line 6 instead, the robot would stop as soon as you let go. Velocity makes movements like this much easier.

{{</ collapse >}}

### Why use blocks that hide code?
{{< collapse summary="Click here to reveal the answer." >}}

So you can spend your brainpower on harder problems instead of the details of simple ones.

- You write less code, and you don't have to rewrite the same pattern again and again.
- Your code is easier to read. `velocityX = 2` says what it does.
- Everything you'll do today is possible without these blocks, but it would be very complicated to code. You'll keep using blocks like these to build more and more complicated games.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: predict whether the velocity block or the counter pattern moves the sprite faster, then run it to check.
2. Levels 2-7: follow the instructions on each level to try `velocityX`, `velocityY`, and `rotationSpeed`.
3. Level 8: make a robot fly after you press the space bar, dip a paint brush in paint, or move a wizard's star across the screen.
4. Level 9: open the "Rubric" tab first to see how to prove you understand velocity.
5. Level 10 (challenge): change velocities 4 times, make objects burst from the center, bring a scene from a book or movie to life, or race sprites with keys.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-create %}}
{{% instructions-unit-journal-update %}}

### Design Your Own Block ~10mins
Hand-draw a new block you wish Game Lab had.

1. Draw the block, and write its name on it.
2. Under it, write what it would do and the code it would hide inside.
3. Write one way it would help you as a programmer.

{{% unit-journal-question-of-the-day question="How can programming languages hide complicated patterns so that it is easier to program?" hint="Write one counter pattern line, like sprite.x = sprite.x + 2;, next to the velocity block that replaces it. Then describe one movement you made today and how you made it." %}}
