---
description: Computers communicate by uniquely identifying TCP/IP addresses
---

# TCP/IP Protocol

TCP/IP provides a point-to-point connection mechanism that standardizes how data should be encapsulated, addressed, transmitted, routed, and received at the destination.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

[**IP Address**](https://en.wikipedia.org/wiki/IP\_address)

When a device is connected to the network, the device will be assigned an IP address, which is used as a unique identifier. Devices can communicate with each other through IP addresses on the Internet around the world. Without an IP address, we have no way of knowing which device is the sender and which is the receiver. An IP address has two main functions: identifying a device or network and addressing it.

In 1981, the [IETF](https://www.ietf.org/) defined IPv4 for 32-bit IP addresses. With the development of the Internet, IPv4 was gradually allocated and exhausted. Its upgraded version, [IPv6](https://datatracker.ietf.org/doc/html/rfc2460), was officially announced by the [Internet Engineering Task Force](https://en.wikipedia.org/wiki/Internet\_Engineering\_Task\_Force) in the form of Internet Standards Specification ([RFC 2460](https://datatracker.ietf.org/doc/html/rfc2460)) in December 1998.

**IP address space allocation**

IP address space, whether IPv4 or IPv6, is allocated globally by the centralized Internet Assigned Numbers Authority ([IANA](https://en.wikipedia.org/wiki/Internet\_Assigned\_Numbers\_Authority)) and five other regional Regional Internet Registries ([RIR](https://en.wikipedia.org/wiki/Regional\_Internet\_registry)) are assigned to the Internet within their designated area.

**IP address leasing**

When users use the Internet, they need to complete [KYC](https://en.wikipedia.org/wiki/Know\_your\_customer) (Know Your Customer) procedures with the [Internet service provider](https://en.wikipedia.org/wiki/Internet\_service\_provider) before they can rent a globally unique IP address from an ISP.

[**Routing**](https://en.wikipedia.org/wiki/Routing)

Due to the complex structure of the Internet, routing determines how two computers find each other and find a suitable best path. The [router](https://en.wikipedia.org/wiki/Router\_\(computing\)) is the key facility that determines how to forward an [IP data packet](https://en.wikipedia.org/wiki/Network\_packet) and connect to each other on the Internet. IP packets can pass through multiple routes, but there is no guarantee that they will arrive or that they will arrive in order.

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

**Virtual tunnel concept**

Through the layering concept, Internet communication can be simplified into host-to-host network communication and application-to-application network communication.
