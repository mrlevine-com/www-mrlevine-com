---
title: Sprites
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Use sprites to keep track of the characters in your programs and give them images.
weight: 340
---

{{% param summary %}}

## Today's Objectives
- Create and use a sprite.

## Lesson Overview
### Why would you need a sprite?
{{< video title="Introduction to Sprites" src="/videos/introduction-to-sprites.mp4" poster="/images/video-poster-introduction-to-sprites.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

To keep all of a character's information under one label. With shapes alone, you need a separate variable for every detail.

- One shape needs an x, a y, a width, a height, a fill, and a stroke. A detailed character needs even more, like its image and rotation.
- Every extra shape needs a whole new set of variables.
- A sprite stores all of these values for you. Each value is called a property.
- At first, a sprite is just a gray rectangle.

{{</ collapse >}}

{{% define "Sprite" %}}

### How do you create and draw a sprite?
{{< collapse summary="Click here to reveal the answer." >}}

Create it with `createSprite(x, y)`, then draw it with `drawSprites()`.

This code draws a gray square in the middle of the screen:

```js {linenos=table}
var mySprite = createSprite(200, 200);
drawSprites();
```

- Line 1 creates a sprite and labels it `mySprite`, just like a variable. Pick any label you want.
- `(x, y)` marks the sprite's center, like `ellipse` and unlike `rect`.
- The sprite starts as a 100 by 100 gray rectangle.
- Creating a sprite doesn't draw it. Line 2 draws every sprite you've created so far.

{{</ collapse >}}

### How do you give a sprite an image?
{{< video title="Sprite Animations" src="/videos/sprite-animations.mp4" poster="/images/video-poster-sprite-animations.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Add the image in the Animation tab, then attach it to your sprite with `setAnimation`.

1. Click "Animation" above the display.
2. Click the plus sign. Pick an image from the library, upload one, or draw your own.
3. Note the image's name under it. Click the name to change it.
4. Click "Code" to go back to your code.

Then use the sprite's label, a dot, and `setAnimation` with the image's name:

```js {linenos=table}
var bunny = createSprite(200, 200);
bunny.setAnimation("bunny");
drawSprites();
```

- Game Lab calls every image an animation, even one that doesn't move.
- The animation is just one property of the sprite. A sprite can switch animations, and two sprites can share one.

{{</ collapse >}}

### Why does the order of your sprite code matter?
{{< collapse summary="Click here to reveal the answer." >}}

`drawSprites()` draws your sprites exactly as they are at that moment.

- A sprite created after `drawSprites()` won't appear.
- A sprite whose animation is set after `drawSprites()` appears as a gray rectangle.
- Sprites created later appear in front of sprites created earlier.
- `background` covers everything drawn before it, so put it first.

For now, put `background` first and `drawSprites()` last:

```js {linenos=table}
background("skyblue");
var dog = createSprite(100, 200);
dog.setAnimation("corgi");
var elk = createSprite(300, 200);
elk.setAnimation("elk");
drawSprites();
```

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: read the code with a partner, write down what you think will appear, then run it. Were you right?
2. Levels 2-8: watch "Introduction to Sprites" before level 2 and "Sprite Animations" before level 4. Then follow the instructions on each level. In level 8, match each program to what it draws.
3. Level 9: make hidden sprites appear, fix broken animation or sprite names, reorder code so you can see a ladybug and a snail, or make a fish scene or your own scene.
4. Level 10: open the "Rubric" tab first to see how to prove you understand sprites.
5. Level 11 (challenge): upload an image from the web, draw your own characters from scratch, or give sprites your own hairstyles or fashion style.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Sprite" %}}
{{% unit-journal-question-of-the-day question="How can you use sprites to help you keep track of lots of information in your programs?" hint="Draw a sprite as one labeled box holding many values, like its x, y, and animation. So far, you've changed a sprite's location and image. List what else you'd want to change about a sprite." %}}
