---
title: Build Your First Web Page With AI
units: [AI-Generated Design]
summary: AI builds web pages by predicting patterns, so the clearer your prompt, the better your page.
weight: 310
---

{{% param summary %}}

## Today's Objectives
- Generate a simple web page by prompting an AI tool for basic HTML structure and CSS style.
- Refine an AI prompt when the output is flawed or incomplete.
- Use iterative testing when collaborating with AI to generate HTML/CSS.

## Lesson Overview
### What would AI build from this prompt?
> Build a modern landing page for a gourmet pizza restaurant that is easy to navigate and has a red and charcoal color palette.

{{< collapse summary="Click here to reveal the answer." >}}

{{< figure src="/images/ai-generated-pizza-landing-page.png" alt="A pizza restaurant landing page with a charcoal navigation bar, a hero section with a large headline and red Order Now button, three menu cards with prices, an Our Story section, and a footer" caption="Screenshot of a [real web page](/examples/ai-generated-pizza-landing-page/) Claude Opus 5.5 coded from the prompt above, plus extra context from reading this lesson first" >}}

AI builds a page with the same parts you've seen on many other sites:

- **Navigation bar** with Menu, Our Story, Visit, and a red "Order Online" button
- **Hero section** with a large headline and a red "Order Now" button
- **Gallery cards** for each signature pizza, each with a price and an "Add to Order" button
- **Footer** at the bottom of the page
- **Red and charcoal colors** throughout, just like the prompt asked

Here's the navigation bar from the page's `index.html`:

```html {linenos=table}
<header class="nav">
  <div class="container nav-inner">
    <a href="#" class="logo"><span class="logo-mark">●</span> Brace &amp; Ember</a>
    <nav>
      <a href="#menu">Menu</a>
      <a href="#story">Our Story</a>
      <a href="#visit">Visit</a>
      <a href="#order" class="btn btn-small">Order Online</a>
    </nav>
  </div>
</header>
```

And here's the red and charcoal color palette from its `style.css`:

```css {linenos=table}
:root {
  --red: #d6392f;
  --red-dark: #a8261e;
  --charcoal: #2b2d30;
  --charcoal-deep: #1d1e20;
  --charcoal-light: #3a3c40;
  --cream: #f6f2ec;
  --text-muted: #b8b9bc;
}
```

{{</ collapse >}}

### How does AI know what to build?
AI doesn't think like you do; it predicts what to build from patterns in real web apps.

1. **Training data**: AI studies lots of real web apps made by people.
2. **Patterns**: It notices what shows up again and again, like navigation bars at the top, red "Order Now" buttons, and menus with prices.
3. **Predictions**: It builds a new page by predicting what usually comes next.

This is [pattern recognition](/glossary/pattern-recognition/). You use the same skill when you analyze layouts, debug code, and judge what works in a design.

### What's the difference between HTML and CSS?
**HTML** builds a page's structure and content. **CSS** adds its style.

- AI puts them in separate files: one `.html` file per page, plus a `style.css` file.
- The home page is always `index.html`.
- Other pages get their own files, like `about.html` or `contact.html`.

### What is prompt engineering?
{{% define "Prompt Engineering" %}}

AI predicts its response from the words in your prompt, so it pays attention to your:

- Task
- Context
- Tone or format
- Details

| Prompt | What you might get |
|--------|--------------------|
| "Make a homepage for a school club." | A basic page with generic sections and no clear focus |
| "Create a homepage for a high school gaming club. Include a meeting schedule, featured games, and a sign-up section." | A clear layout with sections that match the club's purpose |

### How do you get the page you want?
Test your page and refine your prompt until it matches what you want:

1. Ask AI for one change (don't edit the code yourself).
2. Click "Preview" to see your page.
3. Compare it to what you expected.
4. If it's off, try a different or more specific prompt.
5. Repeat.

Don't like a change? Use "Version History" to go back. You can't break anything.

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

{{% unit-journal-define-terms "Prompt Engineering" %}}

### Show Your Prompt Refinement (~5mins)
Show how refining one of your prompts in Web Lab (Level 3) changed your page:

1. Write a prompt you gave AI, then add a screenshot of the page it made (or sketch it).
2. Write how you refined that prompt to fix or improve the page.
3. Add a screenshot of the new page (or sketch it), and circle what changed.
