---
Date: 2024-04-09
tags:
  - web
  - programming
---
## What is the Internet Protocol (IP)?
The Internet Protocol (IP) is a protocol, or set of rules, for routing and addressing packets of data so that they can travel across networks and arrive at the correct destination. Data traversing the Internet is divided into smaller pieces, called <mark style="background: #ABF7F7A6;">packets</mark>. IP information is attached to each packet, and this information helps <mark style="background: #D2B3FFA6;">routers</mark> to send packets to the right place. Every device or <mark style="background: #CACFD9A6;">domain</mark> that connects to the Internet is assigned an <mark style="background: #FFB86CA6;">IP address</mark>, and as packets are directed to the IP address attached to them, data arrives where it is needed.

>[!info]
>- In networking, a packet is a small segment of a larger message. Data sent over computer networks*, such as the Internet, is divided into packets. These packets are then recombined by the computer or device that receives them.
>- A router is a device that connects two or more packet-switched networks or subnetworks.
>- A domain name is a string of text that maps to an alphanumeric IP address, used to access a website from client software.
>- An IP address is a unique identifier assigned to a device or domain that connects to the Internet.

Once the packets arrive at their destination, they are handled differently depending on which transport protocol is used in combination with IP. The most common transport protocols are TCP and UDP.
## IPv4 vs. IPv6
There are two versions of IP, IPv4 and IPv6. Fourth version uses a decimal notation (e.g., “192.168. 1.1”), while sixth version employs hexadecimal format (e.g., “2001:0db8:85a3:0000:0000:8a2e:0370:7334”). IPv6's 128-bit addressing provides an almost limitless pool of unique addresses, eliminating the address scarcity problem that IPv4 faces. <mark style="background: #BBFABBA6;">But still most of the sites uses IPv4</mark>.
## What is an IP packet?

IP packets are created by adding an IP header to each packet of data before it is sent on its way. An IP header is just a series of bits (ones and zeros), and it records several pieces of information about the packet, including the sending and receiving IP address. IP headers also report:
- Header length
- Packet length
- Time to live(TTL), or the number of network hops a packet can make before it is discarded
- Which transport protocol is being used (TCP, UDP, etc.)
In total there are 14 fields for information in IPv4 headers, although one of them is optional.

## What is TCP/IP?

The Transmission Control Protocol (TCP) is a transport protocol, meaning it dictates the way data is sent and received. A TCP header is included in the data portion of each packet that uses TCP/IP. Before transmitting data, TCP opens a connection with the recipient. TCP ensures that all packets arrive in order once transmission begins. Via TCP, the recipient will acknowledge receiving each packet that arrives. Missing packets will be sent again if receipt is not acknowledged.

TCP is designed for reliability, not speed. Because TCP has to make sure all packets arrive in order, loading data via TCP/IP can take longer if some packets are missing.

TCP and IP were originally designed to be used together, and these are often referred to as the TCP/IP suite. However, other transport protocols can be used with IP.

## What is UDP/IP?

The User Datagram Protocol, or UDP, is another widely used transport protocol. It is faster than TCP, but it is also less reliable. UDP does not make sure all packets are delivered and in order, and it does not establish a connection before beginning or receiving transmissions.

# References
1. https://www.cloudflare.com/learning/network-layer/internet-protocol/