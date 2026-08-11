---
title: Binary Numbers
units: [Digital Information]
summary: Binary is the fundamental language of computers.
weight: 40
---

{{% param summary %}}

## Today's Objectives
- Explain how the position of each binary digit determines its place value and numeric value.
- Represent binary numbers using combinations of decimal (base 10) digits 0-9.
- Represent decimal numbers using combinations of binary (base 2) digits 0 and 1.

## Lesson Overview
### What can you communicate using only two symbols? Is there a limit?
{{< collapse summary="Click here to reveal the answer." >}}

- The answer to a yes/no or true/false question
- Flipping a switch on/off
- Combinations of yes/no answers by using multiple symbols in a row
- We can keep adding more of the same symbols, so the only limit is how much space we have to write or store those symbols

{{</ collapse >}}

### Using only circles and squares, how many unique patterns can you make with one place value?
{{< collapse summary="Click here to reveal the answer." >}}

You can make two unique patterns:
1. :red_circle:
2. :blue_square:

{{</ collapse >}}

### Two place values?
{{< collapse summary="Click here to reveal the answer." >}}

You can make four unique patterns:
1. :red_circle: :red_circle:
2. :red_circle: :blue_square:
3. :blue_square: :red_circle:
4. :blue_square: :blue_square:

{{</ collapse >}}

### Three place values?
{{< collapse summary="Click here to reveal the answer." >}}

You can make eight unique patterns:
1. :red_circle: :red_circle: :red_circle:
2. :red_circle: :red_circle: :blue_square:
3. :red_circle: :blue_square: :red_circle:
4. :red_circle: :blue_square: :blue_square:
5. :blue_square: :red_circle: :red_circle:
6. :blue_square: :red_circle: :blue_square:
7. :blue_square: :blue_square: :red_circle:
8. :blue_square: :blue_square: :blue_square:

{{</ collapse >}}

### Now using ten shapes instead of two, how many unique patterns can you make with one place value?
{{< collapse summary="Click here to reveal the answer." >}}

You can make ten unique patterns:
1. :zero:
2. :one:
3. :two:
4. :three:
5. :four:
6. :five:
7. :six:
8. :seven:
9. :eight:
10. :nine:

{{</ collapse >}}

### Two place values?
{{< collapse summary="Click here to reveal the answer." >}}

You can make one hundred unique patterns:
1. :zero: :zero:
2. :zero: :one:
3. :zero: :two:
4. :zero: :three:
---
97. :nine: :six:
98. :nine: :seven:
99. :nine: :eight:
100. :nine: :nine:

{{</ collapse >}}

### What is binary?
{{< collapse summary="Click here to reveal the answer." >}}

{{% define "Binary" %}}

Binary is the fundamental language of computers.

Binary is a base 2 number system, meaning it uses two symbols to represent information. Instead of circles and squares, binary uses zeros and ones.

| Circle Square                             | Binary |
|------------------------------------------:|-------:|
| :red_circle: :red_circle: :red_circle:    | 000    |
| :red_circle: :red_circle: :blue_square:   | 001    |
| :red_circle: :blue_square: :red_circle:   | 010    |
| :red_circle: :blue_square: :blue_square:  | 011    |
| :blue_square: :red_circle: :red_circle:   | 100    |
| :blue_square: :red_circle: :blue_square:  | 101    |
| :blue_square: :blue_square: :red_circle:  | 110    |
| :blue_square: :blue_square: :blue_square: | 111    |

{{</ collapse >}}

### Why binary?
{{< collapse summary="Click here to reveal the answer." >}}

Computers use binary numbers as a representation of electrical signals on a wire. The wire is always either off or on, so the "off" state can be represented by 0 and the "on" state by 1.

You are already familiar with the decimal number system, which is base 10, meaning it uses ten symbols to represent information: 0-9, also known as the ten decimal digits.

{{% define "Decimal" %}}

In today's assignment, you will make a Flippy Do, which will help you convert between binary and decimal numbers.

Similar to the rules you created for your circle square system, the binary and decimal number systems both leverage a concept called place value.

{{</ collapse >}}

### What is place value?
{{< collapse summary="Click here to reveal the answer." >}}

Place value is the value of each digit in a number based on its position. For example, in decimal, the 1 in the number 124 represents 100, the 2 represents 20, and the 4 represents 4.

In binary, each place value represents one **bit** (**b**~inary dig~**it**). Your Flippy Do will have eight bits which together makes one **byte**.

{{% define "Bit" %}}
{{% define "Byte" %}}

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Make Your Flippy Do
{{< collapse summary="Click here to see what it looks like." >}}

| 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |
| _             | _             | _             | _             | _             | _             | _             | _             |

{{</ collapse >}}

{{< collapse summary="Click here to see how to use it." >}}

#### Convert Binary to Decimal
**Example: Convert 1010 to decimal.**

1. Place the rightmost bit of your number in the rightmost column of the third row.

| 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |
|               |               |               |               |               |               |               | **0**         |

2. Place the next bit to the left in the next column to the left in the third row.

| 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |
|               |               |               |               |               |               | **1**         | 0             |

3. Repeat step 2 until you have placed every bit.

| 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |
|               |               |               |               | **1**         | **0**         | 1             | 0             |

4. Place a 0 in the remaining columns in the third row.

| 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |
| **0**         | **0**         | **0**         | **0**         | 1             | 0             | 1             | 0             |

5. Add up the numbers in the second row that have a 1 in the same column in the third row.

`8 + 2 = 10`

Congrats! You have successfully converted the binary number 1010 to the decimal number 10.

#### Reset Your Flippy Do
Reset your Flippy Do by erasing the zeros and ones in the third row.

#### Convert Decimal to Binary
**Example: Convert 25 to binary.**

1. Find the largest number in the second row that is less than or equal to your number.

{{< collapse summary="Click here to reveal the answer." >}}

1. The largest number in the second row that is less than or equal to 25 is 16.
2. The largest number in the second row that is less than or equal to 9 is 8.
3. The largest number in the second row that is less than or equal to 1 is 1.

{{</ collapse >}}

2. Place a 1 in the same column as the number you found in the third row.

{{< collapse summary="Click here to reveal the answer." >}}

| 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |
|               |               |               | **1**         | **1**         |               |               | **1**         |

{{</ collapse >}}

3. Subtract the number you found from your number to find the remainder.

{{< collapse summary="Click here to reveal the answer." >}}

1. `25 - 16 = 9`
2. `9 - 8 = 1`
3. `1 - 1 = 0`

{{</ collapse >}}

4. Repeat steps 1-3 with the remainder until the remainder is 0.

5. Place a 0 in the remaining columns in the third row.

| 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |
| **0**         | **0**         | **0**         | 1             | 1             | **0**         | **0**         | 1             |

6. Put together the bits in the third row to reveal the binary number.

`00011001`

Since the leading zeros do not affect the value of the number, you can safely remove them.

`11001`

Congrats! You have successfully converted the decimal number 25 to the binary number 11001.

{{</ collapse >}}

### Answer the Questions

Under your Flippy Do, answer the following questions.

{{< collapse summary="Click here to see the questions." >}}

_Remember to reset your Flippy Do before each conversion._

1. **All 4-bit numbers**: Fill in the binary equivalents for the decimal numbers below. The first three are done for you!

| Binary: 4-bit number | Decimal |
|---------------------:|--------:|
| 0000                 | 0       |
| 0001                 | 1       |
| 0010                 | 2       |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |
| ____                 | __      |

2. What do you notice when you compare the odd numbers with the even numbers? What might explain this?

3. **Binary numbers with exactly one 1**: Complete the chart with all 8-bit binary numbers that have exactly one 1. The first two are done for you!

| Binary: 8-bit number | Decimal |
|---------------------:|--------:|
| 00000001             | 1       |
| 00000010             | 2       |
| 00000100             | __      |
| ________             | __      |
| ________             | __      |
| ________             | __      |
| ________             | __      |
| ________             | __      |

4. What do you notice about the decimal equivalents above?

5. **Conversion practice**: Find the equivalent binary or decimal numbers below.

| Binary   | Decimal |
|---------:|--------:|
| 100      |         |
| 101      |         |
| 1101     |         |
| 00011111 |         |
| 00100000 |         |
| 10101010 |         |
| 11111111 |         |
|          | 5       |
|          | 17      |
|          | 63      |
|          | 64      |
|          | 127     |
|          | 256     |
|          | 513     |

6. When you add a zero to the right of a decimal number, it multiplies its value by 10 (For example, 15 becomes 150). What similar result happens to the value of a binary number when you add a zero on the right? (For example, 11 would become 110).

7. Do the binary numbers 0011 and 000011 have the same value or different values? Explain.

8. Would two bits be enough to assign a unique binary number to each vowel in the English language? Explain.

9. How many bits would you need if you wanted to count up to the decimal number 1000?

10. Write a concise definition or draw a sketch for the following vocabulary words:
- Binary
- Bit
- Byte
- Decimal

{{</ collapse >}}

{{% instructions-code-org-update %}}
