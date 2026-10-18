---
title: Site Maps
units: [AI-Generated Design]
summary: Before anyone builds a site, a UX designer maps out how its pages connect.
weight: 360
---

{{% param summary %}}

## Today's Objectives
- Articulate a site map as a clear prompt to AI.
- Create a site map showing page hierarchy and navigation.
- Trace a possible user flow across a web app.

## Lesson Overview
### Which pages would a user click?
Starting at Home, which pages would a user click to:

- **A**: Buy pants.
- **B**: Find return information.

{{< figure src="/images/site-map-clothing-store.svg" alt="A site map. Home connects to Shop and Support. Shop connects to Clothes and Shoes. Clothes connects to Shirts and Pants. Support connects to FAQs and Contact. FAQs connects to Shipping, Returns, and Sizes." >}}

{{< collapse summary="Click here to reveal the answer." >}}

{{< figure src="/images/user-flow-clothing-store.svg" alt="The same site map with two highlighted paths. Path A goes Home, Shop, Clothes, Pants. Path B goes Home, Support, FAQs, Returns. All other pages are grayed out." >}}

- **A**: Home → Shop → Clothes → Pants
- **B**: Home → Support → FAQs → Returns

Both paths start on a broad page and get more specific with each click.

{{</ collapse >}}

### What is a site map?
{{% define "Site Map" %}}

UX designers hand a site map to developers so everyone agrees on the structure before writing any code. Strong site maps:

- Put Home at the top.
- Put key pages, like Contact, in the [navigation bar](/glossary/navigation-bar/).
- Group related pages under a parent page, not in one flat list.

### What is a user flow?
{{% define "User Flow" %}}

Paths A and B above are user flows.

### How do you turn a site map into a prompt?
List every page and what each one links to. Here's the clothing store's site map as a prompt:

> Build a clothing store web app with these pages: Home, Shop, Clothes, Shoes, Shirts, Pants, Support, FAQs, Contact, Shipping, Returns, and Sizes. Put Home, Shop, and Support in the navigation bar on every page. Shop links to Clothes and Shoes. Clothes links to Shirts and Pants. Support links to FAQs and Contact. FAQs links to Shipping, Returns, and Sizes.

AI can leave out pages or create broken links, so check its work:

1. Click every link in the navigation bar, and watch the URL change, like from `index.html` to `challenges.html`.
2. Compare the pages to your site map.
3. If something's wrong, reword that part of your prompt.

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

{{% unit-journal-define-terms "Site Map" "User Flow" %}}
