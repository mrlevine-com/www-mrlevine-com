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
### What is a site map?
{{% define "Site Map" %}}

{{< figure src="/images/site-map-clothing-store.svg" alt="A site map. Home connects to Shop and Support. Shop connects to Clothes and Shoes. Clothes connects to Shirts and Pants. Support connects to FAQs and Contact. FAQs connects to Shipping, Returns, and Sizes." >}}

Put Home at the top, and group related pages under a parent page, not in one flat list.

### What is a user flow?
{{% define "User Flow" %}}

{{< figure src="/images/user-flow-clothing-store.svg" alt="The same site map with two highlighted paths. Path A goes Home, Shop, Clothes, Pants. Path B goes Home, Support, FAQs, Returns. All other pages are grayed out." >}}

To buy pants, a user clicks Home → Shop → Clothes → Pants. Each click gets more specific.

### How do you prompt AI to build a site map?
List every page and what it links to:

> Build a clothing store web app with these pages: Home, Shop, Clothes, Shoes, Shirts, Pants, Support, FAQs, Contact, Shipping, Returns, and Sizes. Put Home, Shop, and Support in the navigation bar on every page. Shop links to Clothes and Shoes. Clothes links to Shirts and Pants. Support links to FAQs and Contact. FAQs links to Shipping, Returns, and Sizes.

Then click every link to check that AI didn't leave out pages or break links.

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

{{% unit-journal-define-terms "Site Map" "User Flow" %}}
