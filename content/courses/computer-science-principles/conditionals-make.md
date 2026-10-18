---
title: Conditionals Make
units: ["Variables, Conditionals, and Functions"]
summary: Build the Museum Ticket Generator App from a blank screen using variables, if-else-if statements, and comments.
weight: 370
---

{{% param summary %}}

## Today's Objectives
- Implement programming patterns with Boolean expressions and conditional statements to develop a functioning app.
- Recognize the need for programming patterns with Boolean expressions and conditional statements as part of developing a functioning app.
- Use debugging skills as part of developing an app.
- Write comments to clearly explain both the purpose and function of different segments of code within an app.

## Lesson Overview
### What will you make today?
The Museum Ticket Generator App. Its screen is already designed; you write all of its code, starting from a blank screen.

It prices each ticket by these rules:

- On weekends (`"Saturday"` and `"Sunday"`), everyone pays full price: $10.
- On weekdays (Monday through Friday), if you're 18 or younger, you pay $5.
- If you use the discount code `"FREEFRIDAY"` on a Friday, you pay $0. No other code works, and it only works on Fridays.

Try the working app in Level 1 on Code.org to see each rule in action.

## Assignment
{{% instructions-unit-journal-update %}}

### Copy the Museum Ticket Plan (~10mins)
Copy this plan for your code into your Unit Journal.

1. Copy the variables table:

    | Variable       | What it stores                                     |
    |----------------|----------------------------------------------------|
    | `day`          | The day from the dropdown                          |
    | `age`          | The age from the dropdown                          |
    | `discountCode` | The code the user types                            |
    | `price`        | The ticket price, based on the day, age, and code  |
    | `ticketText`   | The ticket information shown to the user           |

2. Draw the flowchart:

    ![A flowchart. A box labeled day, age, discountCode points to a diamond containing discountCode == "FREEFRIDAY" && day == "Friday". Its true arrow leads to price = 0. Its false arrow leads to a diamond containing day == "Saturday" || day == "Sunday", whose true arrow leads to price = 10. Its false arrow leads to a diamond containing age <= 18, whose true arrow leads to price = 5 and whose false arrow leads to price = 10.](/images/flowchart-museum-tickets.svg)

{{% instructions-code-org-update %}}

Build the app in Level 2, using your plan:

1. Create your variables at the top of your program and give them starting values with `=`.
2. Add an `onEvent()` for `calculateButton`. Inside it, read the inputs, then turn your flowchart into an if-else-if statement that sets `price`.

    | ID                | Element            | Use                         |
    |-------------------|--------------------|-----------------------------|
    | `dayDropdown`     | Day dropdown       | `getText("dayDropdown")`    |
    | `ageDropdown`     | Age dropdown       | `getNumber("ageDropdown")`  |
    | `discountInput`   | Discount code box  | `getText("discountInput")`  |
    | `calculateButton` | Create My Ticket!  | `onEvent(...)`              |
    | `ticketOutput`    | Ticket             | `setText(...)`              |

3. Show the day, age, and price on the ticket, then try each test case:

    | Age | Day      | Discount Code | Price |
    |----:|----------|---------------|------:|
    | 18  | Monday   | _none_        | $5    |
    | 18  | Saturday | _none_        | $10   |
    | 50  | Monday   | _none_        | $10   |
    | 50  | Saturday | _none_        | $10   |
    | 18  | Tuesday  | FREEFRIDAY    | $5    |
    | 50  | Friday   | FREEFRIDAY    | $0    |
    | 18  | Friday   | FREE          | $5    |
    | 50  | Friday   | FREE          | $10   |

Before you submit, check that:

- [ ] `calculateButton` has an `onEvent()`.
- [ ] Variables store the day, age, discount code, and price.
- [ ] Your code runs with no errors and gives the right price for every test case.
- [ ] The ticket shows the day, age, and price.
- [ ] Comments explain the purpose and function of your `onEvent()` and your if-else-if statement.

_For extra credit, add another discount code for a different day or age range, or make guests 65 and older always pay $5 unless they use a discount code._
