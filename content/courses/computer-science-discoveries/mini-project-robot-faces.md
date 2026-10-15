---
title: "Mini-Project: Robot Faces"
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Plan and code a robot face that uses shapes, variables, and random numbers to look different every time it runs.
weight: 330
---

{{% param summary %}}

## Today's Objectives
- Apply variables, shapes, and randomNumber concepts to create a program.
- Use a structured process to plan and develop a program.

## Lesson Overview
### What will you make today?
{{< collapse summary="Click here to reveal the answer." >}}

A robot face, drawn with code, that looks different every time it runs.

- You choose everything: the shape of its head, how many eyes or mouths it has, whether it has antennas, and more.
- There's no starter code. You start from a blank screen with an idea of your own.
- Plan first with [the problem solving process]({{< relref "the-problem-solving-process.md" >}}): Define and Prepare in your Unit Journal, Try in Game Lab, then Reflect.

{{</ collapse >}}

### Which drawing commands can you use?
{{< collapse summary="Click here to reveal the answer." >}}

Way more than `rect` and `ellipse`. Each of the 7 shape commands in the first 4 rows counts as a different type of shape:

| Commands                                                              | What they draw                                                                                                          |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `rect(x, y, w, h)`, `ellipse(x, y, w, h)`                             | Rectangles, and circles or ovals                                                                                        |
| `regularPolygon(x, y, sides, size)`                                   | A shape with equal sides, like a triangle or hexagon. `size` is the distance from the center to each corner.            |
| `shape(x1, y1, x2, y2, ... xN, yN)`                                   | Any shape you want. It connects the points you list, in order, and fills it in.                                         |
| `line(x1, y1, x2, y2)`, `arc(x, y, w, h, start, stop)`, `point(x, y)` | A line between 2 points, a curved piece of an ellipse's outline, or a single dot. For `arc`, 0 points right and 90 points down. |
| `fill`, `noFill`, `stroke`, `noStroke`, `strokeWeight`                | Inside color, no inside color, outline color, no outline, and outline thickness                                        |

{{</ collapse >}}

### How can you use variables with random numbers to make a program different every run?
{{< collapse summary="Click here to reveal the answer." >}}

Store a `randomNumber` in a variable, then use that variable in your shapes. Each run rolls a new value.

This code draws a head with a random color and two eyes with a random size:

```js {linenos=table}
var headColor = rgb(randomNumber(50, 200), randomNumber(100, 255), randomNumber(50, 200));
var eyeSize = randomNumber(20, 60);
background("lightblue");
fill(headColor);
rect(100, 100, 200, 200);
fill("white");
ellipse(160, 170, eyeSize, eyeSize);
ellipse(240, 170, eyeSize, eyeSize);
```

- `rgb(red, green, blue)` mixes a color from 3 numbers, each from 0 to 255. Line 1 rolls all 3.
- Line 2 rolls once, and both eyes use `eyeSize`, so they always match. Want eyes that don't match? Give each eye its own variable.
- The head (line 5) is drawn before the eyes (lines 7-8), so the eyes land on top. Swap them, and the head covers the eyes.

{{</ collapse >}}

### How will your robot face be graded?
| Criteria         | Full credit looks like                                                                                                                                   |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Program Sequence | You sequence your code so every shape appears as intended, with none hidden behind others by mistake.                                                   |
| Shapes           | You use at least 4 different types of shapes and place each one with your own coordinates, not the default values (unless your face needs a default). |
| Variables        | You create and correctly use at least 4 variables. All have descriptive names and use `randomNumber`, so your face looks different every run.          |
| Robot Face       | Your program follows your plan and clearly shows a robot face.                                                                                          |

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Finish your plan first (see the Assignment). Then:

1. Level 1 (optional): review the shape blocks you've learned. Keep it open as a reference while you code.
2. Level 2: code your robot face from your plan, back to front: background, then head, then features. Add one shape at a time, click "Run," and check that shape off on your sketch.
3. When you finish, run your program 3 times and check it against the rubric above.

Stuck? Pick one or two of these from the problem solving process:

- Define: reread the rubric, and say the problem in your own words.
- Prepare: write what you want in plain English, sketch it in your Unit Journal, or look back at programs you wrote in earlier lessons.
- Try: write one small piece of code at a time, and run it after every change.
- Reflect: compare your screen to your sketch. Ask a classmate to try your program or read your code.

Still stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Plan Your Robot Face ~15mins
Hand-draw a plan for a robot face that looks different every time it runs.

1. Write 2-3 sentences describing your robot face, including its shapes and which features will be random.
2. Draw an 8 by 8 grid, and label its lines 0, 50, 100, and so on up to 400, across the top and down the side. Hand-draw your robot face on it using at least 4 different shape commands, and label each shape with its command.
3. Make a table listing at least 4 variables. For example:
    | Variable Name | Description                                                      |
    |---------------|------------------------------------------------------------------|
    | `mouthWidth`  | How wide the mouth is: `randomNumber(75, 200)`                   |
    | `eyeColor`    | The eye color: `randomNumber(0, 255)` for each of red, green, and blue |

Idea too big? Shrink it: get the head and one random feature working first, then add more if you have time.

{{% instructions-code-org-update %}}

{{% unit-journal-question-of-the-day question="How can you use shapes, variables, and randomness to express your creativity?" hint="Use your robot face as an example: what you're most proud of, what was most challenging, and what you'd change next time. Then look at your classmates' robot faces, and add one especially creative way someone used the blocks." %}}
