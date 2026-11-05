---
title: Exploring Two Columns
units: [Data]
summary: To find how two things relate, chart two columns at once with a crosstab or a scatter chart.
weight: 460
---

{{% param summary %}}

## Today's Objectives
- Create crosstab and scatter charts in App Lab's Data Visualizer.
- Draw conclusions by reading crosstab and scatter charts.
- Explain the reasons that someone would create either a crosstab or scatter chart in order to explore two columns of data.

## Lesson Overview
### Why chart two columns at once?
Imagine you want to know which hour of the day you and your classmates are happiest. What data would you collect?

{{< collapse summary="Click here to reveal the answer." >}}

At least two pieces of information: the time of day and how happy each person is.

- Bar charts and histograms only show one column.
- To find a relationship between two things, you need a chart that shows two columns.

{{</ collapse >}}

### What does a crosstab chart show?
This crosstab shows the maximum life span (columns) of each breed group (rows) of dogs:

| Breed Group  | 8 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 20 |
|--------------|--:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Herding      | 0 | 0  | 0  | 4  | 2  | 3  | 2  | 1  | 0  | 0  | 0  |
| Hound        | 1 | 2  | 0  | 4  | 3  | 4  | 3  | 1  | 0  | 0  | 0  |
| Mixed        | 0 | 0  | 0  | 0  | 2  | 0  | 0  | 0  | 0  | 0  | 0  |
| Non-Sporting | 0 | 0  | 0  | 0  | 2  | 1  | 5  | 1  | 0  | 0  | 0  |
| Sporting     | 0 | 0  | 1  | 5  | 1  | 6  | 5  | 1  | 0  | 0  | 0  |
| Terrier      | 0 | 0  | 0  | 0  | 1  | 2  | 5  | 1  | 0  | 0  | 1  |
| Toy          | 0 | 0  | 0  | 1  | 0  | 4  | 3  | 1  | 1  | 2  | 0  |
| Working      | 1 | 6  | 1  | 8  | 2  | 3  | 2  | 0  | 0  | 0  | 0  |

_Source: the Dogs dataset in App Lab's Data Library, from Code.org._

1. How many Herding breeds live a maximum of 12 years?
2. What is the most common maximum life span for Working breeds?
3. Which breed group seems to live the shortest? The longest?

{{< collapse summary="Click here to reveal the answers." >}}

1. 4 breeds.
2. 12 years, with 8 breeds.
3. Working breeds seem to live the shortest, and Toy breeds seem to live the longest. You can't be sure, though, since each group has a spread of life spans.

{{</ collapse >}}

A **crosstab** counts how often each pair of values from two columns appears.

- **Useful for:** finding the most and least common pairs, finding patterns across two columns, and columns of strings.
- **Not useful when:** either column has too many values, since the chart gets enormous.

### What does a scatter chart show?
{{< collapse summary="Click here to reveal the answer." >}}

A dot for each row, placed by its values in two number columns.

- **Useful for:** seeing patterns and trends between two columns of numbers with lots of different values.
- **Not useful when:** there are lots of repeated values, since dots land on top of each other.

{{</ collapse >}}

When two columns change together, they have a **correlation**. Remember that correlation does not equal causation: a scatter chart can't tell you whether one column causes the other.

{{% define "Correlation" %}}

### Which chart should you make?
![A decision tree. How many columns? With 1 column, ask how many values: few means bar chart, many means histogram. With 2 columns, ask if the values are strings: yes means crosstab. If not, ask how many values: few means crosstab, many means scatter.](/images/which-chart-to-make.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Start with how many columns you're looking at:

- **1 column:** shows what's in your dataset, like which values appear and how common they are.
- **2 columns:** shows relationships, like how a change in one value goes with a change in another.

{{</ collapse >}}

### How do you get through today's levels?
{{< video title="Data Visualizer in App Lab - Part 2" src="/videos/data-visualizer-in-app-lab-part-2.mp4" poster="/images/video-poster-data-visualizer-in-app-lab-part-2.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1 (Making Crosstabs and Scatter Plots): in the Data Visualizer, pick "Cross Tab" or "Scatter Plot" as the chart type, then pick a column for "X Values" and "Y Values."
2. Level 2 (Which Type of Chart): use the decision tree above to pick a chart.
3. Level 3 (Check for Understanding): explain how questions you can answer with scatter or crosstab charts differ from ones you can answer with bar charts or histograms.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Correlation" %}}

_Tip: For "Correlation," sketch a scatter chart whose dots rise together from left to right._

### Sketch and Read Two-Column Charts (~30mins)
Make each chart in Level 1, sketch it, then answer its questions:

1. **Crosstab:** use "Length" and "Part of Speech" from the Words dataset.
    - Which part of speech shows up most often?
    - Which part of speech seems longest on average? Shortest?
    - About how long is a typical noun? How can you tell?
2. **Crosstab:** use "Grade" and "Favorite Class" from the Favorite Classes dataset.
    - Which class do seniors like most?
    - Which grade likes History most?
    - What is one other interesting pattern?
3. **Scatter:** use "Median Household Income" and "Percent Adult College Graduates" from the US States dataset, then pick two other US States columns that show an interesting pattern.
    - What are the ranges of incomes and of percentages in your first chart? What relationship do you see?
    - What pattern do you see in your second chart, and what might it mean?
    - How could you research what causes that pattern?

{{% instructions-code-org-update %}}
