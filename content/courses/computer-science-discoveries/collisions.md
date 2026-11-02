---
title: Collisions
units: [Interactive Animations and Games, Building Games]
summary: Use collision blocks to make sprites push, stop, and bounce off each other.
weight: 510
---

{{% param summary %}}

## Today's Objectives
- Describe how abstractions can be built upon to develop even further abstractions.
- Model different types of interactions between sprites.

## Lesson Overview
### How could you make one sprite push another across the screen?
{{< collapse summary="Click here to reveal the answer." >}}

When they touch, give the second sprite the same velocity as the first. You already know every block you need.

This code makes a giraffe walk into a monkey and push it to the right:

```js {linenos=table}
var giraffe = createSprite(50, 200);
giraffe.setAnimation("giraffe");
giraffe.velocityX = 2;
var monkey = createSprite(250, 200);
monkey.setAnimation("monkey");
function draw() {
  background("white");
  if (giraffe.isTouching(monkey)) {
    monkey.velocityX = giraffe.velocityX;
  }
  drawSprites();
}
```

- Line 8 checks if they're touching. You don't need to think about how `isTouching` works. It hides that math for you.
- Line 9 makes the monkey move at the giraffe's speed, so they move together.
- To push down instead, use `velocityY`.

{{</ collapse >}}

{{% define "Abstraction" %}}

### Is there a block that pushes for you?
{{< collapse summary="Click here to reveal the answer." >}}

Yes: `giraffe.displace(monkey);` does the same job as lines 8-10 above, in one line.

Each block hides the one below it, so you can build bigger ideas without the details:

1. The counter pattern changes `x` a little every frame.
2. `velocityX` hides the counter pattern.
3. `isTouching` hides the math that compares sprite positions.
4. `displace` hides `isTouching` and velocity together.

{{</ collapse >}}

### Which collision block should you use?
{{< collapse summary="Click here to reveal the answer." >}}

Pick the block by what should happen when the sprites touch. Put it inside the draw loop, so it checks every frame.

| Block                   | What happens when `sprite` touches `target`                  | Example                       |
|-------------------------|--------------------------------------------------------------|-------------------------------|
| `sprite.displace(target)` | `sprite` pushes `target` out of the way.                     | A cart pushes the next cart.  |
| `sprite.collide(target)`  | `sprite` stops. `target` stays put.                          | An arrow stops at an apple.   |
| `sprite.bounce(target)`   | Both sprites bounce off each other.                          | Two bumper cars crash.        |
| `sprite.bounceOff(target)` | `sprite` bounces off. `target` stays put.                    | A basketball bounces off the floor. |

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: watch the giraffe push the monkey. Plan how you'd code it with blocks you already know.
2. Levels 2-3: code your plan to make the giraffe push the monkey right, then make an elephant push a hippo down.
3. Levels 4-5: try `displace`, then the other collision blocks.
4. Level 6: bounce a basketball off a floor, stop an arrow at an apple, make one cart push the next, or help someone push a suitcase. Then, in Level 7, open the "Rubric" tab first to see how to prove you understand collisions.
5. Level 8 (challenge): see a sprite's collider with `debug`, change a collider's shape, control `bounciness`, or make a scene where one sprite collects or deflects other sprites.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Draw the 4 Collision Types ~10mins
Hand-draw what each collision block does.

1. Make 4 rows, labeled `displace`, `collide`, `bounce`, and `bounceOff`.
2. In each row, draw 2 frames: just before the sprites touch, and just after. Add arrows to show which way each sprite moves.
3. Next to each row, write one thing in a game you'd use it for.

{{% unit-journal-question-of-the-day question="How can programmers build on abstractions to create further abstractions?" hint="Name the blocks that displace hides, and the blocks that those hide. Then explain how hiding those details made it easier to make one sprite push another." %}}
