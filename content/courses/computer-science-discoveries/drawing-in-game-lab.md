---
title: Drawing in Game Lab
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Write code that tells a computer where to draw shapes, what color to make them, and in what order.
weight: 290
---

{{% param summary %}}

## Today's Objectives
- Sequence code correctly to overlay shapes.
- Use a coordinate system to place elements on the screen.

## Lesson Overview
### How do you tell a computer what to draw?
{{< video title="Game Lab: Intro to Drawing" src="/videos/game-lab-intro-to-drawing.mp4" poster="/images/video-poster-game-lab-intro-to-drawing.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Use exact commands in a language the computer understands. A person can guess what you mean. A computer can't.

- Game Lab uses JavaScript.
- You can code with blocks or with text. Both are real code.
- Blocks: easier to remember commands, and no parentheses or semicolons to worry about.
- Text: easier to edit, and takes up less space.

{{</ collapse >}}

{{% define "Program" %}}

### What do the drawing commands do?
{{< collapse summary="Click here to reveal the answer." >}}

| Command                  | What it does                                        | What (x, y) marks   |
|--------------------------|-----------------------------------------------------|---------------------|
| `rect(x, y, w, h)`       | Draws a rectangle `w` wide and `h` tall             | Its top left corner |
| `ellipse(x, y, w, h)`    | Draws a circle or oval `w` wide and `h` tall        | Its center          |
| `fill(color)`            | Colors in every shape drawn after it                | Nothing             |

Reminder: x is the distance from the left edge, and y is the distance from the top edge. (0, 0) is the top left corner.

This code draws a blue square with a yellow circle in its middle:

```js {linenos=table}
fill("blue");
rect(100, 100, 200, 200);
fill("yellow");
ellipse(200, 200, 100, 100);
```

For colors, use names like `"red"`, `"green"`, or `"brown"`.

{{</ collapse >}}

### Why does the order of your code matter?
{{< video title="Game Lab: Adding Colors" src="/videos/game-lab-adding-colors.mp4" poster="/images/video-poster-game-lab-adding-colors.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Game Lab runs your code from top to bottom, one line at a time.

- Each new shape is drawn on top of the shapes before it.
- `fill` only colors shapes that come after it. It stays on until you use `fill` again.
- Fill is the color inside a shape. Stroke is the color of its border.

Swap the order from the last example, and the square now covers the circle completely:

```js {linenos=table}
fill("yellow");
ellipse(200, 200, 100, 100);
fill("blue");
rect(100, 100, 200, 200);
```

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change. Watching your shape move is how you learn what each number does. Read all instructions carefully.

When you get stuck:

1. Open the "Help & Tips" tab.
2. Hover over a block to see what it does. Click "Examples" for more.
3. Made a big mistake? Click "Version History" to go back to an earlier version.

{{</ collapse >}}

{{% define "Bug" %}}
{{% define "Debugging" %}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Program" "Bug" "Debugging" %}}
{{% unit-journal-question-of-the-day question="How can you communicate to a computer how to draw shapes on the screen?" %}}
