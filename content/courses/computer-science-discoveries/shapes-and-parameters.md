---
title: Shapes and Parameters
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Use parameters to control the size of your shapes and the color of your background.
weight: 300
---

{{% param summary %}}

## Today's Objectives
- Use and reason about drawing commands with multiple parameters.

## Lesson Overview
### What does `rect` need to draw rectangles of different sizes?
{{< collapse summary="Click here to reveal the answer." >}}

Two more inputs: a width and a height.

- `x` and `y` only tell `rect` where to draw.
- To change what a block does, give it more inputs. These inputs are called parameters.

{{</ collapse >}}

{{% define "Parameter" %}}

### How do the width and height parameters work?
{{< collapse summary="Click here to reveal the answer." >}}

`rect(x, y, w, h)` and `ellipse(x, y, w, h)` take 4 parameters, in this order:

1. `x`: how far from the left edge.
2. `y`: how far from the top edge.
3. `w`: how wide the shape is.
4. `h`: how tall the shape is.

`w` and `h` are optional. Leave them off, and `rect` draws a 50 by 50 square. In blocks, click the arrow on the right side of `rect` or `ellipse` to show or hide them.

This code draws a long blue rectangle above a shorter red one:

```js {linenos=table}
fill("blue");
rect(50, 50, 300, 100);
fill("red");
rect(50, 200, 150, 100);
```

To make the red rectangle longer than the blue one, change its `w` (line 4, third number) to something bigger than `300`.

{{</ collapse >}}

### How do you color the whole background?
{{< collapse summary="Click here to reveal the answer." >}}

Use `background(color)`. It paints the entire canvas one color.

- Put it first. It covers everything drawn before it.
- It takes one parameter: the color, like `"lightblue"` or `"black"`.

This code draws a sky, grass, and a sun:

```js {linenos=table}
background("lightblue");
fill("green");
rect(0, 300, 400, 100);
fill("yellow");
ellipse(320, 80, 60, 60);
```

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Work with a partner. Click "Run" after every change.

1. Level 1: predict what the last two numbers in `rect` do, then run the code to check
2. Levels 2-6: follow the instructions on each level
3. Level 7: reveal a hidden picture, fix a missing one, or finish a scene
4. Level 8: open the "Rubric" tab first to see how to prove you understand the skills
5. Level 9 (challenge): learn blocks for polygons, custom shapes, lines, and arcs to make your own shape scene

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Parameter" %}}
{{% unit-journal-question-of-the-day question="How can you use parameters to give the computer more specific instructions?" hint="Think beyond shapes too. An alarm needs a time, and a music app needs a song title." %}}
