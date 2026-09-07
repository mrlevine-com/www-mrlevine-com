---
title: Packets
units: [The Internet]
summary: Information flows through the Internet as a datastream of packets.
weight: 180
---

{{% param summary %}}

## Today's Objectives
- Describe how information flows through the Internet as a datastream of packets.
- Explain how packet numbering and re-ordering can allow for large messages to reliably be sent even if packets are dropped or arrive out of order.
- Explain the differences between the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP).

## Lesson Overview
### What are packets?
{{% define "Datastream" %}}
{{% define "Packet" %}}
{{% define "Packet Metadata" %}}
{{< video title="The Internet: Packets, Routing, and Reliability" src="/videos/the-internet-packets-routing-and-reliability.mp4" poster="/images/video-poster-the-internet-packets-routing-and-reliability.jpg" >}}
{{< collapse summary="Click here to reveal key video takeaways." >}}

- Large files are split into packets to be sent
- Packets may take different routes through the network and arrive out of order
- TCP ensures that packets that arrive out of order or are lost are re-ordered
- Packets include metadata like their IP address or a packet number to help move them through the network or reorganize them when they arrive
- Collectively this system makes the Internet more reliable

{{</ collapse >}}

### What are the differences between the two main protocols for sending packets?
{{% define "User Datagram Protocol (UDP)" %}}
{{% define "Transmission Control Protocol (TCP)" %}}
{{< collapse summary="Click here to reveal the answer." >}}

|                        | User Datagram Protocol (UDP)                                                                                                | Transmission Control Protocol (TCP)                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Main Idea              | The goal is to send information quickly without worrying about accuracy                                                    | Slower but more accurate                                                                                                                                            |
| Basics of How It Works | Send all the packets but don't check if they all get through or arrive in the right order                                  | Number packets so they can be re-ordered, confirm all were received, resend any missing packets; multiple back and forth communications between sender and receiver |
| Use in Real Life       | Useful when split seconds matter more than correcting errors, e.g. video-conferencing, live streaming, online gaming, etc. | Useful when accuracy matters more than saving a split second, e.g. sending emails, photos, browsing websites, etc.                                                  |

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Internet Simulator
Use the new Internet Simulator on Code.org.

Team up with a classmate and join different routers.

#### Protocol 1: Just Send All the Packets
Write a single sentence that uses 5-10 packets. Send all the packets at once to your partner. Then click "Log Browser". **Set the Router logs to "show my traffic" and "show all routers".**

Record your answers to the following questions:
1. Do all of the packets in your sent messages always follow the same path? If not, describe at least two different paths packets took.
2. Did every packet arrive in the correct order? Describe what went wrong and whether your partner was able to read the message. If neither you nor your partner had an issue, try sending another message.

#### Protocol 2: Check for Errors
Create a protocol that will solve the problems you saw with Protocol 1 by doing some error-checking. The sender should be able to construct a single multi-packet message that is sent at once. Afterwards, they can keep communicating to fix any errors in the transmission. Things to consider:
- How will the receiver know the order of the packets or if any are missing?
- How will the receiver request missing packets and what will the sender do in response?
- How will both sender and receiver know the full message arrived successfully?

Record the details of your protocol.

Congrats! You just developed a protocol that in the real world is known as Transmission Control Protocol (TCP).

{{< collapse summary="Click here to reveal features your protocol might include." >}}

- Each packet is numbered or otherwise indicates which order it should go in
- Each packet includes the total number of packets, again, perhaps with a number, so the receiver knows how many packets to expect
- The receiver requests missing packets or confirms received packets so the sender knows which to resend
- The sender and receiver both know when the message has been successfully received

{{</ collapse >}}

{{% unit-journal-define-terms "Datastream" "Packet" "Packet Metadata" "User Datagram Protocol (UDP)" "Transmission Control Protocol (TCP)" %}}
{{% instructions-code-org-update %}}
