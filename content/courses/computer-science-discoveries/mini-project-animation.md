---
title: "Mini-Project: Animation"
units: [Interactive Animations and Games, Animation and Interaction]
summary: Plan and code an animated scene that uses random numbers and the counter pattern to make sprites move.
weight: 410
---

{{% param summary %}}

## Today's Objectives
- Use a structured process to plan and develop a program.

## Lesson Overview
### What will you make today?
{{< collapse summary="Click here to reveal the answer." >}}

An animated scene: shapes, sprites, and text, with at least 2 things moving in different ways.

- It's like your captioned scene, but now it moves.
- One thing should move randomly with `randomNumber`. Another should move with the counter pattern, like `sprite.x = sprite.x + 1`.
- Plan first with [the problem solving process]({{< relref "the-problem-solving-process.md" >}}): Define and Prepare in your Unit Journal, Try in Game Lab, then Reflect.

{{</ collapse >}}

### Which types of movement can you use?
{{< collapse summary="Click here to reveal the answer." >}}

Pick a property, then pick random or counter pattern. Put the line inside the draw loop.

| Movement                       | Example                                         |
|--------------------------------|-------------------------------------------------|
| Shake or jump around (random)  | `sprite.x = randomNumber(200, 220);`            |
| Slide right, left, up, or down | `sprite.x = sprite.x + 2;` or `sprite.y = sprite.y - 2;` |
| Spin                           | `sprite.rotation = sprite.rotation + 3;`        |
| Grow or shrink                 | `sprite.scale = sprite.scale + 0.01;`           |
| Fade in or out                 | `sprite.alpha = sprite.alpha - 0.01;`           |

Other properties work too: `y`, `tint`, `width`, and `height`.

{{</ collapse >}}

### Which code goes inside the draw loop, and which goes outside?
{{< collapse summary="Click here to reveal the answer." >}}

Outside: create your sprites and variables once. Inside: everything that's drawn each frame.

This code makes a balloon float up while a bird flaps randomly:

```js {linenos=table}
var balloon = createSprite(100, 380);
balloon.setAnimation("balloon");
var bird = createSprite(300, 100);
bird.setAnimation("bird");
function draw() {
  background("skyblue");
  fill("green");
  rect(0, 350, 400, 50);
  balloon.y = balloon.y - 1;
  bird.y = randomNumber(95, 105);
  drawSprites();
  fill("black");
  textSize(20);
  text("Up, up, and away!", 20, 30);
}
```

- Lines 1-4 run once to set up the sprites.
- Lines 6-8 draw the background and grass every frame, so old frames get covered.
- Line 9 uses the counter pattern. Line 10 uses random numbers.
- Text goes after `drawSprites()` (line 11), so it lands on top.

{{</ collapse >}}

### How will your animated scene be graded?
| Criteria               | Full credit looks like                                                                                                                                           |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Program Sequence       | You sequence your code so nothing is hidden by mistake, and you put code in and out of the draw loop correctly.                                                 |
| Sprites and Properties | You create at least 2 sprites outside the draw loop. Each one has at least one property (`x`, `y`, `rotation`, `scale`, `tint`, `alpha`, `width`, or `height`) that changes inside the draw loop. |
| Position and Movement  | You place at least 2 shapes, 2 sprites, and 2 lines of text correctly using the coordinate system. At least 2 things move in different ways: one with `randomNumber`, one with the counter pattern. |
| Variables (optional stretch) | You create at least 2 variables that aren't sprites, update them in the draw loop, and use them to change what's on the screen.                         |

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Finish your plan first (see the Assignment). Then:

1. Level 1 (optional): look at an example animated scene.
2. Levels 2-4: code your plan one part at a time: the background in level 2, sprites in level 3, and text in level 4. Click "Run" after each change, and check each part off on your sketch.
3. Level 5: add movement, one sprite at a time.
4. Level 6: review your scene, and check it against the rubric above.

Stuck? Pick one or two of these from the problem solving process:

- Define: reread the rubric, and say the problem in your own words.
- Prepare: write what you want in plain English, sketch it in your Unit Journal, or look back at programs you wrote in earlier lessons.
- Try: write one small piece of code at a time, and run it after every change.
- Reflect: compare your screen to your sketch. Ask a classmate to try your program or read your code.

Still stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Plan Your Animated Scene ~15mins
Hand-draw a plan for an animated scene with at least 2 shapes, 2 sprites, and 2 lines of text.

1. Write 2-3 sentences describing your scene, including what moves and how.
2. Draw an 8 by 8 grid, and label its lines 0, 50, 100, and so on up to 400, across the top and down the side. Hand-draw how your scene looks when it starts, and label each shape, sprite, and line of text. Draw an arrow on each sprite that moves, showing which way it goes.
3. Make a table of your sprites and a table of your text. For example:
    | Sprite Label | Description    | Property to Change | Counter Pattern or Random? |
    |--------------|----------------|--------------------|----------------------------|
    | `balloon`    | A red balloon  | `y`                | Counter pattern            |
    | `bird`       | A flapping bird | `y`               | Random                     |

    | Text                | Style                              |
    |---------------------|------------------------------------|
    | "Up, up, and away!" | Black, 20 pixels tall, at (20, 30) |

Idea too big? Shrink it: get the background and 2 moving sprites working first, then add more if you have time.

{{% instructions-code-org-update %}}
