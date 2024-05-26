---
Date: 2024-04-09
tags:
  - web
  - programming
---
## What is a network protocol?
In networking, a protocol is a set of rules for formatting and processing data. Network protocols are like a common language for computers. The computers within a network may use vastly different software and hardware; however, the use of protocols enables them to communicate with each other.
If one computer uses the [Internet Protocol (IP)](IP.md) and a second computer does as well, they will be able to communicate.
>[!hint]
>Most protocols are assigned to a specific  layer in [[Open Systems Interconnection (OSI) model]]

## Which protocols run on the network layer?(3 layer)
[[IP]] is a network layer protocol responsible for routing. But it is not the only network layer protocol.
- IPsec: Internet Protocol Security (IPsec) sets up encrypted, authenticated IP connections over a virtual private network (VPN). Technically IPsec is not a protocol, but rather a collection of protocols that includes the Encapsulating Security Protocol (ESP), Authentication Header (AH), and Security Associations (SA).
- ICMP: The Internet Control Message Protocol (ICMP) reports errors and provides status updates. For example, if a router is unable to deliver a packet, it will send an ICMP message back to the packet's source.
- IGMP: The Internet Group Management Protocol (IGMP) sets up one-to-many network connections. IGMP helps set up multicasting, meaning multiple computers can receive data packets directed at one IP address.
## What other protocols are used on the Internet?
Some of the most important protocols to know are:
- **TCP**: As described above, TCP is a transport layer protocol that ensures reliable data delivery. TCP is meant to be used with IP, and the two protocols are often referenced together as TCP/IP. <mark style="background: #CACFD9A6;">(4 OSI layer)</mark>
- **HTTP**: The Hypertext Transfer Protocol (HTTP) is the foundation of the World Wide Web, the Internet that most users interact with. It is used for transferring data between devices. HTTP belongs to the application layer, because it puts data into a format that applications (e.g. a browser) can use directly, without further interpretation. The lower layers of the OSI model are handled by a computer's operating system, not applications.<mark style="background: #CACFD9A6;">(7 OSI layer)</mark>
- **HTTPS**: The problem with HTTP is that it is not encrypted — any attacker who intercepts an HTTP message can read it. HTTPS (HTTP Secure) corrects this by encrypting HTTP messages.<mark style="background: #CACFD9A6;">(7 OSI layer)</mark>
- **TLS/SSL**: Transport Layer Security (TLS) is the protocol HTTPS uses for encryption. TLS used to be called Secure Sockets Layer (SSL).<mark style="background: #CACFD9A6;">(4 OSI layer)</mark>
- **UDP**: The User Datagram Protocol (UDP) is a faster but less reliable alternative to TCP at the transport layer. It is often used in services like video streaming and gaming, where fast data delivery is paramount.<mark style="background: #CACFD9A6;">(4 OSI layer)</mark>


# References 
1. https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/