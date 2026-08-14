---
title: The AI's Brain
units: [Problem Solving With AI]
summary: AI makes better predictions with more data.
weight: 30
days: 2
---

{{% param summary %}}

## Today's Objectives
- Analyze how training data shapes AI behavior and biases.
- Evaluate how AI’s learning affects accuracy and reliability.
- Experiment with AI responses to identify learning patterns.
- Explain how AI models, especially LLMs, use neural networks and training data.

## Lesson Overview
### How do you predict future events?
Think of a time you predicted:

- What would happen to a character in a book or movie
- Which team would win a sports game
- Something else

{{< collapse summary="Click here to reveal the answer." >}}

Your brain helps you notice patterns based on what you have experienced before.

{{</ collapse >}}

### How is AI's brain similar to your brain?
{{< collapse summary="Click here to reveal the answer." >}}

- Both process an enormous amount of data.
- Both predict based on pattern recognition.
- Both are able to make better predictions with more data.

{{</ collapse >}}

### What is a neural network?
{{< collapse summary="Click here to reveal the answer." >}}

{{% define "Neural Network" %}}

{{</ collapse >}}

<!--
### What is the difference between LLMs and typical neural networks?
### Why is it important for the AI to look at longer sequences such as sentences or paragraphs?
### How does this relate to the context we provide in our prompts?
### How does human feedback improve AI responses?
### Why is it still important to be cautious when using AI, even with fine-tuning?
{{< collapse summary="Click here to reveal the answer." >}}

todo: add video

{{</ collapse >}}
-->

### What is a Large Language Model?
{{< collapse summary="Click here to reveal the answer." >}}

{{% define "Large Language Model (LLM)" %}}

{{</ collapse >}}

### What is training data?
{{< collapse summary="Click here to reveal the answer." >}}

{{% define "Training Data" %}}

{{</ collapse >}}

### What is training?
{{< collapse summary="Click here to reveal the answer." >}}

{{% define "Training" %}}

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}
{{% unit-journal-define-terms "Large Language Models (LLM)" "Neural Network" "Training" "Training Data" %}}

### Unplugged Neural Networks (Day 1)
#### Round 1: Limited Context Prediction
Get in a groups (up to five per group).

Take turns adding one word based only on the last three words.

1. Neuron 1: Look at the starting prompt and write one word in your column to continue the sentence.
2. Neuron 2-5: Look only at the **last three words** and write one word in your column to continue the sentence.

| Starting prompt   | Neuron 1 | Neuron 2 | Neuron 3 | Neuron 4 | Neuron 5 |
|-------------------|----------|----------|----------|----------|----------|
| _Space travel is_ |          |          |          |          |          |

#### Round 2: More Context Available
Take turns adding one word based on the full starting prompt.

1. Look at the starting prompt and the words added to the sentence by previous Neurons and write one word in your box to continue the sentence and pass the paper to the next Neuron.

| Starting Prompt | _The exhausted student left school to go home to_ |
|-----------------|---------------------------------------------------|
| Neuron 1        |                                                   |
| Neuron 2        |                                                   |
| Neuron 3        |                                                   |
| Neuron 4        |                                                   |
| Neuron 5        |                                                   |

### Prompting Challenge (Day 2)
AI responds differently based on how much detail you provide in your prompt.

In today's Code.org levels, you will test three levels of prompting:

- Zero-shot
- One-shot
- Multi-shot

Your Task:

1. Choose a career scenario:
    - Sports Journalist
    - Video Game Developer
    - Travel Agent
2. At each level, write and test a prompt.
3. Answer the reflection question using the sentence frames provided.

#### Level 1: Minimal Context Given
Question: _What kind of response does AI give when you don’t provide much detail?_

Use these sentence frames:

- The AI’s response was mostly about  ______.
- I noticed the response felt  ______ (e.g., vague, specific, repetitive, creative).
- I think the AI made assumptions like  ______.

#### Level 2: Providing a Single Example
Question: _How does adding one example change the AI’s response?_

Use these sentence frames:

- Compared to before, the AI’s response was more  ______ because  ______.
- The example I included helped the AI  ______ (e.g., change tone, add detail, focus the topic).
- Adding one example made the result feel  ______.

#### Level 3: Providing Multiple Examples for Refinement
Question: _How does more structure or multiple examples improve the AI’s response?_

Use these sentence frames:

- With more structure/examples, the AI’s response became  ______.
- One new thing the AI did this time was  ______.
- This shows that AI responds better when you  ______.

{{% instructions-code-org-update %}}
{{% unit-journal-question-of-the-day question="How do AI models learn?" hint="Reflect on what you learned about how AI learns, predicts, or responds to prompts" %}}
