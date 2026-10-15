---
title: Sprite Properties
units: [Interactive Animations and Games, Drawing and Sprites]
summary: Change a sprite's properties to control where it is and how it looks.
weight: 350
---

{{% param summary %}}

## Today's Objectives
- Use dot notation to update a sprite's properties.

## Lesson Overview
### What can you already control about a sprite?
{{< collapse summary="Click here to reveal the answer." >}}

Only its location and its animation. A sprite stores many more properties, and today you'll change them.

- You set its location with `createSprite(x, y)`.
- You set its animation with `setAnimation`.
- Other properties control things like its size and how far it's turned.

{{</ collapse >}}

### How do you change a sprite's properties?
{{< video title="Sprite Properties" src="/videos/sprite-properties.mp4" poster="/images/video-poster-sprite-properties.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Connect the sprite's label and the property with a dot, then use it like a variable.

This code moves a sprite to the left and makes it skinny:

```js {linenos=table}
var mySprite = createSprite(200, 200);
mySprite.x = 100;
mySprite.width = 50;
drawSprites();
```

- Read line 2 as "`mySprite.x` gets 100."
- Read a property the same way: `mySprite.x = mySprite.x + 50;` moves the sprite 50 to the right of wherever it is.
- In blocks, drag a property onto its own line to change it. Drag it into a slot to read it.
- Changes show up the next time `drawSprites()` runs.

{{</ collapse >}}

{{% define "Property" %}}
{{% define "Dot Notation" %}}

### Which properties can you change?
{{< collapse summary="Click here to reveal the answer." >}}

| Example                    | What it does                                                                           |
|----------------------------|----------------------------------------------------------------------------------------|
| `mySprite.x = 100;`        | Moves the sprite's center to x = 100. `mySprite.y` works the same way for y.          |
| `mySprite.rotation = 45;`  | Turns it 45 degrees clockwise. Negative numbers turn it counterclockwise. It starts at 0. |
| `mySprite.scale = 2;`      | Makes it twice as big without stretching it. `0.5` makes it half as big. It starts at 1. |
| `mySprite.width = 50;`     | Stretches or squishes it sideways. `mySprite.height` works the same way up and down.  |
| `mySprite.visible = false;`| Hides it. Set it to `true` to show it again.                                           |

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

Click "Run" after every change.

1. Level 1: read the code and predict where the bee sprites will appear. Then watch the video above.
2. Levels 2-3: follow the instructions on each level.
3. Level 4: scale animals to the right size, rotate cars to fit their lanes, or rotate and scale sprites so they float in space.
4. Level 5: open the "Rubric" tab first to see how to prove you understand sprite properties.
5. Level 6 (challenge): learn new properties. Use `tint` to change a sprite's color, `height` and `width` to stretch it, or `alpha` to make it see-through.

Stuck? Open the "Help & Tips" tab, or hover over a block and click "Examples." Made a big mistake? Click "Version History" to go back.

{{</ collapse >}}

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Property" "Dot Notation" %}}
{{% unit-journal-question-of-the-day question="How can you use sprite properties to change their appearance on the screen?" hint="Draw a sprite with arrows pointing to 3 of its properties, and label each arrow with the code that changes it. Then write one way properties are like variables and one way they're different." %}}
