---
title: Overflow and Rounding
summary: Bits can represent a limited amount of information.
weight: 50
---

{{% param summary %}}

## Today's Objectives
- Understand that overflow and roundoff errors result from real-world limitations in representing place value.

## Lesson Overview
### Vocabulary
- **Overflow Error**: Error from attempting to represent a number that is too large
- **Round-off Error**: Error from attempting to represent a number that is too precise (the value is rounded)

### What value would cause your Flippy Do to overflow?
| 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |
| _             | _             | _             | _             | _             | _             | _             | _             |

{{< collapse summary="Click here to reveal the answer." >}}

The decimal number 256 would cause your Flippy Do to overflow.

{{</ collapse >}}

### What adaptation could you make to your Flippy Do to represent that value?
{{< collapse summary="Click here to reveal the answer." >}}

You could add an additional column/bit to the Flippy Do to represent that value.

{{</ collapse >}}

### Using your newly adapted Flippy Do, how many total numbers can be represented?
{{< collapse summary="Click here to reveal the answer." >}}

512 numbers can be represented with a 9-bit Flippy Do, the smallest number being 0 and the largest being 511.

Trying to represent the decimal number 512 using this newly adapted Flippy Do would cause an overflow.

{{</ collapse >}}

### How do you convert fractional amounts from decimal to binary?
> You will not be asked to convert fractional amounts from decimal to binary on any quiz or exam in Mr. Levine's class nor on the AP Exam. However, you do need to understand it conceptually as it relates to round-off errors.

You can convert fractional amounts from decimal to binary by adapting your Flippy Do to use negative exponents like 2<sup>-1</sup>.

| 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> | 2<sup>-1</sup> | 2<sup>-2</sup> | 2<sup>-3</sup> |
|--------------:|--------------:|--------------:|--------------:|---------------:|---------------:|---------------:|
| 8             | 4             | 2             | 1             | 0.5            | 0.25           | 0.125          |
| _             | _             | _             | _             | _              | _              | _              |

### Convert the fractional decimal amount 4.75 to binary.
{{< collapse summary="Click here to reveal the answer." >}}

| 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> | 2<sup>-1</sup> | 2<sup>-2</sup> | 2<sup>-3</sup> |
|--------------:|--------------:|--------------:|--------------:|---------------:|---------------:|---------------:|
| 8             | 4             | 2             | 1             | 0.5            | 0.25           | 0.125          |
| 0             | 1             | 0             | 0             | 1              | 1              | 0              |

4.75 in decimal is 0100.110 in binary.

{{</ collapse >}}

### Convert the fractional decimal amount 0.39 to binary.
{{< collapse summary="Click here to reveal the answer." >}}

Even if you kept adding additional columns to your Flippy Do, you would discover that binary cannot precisely represent certain fractional decimal values like 0.39.

You could only represent a value close to 0.39 which could cause a round-off error.

{{</ collapse >}}

## Assignment
### Instructions
#### Complete Code.org Unit 1 Lesson 5

### Submission
#### Deliverables
| Item                                  | Est. Time |
|---------------------------------------|----------:|
| Unit 1 Lesson 5 submitted on Code.org | ~10 mins  |

#### Rubric
| Criteria                 | Points |
|--------------------------|-------:|
| Code.org Unit 1 Lesson 5 | 100    |
