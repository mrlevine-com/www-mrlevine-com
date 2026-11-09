---
title: Machine Learning
units: [Data]
summary: Machines learn from the examples you give them, including your biases.
weight: 480
---

{{% param summary %}}

## Today's Objectives
- Explain ways that designers and developers can consider the potential effects of their programs.
- Reason about how human bias plays a role in machine learning.

## Lesson Overview
### How can machines "learn"?
{{< video title="What Is Machine Learning?" src="/videos/what-is-machine-learning.mp4" poster="/images/video-poster-what-is-machine-learning.jpg" >}}

![Three steps: 1. You label images as "fish" or "not fish." 2. AI trains by finding patterns in your labels. 3. AI predicts labels for new images itself. A dashed line from step 1 to step 3 reads: biased labels in = biased predictions out.](/images/machine-learning-training.svg)

{{< collapse summary="Click here to reveal the answer." >}}

From examples, not step-by-step code. **Machine learning** is how computers recognize patterns and make decisions without being explicitly programmed.

- **Training data:** the examples you label become the data the AI learns from.
- **Patterns:** the AI looks for what your examples have in common.
- **Predictions:** the AI uses those patterns to label new data on its own.

{{</ collapse >}}

The patterns the AI finds are new **information**, and people use that information to make decisions.

### How does training data affect what AI learns?
{{< video title="Training Data & Bias" src="/videos/training-data-and-bias.mp4" poster="/images/video-poster-training-data-and-bias.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

AI learns whatever your data teaches it, including your blind spots.

- If X-ray data only comes from men, the AI may not recognize diseases in women.
- Before you train, ask: is this enough data, and does it represent all possible scenarios and users?

{{</ collapse >}}

{{% define "Data Bias" %}}

### How can machine learning reflect human bias?
Watch [How I'm Fighting Bias in Algorithms](https://www.ted.com/talks/joy_buolamwini_how_i_m_fighting_bias_in_algorithms), a TED talk by computer scientist Joy Buolamwini.

{{< collapse summary="Click here to reveal the answer." >}}

Through biased data or biased algorithms. Collecting more data doesn't remove bias on its own.

- **Harm:** machine learning has led to new discoveries in medicine, business, and science, but it has also been used to discriminate against groups of people.
- **Your job:** as a programmer, look for bias at every step of building software, and act to reduce it.

{{</ collapse >}}

### Why does bias in AI matter so much?
{{< video title="Impact on Society" src="/videos/ai-impact-on-society.mp4" poster="/images/video-poster-ai-impact-on-society.jpg" >}}

{{< collapse summary="Click here to reveal the answer." >}}

Because AI makes decisions that affect people's lives.

| Use          | Examples                                                    |
|--------------|-------------------------------------------------------------|
| **Benefits** | Diagnosing diseases, creating medicines, helping the blind see |
| **Risks**    | Choosing who gets into college or gets a loan, predicting crime |

To use AI for good, avoid training data that would repeat human bias.

{{</ collapse >}}

### How do you get through today's levels?
{{< collapse summary="Click here to reveal the answer." >}}

1. Levels 1–4 (AI for Oceans): watch the video, then label each image "Fish" or "Not Fish" to train A.I. Then A.I. labels 100 new images on its own and fills the ocean with what it thinks are fish.
2. Levels 5–7: watch the video, then pick a word, like "angry" or "fun," and label fish that match it. You decide what the word looks like, so your opinions become A.I.'s training data.
3. Level 8 (Check for Understanding): describe a time a recommendation, like a suggested video, was wrong or unfair, and how it could be fixed.

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Data Bias" %}}

### Draw How Your Bias Trained A.I. (~10mins)
Show how your opinions in Levels 6–7 became A.I.'s training data:

1. Sketch two fish you labeled with your word, and circle the traits that made you choose them.
2. Compare with a classmate who chose the same word, and write one way your choices differed.
3. Write one way biased training data could cause a real problem, and one way to reduce it.

{{% instructions-code-org-update %}}
