---
description: Challenging the technical limits of data transmission
---

# Web2 Bridging

**Introduction**

Bridge Proxy is a commercial application based on the decentralized, zero-trust, privacy-first CONET Layer Minus  network.

Proxy services are commonly used on the Internet to help clients conceal their real IP addresses. They work by accessing websites on behalf of the client through a proxy server, offering a way to maintain privacy. Many applications natively support the use of proxy servers, such as the Firefox browser, Telegram, gaming apps, and more. Traditional proxy servers are typically remote, and clients access them over the network.

<figure><img src=".gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

**Proxy Service Structure**

1. **Traffic Reception Layer:** Receives traffic from client requests to access the Internet.
2. **Proxy Protocol Layer:** Responds to clients using different proxy protocols.
3. **Proxy Access Client:** Substitutes for the client to send Internet access requests to the target website, and the website's response is sent back to the client.

**CONET Proxy Service Structure:**

CONET divides the traditional proxy server into two parts.

1. **Client Local Part:** Receives network access traffic from the client, then packages it into CONET network communication packets and sends it to the CONET privacy network, linking to the proxy server using a wallet address.
2. **Remote Part:** Receives client requests entering through wallet addresses. The proxy server uses its own IP address to replace the client in accessing the target website, and the website's response is sent back to the client.

**CONET Proxy Service Features**

**Fragmented Traffic**

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* The CONET proxy server can take the 42 different types of requests that make up the Google homepage, use different nodes within the CONET network to simultaneously proxy the client's requests to Google.
* From Google's perspective, it cannot imagine 42 requests from different IP addresses originating from the same browser page. From the viewpoint of network monitors, the client appears to be accessing multiple different websites, disrupting the big data analysis of the monitors. The proxy services provided by participants within CONET also cannot piece together the client's network access traces.

1.  **Traffic Obfuscation Technology:**

    Benefit from the traffic obfuscation technology of the CONET wallet address communication network, CONET proxy services conceal the clear fingerprints of proxy service communication, making it difficult for network monitors to identify that the client is using VPN privacy communication. CONET proxy usage can be employed to bypass network blocking technologies.

\
