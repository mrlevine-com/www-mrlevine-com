---
title: Using the Game Design Process
units: [Interactive Animations and Games, Building Games]
summary: Write your own plan for a platform jumper game, then build it.
weight: 550
days: 2
---

{{% param summary %}}

## Today's Objectives
- Implement different features of a program by following a structured project guide.
- Identify core programming constructs necessary to build different components of a game.

## Lesson Overview
### How does the problem solving process help you build a game?
{{< collapse summary="Click here to reveal the answer." >}}

It turns one big project into 4 smaller jobs. Last lesson, the plan was written for you. This time, you write it.

| Step    | What It Looks Like for a Game                                                  |
|---------|--------------------------------------------------------------------------------|
| Define  | Decide what your game looks like, how it works, and who will play it.          |
| Prepare | Plan your code: sketch the game, then list its sprites, variables, and functions. |
| Try     | Write the code, following your plan.                                           |
| Reflect | Play your game to test it, and get feedback to make it better.                 |

{{</ collapse >}}

### What will you build?
{{< collapse summary="Click here to reveal the answer." >}}

A platform jumper: an alien jumps between falling platforms to catch falling stars. This takes 2 days.

- The left and right arrows move the alien. The up arrow makes it jump.
- Platforms fall slowly. Stars fall faster. Both loop back to the top when they fall off the bottom.
- Each star you catch adds 1 point. Score high enough, and the background changes.
- There are many correct ways to plan this game. Plan yours first (see the Assignment).

{{</ collapse >}}

### Which code builds each part of a game?
{{< collapse summary="Click here to reveal the answer." >}}

You already know every block you need. Put each part in its own function, and call it in the draw loop.

| Part of the Game                    | Code That Builds It                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Backgrounds that change             | A function for each background, and an `if`/`else` that checks `score` to pick one        |
| Scoreboard                          | A `score` variable that starts at 0, shown with `text` in a `showScore` function           |
| Falling platforms and stars         | `velocityY`, and an `if` that moves them back to the top after `y` passes 400              |
| Jumping player                      | `keyDown`, plus the counter pattern on `velocityY`                                         |
| Landing on platforms, catching stars | `player.collide(platform1)`, and `isTouching` with the counter pattern on `score`         |

{{</ collapse >}}

### How do you make a player jump?
{{< collapse summary="Click here to reveal the answer." >}}

Launch it up with a negative `velocityY`, then use the counter pattern to pull it back down, like gravity:

```js {linenos=table}
function controlPlayer() {
  if (keyDown("left")) {
    player.x = player.x - 5;
  }
  if (keyDown("right")) {
    player.x = player.x + 5;
  }
  if (keyDown("up")) {
    player.velocityY = -4;
  }
}
function playerFall() {
  player.velocityY = player.velocityY + 0.1;
}
```

- Line 9 sends the player up 4 pixels per frame.
- Line 13 adds a little to `velocityY` every frame. The player slows down, stops, then falls faster and faster.
- Call both functions in the draw loop.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Keep your plan open while you code, and update it if your code changes. Click "Run" after every change. Pick up where you left off on day 2.

1. Levels 1-2: play the sample game, then finish your plan (see the Assignment).
2. Levels 3-6: write a second background function, create `score`, pick the background with `if`/`else`, and show the score. To test, change the starting score to 100.
3. Levels 7-12: create one platform, make it loop, then copy and paste it to make a second. Do the same for stars, which start at a random `x` from 50 to 350 and a random `y` from -60 to -30, just above the screen. Copying is easier in text mode.
4. Levels 13-17: create the player, then add `playerFall`, `controlPlayer`, `playerLands` (with `collide`), and `collectItems`. In level 17, play your game a few times and check it against your plan.
5. Level 18 (challenge): flip the player's animation when it turns, add lives, add a new item, keep the player on the screen with `createEdgeSprites()`, or give the game a new theme.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Plan Your Platform Jumper ~20mins
Hand-draw a plan for your platform jumper after you play the sample game in Level 1.

1. Write 1-2 sentences describing your game. Sketch it, and label each sprite and how it moves.
2. Make a table of your sprites. For example:
    | Sprite Label | At Start of Game                          | How It Moves and Interacts                                   |
    |--------------|-------------------------------------------|--------------------------------------------------------------|
    | `platform1`  | Platform, at (100, 200), `velocityY` is 0.5 | Falls slowly and loops back to the top. The player lands on it. |
3. Make a table of your variables and a table of your functions. For example:
    | Variable | What It Keeps Track Of | How It Changes                             |
    |----------|------------------------|--------------------------------------------|
    | `score`  | Stars caught           | Starts at 0. Goes up 1 for each star caught. |

    | Function          | What Happens in It                                          |
    |-------------------|-------------------------------------------------------------|
    | `loopPlatforms()` | Moves platforms back to the top when they fall off the bottom. |

{{% unit-journal-question-of-the-day question="How can the problem solving process help programmers to manage large projects?" hint="Explain how having a plan changed the way you coded your game. Then name one thing you'll do differently when you plan your final project." %}}
