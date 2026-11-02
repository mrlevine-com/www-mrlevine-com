---
title: Keyboard Input
units: [Interactive Animations and Games, Animation and Interaction]
summary: Use keyDown and if statements to control sprites with the keyboard.
weight: 430
---

{{% param summary %}}

## Today's Objectives
- Move sprites in response to keyboard input.
- Use conditionals to react to keyboard input.

## Lesson Overview
### How could user input make your programs better?
{{< collapse summary="Click here to reveal the answer." >}}

It lets the user control what happens, which turns an animation into something you can play. So far, your programs have run without any input from the user.

- A user can give input with a keyboard, a mouse, a touchscreen, and more.
- Today, you'll use the keyboard to move sprites.

{{</ collapse >}}

### How do you check whether a key is pressed?
{{< collapse summary="Click here to reveal the answer." >}}

Use `keyDown("key")`. It's a Boolean expression: `true` while the key is held down, `false` when it's not.

- Put the key's name in quotes: `"left"`, `"right"`, `"up"`, `"down"`, `"space"`, or a letter like `"a"`.
- Find it in the "Game Lab" drawer of the toolbox.

{{</ collapse >}}

### How do you move a sprite with the arrow keys?
{{< collapse summary="Click here to reveal the answer." >}}

Put `keyDown` inside an `if` statement in the draw loop. Inside the `if`, use the counter pattern to move the sprite.

This code moves a fish left and right with the arrow keys:

```js {linenos=table}
var fish = createSprite(200, 200);
fish.setAnimation("fish");
function draw() {
  background("lightblue");
  if (keyDown("left")) {
    fish.x = fish.x - 3;
  }
  if (keyDown("right")) {
    fish.x = fish.x + 3;
  }
  drawSprites();
}
```

- Line 5 checks the left arrow every frame. While it's held down, line 6 moves the fish 3 pixels left.
- Lines 8-10 do the same for the right arrow. Each key gets its own `if` statement.
- Add `"up"` and `"down"` the same way, but change `y` instead of `x`.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: predict what happens when you press a key, then run it to check.
2. Levels 2-4: follow the instructions on each level.
3. Level 5: move a fish with the left arrow key, or debug a turtle that breaks when it moves left or won't move at all.
4. Level 6: open the "Rubric" tab first to see how to prove you understand keyboard input.
5. Level 7 (challenge): count space bar presses with `keyWentDown`, change a sprite's animation for each direction, add a speed boost, play music with keys, or make a simple version of your favorite game.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-question-of-the-day question="How can your programs react to user input?" hint="Pick a program you made in an earlier lesson. Draw it, and label which keys you'd add and what each one would do. Then write the `if` statement for one of those keys." %}}
