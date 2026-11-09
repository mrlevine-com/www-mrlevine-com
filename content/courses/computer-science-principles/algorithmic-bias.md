---
title: Algorithmic Bias
units: [Data]
summary: Twitter's photo-cropping algorithm favored white faces. Some decisions are best left to people.
weight: 490
---

{{% param summary %}}

## Today's Objectives
- Reason about which types of tasks should not be completed by an algorithm.

## Lesson Overview
### How do you decide how to crop a photo?
Try it in Level 1: crop each photo as if you were posting it on social media. Then compare your crops with a partner's.

{{< collapse summary="Click here to reveal the answer." >}}

It depends on why you're sharing it, so there's no one right way.

- You and your partner probably cropped some photos differently.
- Whatever you crop out never gets seen. Look back: what or who got left out?

{{</ collapse >}}

### What if your class's crops trained an AI?
Imagine your class's crops became training data for an AI that crops everyone's photos, like in AI for Oceans. How might it be biased?

{{< collapse summary="Click here to reveal the answer." >}}

Through both the photos and the people cropping them.

- **The photos:** a few photos in one app don't represent everything people post.
- **The croppers:** teenagers might focus on different things than other people do.

{{</ collapse >}}

### What went wrong with Twitter's cropping algorithm?
Watch [Are We Automating Racism?](https://youtu.be/Ok5sKLXqynQ) from 0:00 to 4:05, then from 9:30 to 13:46.

![Three steps: Training data shows where people's eyes looked first in photos. The algorithm crops each photo around its "most interesting" spot. The effect: crops favored white faces over Black faces.](/images/twitter-cropping-bias.svg)

{{< collapse summary="Click here to reveal the answer." >}}

Its training data was biased, so its crops were too.

- **How it worked:** it learned from data about where people's eyes looked first in photos, then cropped around that spot.
- **What went wrong:** some of that data came from photo collections that don't represent everyone, so its crops favored white faces over Black faces.
- **The machine isn't racist:** its algorithm and data are biased. People built both.

{{</ collapse >}}

### Which tasks shouldn't an algorithm do?
In 2021, Twitter tested its algorithm and found it favored white people over Black people by 4% ([CBS News](https://www.cbsnews.com/news/twitter-kills-its-automatic-cropping-feature-after-complaints/)). Twitter stopped using it and let people crop their own photos.

{{< collapse summary="Click here to reveal the answer." >}}

Ones that are best done by people, like choosing how to show yourself. Twitter's Rumman Chowdhury, who led its machine learning ethics team, explained:

> "One of our conclusions is that not everything on Twitter is a good candidate for an algorithm, and in this case, how to crop an image is a decision best made by people."

Even a perfectly fair algorithm can cause harm when it stops people from representing themselves as they wish.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Level 1 (Cropping Widget): crop each photo as if you were posting it. You can also upload your own photos.
2. Levels 2–3 (Check for Understanding): answer questions about the unintended effects of Twitter's cropping algorithm.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Respond to Twitter's Biased Algorithm (~20mins)
Think through what happened, as both a user and a CEO:

1. Sketch one photo from the Cropping Widget twice, once with your crop and once with your partner's, and circle what each crop left out.
2. Read [Twitter says its image-cropping algorithm was biased, so it's ditching it](https://www.cnn.com/2021/05/19/tech/twitter-image-cropping-algorithm-bias/index.html), then write a 10-word summary of it.
3. Write how you'd respond if you were Twitter's CEO and found this bias, then whether Twitter's real response was appropriate.

{{% instructions-code-org-update %}}
