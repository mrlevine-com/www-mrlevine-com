---
title: Filtering and Cleaning Data
units: [Data]
summary: Clean data so the same thing is always written the same way. Filter data to focus on just the rows you need.
weight: 450
---

{{% param summary %}}

## Today's Objectives
- Create filtered charts that answer specific questions.
- Explain why data needs to be cleaned.
- Use the Data Visualizer to filter data.

## Lesson Overview
### Why does data need to be cleaned?
Imagine you surveyed your classmates, and some typed `4` for hours of sleep while others typed `"four"`. What happens when you chart it?

{{< collapse summary="Click here to reveal the answer." >}}

The chart counts `4` and `"four"` as two different values, so it's wrong. Messy data makes misleading charts.

- **When to clean:** when data is incomplete, invalid, or combined from more than one table.
- **The goal:** make the data uniform without changing its meaning. For example, change `"two"` to `2`.

{{</ collapse >}}

{{% define "Cleaning Data" %}}

Look for these four kinds of messy data:

| Problem                  | Example                           |
|--------------------------|-----------------------------------|
| **Different types**      | `"two"` and `2`                   |
| **Abbreviations**        | `"February"`, `"Feb"`, and `"Febr"` |
| **Spellings**            | `"color"` and `"colour"`          |
| **Capitalization**       | `"spring"` and `"Spring"`         |

You can clean data by hand, or write a program to find and fix it. Today you'll clean by hand. The datasets in App Lab's Data Library are already clean.

### What if you only want to look at part of your data?
For example, what if you only want to investigate the percentage of female legislators in your state?

![Two diagrams. Clean: the values 4, "four", Spring, and spring become 4, 4, Spring, and Spring, with the same rows and meaning. Filter: four rows for Ohio, Texas, Texas, and Utah become just the two Texas rows.](/images/clean-vs-filter-data.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Filter it. A filter shows only the rows you choose, without deleting any data.

- **Decide what to filter by:** ask what every row you want has in common, like being from your state.
- **Switch back anytime:** the full dataset is still there for your next question.

{{</ collapse >}}

{{% define "Data Filtering" %}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1 (Data Cleaning): open the "Data" tab, open the "Student Info" table, then make charts of "Average Hours of Sleep" and "Favorite Subject" and look for problems. To fix a cell, click "Edit" at the end of its row, change it, then click "Save." Remake both charts when you're done.
2. Level 2 (Data Filtering): open the "Data" tab, then open the "Female State Legislators" and "US Women Running for Elected Office in 2020" tables. Use "Filter" and "By" at the bottom of the Data Visualizer to choose which rows to chart. Then do the Assignment below.
3. Level 3 (Check for Understanding): explain what makes cleaning data by hand challenging.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Cleaning Data" "Data Filtering" %}}

_Tip: For "Cleaning Data," sketch a messy column and its clean version. For "Data Filtering," sketch a table with only some rows circled._

### Answer Questions With Filtered Charts (~25mins)
Filter two datasets in Level 2, and sketch each chart you make:

1. **Female State Legislators:** filter "Year" by the year you were born, make a histogram of "Percentage of Females in Legislature" with a bucket size of 5, and sketch it. Then change the filter to 2019, and sketch that chart too.
2. **Compare:** write how many states had 25–30% female legislators in each year, what this data shows, and why that might be the case.
3. **US Women Running for Elected Office in 2020:** pick any chart type, then filter to answer each question and sketch its chart:
    - Which states had at least one woman run for Governor?
    - Which states had more than 10 women win their primary race?

{{% instructions-code-org-update %}}
