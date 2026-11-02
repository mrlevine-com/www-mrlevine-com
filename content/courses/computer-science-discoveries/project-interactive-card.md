---
title: "Project: Interactive Card"
units: [Interactive Animations and Games, Animation and Interaction]
summary: Plan and code an interactive card that reacts to the keyboard and mouse, then share it with someone you care about.
weight: 450
days: 2
---

{{% param summary %}}

## Today's Objectives
- Apply an iterator pattern to variables or properties in a loop.
- Sequence commands to draw in the proper order.
- Use conditionals to react to keyboard input or changes in variables / properties.

## Lesson Overview
### What will you make?
{{< collapse summary="Click here to reveal the answer." >}}

An interactive card for someone you care about, like a birthday card, a thank-you card, or a card to cheer someone up. When you finish, you can send it to them by text or email.

- Your card mixes shapes, text, and sprites that move and react to the keyboard and mouse.
- Pick who it's for first. Then ask: what would make this card special for them?
- Plan first with [the problem solving process]({{< relref "the-problem-solving-process.md" >}}): Define and Prepare in your Unit Journal, Try in Game Lab, then Reflect.

{{</ collapse >}}

### Which blocks can you use?
{{< collapse summary="Click here to reveal the answer." >}}

Everything you've learned in Game Lab so far:

| Use                      | Blocks                                                                                          |
|--------------------------|-------------------------------------------------------------------------------------------------|
| Background, shapes, text | `background`, `rect`, `ellipse`, `line`, `text`, `textSize`, `fill`, `noFill`, `stroke`, `noStroke`, `strokeWeight` |
| Sprites                  | `createSprite`, `setAnimation`, `drawSprites`, and properties like `x`, `y`, `rotation`, `scale`, `tint`, `alpha`, `visible` |
| Movement                 | The counter pattern, like `sprite.x = sprite.x + 1;`, and `randomNumber(min, max)`             |
| User input               | `keyDown`, `keyWentDown`, `mouseDown`, `mouseWentDown`, `mouseDidMove`, `World.mouseX`, `World.mouseY` |
| Conditionals             | `if`, `if/else`, and comparisons like `>`, `<`, and `==`                                       |

{{</ collapse >}}

### How do you put it all together?
{{< collapse summary="Click here to reveal the answer." >}}

Create your sprites once, outside the draw loop. Put everything that changes inside it.

This birthday card floats a balloon, wobbles a star, and reacts to the keyboard and mouse. Your animation names will match the ones you add in the Animation tab:

```js {linenos=table}
var balloon = createSprite(100, 400);
balloon.setAnimation("balloon");
var cake = createSprite(200, 300);
cake.setAnimation("cake");
var star = createSprite(300, 100);
star.setAnimation("star");
function draw() {
  background("lavender");
  balloon.y = balloon.y - 2;
  star.rotation = randomNumber(-10, 10);
  if (balloon.y < 0) {
    balloon.y = 400;
  }
  if (keyDown("space")) {
    cake.scale = cake.scale + 0.01;
  }
  if (mouseWentDown("leftButton")) {
    star.x = randomNumber(50, 350);
  }
  drawSprites();
  fill("purple");
  textSize(30);
  text("Happy Birthday!", 90, 50);
}
```

- Line 9 moves the balloon smoothly with the counter pattern, also called an iterator pattern. Line 10 moves the star randomly. Your card needs both kinds of movement.
- Lines 11-13 react to a sprite property, and lines 14-19 react to 2 types of user input.
- The background, `drawSprites()`, and text are all inside the draw loop, because the background covers up everything each frame.
- Setting a property to a plain number in the draw loop, like `cake.scale = 0.4;`, doesn't count as updating it unless it's inside a conditional.

{{</ collapse >}}

### How will your interactive card be graded?
| Criteria                   | Full credit looks like                                                                                                                                         |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Peer Feedback and Sequence | You give thoughtful feedback to a classmate and improve your card based on the feedback you get. Every element appears as intended, with setup code outside the draw loop and changing code inside it. |
| Sprites and Movement       | You create at least 3 sprites, placed using the coordinate system, each with at least one property updating in the draw loop. Some move randomly with `randomNumber`, and some move smoothly with the counter pattern. |
| User Input                 | Your card responds to at least 2 different types of user input, like `keyDown("left")` and `keyDown("space")`, or a key and the mouse.                       |
| Conditionals               | You use at least 3 conditionals inside the draw loop: at least 2 respond to user input, and at least 1 is triggered by a variable or sprite property, like `sprite.y > 300` or `World.mouseX < 200`. |
| Variables (optional)       | You create at least 2 variables that aren't sprites, and their values update in the draw loop and change how your card runs.                                  |

### How do you get through the levels?
{{< collapse summary="Click here to reveal the answer." >}}

Finish your plan first (see the Assignment). Then:

1. Level 1: try the example card. Look for clues that it uses sprites, conditionals, and the counter pattern.
2. Level 2 (optional): look at more example cards for ideas.
3. Levels 3-6: code your plan one part at a time: the background in level 3, sprites in level 4, user input in level 5, and other conditionals in level 6. Click "Run" after each change, and check each part off on your sketch.
4. Level 7: finish your card, and check it against the rubric above.
5. Level 8: answer the reflection survey. Your answers are anonymous.

Stuck? Pick one or two of these from the problem solving process:

- Define: reread the rubric, and say the problem in your own words.
- Prepare: write what you want in plain English, sketch it in your Unit Journal, or look back at programs you wrote in earlier lessons.
- Try: write one small piece of code at a time, and run it after every change.
- Reflect: compare your screen to your sketch. Ask a classmate to try your program or read your code.

Still stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Plan Your Interactive Card ~20mins
Hand-draw a plan for a card with at least 3 sprites, 2 types of user input, and 3 conditionals.

1. Write 2-3 sentences describing your card, who it's for, and how they'll interact with it.
2. Draw an 8 by 8 grid, and label its lines 0, 50, 100, and so on up to 400, across the top and down the side. Hand-draw your background, sprites, and text on it, and label each shape with its command.
3. Make a table of your sprites and a table of your conditionals. For example:
    | Sprite Label | Image(s)  | Properties That Change                                  |
    |--------------|-----------|---------------------------------------------------------|
    | `balloon`    | A balloon | `y` goes down by 2 each frame, so it floats up (counter pattern) |

    | If / Else    | Condition              | Action                     |
    |--------------|------------------------|----------------------------|
    | `if`         | `balloon.y < 0`        | Move the balloon back to the bottom |

Idea too big? Shrink it: get the background, 3 sprites, and 1 conditional working first, then add more if you have time.

{{% instructions-code-org-update %}}

### Review a Classmate's Card ~15mins
Give a classmate feedback on their card, then use the feedback you get to improve yours.

1. Write one thing you want feedback on, then swap cards with a classmate.
2. Check their card against each rubric row above. Then write one "I like...," one "I wish...," and one "What if..." for them.
3. Back at your card, write the most helpful feedback you got and the changes you'll make. Then make them.
