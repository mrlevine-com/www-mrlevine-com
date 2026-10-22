---
title: "Mini-Project: Captioned Scenes"
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Plan and code a scene that combines shapes, sprites, and text, like a panel in a comic.
weight: 370
---

{{% param summary %}}

## Today's Objectives
- Use a structured process to plan and develop a program.

## Lesson Overview
### What will you make today?
{{< collapse summary="Click here to reveal the answer." >}}

A scene that combines shapes, sprites, and text. Think of it as a page in a story, a panel in a comic, or a scene on its own.

- You're not limited to shapes, sprites, and text. You can add variables and randomness too.
- Plan first with [the problem solving process]({{< relref "the-problem-solving-process.md" >}}): Define and Prepare in your Unit Journal, Try in Game Lab, then Reflect.

{{</ collapse >}}

### Which blocks can you use?
{{< collapse summary="Click here to reveal the answer." >}}

Everything you've learned in Game Lab so far:

| Use                 | Blocks                                                                                         |
|---------------------|------------------------------------------------------------------------------------------------|
| Background and shapes | `background(color)`, `rect(x, y, w, h)`, `ellipse(x, y, w, h)`, `line(x1, y1, x2, y2)`, and more |
| Colors and outlines | `fill`, `noFill`, `stroke`, `noStroke`, `strokeWeight`                                         |
| Sprites             | `var label = createSprite(x, y);`, `label.setAnimation("name");`, `drawSprites();`             |
| Sprite properties   | `label.rotation`, `label.scale`, `label.width`, `label.height`, `label.tint`, `label.alpha`    |
| Text                | `text("words", x, y, w, h)`, `textSize(pixels)`                                                |

{{</ collapse >}}

### How do you put shapes, sprites, and text together?
{{< collapse summary="Click here to reveal the answer." >}}

Code your scene back to front: background, then shapes, then sprites, then text.

This code draws two aliens floating in space past a few planets. Your animation names will match the ones you add in the Animation tab:

```js {linenos=table}
background("navy");
fill("green");
ellipse(100, 70, 120, 120);
fill("yellow");
ellipse(380, 0, 250, 250);
var alien1 = createSprite(110, 210);
alien1.setAnimation("alien1");
alien1.rotation = -15;
var alien2 = createSprite(270, 290);
alien2.setAnimation("alien2");
alien2.scale = 0.8;
drawSprites();
fill("white");
textSize(20);
text("Two aliens explore space.", 20, 120);
text("Next stop: the stars!", 200, 200);
```

- Lines 8 and 11 change a property after each sprite gets its animation.
- Line 12 draws both sprites on top of the planets.
- The text comes after `drawSprites()`, so it lands on top of the sprites.
- `fill` on line 13 colors the text, just like it colors shapes.

{{</ collapse >}}

### How will your captioned scene be graded?
| Criteria               | Full credit looks like                                                                                                                       |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Program Sequence       | You sequence your code so every shape, sprite, and line of text appears as intended, with none hidden behind others by mistake.             |
| Sprites and Properties | You create at least 2 sprites. After you set each one's animation, you change at least one of its properties: `rotation`, `scale`, `tint`, `alpha`, `width`, or `height`. |
| Position               | You place at least 2 shapes, 2 sprites, and 2 lines of text correctly using the coordinate system.                                          |
| Captioned Scene        | Your program follows your plan and clearly shows a captioned scene.                                                                         |

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Finish your plan first (see the Assignment). Then:

1. Level 1 (optional): look at an example captioned scene.
2. Levels 2-4: code your plan one part at a time: the background in level 2, sprites in level 3, and text in level 4. Click "Run" after each change, and check each part off on your sketch.
3. Level 5: review your scene, and check it against the rubric above.

Stuck? Pick one or two of these from the problem solving process:

- Define: reread the rubric, and say the problem in your own words.
- Prepare: write what you want in plain English, sketch it in your Unit Journal, or look back at programs you wrote in earlier lessons.
- Try: write one small piece of code at a time, and run it after every change.
- Reflect: compare your screen to your sketch. Ask a classmate to try your program or read your code.

Still stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Plan Your Captioned Scene ~15mins
Hand-draw a plan for a scene with at least 2 shapes, 2 sprites, and 2 lines of text.

1. Write 2-3 sentences describing your scene, including what your text will say.
2. Draw an 8 by 8 grid, and label its lines 0, 50, 100, and so on up to 400, across the top and down the side. Hand-draw your background on it using at least 2 shapes, then sketch your sprites and text on top. Label each shape with its command.
3. Make a table of your sprites and a table of your text. For example:
    | Sprite Label | Description  | Property to Change  |
    |--------------|--------------|---------------------|
    | `alien1`     | A blue alien | `rotation` and `scale` |

    | Text                        | Style                               |
    |-----------------------------|-------------------------------------|
    | "Two aliens explore space." | White, 20 pixels tall, at (20, 120) |

Idea too big? Shrink it: get the background, 2 sprites, and 2 lines of text working first, then add more if you have time.

{{% instructions-code-org-update %}}
