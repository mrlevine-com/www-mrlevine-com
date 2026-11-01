---
title: Sprite Movement
units: [Interactive Animations and Games, Animation and Interaction]
summary: Use the counter pattern to move sprites on purpose.
weight: 400
---

{{% param summary %}}

## Today's Objectives
- Identify which sprite properties need to be changed, and in what way, to achieve a specific movement.
- Use the counter pattern to increment or decrement sprite properties.

## Lesson Overview
### What would happen if you kept adding to a sprite's `x` property?
{{< collapse summary="Click here to reveal the answer." >}}

It would slide to the right, a little more every frame. So far, the draw loop has made sprites jump around randomly. Today, you'll make them move on purpose.

- Keep adding to `y`, and the sprite slides down. In Game Lab, `y` gets bigger as you go down the screen.
- Keep adding to `rotation`, and it spins. Keep adding to `scale`, and it grows.
- Change more than one property at a time to combine movements.

{{</ collapse >}}

### How do you control a sprite's movement?
{{< video title="Sprite Movement" src="/videos/sprite-movement.mp4" poster="/images/video-poster-sprite-movement.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Use the **counter pattern**: inside the draw loop, set a property to itself plus (or minus) a number. It counts up or down by that number every frame.

This code makes an alien walk to the right:

```js {linenos=table}
var sprite = createSprite(0, 200);
sprite.setAnimation("greenAlien");
function draw() {
  background("orange");
  sprite.x = sprite.x + 2;
  drawSprites();
}
```

- Read line 5 as "`sprite.x` gets `sprite.x` plus 2." Each frame, the sprite moves 2 pixels right of where it was.
- Bigger numbers make it move faster. Try `+ 5`.
- Subtract instead to count down: `sprite.x = sprite.x - 2;` moves it left.
- Movement is just a change in position. Change `x` to move sideways. Change `y` to move up or down.

{{</ collapse >}}

### Which property should you change for each movement?
{{< collapse summary="Click here to reveal the answer." >}}

Pick the property, then pick add (count up) or subtract (count down). Put the line inside the draw loop.

| Movement                | Example                                                    |
|-------------------------|------------------------------------------------------------|
| Right (or left)         | `sprite.x = sprite.x + 1;` (use `- 1` for left)            |
| Down (or up)            | `sprite.y = sprite.y + 1;` (use `- 1` for up)              |
| Spin clockwise (or counterclockwise) | `sprite.rotation = sprite.rotation + 3;` (use `- 3` for counterclockwise) |
| Grow (or shrink)        | `sprite.scale = sprite.scale + 0.01;` (use `- 0.01` to shrink) |
| Diagonal                | Change `x` and `y` on two lines, one after the other.      |

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: read the program and predict what the counter will show. Run it to check, then watch the video above.
2. Levels 2-5: follow the instructions on each level.
3. Level 6: make a frying pan spin, fix a motorcycle going the wrong way, or make gears rotate together. To fix the motorcycle, watch the "Watchers" panel to see its properties change each frame.
4. Level 7: open the "Rubric" tab first to see how to prove you understand the counter pattern.
5. Level 8 (challenge): make fish wiggle, use ellipses to make bubbles rise, add a shark, a falling starfish, or more sea creatures, or animate your favorite dance moves or school activity.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-question-of-the-day question="How can you control sprite movement in Game Lab?" hint="Draw a sprite in 3 frames as it moves diagonally, and label each arrow between frames with the counter pattern code that moved it. Then name one movement you'd make with random numbers and one you'd make with the counter pattern." %}}
