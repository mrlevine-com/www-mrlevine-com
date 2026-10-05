---
title: Variables Investigate
units: ["Variables, Conditionals, and Functions"]
summary: Real apps use variables to remember and update information, like the temperature in a thermostat app.
weight: 310
---

{{% param summary %}}

## Today's Objectives
- Explain the purpose of those programming patterns with variables both in terms of how they work and what they accomplish.
- Identify common programming patterns when using variables as part of an app.
- Modify apps that make use of common programming patterns with variables to adjust their functionality.

## Lesson Overview
### How does the Thermostat App use variables?
The Thermostat App, which you'll find on Code.org, shows a temperature in °F and °C. Clicking the down arrow lowers it by one degree. Here's the code for the start of the app and the down arrow:

```js {linenos=table}
// Create and assign variables
var tempF = 70;
var tempC = Math.round((tempF - 32) * (5 / 9));
var tempDisplayF = tempF + " F";
var tempDisplayC = tempC + " C";

// Set temperature on the screen
setText("temperatureF", tempDisplayF);
setText("temperatureC", tempDisplayC);

// Button to decrease the temperature by
// one degree F.
onEvent("downButton", "click", function() {
  tempF = tempF - 1;
  tempC = Math.round((tempF - 32) * (5 / 9));

  tempDisplayF = tempF + " F";
  tempDisplayC = tempC + " C";
  setText("temperatureF", tempDisplayF);
  setText("temperatureC", tempDisplayC);
  playSound("sound://category_objects/sharp_switch.mp3");
});
```

Here's what each part does:

| Lines | What happens                                              |
|------:|-----------------------------------------------------------|
| 2–5   | Create 4 variables: 2 numbers and 2 strings to display    |
| 8–9   | Show the strings on the screen                            |
| 14    | Lower `tempF` by 1                                        |
| 15–20 | Recalculate the other 3 variables, then update the screen |
| 21    | Play a click sound                                        |

The up arrow's code is the same, except line 14 becomes `tempF = tempF + 1;`.

Click the down arrow once. What does each variable hold now?

{{< collapse summary="Click here to reveal the answer." >}}

| Variable       | Value    |
|----------------|----------|
| `tempF`        | `69`     |
| `tempC`        | `21`     |
| `tempDisplayF` | `"69 F"` |
| `tempDisplayC` | `"21 C"` |

{{</ collapse >}}

_Tip: On Code.org, open the "Watch" panel below your code and type a variable's name to watch its value change while the app runs._

### What does `Math.round` do?
`Math.round(x)` rounds `x` to the nearest whole number.

Line 3 converts °F to °C. Without `Math.round`, 70 °F would show as `21.11111111111111 C`.

What do these evaluate to?

1. `Math.round(4.2)`
2. `Math.round(4.7)`
3. `Math.round((69 - 32) * (5 / 9))`

{{< collapse summary="Click here to reveal the answers." >}}

1. `4`
2. `5`
3. `21` (because `(69 - 32) * (5 / 9)` is about `20.56`)

{{</ collapse >}}

### What does `getText` do?
`getText(id)` gets the text inside the screen element with that id, as a string.

A later version of the app has a login screen. Here's the code for its login button:

```js {linenos=table}
onEvent("loginButton", "click", function() {
  userName = "Hi, " + getText("nameInput");
  setText("usernameText", userName);
  setScreen("homeScreen");
});
```

If you type `Lola` into the `"nameInput"` text box and click the login button, `userName` holds `"Hi, Lola"`. How would you change line 2 so it holds `"Hi, Lola!"`?

{{< collapse summary="Click here to reveal the answer." >}}

Concatenate `"!"` to the end:

```js {linenos=table}
userName = "Hi, " + getText("nameInput") + "!";
```

{{</ collapse >}}

### What is the Counter Pattern with Event?
It's a pattern for updating a variable every time something happens, like a click:

```js {linenos=table}
var myVar = 0;
onEvent("id", "click", function() {
  myVar = myVar + 1;
});
```

1. `myVar` gets `0`.
2. Each click, `myVar` gets its current value plus `1`.

Use it to count anything, like points in a game each time you click an item. The Thermostat App uses this pattern for `tempF`, but it starts at `70` (line 2) and counts down (line 14) or up (the up arrow's code).

How would you change the Thermostat App so each click changes the temperature by 2 degrees?

{{< collapse summary="Click here to reveal the answer." >}}

Change the `1` to a `2` in both buttons:

- Down button: `tempF = tempF - 2;`
- Up button: `tempF = tempF + 2;`

{{</ collapse >}}

### What is the Variable with String Concatenation Pattern?
It's a pattern for storing glued-together strings in a variable:

```js {linenos=table}
var myString = "rock";
var myOtherString = "roll";
var myStory = myString + " and " + myOtherString;
```

1. `myString` gets `"rock"`.
2. `myOtherString` gets `"roll"`.
3. `myStory` gets `"rock"` + `" and "` + `"roll"`, which is `"rock and roll"`.

Spaces inside quotes count. The Thermostat App shows `70 F` because of the space in `" F"`.

How would you change the Thermostat App to show `70F` instead?

{{< collapse summary="Click here to reveal the answer." >}}

Remove the space inside the quotes everywhere it appears: change `" F"` to `"F"` and `" C"` to `"C"`.

{{</ collapse >}}

### Why give variables meaningful names?
You write code for people, not just the computer.

- A name like `tempF` tells readers what's stored inside.
- A name like `x` makes readers guess.

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Draw the Thermostat's Variables (~10mins)
Draw the Thermostat App's `tempF` and `tempDisplayF` variables as safes with name tags (like in Variables Explore), before and after clicks.

1. Draw both safes with their starting values: `70` and `"70 F"`.
2. Draw them again after each click: down, down, up.
3. Under your drawing, explain in 1–2 sentences how the Counter Pattern with Event updates `tempF`.
