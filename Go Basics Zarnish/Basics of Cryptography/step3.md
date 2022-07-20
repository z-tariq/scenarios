---
title: Basic Principles
---

There are five primary functions of cryptography:

**Privacy/confidentiality:** Ensuring that no one can read the message except the intended receiver.
**Authentication:** The process of proving one's identity.
**Integrity:** Assuring the receiver that the received message has not been altered in any way from the original.
**Non-repudiation:** A mechanism to prove that the sender really sent this message.
**Key exchange:** The method by which crypto keys are shared between sender and receiver.

**Forward Secrecy (aka Perfect Forward Secrecy):** This feature protects past encrypted sessions from compromise even if the server holding the messages is compromised. This is accomplished by creating a different key for every session so that compromise of a single key does not threaten the entirely of the communications.

**Perfect Security:** A system that is unbreakable and where the ciphertext conveys no information about the plaintext or the key. To achieve perfect security, the key has to be at least as long as the plaintext, making analysis and even brute-force attacks impossible. One-time pads are an example of such a system.

**Deniable Authentication (aka Message Repudiation):** A method whereby participants in an exchange of messages can be assured in the authenticity of the messages but in such a way that senders can later plausibly deny their participation to a third-party
