---
title: Exploring One Column
units: [Data]
summary: A bar chart counts each value in a column. A histogram counts each range of values.
weight: 440
---

{{% param summary %}}

## Today's Objectives
- Create a bar chart and a histogram in App Lab's data visualizer.
- Draw conclusions by reading bar charts and histograms.
- Explain the reasons that someone would create either a bar chart or a histogram in order to explore a single column of data.

## Lesson Overview
### Why do people make charts out of data?
{{< collapse summary="Click here to reveal the answer." >}}

To see patterns that are hard to spot in a table.

- **Answer questions:** a chart can answer a question at a glance.
- **See it all at once:** a chart shows lots of data in one picture.
- **Find patterns:** some patterns are "invisible" until you chart them.

{{</ collapse >}}

### How do you turn data into new information?
![A cycle of five steps: 1. Ask Questions, 2. Collect/Choose Data, 3. Clean/Filter Data, 4. Visualize Data, 5. Generate New Information, then back to 1.](/images/data-analysis-process.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Follow the **Data Analysis Process**. You'll use it for the rest of this unit.

- Each step leads to the next, starting with a question.
- New information leads to new questions, so the cycle starts again.

{{</ collapse >}}

### What questions does a bar chart answer?
{{< figure src="/images/bar-chart-dog-life-span.svg" alt="A bar chart of the maximum life span of dog breeds. 15 years is the most common, with 25 breeds. 17 and 20 years are the least common, with 1 breed each." caption="Source: the Dogs dataset in App Lab's Data Library, from Code.org." >}}

Which of these questions does this chart answer?

1. What is the most common maximum life span of a dog?
2. What is the fluffiest breed of dog?
3. What is the shortest maximum life span of a dog?
4. How long will my dog live?
5. What is the longest maximum life span of a cat?

{{< collapse summary="Click here to reveal the answer." >}}

Only questions 1 and 3:

1. 15 years, since it has the tallest bar.
2. No, since fluffiness isn't in the chart.
3. 8 years, since it's the leftmost bar.
4. No, since the chart shows breeds, not your dog.
5. No, since the chart shows dogs, not cats.

{{</ collapse >}}

A **bar chart** counts how many times each value appears in a column. Use it to find:

- **Most common:** the value(s) with the tallest bar.
- **Least common:** the value(s) with the shortest bar.
- **Unique values:** the list of different values in the column.

### What if a column has too many different values?
{{< figure src="/images/histogram-dog-max-weight.svg" alt="A histogram of the maximum weight of dog breeds with a bucket size of 20. The 60 to 80 bucket is tallest, with 20 breeds. Buckets above 140 have only 1 or 2 breeds each." caption="Source: the Dogs dataset in App Lab's Data Library, from Code.org." >}}

{{< collapse summary="Click here to reveal the answer." >}}

Make a **histogram**. It works like a bar chart, but first it groups numbers into ranges called **buckets**.

- With a bucket size of 20, the numbers 41, 48, and 53 all go in the 40–60 bucket.
- It only works with numbers.
- It shows the most common ranges, the least common ranges, and which ranges are missing.

{{</ collapse >}}

| Chart         | Counts each...      | Use it when the column has... |
|---------------|---------------------|-------------------------------|
| **Bar chart** | value               | a few different values        |
| **Histogram** | range of numbers    | many different numbers        |

### How do you get through today's levels?
{{< video title="Data Visualizer in App Lab - Part 1" src="/videos/data-visualizer-in-app-lab-part-1.mp4" poster="/images/video-poster-data-visualizer-in-app-lab-part-1.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1 (Making Bar Charts and Histograms): open the "Data" tab, open the "Dogs" table, then click "Visualize Data." Pick a chart type and a column, and your chart appears. Then do the Assignment below.
2. Level 2 (Check for Understanding): explain why someone would make a histogram instead of a bar chart. Use the table above for a hint.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Sort and Sketch Bar Charts (~15mins)
Make a bar chart for every column in the Dogs table in Level 1, and decide which ones are useful:

1. Draw a table with two columns, "Useful" and "Not Useful," and write each column name in one of them.
2. Sketch one useful chart, and write one thing someone could learn from it.
3. Write any pattern you notice in which charts are or aren't useful.

### Sketch Histograms (~15mins)
Make histograms in Level 1, and pick the bucket size that makes each one easiest to read:

1. Make a histogram of "Max Weight," try a few bucket sizes, then sketch the best one and write why you chose it.
2. Label the most common and least common ranges of maximum weights on your sketch.
3. Sketch a histogram of one other number column, then write why you chose its bucket size and one question it could help answer.

{{% instructions-code-org-update %}}
