---
title: The Game Design Process
units: [Interactive Animations and Games, Building Games]
summary: Follow a plan to build a defender game, one function at a time.
weight: 540
---

{{% param summary %}}

## Today's Objectives
- Implement different features of a program by following a structured project guide.

## Lesson Overview
### Why plan a game before you code it?
{{< collapse summary="Click here to reveal the answer." >}}

A plan breaks a big game into small parts you can code and test one at a time.

- A **project guide** is a plan that lists your game's sprites, variables, and functions before you write any code.
- There's usually more than one way to build a game that works. A plan just picks one.
- Today, you'll follow a finished plan to build a defender game. In the next 2 lessons, you'll write more of the plan yourself.

{{</ collapse >}}

### What's the plan for the defender game?
{{< collapse summary="Click here to reveal the answer." >}}

You're an alien defending your cake from evil ladybugs. Ladybugs march across a bridge toward your cake. Push them off the bridge into the water to get points. You lose points when they reach the cake.

| Sprite Label (Look) | At Start of Game                                      | How It Moves and Interacts                                                                                  |
|---------------------|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `player` (alien)    | At (200, 200)                                         | The arrow keys move it in 4 directions. It pushes the ladybugs.                                             |
| `cake` (cake)       | At (350, 200)                                         | Never moves. When a ladybug touches it, you lose 2 points.                                                  |
| `enemy1` (ladybug)  | `x` is 0, `y` is random from 150 to 250, `velocityX` is 2 | Moves right across the bridge. When it falls in the water or touches the cake, it goes back to the start. |
| `enemy2` (ladybug)  | Same as `enemy1`                                      | Same as `enemy1`                                                                                            |

| Variable | What It Keeps Track Of | How It Changes                                                                                   |
|----------|------------------------|--------------------------------------------------------------------------------------------------|
| `score`  | Your score             | Starts at 0. Goes up 1 when a ladybug falls in the water. Goes down 2 when one reaches the cake. |

{{</ collapse >}}

### How do functions keep the draw loop simple?
{{< collapse summary="Click here to reveal the answer." >}}

Each line of the draw loop calls one function from the plan. Read the draw loop, and you can see the whole game:

```js {linenos=table}
function draw() {
  gameBackground();
  movePlayer();
  displaceEnemies();
  enemiesTouchCake();
  enemiesTouchWater();
  showScore();
  drawSprites();
}
```

| Function              | What Happens in It                                                    |
|-----------------------|-----------------------------------------------------------------------|
| `gameBackground()`    | Draws the water and the bridge.                                       |
| `movePlayer()`        | Moves the player with the arrow keys, and changes its animation.      |
| `displaceEnemies()`   | Lets the player push the ladybugs.                                    |
| `enemiesTouchCake()` and `enemiesTouchWater()` | Send ladybugs back to the start, and change the score. |
| `showScore()`         | Shows the score on the screen.                                        |

Your starter code already has the sprites, the `score` variable, and some empty functions. Your job is to write the code inside each function, one level at a time.

{{</ collapse >}}

### What should you do when you write the same code twice?
{{< collapse summary="Click here to reveal the answer." >}}

Move it into a new function, then call that function everywhere you need it.

Both ladybugs go back to the start when they touch the cake, and again when they fall in the water. Instead of copying the same 3 lines into every spot, this code puts them in `setEnemy1()`:

```js {linenos=table}
function enemiesTouchCake() {
  if (enemy1.isTouching(cake)) {
    setEnemy1();
    score = score - 2;
  }
}
function setEnemy1() {
  enemy1.x = 0;
  enemy1.y = randomNumber(150, 250);
  enemy1.velocityX = 2;
}
```

- Line 3 calls `setEnemy1()`, which runs lines 8-10.
- `setEnemy2()` works the same way for `enemy2`.
- Need to change how ladybugs start? Change it once, in the function, instead of in every copy.
- Plans change as you code. When you add a function, add it to your plan too.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Keep the plan above open while you code. Click "Run" after every change.

1. Level 1: play the game. You can't see its code yet. Then make your own plan (see the Assignment) before you look at the plan above.
2. Levels 2-4: read the plan, give each sprite the animation from the Animation tab, then start each ladybug at a random spot on the left, moving right.
3. Levels 5-7: in `movePlayer`, use the arrow keys to move the player 3 pixels at a time in all 4 directions. In level 7, copy the player's animation in the Animation tab, flip it, and switch to it when the player turns around.
4. Levels 8-12: code the sprite interactions. A ladybug is off the bridge when its `y` is less than 142 or greater than 258. Can't see why sprites aren't touching? Add `player.debug = true;` to see their outlines.
5. Level 13 (challenge): show a new background at a high score, give ladybugs random speeds, change the look of the sprites, or end the game after 3 ladybugs reach the cake.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Predict the Defender Game's Plan ~10mins
Hand-draw your own plan for the game in Level 1 before you look at the plan above.

1. Play Level 1, then sketch the game and label each sprite.
2. Next to your sketch, list the variables and functions you think the game needs.
3. Open "What's the plan for the defender game?" above, and circle everything you matched. Different isn't wrong: there's more than one way to build the same game.

{{% unit-journal-question-of-the-day question="How does having a plan help to make a large project easier?" hint="Name one way the plan helped you while you coded today. Then name one thing you'll remember when you write your own plan." %}}
