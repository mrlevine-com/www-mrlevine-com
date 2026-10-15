---
title: Text
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Add words to your scenes and control where they go and how they look.
weight: 360
---

{{% param summary %}}

## Today's Objectives
- Place text on the screen using a coordinate plane.
- Use arguments to control how text is displayed on a screen.

## Lesson Overview
### What's missing from your Game Lab scenes so far?
{{< collapse summary="Click here to reveal the answer." >}}

Text. Your characters can't talk yet, and your games can't show a score.

- Imagine a cartoon of an alien with an empty speech bubble. What should it say?
- Today, you'll fill in bubbles like that with code.
- Text is the last kind of thing you'll learn to put on the screen. Next, you'll make things move.

{{</ collapse >}}

### How do you put text on the screen?
{{< collapse summary="Click here to reveal the answer." >}}

Use `text("words", x, y)`. Put the words in quotes.

This code writes "Hello!" in big letters near the top left:

```js {linenos=table}
textSize(30);
text("Hello!", 50, 100);
```

- `(x, y)` marks the bottom left corner of the first letter, not the top left like `rect`.
- `textSize` sets how tall the letters are, in pixels. It starts at 12.
- Like `fill`, `textSize` changes all the text after it until you change it again.
- Text is drawn right away, like shapes. You don't need `drawSprites()`.
- Text that runs off the screen won't show up.

{{</ collapse >}}

### How do you change how your text looks?
{{< collapse summary="Click here to reveal the answer." >}}

Use the same color commands as shapes, and add a width and height to wrap long text.

The values you put into a command's parameters are called arguments. Change the arguments, and you change how the text looks:

| Command                        | What it does to text                                        |
|--------------------------------|-------------------------------------------------------------|
| `fill("red")`                  | Colors the letters                                          |
| `stroke("black")`              | Outlines the letters                                        |
| `strokeWeight(3)`              | Sets how thick the outline is                               |
| `text("words", x, y, w, h)`    | Wraps the text inside a box `w` wide and `h` tall. Now `(x, y)` is the box's top left corner. |

This code writes a long yellow sentence with a red outline that wraps to fit the screen:

```js {linenos=table}
textSize(40);
fill("yellow");
stroke("red");
strokeWeight(3);
text("Ada Lovelace was one of the first computer programmers!", 20, 20, 360, 360);
```

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: read the code with a partner. Predict what it will show and where, then run it.
2. Levels 2-3: follow the instructions on each level.
3. Level 4: reorder code so a strawberry sits on top of the lines but behind the text and eyes, fix a bug so a riddle appears, or add a score to a soccer field.
4. Level 5: open the "Rubric" tab first to see how to prove you understand text.
5. Level 6 (challenge): change text color, make white text stand out on a white background, wrap long text in a box, or make a scene for your favorite quote or your favorite book, movie, show, or game.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Caption a Scene ~10mins
Hand-draw a scene with a speech bubble, then write the code that would fill it in.

1. Draw a square for the 400 by 400 screen, with a character and an empty speech bubble.
2. Write what your character says inside the bubble. Mark the dot where the text starts (the bottom left of the first letter) and label it with its `(x, y)`.
3. Below the square, write the `textSize` and `text` code that would draw your words there.

{{% unit-journal-question-of-the-day question="How can you use text to improve your scenes and animations?" hint="Also list two ways drawing text is like drawing shapes, and one way it's different." %}}
