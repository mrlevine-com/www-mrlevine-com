---
title: Mouse Input
units: [Interactive Animations and Games, Animation and Interaction]
summary: Use if/else statements and the mouse to make your programs react in more ways.
weight: 440
---

{{% param summary %}}

## Today's Objectives
- Respond to a variety of types of user input.
- Use an if-else statement to control the flow of a program.

## Lesson Overview
### How do you make a program do one thing if a condition is true, and something else if it's false?
{{< video title="If/Else Statements" src="/videos/game-lab-if-else-statements.mp4" poster="/images/video-poster-game-lab-if-else-statements.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Use an **if/else statement**. If the condition is true, the code under `if` runs. If it's false, the code under `else` runs instead.

This code moves an alien right while you hold the right arrow, and left the rest of the time:

```js {linenos=table}
var sprite = createSprite(200, 200);
sprite.setAnimation("greenAlien");
function draw() {
  background("white");
  if (keyDown("right")) {
    sprite.x = sprite.x + 2;
  } else {
    sprite.x = sprite.x - 2;
  }
  drawSprites();
}
```

- Exactly one of the two parts runs every frame: line 6 or line 8, never both.
- To add `else` to an `if` block, click the plus button at the bottom of the block.
- Use a plain `if` when nothing should happen while the condition is false. Use `if/else` when you want 2 different things to happen.

{{</ collapse >}}

{{% define "Conditionals" %}}

### How can your program react to the mouse?
{{< collapse summary="Click here to reveal the answer." >}}

Put a mouse command in a conditional inside the draw loop. Each one checks the mouse in a different way:

| Command                         | What it checks                                                                       |
|---------------------------------|--------------------------------------------------------------------------------------|
| `mouseDown("leftButton")`       | True every frame the button is held down                                             |
| `mouseWentDown("leftButton")`   | True only on the one frame the button is first pressed                               |
| `mouseWentUp("leftButton")`     | True only on the one frame the button is let go                                      |
| `mouseDidMove()`                | True on any frame the mouse moves                                                    |
| `World.mouseX`, `World.mouseY`  | Not true or false: the mouse's position. Compare it, like `World.mouseY > 300`.      |

The keyboard works the same way: `keyWentDown("space")` and `keyWentUp("space")` are true for just one frame, unlike `keyDown("space")`.

{{</ collapse >}}

### When should you use `mouseDown` instead of `mouseWentDown`?
{{< collapse summary="Click here to reveal the answer." >}}

Use `mouseDown` for something that keeps happening while the button is held. Use `mouseWentDown` for something that happens once per click.

This code spins the alien while you hold the button, and grows it a little each time you click:

```js {linenos=table}
var sprite = createSprite(200, 200);
sprite.setAnimation("greenAlien");
function draw() {
  background("skyblue");
  if (mouseDown("leftButton")) {
    sprite.rotation = sprite.rotation + 5;
  }
  if (mouseWentDown("leftButton")) {
    sprite.scale = sprite.scale + 0.1;
  }
  drawSprites();
}
```

- Hold the button for 1 second, and line 6 runs about 30 times, once per frame.
- That same click makes line 9 run only once.
- Want a sprite to follow the mouse? Set `sprite.x = World.mouseX;` and `sprite.y = World.mouseY;` inside the draw loop.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: predict what the if/else program will do, then run it to check.
2. Levels 2-5: follow the instructions on each level.
3. Level 6: move a ladybug only when the mouse is near the bottom, move a ghost toward the mouse, swap an emoji on click, or show musical notes while the mouse is pressed.
4. Level 7: open the "Rubric" tab first to see how to prove you understand mouse input and if/else.
5. Level 8 (challenge): reverse spirals on a click, make a bee follow (or buzz around) the mouse, shake a salt shaker as the mouse moves, or make emoji art or a food scene that changes with the mouse.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Draw One Click, Frame by Frame ~10mins
Hand-draw what each mouse command reports during one click.

1. Draw 5 boxes in a row, labeled "Frame 1" to "Frame 5." Under them, draw the mouse button: up in frame 1, down in frames 2-4, and up again in frame 5.
2. Under each frame, write `true` or `false` for `mouseDown`, `mouseWentDown`, and `mouseWentUp`.
3. Circle the command you'd use to count clicks, and explain why in one sentence.

{{% unit-journal-question-of-the-day question="What are more ways that the computer can react to user input?" hint="Pick 3 different input commands from today, like keyDown, mouseWentDown, or mouseDidMove. For each one, give an example of when you'd use it in a program." %}}
