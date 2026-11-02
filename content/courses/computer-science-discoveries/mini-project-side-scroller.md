---
title: "Mini-Project: Side Scroller"
units: [Interactive Animations and Games, Building Games]
summary: Plan and code a side scroller game with a player, a target, an obstacle, and a scoreboard.
weight: 490
---

{{% param summary %}}

## Today's Objectives
- Use a structured process to plan and develop a program.

## Lesson Overview
### What will you make today?
{{< collapse summary="Click here to reveal the answer." >}}

A side scroller: a game where things move across the screen from side to side.

- In the example game, a frog (the player) jumps with the up arrow. A fly (the target) and a mushroom (the obstacle) slide in from the right.
- Catch the fly, and your score goes up. Hit the mushroom, and your health goes down.
- You can make your game just like the example, or change it to fit your own idea.
- Plan first with [the problem solving process]({{< relref "the-problem-solving-process.md" >}}): Define and Prepare in your Unit Journal, Try in Game Lab, then Reflect.

{{</ collapse >}}

### Which blocks can you use?
{{< collapse summary="Click here to reveal the answer." >}}

Everything you've learned in Game Lab so far, especially these:

| Use                 | Blocks                                                                 |
|---------------------|------------------------------------------------------------------------|
| Sprites             | `var label = createSprite(x, y);`, `label.setAnimation("name");`, `drawSprites();` |
| Movement            | `label.velocityX`, `label.velocityY`, `label.rotation`                  |
| Player controls     | `if (keyDown("up")) { ... }`                                            |
| Sprite interactions | `if (label.isTouching(target)) { ... }`                                 |
| Score and health    | `var score = 0;`, `score = score + 1;`, `text("Score: " + score, x, y);` |

{{</ collapse >}}

### How do you make the player jump?
{{< collapse summary="Click here to reveal the answer." >}}

Use 3 conditionals in the draw loop: one to jump, one to fall back down, and one to land.

```js {linenos=table}
var frog = createSprite(100, 300);
frog.setAnimation("frog");
function draw() {
  background("skyblue");
  if (keyDown("up")) {
    frog.velocityY = -6;
  }
  if (frog.y < 150) {
    frog.velocityY = 6;
  }
  if (frog.y > 300) {
    frog.y = 300;
    frog.velocityY = 0;
  }
  drawSprites();
}
```

- Lines 5-7: pressing the up arrow sends the frog up.
- Lines 8-10: at the top of the jump, the frog falls back down on its own.
- Lines 11-14: when the frog reaches the ground, it lands right where it started.

{{</ collapse >}}

### How do you make sprites loop and keep score?
{{< collapse summary="Click here to reveal the answer." >}}

Set the target's speed once, outside the draw loop. Then, inside the draw loop, send it back to the right when it leaves the screen or gets caught.

This code adds a fly to the frog program above. The frog's code is left out to keep it short:

```js {linenos=table}
var score = 0;
var fly = createSprite(400, 150);
fly.setAnimation("fly");
fly.velocityX = -3;
function draw() {
  background("skyblue");
  if (fly.x < 0) {
    fly.x = 400;
  }
  if (frog.isTouching(fly)) {
    score = score + 1;
    fly.x = 400;
  }
  drawSprites();
  textSize(20);
  text("Score: " + score, 10, 30);
}
```

- Line 4 keeps the fly moving left forever, so it never needs to go in the draw loop.
- Lines 7-9 loop the fly back to the right side. Do the same for your obstacle.
- Lines 10-13 add a point and loop the fly back when the frog catches it. For the obstacle, subtract from `health` instead, and change it somehow, like tipping it over with `rotation`.
- Lines 15-16 draw the scoreboard after `drawSprites()`, so it lands on top.

{{</ collapse >}}

### How will your side scroller be graded?
| Criteria         | Full credit looks like                                                                                                                                  |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Plan             | Your plan in your Unit Journal is complete and matches the game you made.                                                                                |
| Program Sequence | You sequence your code so nothing is hidden behind something else by mistake. Setup code is outside the draw loop, and anything that changes while the game runs is inside it. |
| Sprites          | You create at least 3 sprites and set their animations. You set the `velocityX` of the target and obstacle outside the draw loop.                         |
| Conditionals     | Inside the draw loop, you use conditionals to make the player jump and land, loop both the target and obstacle back to the right, and react when the player touches each of them. |
| Variables        | You update 2 variables, like `score` and `health`, during the game and show both on the screen.                                                           |

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Play the example game in Level 1 a few times, then finish your plan (see the Assignment). Then:

1. Levels 2-3: draw your background, then create your sprites. Click "Run" after each change, and check each part off on your sketch.
2. Level 4: add player controls so your player jumps.
3. Level 5: make your target and obstacle loop back to the right side.
4. Levels 6-7: add sprite interactions, then a scoreboard for your variables.
5. Level 8: review your game, and check it against the rubric above.

Stuck? Pick one or two of these from the problem solving process:

- Define: reread the rubric, and say the problem in your own words.
- Prepare: write what you want in plain English, sketch it in your Unit Journal, or look back at programs you wrote in earlier lessons.
- Try: write one small piece of code at a time, and run it after every change.
- Reflect: try to "break" your game. Ask a classmate to play it or read your code.

Still stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Plan Your Side Scroller ~15mins
Hand-draw a plan for a side scroller with a player, a target, and an obstacle.

1. Write 2-3 sentences describing your game: your 3 sprites, how the player moves, and what happens when sprites touch.
2. Draw an 8 by 8 grid, and label its lines 0, 50, 100, and so on up to 400, across the top and down the side. Hand-draw your background on it, sketch your 3 sprites, and draw an arrow showing how each one moves.
3. Make a table of your conditionals, and list your 2 variables below it. For example:
    | Condition                    | Action                                           |
    |------------------------------|--------------------------------------------------|
    | `keyDown("up")`              | The frog jumps.                                  |
    | `fly.x < 0`                  | The fly loops back to the right side.            |
    | `frog.isTouching(fly)`       | `score` goes up, and the fly loops back.         |
    | `frog.isTouching(mushroom)`  | `health` goes down, and the mushroom tips over.  |

Idea too big? Shrink it: get the player jumping and one sprite looping first, then add more if you have time.

{{% instructions-code-org-update %}}
