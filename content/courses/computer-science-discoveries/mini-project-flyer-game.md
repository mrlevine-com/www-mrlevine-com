---
title: "Mini-Project: Flyer Game"
units: [Interactive Animations and Games, Building Games]
summary: Plan and code a flyer game where your player flies, falls, collects a target, and dodges obstacles.
weight: 520
---

{{% param summary %}}

## Today's Objectives
- Use a structured process to plan and develop a program.

## Lesson Overview
### What will you make today?
{{< collapse summary="Click here to reveal the answer." >}}

A flyer game. You've learned every type of sprite movement and interaction in this unit, and today you'll put them all together.

- In the sample game, a flybot flies up when you press the up arrow, floats left and right with the left and right arrows, and falls when you let go.
- It collects a coin that jumps to a random spot, and dodges 2 rocks that loop across the screen and push it around.
- Make your game just like the sample, or change the sprites, controls, and interactions to fit your own idea.
- Plan first with [the problem solving process]({{< relref "the-problem-solving-process.md" >}}): Define and Prepare in your Unit Journal, Try in Game Lab, then Reflect.

{{</ collapse >}}

### Which blocks can you use?
{{< collapse summary="Click here to reveal the answer." >}}

Everything you've learned in Game Lab so far, especially:

| Use                     | Blocks                                                                                   |
|-------------------------|------------------------------------------------------------------------------------------|
| Sprites and movement    | `createSprite`, `setAnimation`, `velocityX`, `velocityY`, `drawSprites()`                |
| Player controls         | `if (keyDown("up")) { ... }`, with `"left"` and `"right"` too                            |
| Gravity                 | The counter pattern on velocity: `player.velocityY = player.velocityY + 0.2;`            |
| Looping and interactions | `if (rock.x < 0) { ... }`, `isTouching`, `displace`, `collide`, `bounce`, `bounceOff`   |
| Score (optional)        | A variable like `var score = 0;`, updated with `score = score + 1;` and shown with `text` |

{{</ collapse >}}

### How do you put the pieces together?
{{< collapse summary="Click here to reveal the answer." >}}

Create your sprites and set their starting velocities outside the draw loop. Put controls, looping, and interactions inside it.

This code makes a small flyer game with a player, a coin, and one rock. Your animation names will match the ones in your Animation tab:

```js {linenos=table}
var player = createSprite(200, 100);
player.setAnimation("flybot");
var coin = createSprite(300, 300);
coin.setAnimation("coin");
var rock = createSprite(400, 250);
rock.setAnimation("rock");
rock.velocityX = -3;
function draw() {
  background("skyblue");
  if (keyDown("up")) {
    player.velocityY = -4;
  }
  player.velocityY = player.velocityY + 0.2;
  if (rock.x < 0) {
    rock.x = 400;
  }
  if (player.isTouching(coin)) {
    coin.x = randomNumber(50, 350);
    coin.y = randomNumber(50, 350);
  }
  rock.displace(player);
  drawSprites();
}
```

- Lines 10-13 fly the player up while you press the up arrow. Line 13 makes it fall faster and faster when you let go, like gravity.
- Lines 14-16 loop the rock back to the right side after it leaves the left side.
- Lines 17-20 move the coin to a random spot when the player touches it.
- Line 21 lets the rock push the player. Try `collide` or `bounceOff` instead.

{{</ collapse >}}

### How will your flyer game be graded?
| Criteria            | Full credit looks like                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Plan                | Your plan in your Unit Journal is complete and matches your finished game.                                                                                                |
| Program Sequence    | You sequence your code so nothing is hidden behind something else by mistake. Code that sets up your game is outside the draw loop, and code that changes while it runs is inside it. |
| Sprites             | You create at least 4 sprites and set their animations outside the draw loop. You set the velocities of at least 2 obstacles outside the draw loop.                      |
| Controls and Looping | Inside the draw loop, at least 3 conditionals respond to keys or the mouse to move the player as expected: up makes it fly, it falls back down on its own, and left and right move it sideways. Each obstacle has at least 1 conditional to loop it across the screen. |
| Sprite Interactions | Inside the draw loop, a conditional moves the target to a random spot when the player touches it. At least 2 collision blocks, like `collide` or `bounceOff`, make the obstacles interact with the player. |

Stretch (optional): create at least 2 variables that aren't sprites, like `score` or `health`. Update them during the game, and show them on the screen.

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1: play the sample flyer game a few times, then finish your plan (see the Assignment).
2. Level 2: add your sprites. Click "Run" after each change, and check each part off on your plan.
3. Levels 3-5: code your player controls.
4. Levels 6-7: make your obstacles move, then code how your sprites interact.
5. Level 8: review your game, and check it against the rubric above.

Stuck? Pick one or two of these from the problem solving process:

- Define: reread the rubric, play the sample game again, and say the problem in your own words.
- Prepare: write what you want in plain English, sketch it in your Unit Journal, or look back at programs you wrote in earlier lessons.
- Try: write one small piece of code at a time, and run it after every change.
- Reflect: compare your game to your plan. Ask a classmate to play your game or read your code, or try to "break" it.

Still stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Plan Your Flyer Game ~15mins
Hand-draw a plan for a flyer game with at least 4 sprites: a player, 2 obstacles, and a target.

1. Play the sample game in Level 1. Write 2-3 sentences on what you'll keep the same and what you'll change.
2. Draw an 8 by 8 grid, and label its lines 0, 50, 100, and so on up to 400, across the top and down the side. Hand-draw your background on it, then sketch your sprites on top. Label each sprite with its name.
3. Make a table of how each sprite moves and interacts. For example:
    | Sprite   | Condition                  | Action                               |
    |----------|----------------------------|--------------------------------------|
    | `player` | `keyDown("up")`            | Fly up the screen                    |
    | `rock`   | `rock.x < 0`               | Move back to the right side          |
    | `coin`   | `player.isTouching(coin)`  | Move to a random spot                |

Idea too big? Shrink it: get the player flying and falling first, then add the target, then the obstacles.

{{% instructions-code-org-update %}}
