---
title: Color Images
units: [Digital Information]
summary: Bits can represent a color image.
weight: 80
---

{{% param summary %}}

## Today's Objectives
- Explain how bits can be used to represent the individual pixels of a color image.
- Explain how digital data is used to approximate real-world analog data.

## Lesson Overview
### How does creating a color image with bits differ from creating a black and white image with bits?
{{< collapse summary="Click here to reveal the answer." >}}

Creating a black and white image with bits only requires one bit per pixel. One bit is enough to represent a pixel that is either black or white.

Creating a color image with bits requires more than one bit per pixel.

{{</ collapse >}}

### What are the layers of abstraction in color images?
{{< collapse summary="Click here to reveal the answer." >}}

- **Digital Image Layer**: Displays a digital approximation based on a sampling of an analog image
- **Sampling Layer**: Samples of equal size are read from the analog image and assigned to pixels
- **Pixel Layer**: Each pixel is represented by levels of red, green, and blue light
- **Binary Layer**: The red, green, and blue values are represented using a sequence of binary numbers and sent out via electrical signals

{{</ collapse >}}

### What have you learned so far?
{{< video title="How Computers Work - Data and Binary" src="/videos/how-computers-work-data-and-binary.mp4" poster="/images/video-poster-how-computers-work-data-and-binary.jpg" >}}

## Assignment
{{% instructions-code-org-update %}}
