---
title: HTTP and DNS
units: [The Internet]
summary: DNS and HTTP let you easily find and load web pages.
weight: 190
---

{{% param summary %}}

## Today's Objectives
- Describe how HTTP is used for sharing the files and pages that make up the World Wide Web.
- Describe how the Domain Name System helps the Internet scale by allowing devices to find the IP addresses associated with a domain name.
- Explain how different layers of protocols on the Internet build upon and rely on one another.

## Lesson Overview
### What happens when you open a URL in your browser?
{{< collapse summary="Click here to reveal the answer." >}}

On your computer, open your browser and open any URL.

Notice how quickly the web page loads.

Now see if you can understand how each step happens behind the scenes:

1. Your browser asks the Domain Name System (DNS) for the IP address that goes with the domain name, e.g. `mrlevine.com`.
2. DNS replies with the IP address of a server that hosts the site, e.g. `2606:4700:3036::6815:da6`.
3. Your browser uses HyperText Transfer Protocol (HTTP) to send that server a request for the page, e.g. `GET https://www.mrlevine.com/`.
4. The server responds over HTTP with the files that make up the page: HTML, images, styles, and scripts; in your browser, right click any web page and click `View Source` to see the raw HTML code of the page.
5. Your browser interprets those files and displays the page.

Every step relies on the lower layers you already studied: IP for addressing, TCP for reliable delivery, and the physical Internet for moving the bits.

{{</ collapse >}}

### How does the Domain Name System help the Internet scale?
{{% define "Domain Name System (DNS)" %}}
{{< video title="The Internet: IP Addresses and DNS" src="/videos/the-internet-ip-addresses-and-dns.mp4" poster="/images/video-poster-the-internet-ip-addresses-and-dns.jpg" >}}
{{< collapse summary="Click here to reveal key video takeaways." >}}

- The DNS is a network of servers that track the IP addresses of different domain names like mrlevine.com.
- When you visit a website, you first ask the DNS for the IP address of the domain you want to visit. The first server you ask may have to ask other servers for this information.
- This system allows billions of devices to get added to the network without putting pressure on any one computer or server to know all the IP addresses in the world.

{{</ collapse >}}

### How do the layers of Internet protocols build on one another?
{{% define "HyperText Transfer Protocol (HTTP)" %}}
{{% define "World Wide Web (WWW)" %}}
{{< video title="The Internet: HTTP and HTML" src="/videos/the-internet-http-and-html.mp4" poster="/images/video-poster-the-internet-http-and-html.jpg" >}}
{{< collapse summary="Click here to reveal key video takeaways." >}}

- When you visit a website, you're actually getting sent a file by a server. HTTP is solving the problem of how to ask for that file.
- Your computer and that server communicate using a protocol called HTTP.
- HTTP is plain-text, so it literally includes the ASCII word "GET ..." and the file name requested.
- All of your communications are being sent over the Internet so these requests are being sent inside TCP/IP packets and over the physical wires of the Internet.
- HTTP is insecure because it sends information as plain text; HTTPS provides a more secure alternative.
- Certificate authorities ensure that when you start a secure connection you're talking to the website you think you're talking to.

{{</ collapse >}}
{{< collapse summary="Click here to reveal the answer." >}}

The Internet is actually made up of many protocols that all work together to move information around a vast network of devices. These protocols are designed to work together and build upon each other like layers, with higher layers relying on the ones below them.

Together these layers and protocols solve all the different problems necessary for the computer to work at a scale where billions of devices can communicate with one another.

| Protocol / Layer | What Problem Does It Solve? | How Does It Work? |
|------------------|----------------------------|-------------------|
| **Physical Network** | Physically connecting devices to one another so that information can move through the network. | Fiber optic cables, wifi signals, or copper wires physically connect the computers, smart phones, servers, etc. that make up the Internet. Computers don't need to be directly connected to each other, just a single point on the network. |
| **IP: Internet Protocol** | Uniquely identifying people on the internet and routing messages between them. | Each device on the internet is given a unique IP address. Packets sent on the internet include to and from IP addresses. Routers along the way use this information to move data along a path of direct connections. Routing happens dynamically, meaning the path is unpredictable and changes based on network conditions. |
| **TCP: Transmission Control Protocol** | Send large messages over the Internet when accuracy is most important. You would either use TCP or UDP. | Messages are divided into packets and sent all at once. Packets are numbered so that they can be re-ordered and missing packets can be requested by the receiver. TCP is slower than UDP because error checking like this takes more time, but it is much more reliable. |
| **UDP: User Datagram Protocol** | Send large messages over the Internet when speed is most important. You would either use TCP or UDP. | Messages are divided into packets and sent all at once. There is no error-checking to ensure all packets arrive or that they're in order. UDP is faster than TCP but more errors are possible. This is useful for streaming video or online gaming because having the picture displayed quickly is more important than it being displayed with a perfectly clear picture. |
| **DNS: Domain Name System** | Translate human-readable domains like code.org or example.com into IP addresses that can be used by the Internet. | When you try to go to a domain like example.com, you computer first contacts a system of servers collectively called the DNS which keeps track of the IP addresses associated with each domain name. Communication with DNS servers happens over the Internet, meaning the request to and from servers are sent as TCP/ IP packets. |
| **HTTP: HyperText Transfer Protocol** | Allow computers to request and share webpages, audio, images, videos, and other file types on the Internet, collectively known as the world wide web. | Computers communicate in plain text like GET to request files or send data. The server that receives the request responds with the files requested which are displayed by your browser. HTTP requests are sent between computers over the internet as part of TCP/IP packets. The world wide web is just files that are requested using HTTP and sent over the Internet. |

{{</ collapse >}}

## Assignment
{{% instructions-unit-journal-update %}}

### Open a URL
Record the following in your journal:

- The URL you opened today
- A hand-drawn diagram showing _everything_ that happened behind the scenes when you opened that URL

### Internet Simulator
Log into the new version of the Internet Simulator on Code.org with a partner.

- No talking
- Ask the DNS for your classmate's IP address
- Use the IP address you get back to say hello to your classmate

{{% unit-journal-define-terms "Domain Name System (DNS)" "HyperText Transfer Protocol (HTTP)" "World Wide Web (WWW)" %}}
{{% instructions-code-org-update %}}
