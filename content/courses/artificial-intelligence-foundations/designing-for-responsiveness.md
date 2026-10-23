---
title: Designing for Responsiveness
units: [AI-Generated Design]
summary: Most people browse on their phones, so test engineers check that a site works on every screen size.
weight: 400
---

{{% param summary %}}

## Today's Objectives
- Identify responsiveness issues in AI-generated layouts.
- Test and refine layouts to adapt across screen sizes.

## Lesson Overview
### What is responsiveness?
{{% define "Responsiveness" %}}

**Over 65% of web traffic comes from mobile devices, like phones**, and Google ranks sites higher when they work well on mobile. AI learns from older websites that weren't built for phones, so you have to test its layouts yourself, like a software test engineer.

### What should you check?
Resize the preview from desktop to phone width, and check that:

| Part | Check that... |
|------|---------------|
| **Layout** | Everything fits without scrolling sideways, and columns stack neatly |
| **Navigation** | Menus fit or collapse on small screens |
| **Images** | Images shrink without stretching, squashing, or getting cut off |
| **Text** | Text stays readable (about 16px or larger) and never overlaps |
| **Buttons** | Buttons stay large enough to tap (about 44px or larger) and spaced apart |

### How do you fix an issue?
Fix one issue per prompt, then resize the preview again to test it:

| Vague | Specific |
|-------|----------|
| "Make it work on phones." | "On small screens, stack the three menu cards in one column instead of side by side." |

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

{{% unit-journal-define-terms "Responsiveness" %}}

## Upcoming Quiz
To prepare for your upcoming quiz, study all of the terms and definitions that you have written in your Unit Journal. You can find all twenty-two terms [here](/units/ai-generated-design/) listed in alphabetical order after the lessons.
