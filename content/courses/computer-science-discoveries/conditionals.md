---
title: Conditionals
units: [Interactive Animations and Games, Animation and Interaction]
summary: Use if statements to make your programs react to changes while they run.
weight: 420
---

{{% param summary %}}

## Today's Objectives
- Use conditionals to react to changes in variables and sprite properties.

## Lesson Overview
### How are these instructions different from the ones you've given Game Lab?
1. If your last name has more than 5 letters, draw a square.
2. If you're wearing anything green, add 3 + 2.
3. If your teacher is tapping a pencil, draw an "X."

{{< collapse summary="Click here to reveal the answer." >}}

You have to check whether something is true before you know what to do. Your answers might change depending on when you check.

- So far, your programs have done the same steps no matter what.
- Today, you'll write programs that check something first, then decide what to do.

{{</ collapse >}}

{{% define "Condition" %}}
{{% define "Conditionals" %}}

### How does a program check whether something is true?
{{< video title="Boolean Expressions" src="/videos/game-lab-boolean-expressions.mp4" poster="/images/video-poster-game-lab-boolean-expressions.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

It uses a Boolean expression, which is like a yes-or-no question. The computer answers it with `true` or `false`.

| Operator | Means                    | Evaluates to `true`  |
|----------|--------------------------|----------------------|
| `==`     | Equal to                 | `4 == 4`             |
| `!=`     | Not equal to             | `4 != 7`             |
| `<`, `>` | Less than, greater than  | `3 > 1`              |
| `<=`, `>=` | Less than or equal to, greater than or equal to | `4 <= 7` |

- Use `==` to check if two things are equal. A single `=` changes a value instead.
- Boolean expressions get more useful with variables and properties, like `sprite.x > 400`. The answer changes as the sprite moves.

{{</ collapse >}}

{{% define "Boolean Expression" %}}

### How do you make a program react to a change?
{{< video title="Conditional Statements" src="/videos/conditional-statements.mp4" poster="/images/video-poster-conditional-statements.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Use an `if` statement. The code inside its curly braces runs only when the condition is `true`.

This code moves a car right, then sends it back to the left side once it drives off the screen:

```js {linenos=table}
var car = createSprite(0, 200);
car.setAnimation("car");
function draw() {
  background("white");
  car.x = car.x + 3;
  if (car.x > 400) {
    car.x = 0;
  }
  drawSprites();
}
```

- Line 6 checks the condition every frame, because it's inside the draw loop.
- Line 7 runs only on the frame when `car.x` is bigger than 400.
- Use `if` statements whenever your program should act differently in different situations, like a character speeding up when a bonus is on.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: predict whether each Boolean expression is `true` or `false`, then run it to check. Then watch the first video above.
2. Levels 2-5: follow the instructions on each level. After level 4, watch the second video above.
3. Level 6: change sprite properties so every Boolean expression is `true`, empty a soup bowl when it turns upside down, or make an alien dance when a spaceship takes off.
4. Level 7: open the "Rubric" tab first to see how to prove you understand conditionals.
5. Level 8 (challenge): make sprites appear and disappear with `visible`, wrap sprites around the screen, build a never-ending fish scene, or animate a sci-fi scene or your favorite quote.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Boolean Expression" "Condition" "Conditionals" %}}
