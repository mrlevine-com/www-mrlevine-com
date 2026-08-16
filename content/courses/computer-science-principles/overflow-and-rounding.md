---
title: Overflow and Rounding
units: [Digital Information]
summary: Bits can only represent a limited amount of information.
weight: 50
---

{{% param summary %}}

## Today's Objectives
- Understand that overflow and roundoff errors result from real-world limitations in representing place value.

## Lesson Overview
### What value would cause your Flippy Do to overflow?
{{% define "Overflow Error" %}}

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

### How many numbers could you represent using your newly adapted Flippy Do?
{{< collapse summary="Click here to reveal the answer." >}}

You could represent 512 numbers with a 9-bit Flippy Do, the smallest being 0 and the largest being 511.

Trying to represent the decimal number 512 using this newly adapted Flippy Do would cause an overflow.

{{</ collapse >}}

### How do you convert fractional amounts from decimal to binary?
> You will not be asked to convert fractional amounts from decimal to binary on any quiz or exam in Mr. Levine's class nor on the AP Exam. However, you do need to understand it conceptually as it relates to round-off errors.

{{< collapse summary="Click here to reveal the answer." >}}

You can convert fractional amounts from decimal to binary by adapting your Flippy Do to use negative exponents like 2<sup>-1</sup>.

| 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> | 2<sup>-1</sup> | 2<sup>-2</sup> | 2<sup>-3</sup> |
|--------------:|--------------:|--------------:|--------------:|---------------:|---------------:|---------------:|
| 8             | 4             | 2             | 1             | 0.5            | 0.25           | 0.125          |
| _             | _             | _             | _             | _              | _              | _              |

{{</ collapse >}}

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

{{% define "Round-off Error" %}}

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Overflow Error" "Round-off Error" %}}
{{% instructions-code-org-update %}}
