---
title: Introduction to the Internet
units: [The Fabric of the Internet and AI]
summary: Routers, switches, Internet towers, and servers work together to send data between billions of devices across the globe.
weight: 290
---

{{% param summary %}}

## Today's Objectives
- Describe the basic infrastructure of the Internet.
- Explain how devices communicate over the Internet.

## Lesson Overview
### What physical devices make up the Internet?
{{% define "Router" %}}
{{% define "Switch" %}}
{{% define "Internet Tower" %}}
{{% define "Server" %}}

These devices connect to each other in two ways:

| Connection | Example | Trade-off |
|---|---|---|
| Wired | Ethernet cable | More stable |
| Wireless | WiFi | No cables, but can be slower |

### How does a request for a website travel?
1. Your device sends the request to a router, over WiFi or an Ethernet cable.
2. Routers, switches, and Internet towers forward the request across the network to the website's server.
3. The server sends the website data back the same way to your device.

Along the way, all of this data travels as binary: 1s and 0s that can represent letters, numbers, or images.

### How do you get good answers from AI Chat?
| Strategy | Why | Example |
|---|---|---|
| Start broad | Get basic information, like definitions | "What is a router?" |
| Get more specific | Focus on uses or real-world scenarios | "What does a router do when I visit a website?" |
| Dig deeper or compare | Connect topics to show relationships | "How do routers and switches work together in a network?" |

Not getting a good answer? Try one of the following:

- Rephrase your question with different words.
- Ask the AI to break its answer into steps.
- Be more specific or add examples. Instead of "What is the Internet?", try "What happens when I use WiFi to visit a website?"

AI can still get things wrong, so today you'll check its answers against verified information. Code.org's AI Chat checks every message for inappropriate content and deletes your chats after 90 days.

## Assignment
{{% instructions-unit-journal-create %}}
{{% instructions-code-org-update %}}
{{% instructions-unit-journal-update %}}

### Hand-Draw a Network Diagram (~10mins)
Go to Code.org Level 1 and use AI Chat to learn about each device, then hand-draw a network diagram showing how devices connect to a website's server. Include the following:

- A router, a switch, an Internet tower, and a server, each labeled with what it does
- Three devices on WiFi (like phones or a laptop) and one desktop on an Ethernet cable
- Dotted arrows for wireless connections
- Solid arrows for wired connections

{{< collapse summary="Click here for suggested AI Chat prompts." >}}

About the devices:

- What does a router do when I try to visit a website?
- What is a switch, and how does it help my data get to the right place?
- What is a server, and why do I need it to open a website?
- What happens to my data when I'm connected via WiFi versus an Ethernet cable?

About your data's journey:

- When I open a web browser on my computer and search for a website, which component do I visit first?
- What happens to my data when I send an email?
- What does TCP/IP do when I send or receive data online?
- When I send a message online, how does my data get packaged and sent?
- What happens if my data doesn't reach its destination?

{{</ collapse >}}

### Get AI Feedback (~5mins)
Take a screenshot of your hand-drawn diagram, upload it to AI Chat, and ask it for feedback. Record what feedback the AI gave you, and whether it pointed out anything you missed or explained something in a new way.

### Verify the AI (~5mins)
Go to Code.org Level 2 and review the "Verifying AI Information: How Devices Transmit Data" panels. Record one or two sentences about how well the AI's explanations matched the panels. Consider the following:

- Did the AI's answers match what the panels showed about how data travels between devices?
- Were any parts of your diagram or the AI's answers incomplete or inaccurate?
- How do the connections between devices (like router → tower → server) compare across your diagram and the panels?

Then complete the Check for Understanding on Level 3.

### Explore the Internet Simulator (~10mins)
Go to Code.org Level 4 and connect with a partner in the Internet Simulator: one of you clicks "Join" next to the other's name, and the other clicks "Accept". Then try the following:

- Send each other messages.
- Turn ASCII, decimal, and binary on and off in the "My Device" tab.
- Check the "Sent Message Log" and "Received Message Log".

Record one way the Internet Simulator is similar to the real Internet and one way it's different.

{{% unit-journal-define-terms "Router" "Switch" "Internet Tower" "Server" %}}
{{% unit-journal-question-of-the-day question="How does the Internet connect billions of devices across the globe?" hint="Name the devices from your network diagram and describe how a request for a website travels to a server and back." %}}
