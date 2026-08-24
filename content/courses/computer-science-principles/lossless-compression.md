---
title: Lossless Compression
units: [Digital Information]
summary: Data can be represented with fewer bits without losing any information.
weight: 90
---

{{% param summary %}}

## Today's Objectives
- Analyze patterns in data to determine compression strategies.
- Create lossless compressions of text files.

## Lesson Overview
### What is lossless compression?
{{% define "Lossless Compression" %}}

### What are the advantages of using abbreviations when sending messages?
> Why waste time say lot word when few word do trick?
>
> — <cite>Kevin Malone[^1]</cite>

[^1]: The above quote is excerpted from [The Office, S8.E2, The Incentive](https://www.imdb.com/title/tt2051718/), aired September 29, 2011.

{{< video title="Kevin's Small Talk - The Office" src="/videos/kevins-small-talk-the-office.mp4" poster="/images/video-poster-kevins-small-talk-the-office.jpg" cc="none" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Abbreviations save time and space, which is useful in computing where time and space are limited.

{{</ collapse >}}

### How do I use the Text Compression Widget on Code.org?
{{< video title="Text Compression Widget With Aloe Blacc" src="/videos/text-compression-widget-with-aloe-blacc.mp4" poster="/images/video-poster-text-compression-widget-with-aloe-blacc.jpg" >}}


{{< collapse summary="Click here to see an example." >}}

#### Original Text
`Pitter_patter_pitter_patter_listen_to_the_rain_pitter_patter_pitter_patter_on_the_window_pane`

#### Dictionary

| Symbol | Text  |
|--------|-------|
| ☀      | _the  |
| ☂      | tter_ |
| ☃      | Pi☂   |
| ☄      | Pa☂   |
| ★      | ☃☄☃☄  |

#### Compressed Text

`★listen_to☀_rain_★on☀_window_pane`

#### Compression Stats

```
Compressed text size: 33 bytes
     Dictionary size: 24 bytes
               Total: 57 bytes
  Original text size: 93 bytes
         Compression: 38.71%
```

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Lossless Compression" %}}
{{% instructions-code-org-update %}}
