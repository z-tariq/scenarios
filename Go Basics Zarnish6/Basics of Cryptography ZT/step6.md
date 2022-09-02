---
title: Cryptography in Go
---

The root package for cryptography in Go is **crypto**, and it has a number of sub packages, such as aes, cipher, sha, and rsa to name but a few. Also, there is a package called **hash**, which provides Golang developers with a common interface implemented by all hash functions such as MD5, SHA256, and Hashing with Key (HMAC).


The crypto library of Go provides implementation for a number of cryptographic algorithms such as AES, Cipher, SHA, and RSA. Here is a quick use of the AES function. The acronym AES stands for Advanced Encryption Standard. It is a block cipher technique where a plaintext is processed in blocks of 16 bytes. Each block is encrypted separately using a key of 32 bit length.

Go provides functions that implement AES algorithms, – programmers can invoke them in their Go programs as shown in the following Golang code example:
