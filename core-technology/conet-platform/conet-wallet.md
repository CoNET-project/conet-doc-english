# CONET Wallet

The CONET Wallet provides functionalities similar to mainstream wallets such as MetaMask and Coinbase.

In a groundbreaking move for the blockchain decentralized application (DApp) industry, the CONET Wallet utilizes decentralized cloud technology to synchronize information across multiple wallet addresses under the same 12-word mnemonic account, allowing Web3 users to enjoy a user experience similar to that of Web2.

However, the primary concern for Web3 users is wallet security. Why is the CONET Wallet, which stores the most sensitive information, such as private keys, in decentralized cloud storage, more secure than cold wallets protected by physical devices?

The difference between digital and physical reality lies in the fact that digital data can be encrypted, fragmented, and decrypted for recovery, maintaining its original value even after recovery. In contrast, physical reality loses its value once it is fragmented.

Leveraging the characteristics of digital data and cryptography, CONET introduces a novel approach to wallet security:

**Fragmentation:** The wallet file is split into multiple fragments.&#x20;

**Iterative Encryption:** Each fragment undergoes triple iterative encryption.&#x20;

**Privacy File Naming**: Hash algorithms generate file names associated with mnemonic phrases (with no correlation to wallet addresses or private keys), ensuring concealment. Encrypted fragments are hidden within the decentralized storage ocean of fragments (currently utilizing CONET's proprietary IPFS-compatible decentralized protocol).

```typescript
const SRP: string = ''                                //    Mnemonic Phrase
const currentVer: number = exampleVersion            //    Version number
const root = ethers.Wallet.fromPhrase(SRP)            //    root of account
const FragmentNameWallet = root.deriveChild(65536)    //    connect to no.65536 wallet
const firstVerFileName = ethers.id(FragmentNameWallet.address)    //    hash
const currentVer = '0x' + (BigInt(firstVerFileName) + BigInt(currentVer)).toString(16)
const mainFragmentName = ethers.id( ethers.id( ethers.id(currentVer)))
```

**Difficulty of Retrieval**: With decentralized storage and non-related hash file names, retrieving a user's wallet file from the vast ocean of fragments becomes exceedingly challenging. This ensures that even if someone gains access to the fragments, they would struggle to identify and assemble the relevant pieces.

**Sequential Reconstruction**: Even if all the fragments are obtained, reconstructing them in the correct order poses a monumental challenge. Without the correct sequence, the wallet file remains unusable.

**Encryption Strength**: The wallet file, encrypted with [AES-256-GCM,](https://en.wikipedia.org/wiki/Galois/Counter\_Mode) is practically impervious to [brute-force attacks.](https://www.kiteworks.com/risk-compliance-glossary/aes-256-encryption/) Additionally, CONET employs triple iterative encryption on the fragments, enhancing security against decryption attempts.

**Cold Wallet Vulnerabilities**: Physical cold wallets, despite their perceived security, are susceptible to various vulnerabilities. Once obtained, the contents are readily accessible. In contrast, accessing a CONET Wallet is akin to finding a needle in a haystack and then solving a complex puzzle. Thus, CONET offers superior security compared to physical cold wallets.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

**CONET Platform Local Unlocking Protected by Anti-Brute Force** [**Scrypt Cryptographic Algorithm**](https://en.wikipedia.org/wiki/Scrypt)

When accessing the CONET platform, users are required to enter a simple 6-digit password for easy recall. The CONET platform utilizes the Scrypt algorithm to randomly generate a strong password that can withstand brute-force attacks by supercomputers, thus safeguarding locally stored fragmented sensitive information.

**Simple Management of Multiple Wallets**

Whether generating new wallets or importing external private keys, a CONET user can manage thousands of wallets, each labeled with a name and color for easy identification.

**One-Click Wallet Recovery with Mnemonic Phrase**

By entering the mnemonic phrase, users can effortlessly restore all wallets from decentralized cloud storage such as IPFS, including wallet images, names, and colors.

Synchronization of Wallet Information Across Different Devices Under the Same CONET Platform Account

Phones and computers can share all wallet information under the same account and synchronize the latest status with each other.

**Intelligent Asset Management**

The CONET platform automatically scans the main network, searching for all wallets and encrypted assets across all major networks, including NFT assets, without requiring manual user input.

**Global Access and Privacy-Preserving On-Chain Information Exchange**

CONET provides high-quality, scientist-resistant private high-speed RPC nodes for all major networks. Users can securely and privately interact with all mainstream blockchains globally through the CONET Layer Minus network without IP addresses, ensuring unrestricted access and privacy.
