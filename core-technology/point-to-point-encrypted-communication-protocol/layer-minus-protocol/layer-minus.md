# Layer Minus

**Layer Minus Protocol in CONET**

The Layer Minus protocol establishes a network protocol for peer-to-peer communication, using wallet addresses as unique identifiers to distinguish devices from each other. This protocol outlines how data should be encapsulated, addressed, transmitted, routed, and received at its destination in a peer-to-peer communication network. The use of wallet addresses as unique identifiers ensures a secure and efficient means of communication within the CONET ecosystem.

<figure><img src="../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

**Asymmetric Cryptography:**

**Cryptography encompasses the following elements:**

Confidentiality: Ensures that messages can only be accessed by authorized parties. Integrity: Detects whether messages have been tampered with. Authentication: Both the sender and receiver need to verify their identities. Non-Reputation: Provides proof of transactions between message sender and receiver.

Asymmetric Cryptography is a cryptographic technique in which each user possesses a pair of keys:

**Public Key:**&#x20;

Used to encrypt messages. Private Key: Used to decrypt messages encrypted with the public key. The private key is a randomly generated string of approximately fifty alphanumeric characters with no fixed logic or pattern. The private and public keys are generated as a pair by a computation process, ensuring uniqueness and non-repetition.

**Wallet Address:**

A wallet address is derived from the public key through specific HASH calculations and encoding in asymmetric encryption. Before using the CONET network, users need to create their public-private key pair and wallet address to distinguish their position on CONET. Wallet addresses are created on-demand by users and do not have a centralized allocation mechanism.

**Public Key Encryption:**

In a public key encryption system, anyone with the public key can encrypt a message, generating ciphertext. However, only those who know the corresponding private key can decrypt the ciphertext to obtain the original message.

**Asymmetric Cryptography Digital Signatures:**

Asymmetric cryptography is widely used in digital signatures to ensure the authenticity and non-repudiation of documents or messages.

**Side-Channel Information Leakage in Ciphertext:**

Anyone obtaining the ciphertext does not need to decrypt it. By performing cryptographic calculations on the ciphertext, one can acquire the public key ID used to encrypt that ciphertext.

**Layer Minus Network Data Packet:**

A Layer Minus network data packet does not contain any metadata. It is a data packet encrypted using the public key of the recipient.

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

**Layer Minus Nodes:**

Nodes are crucial facilities that make up the Layer Minus wallet routing network, and they perform the following tasks:

1. **Inter-Node Data Transmission:**
   * When a node receives encrypted data not associated with itself, it forwards that encrypted data to the intended destination node.
   * The destination node pays the corresponding traffic fee for receiving the forwarded data.
2. **Proxy Recipient:**
   * Nodes accept client commissions to act as proxies for clients receiving encrypted messages at a specific wallet address.
   * When the commissioned client is online, the node forwards the encrypted messages to that client.
   * The node pre-collects the client's payment for using the service and deducts fees for forwarding data from other nodes in the prepaid amount.
3. **Proxy Recipient Data Caching:**
   * Nodes accept client commissions to act as proxies for clients receiving encrypted messages at a specific wallet address.
   * When the commissioned client is offline, the node caches the encrypted messages.
   * Upon the next online session of the commissioned client, the node sends all cached encrypted messages, calculates the corresponding storage fees, and deducts them from the prepaid amount.
4. **Online Client Data Delivery:**
   * Clients, through the HTML protocol, connect to an entry node and link to a proxy recipient node associated with their wallet.
   * The proxy recipient, using the HTML Server-Sent Events (SSE) communication protocol, pushes incoming data packets to the client.

**Routing**

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

**Traffic Obfuscation:**

Layer Minus operates a virtual network established using the W3C HTTP protocol at the application layer of the OSI network communication model. The communication within Layer Minus does not exhibit any distinct characteristics; this is a unique feature of the Layer Minus network.
