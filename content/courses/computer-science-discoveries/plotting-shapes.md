---
title: Plotting Shapes
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Use a coordinate grid to clearly communicate how to draw shapes on a screen.
weight: 280
---

{{% param summary %}}

## Today's Objectives
- Communicate how to draw an image in Game Lab, accounting for shape position, color, and order.
- Reason about locations on the Game Lab coordinate grid.

## Lesson Overview
### What do you need to communicate to draw a shape?
{{< collapse summary="Click here to reveal the answer." >}}

Three things, for every shape:

1. Position: where the shape goes.
2. Color: what color the shape is.
3. Order: which shape goes first. Later shapes cover earlier shapes.

{{</ collapse >}}

### How does the Game Lab coordinate grid work?
{{< collapse summary="Click here to reveal the answer." >}}

Game Lab draws on a 400 by 400 grid. Every location is written as (x, y):

- x: how far from the left edge.
- y: how far from the top edge.

(0, 0) is the top left corner, so y gets bigger as you move down. This is "flipped" from the grid in math class.

Why? You read starting at the top left, so screens start there too. And you never need negative numbers.

{{</ collapse >}}

### Which point on a shape do the coordinates describe?
{{< collapse summary="Click here to reveal the answer." >}}

- Circle: its center.
- Square: its top left corner.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Write Drawing Instructions (~10mins)
Write instructions someone could follow to recreate this picture exactly.

![Six overlapping red, green, and blue circles and squares on a white canvas](/images/plotting-shapes-warm-up.png)

1. On Code.org, recreate this picture in the drawing tool.
2. Write one line per shape, in the order you drew it: color, shape, and (x, y).

{{% unit-journal-question-of-the-day question="How can you clearly communicate how to draw something on a screen?" %}}
