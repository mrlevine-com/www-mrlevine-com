---
title: "Project: Design a Game"
units: [Interactive Animations and Games, Building Games]
summary: Plan, build, and share a game of your own design.
weight: 560
days: 5
---

{{% param summary %}}

## Today's Objectives
- Create a plan for building a piece of software by describing its major components.
- Implement a plan for creating a piece of software.
- Independently scope the features of a piece of software.

## Lesson Overview
### What will you make?
{{< collapse summary="Click here to reveal the answer." >}}

Your own game, planned and coded from scratch, alone or with a partner. You choose the goal, the characters, and how to play. Your game needs:

- At least 3 backgrounds, like an instructions screen, different levels, or a win or lose screen. A variable, like `score`, switches to at least one of them automatically.
- At least 2 types of user input, like 2 different keys, or a key and the mouse.
- Multiple sprite interactions, each controlled by a conditional.
- At least 2 kinds of complex movement: speeding up or slowing down, moving in a curve, jumping, or looping from one side of the screen to the other.
- At least 2 variables, like score or lives, shown on the screen that change how the game plays.

Plan first with [the problem solving process]({{< relref "the-problem-solving-process.md" >}}), the same way you planned the platform jumper.

{{</ collapse >}}

### What will you do each day?
{{< collapse summary="Click here to reveal the answer." >}}

| Day | Work                                                                 |
|-----|----------------------------------------------------------------------|
| 1   | Play sample games, pick an idea, and plan your game.                 |
| 2   | Code your variables, backgrounds, and scoreboard.                    |
| 3   | Code your sprites, their movement, and your player controls.         |
| 4   | Code your sprite interactions, then trade peer reviews.              |
| 5   | Use your feedback to finish your game, then share it with the class. |

{{</ collapse >}}

### What if your idea is too big?
{{< collapse summary="Click here to reveal the answer." >}}

Shrink it into steps: crawl, walk, then run. Get the smallest version working first, then add to it.

| Version | Example                                                                    |
|---------|----------------------------------------------------------------------------|
| Run     | A space game with 3 levels, 4 kinds of enemies, power-ups, and a boss.     |
| Walk    | A space game with 2 levels, 1 kind of enemy, a score, and lives.           |
| Crawl   | A spaceship that moves with the arrow keys and dodges 1 falling rock.      |

Your plan should describe your Walk version. Out of time? A working Walk beats a broken Run.

{{</ collapse >}}

### How should you organize your code?
{{< collapse summary="Click here to reveal the answer." >}}

Like the defender and platform jumper games: create everything outside the draw loop, and keep the draw loop mostly function calls.

```js {linenos=table}
// Variables
var score = 0;
var lives = 3;
// Sprites
var player = createSprite(200, 350);
player.setAnimation("ship");
// Draw loop
function draw() {
  chooseBackground();
  controlPlayer();
  checkCollisions();
  drawSprites();
  showScore();
}
// Functions
function chooseBackground() {
  if (lives <= 0) {
    loseScreen();
  } else if (score >= 10) {
    level2();
  } else {
    level1();
  }
}
```

- Lines 17-23 pick 1 of 3 backgrounds. To add a third choice, click the plus sign at the bottom of the `if` block.
- Write `controlPlayer`, `checkCollisions`, and the other functions below `chooseBackground`.
- Give everything descriptive names, and add comments that start with `//` so others can read your code.
- Need code from earlier? Look back at `displaceEnemies` in [The Game Design Process]({{< relref "the-game-design-process.md" >}}), and `controlPlayer` and `playerFall` in [Using the Game Design Process]({{< relref "using-the-game-design-process.md" >}}).

{{</ collapse >}}

### How will your game be graded?
| Criteria                          | Full credit looks like                                                                                                                                                                                                                        |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Project Guide                     | Your plan is complete and matches the game you turn in.                                                                                                                                                                                       |
| Readable Code                     | You use descriptive names for sprites, variables, and functions, and add comments throughout. You create sprites and functions outside the draw loop, keep the draw loop mostly function calls and `drawSprites()`, and sequence your code so nothing is hidden by mistake. |
| Functions                         | You create at least 3 functions outside the draw loop to organize your code, and you call at least one of them more than once.                                                                                                               |
| Backgrounds and Variables         | At least 3 backgrounds appear while the game runs, and a variable switches to at least one of them automatically, like a "You lose" screen when `lives` reaches 0. At least 2 variables, like `score` or `lives`, are shown on the screen, change during the game, and affect how it plays, like moving to a new level at 10 points. |
| Input, Interactions, and Movement | Your game responds to at least 2 types of user input. Multiple conditionals control sprite interactions that change the sprites, like resetting their position, or the game, like changing the score. A `displace` or `collide` without a conditional doesn't count. Your game has at least 2 kinds of complex movement. |

### How do you get through the levels?
{{< collapse summary="Click here to reveal the answer." >}}

Finish your plan first (see the Assignment). Then click "Run" after every change, and check each part off on your plan.

1. Level 1: play the sample games for ideas.
2. Levels 2-5: create your variables, a function for each background, and a function for each display board, like a scoreboard. Then pick the background with `if`/`else`. To test, change your variables' starting values.
3. Levels 6-9: make your animations, create your sprites, then write functions for their movement and your player controls. Testing a sprite that starts off the screen? Put it on the screen first, then move it back once it looks right.
4. Level 10: write a function for each type of sprite interaction. Test each one before you write the next.
5. Levels 11-12: check your game against the rubric above and your plan, then take the end-of-unit survey.

Stuck? Pick one or two of these from the problem solving process:

- Define: reread the rubric, and say the problem in your own words.
- Prepare: write what you want in plain English, sketch it in your Unit Journal, or look back at programs you wrote in earlier lessons.
- Try: write one small piece of code at a time, and run it after every change.
- Reflect: compare your game to your plan. Ask a classmate to play your game or read your code.

Still stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Day 1: Plan Your Game ~40mins
Hand-draw a plan for your game before you code it.

1. Write 2-3 sentences describing your game and its goal. Then sketch your 3 backgrounds, and label what makes the game switch to each one.
2. Make a table of your sprites and a table of your player controls. For example:
    | Sprite Label | Look and Starting Properties | How It Moves                         | What Happens When It Touches Another Sprite        |
    |--------------|------------------------------|--------------------------------------|----------------------------------------------------|
    | `rock`       | A gray rock, at a random `x`, `y` is -50 | Falls faster and faster, and loops back to the top | Touches `player`: resets to the top, `lives` goes down 1 |

    | User Input | Action                     |
    |------------|----------------------------|
    | Up arrow   | The player jumps.          |
3. Make a table of at least 2 variables (what each keeps track of and how it changes) and a table of at least 3 functions (what happens in each).

Idea too big? Shrink it (see "What if your idea is too big?" above). Then show your plan to Mr. Levine before you code.

{{% instructions-code-org-update %}}

### Day 4: Trade Peer Reviews ~25mins
Review a classmate's game, then use the feedback on your own game to improve it.

1. Write one thing you want feedback on, then switch seats with a classmate.
2. Play their game and read their code. Using the rubric above, write them an "I like...," an "I wish...," and a "What if..." in your Unit Journal, and share it with them.
3. Write which piece of feedback you got was most helpful and what you'll change. Then make that change.
