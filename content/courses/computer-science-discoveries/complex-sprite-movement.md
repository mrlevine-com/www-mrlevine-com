---
title: Complex Sprite Movement
units: [Interactive Animations and Games, Building Games]
summary: Combine velocity with the counter pattern to make sprites speed up, slow down, and jump with gravity.
weight: 500
---

{{% param summary %}}

## Today's Objectives
- Explain how individual programming constructs can be combined to create more complex behavior.
- Use sprite velocity with the counter pattern to create different types of sprite movement.

## Lesson Overview
### How could you make a sprite's jump look more real?
{{< collapse summary="Click here to reveal the answer." >}}

Make it slow down as it rises and speed up as it falls, like gravity does. You can do it with blocks you already know.

- In the side scroller, the frog moves up and down at the same speed the whole time. Its path makes a pointy triangle.
- A real jump starts fast, slows to a stop at the top, then speeds up on the way down. Its path makes a smooth curve.
- Today, you won't learn any new blocks. You'll combine ones you know in new ways.

{{</ collapse >}}

### What happens when you use the counter pattern on velocity?
{{< collapse summary="Click here to reveal the answer." >}}

The sprite speeds up or slows down. The counter pattern changes its speed a little every frame, instead of its position.

This code makes a ball fall faster and faster, like gravity:

```js {linenos=table}
var ball = createSprite(200, 0);
ball.setAnimation("ball");
function draw() {
  background("white");
  ball.velocityY = ball.velocityY + 0.5;
  drawSprites();
}
```

- Read line 5 as "`ball.velocityY` gets `ball.velocityY` plus 0.5."
- Frame 1, the ball moves down 0.5 pixels. Frame 2, it moves 1. Frame 3, it moves 1.5. It keeps getting faster.
- Count toward 0 instead, and the sprite slows down.
- Keep counting past 0, and the sprite reverses direction.

{{</ collapse >}}

### Which combination makes each movement?
{{< collapse summary="Click here to reveal the answer." >}}

Pick a velocity property, then pick how to count it inside the draw loop.

| Movement   | How                                                                                              |
|------------|--------------------------------------------------------------------------------------------------|
| Speed up   | Count `velocityX` (or `velocityY`) away from 0: `sprite.velocityX = sprite.velocityX + 0.2;`       |
| Slow down  | Count it toward 0, and stop at 0 with an `if` statement.                                          |
| Gravity    | Always add a little to `velocityY`: `sprite.velocityY = sprite.velocityY + 0.5;`                  |
| Jump       | Add gravity, set `velocityY` to a negative number when a key is pressed, and land with an `if` statement. |
| Curve      | Keep `velocityX` the same, and count `velocityY` up or down.                                       |

This code makes an alien jump with gravity whenever you press the space bar:

```js {linenos=table}
var alien = createSprite(200, 350);
alien.setAnimation("alien");
function draw() {
  background("navy");
  alien.velocityY = alien.velocityY + 0.5;
  if (keyWentDown("space")) {
    alien.velocityY = -10;
  }
  if (alien.y > 350) {
    alien.y = 350;
    alien.velocityY = 0;
  }
  drawSprites();
}
```

- Line 5 is gravity. It pulls the alien down a little more every frame.
- Line 7 launches the alien up fast. Gravity slows it down, stops it, then pulls it back down in a curve.
- Lines 9-12 land the alien on the ground.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: predict how the sprite will move before you run the code. Run it to check.
2. Levels 2-4: make a sprite speed up sideways, speed up vertically, then slow down.
3. Level 5: make a bubble rise faster and faster, help a mouse slow down and back away from a cat, or make a falling balloon float away.
4. Level 6: open the "Rubric" tab first to see how to prove you understand velocity with the counter pattern.
5. Level 7 (challenge): curve a plane around spikes, stop a car before the top of the screen, make an alien jump, or race cars, spaceships, or animals and slow them down after the finish.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Track a Falling Ball ~10mins
Hand-draw what happens to the ball in the gravity code above over 5 frames. It starts at `y` = 0 with a `velocityY` of 0.

1. Make a table with 3 columns: "Frame," "`velocityY`," and "`y`." Fill in frames 1 to 5. Each frame, add 0.5 to `velocityY` first, then add `velocityY` to `y`.
2. Next to the table, draw a tall rectangle as the screen, and draw a dot for the ball at each frame's `y`.
3. Below the drawing, write what you notice about the space between the dots.

{{% unit-journal-question-of-the-day question="How can previous blocks be combined in new patterns to make interesting movements?" hint="Make 2 lists: new things you can make sprites do after today, and new blocks you learned today. Then explain how the second list can be so short." %}}
