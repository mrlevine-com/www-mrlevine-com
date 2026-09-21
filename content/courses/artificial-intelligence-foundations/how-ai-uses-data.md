---
title: How AI Uses Data
units: [AI and the Systems That Power It, Data and Artificial Intelligence]
summary: AI models need data and specialized hardware to make fast, accurate decisions.
weight: 230
---

{{% param summary %}}

## Today's Objectives
- Describe different examples of AI models and the types of data they need.
- Describe how data is used in AI systems and its role in decision-making.
- Understand the trade-offs between different AI hardware technologies.

## Lesson Overview
### How can AI help you analyze data?
A computer's **processing unit** executes instructions and performs calculations, and it determines how fast and efficiently a computer can run a program. Some processing units are flexible and can handle a variety of tasks, while others are built for efficiency, meaning they're designed for one purpose and run faster using less energy.

{{% define "Central Processing Unit (CPU)" %}}
{{% define "Graphics Processing Unit (GPU)" %}}
{{% define "Field-Programmable Gate Array (FPGA)" %}}
{{% define "Application-Specific Integrated Circuit (ASIC)" %}}

- A **CPU** is best for general computing tasks and is energy efficient for everyday use, but it struggles with very large workloads and isn't optimized for high-speed, data-heavy processing like AI or graphics.
- A **GPU** can handle many tasks at once, making it well-suited for graphics, AI, and simulations, but it uses more power and generates more heat, so it isn't ideal for general computing.
- An **FPGA** can be reprogrammed for specialized tasks like real-time AI, cryptography, and network acceleration, which makes it useful for testing new AI models before a company mass-produces dedicated hardware.
- An **ASIC** is built for one specific task and can't be reprogrammed. It's expensive to develop, but it becomes cost-effective once it's mass produced, and it's used in high-performance applications.

AI models also come in two types that need different amounts of computing power. A **predictive AI task** analyzes existing data to make predictions, so it needs only moderate processing and memory and runs fast using little energy, like a smart city traffic system predicting congestion or a medical imaging AI detecting signs of disease. A **generative AI task** creates new data from patterns it has learned, so it needs much more processing power and memory and runs slower using more energy, like an AI chatbot generating a text response or an image generator creating new artwork.

Today, you'll test how different processing units perform on computing tasks, investigate how a real AI model uses data, and recommend the hardware that fits it best.

## Assignment
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Battle the Processing Units
Go to Code.org level 1. Test each processing unit (CPU, GPU, FPGA, and ASIC) against a variety of computing tasks and observe the performance results. Record which processing unit performed best for each task and why.

### Explore an AI Model
Go to Code.org level 2. In your group, explore your assigned AI model (Voice Assistants, Self-Driving Cars, Medical Imaging, or Translation Tools) and record:

- What the AI model is doing in this scenario.
- What type of data is being input.
- What decision the AI system makes with that data.
- Why this task requires speed and scale.

### Determine AI Hardware
Go to Code.org level 3. Use AI Chat and your findings from the processing unit battle to determine the best hardware for your AI model, then record:

1. Which processing unit (CPU, GPU, FPGA, or ASIC) is the best fit for your AI model, and why.
2. How performance would change if you used a different processing unit instead.
3. What hardware is actually used in a real-world application of your AI model.

{{% unit-journal-define-terms "CPU" "GPU" "FPGA" "ASIC" %}}
{{% unit-journal-question-of-the-day question="How can AI help you analyze data?" %}}
