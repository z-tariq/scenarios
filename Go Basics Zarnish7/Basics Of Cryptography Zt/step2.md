---
title: Principal categories of cryptographic algorithms
---

**Symmetric (or Secret Key) Cryptography:**

Symmetric cryptography using 1 key for en-/decryption or signing/checking

In symmetric cryptography, both sender and receiver uses the same secret key to encrypt and decrypt a message.
Some algorithms include Blowfish, AES, RC4, DES, RC5, and RC6. The most widely used symmetric algorithm is AES-128, AES-192, and AES-256. All AES algorithms uses the block size of 128-bit but different size of key lengths (128, 192, 256).

**Asymmetric (or Public Key) Cryptography:**

Asymmetric cryptography using 2 different keys for en-/decryption or signing/checking

Asymmetric cryptography uses a key pairs — public and private key. It works in a way, message encrypted with either public or private key can only be decrypted using the other key of the pair. That is public key to encrypt, private key to decrypt and private key to encrypt, public key to decrypt. Public keys are disseminated in public network whereas private keys are only known to the owners. This key pair cryptography differs from symmetric cryptography which uses one secret key.

Some algorithms include RSA, ELC, Diffie-Helman key exchange, etc.
Asymmetric Cryptography has 2 usages, data encryption and digital signature.
