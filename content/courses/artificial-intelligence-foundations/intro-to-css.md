---
title: Intro to CSS
units: [AI-Generated Design]
summary: CSS turns your brand kit into a real web page, so plan your prompt before AI writes your stylesheet.
weight: 340
---

{{% param summary %}}

## Today's Objectives
- Explain the difference between HTML (structure) and CSS (styling).
- Refine prompts to correct or adjust styling issues (e.g., wrong color, unreadable font).
- Use prompts to generate CSS that applies their chosen brand colors and fonts.

## Lesson Overview
### What would this page look like without CSS?
Picture the pizza page from [Build Your First Web Page With AI](/courses/artificial-intelligence-foundations/build-your-first-web-page-with-ai/) with its CSS removed. Think about:

- What stays the same?
- What disappears or changes?
- How would users see the brand?

{{< figure src="/images/ai-generated-pizza-landing-page.png" alt="A pizza restaurant landing page with a charcoal navigation bar, a hero section with a large headline and red Order Now button, three menu cards with prices, an Our Story section, and a footer" caption="Screenshot of the [real web page](/examples/ai-generated-pizza-landing-page/) with its CSS" >}}

{{< collapse summary="Click here to reveal the answer." >}}

{{< figure src="/images/ai-generated-pizza-landing-page-no-css.png" alt="The same pizza page as plain black text on a white background, with blue underlined links, a giant pizza drawing filling the page, and the menu cards stacked as plain text" caption="Screenshot of the same page with its CSS removed" >}}

**HTML builds structure. CSS adds style.** Without CSS:

- **Stays the same**: every heading, paragraph, link, and image, in the same order
- **Disappears**: the red and charcoal colors, the fonts, and the spacing
- **Changes**: buttons turn into blue underlined links, the menu cards stack into one long list, and the pizza drawing grows to fill the whole page
- **Brand**: the page no longer feels like a gourmet restaurant; it could be anyone's

{{</ collapse >}}

### What is a stylesheet?
{{% define "Stylesheet" %}}

CSS turns the choices in your [brand kit](/glossary/brand-kit/), like colors and fonts, into code that styles every page the same way. AI saves it in a file called `style.css`.

Here's how the pizza page's `style.css` styles its red buttons:

```css {linenos=table}
.btn {
  background: var(--red);
  color: #fff;
  padding: 14px 28px;
  border-radius: 6px;
  font-weight: 600;
}
```

- **Line 1**: `.btn` picks which HTML to style (every button).
- **Lines 2–6**: each line sets one style, like the background color, text color, or spacing.

### How do you prompt AI to write CSS?
A strong prompt answers three questions. Vague words like "nice" or "good" let AI guess what you mean.

| Question | Vague | Specific |
|----------|-------|----------|
| **What is the goal?** Describe what you want AI to build. | "Style my webpage to look modern and professional." | "Create a CSS stylesheet using my brand's colors and fonts with a bold, modern style. Style the header, navigation, main content, and footer consistently." |
| **What are the constraints?** List the rules the design must follow. | "Make the menu look nice and easy to read on a phone." | "Use a dark color scheme with clean, simple fonts. Make sure the text is easy to read on smaller screens and that spacing is consistent across the page." |
| **What are the edge cases?** Say what should *not* happen. | "Make sure the page looks good." | "Avoid low-contrast text, hard-to-read fonts, and spacing that feels too crowded or uneven. Make sure the design stays readable on smaller screens." |

### How do you plan your prompt?
Plan your answers in a `prompt.md` file before you prompt AI. When it's done, your plan *is* your prompt.

A Markdown (`.md`) file is a plain text file developers keep next to their code to plan and document projects. Here's an example `prompt.md`:

> **Goal:** Make it feel welcoming and modern — warm colors, easy to read, friendly
>
> **Constraints:** Keep the structure, must be readable on mobile, no dark background
>
> **Edge cases:** Long page titles might overflow; small screens should still look clean; links need to be visible against the background

To send it to AI, click the ⋮ next to `prompt.md`, then click "Add to AI Tutor Chat."

### How do you check AI's CSS?
Front-end developers style pages, fix layouts, and make sure a site looks right on every device. AI writes CSS fast, but it doesn't know your brand or your user. Your job is to check its work like a front-end developer:

1. Name what you want to improve, like a wrong color or an unreadable font.
2. Ask AI for one change at a time, then click "Preview."
3. Resize the preview to check smaller screens.
4. If it's off, tell AI *why* it's wrong instead of just retrying the same prompt.

Don't like a change? Use "Version History" to go back.

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

{{% unit-journal-define-terms "Stylesheet" %}}

### Show Your Stylesheet (~10mins)
Show how you styled your web app in Code.org (Levels 2–4) and what CSS changed:

1. Write your `prompt.md` answers, then add a screenshot of your styled page (or sketch it).
2. Sketch your page without CSS next to it, then label one thing HTML kept and one thing CSS added.
3. Write one styling issue you fixed and the prompt you used to fix it, then circle the change on your screenshot.
