---
title: Cryptographic Primitives
subtitle: the building blocks
tags: []
readtime: 5 min read
date: 2017-01-16 14:57:22
---

As every cryptographer knows: (don't roll your own security)[http://security.stackexchange.com/questions/18197/why-shouldnt-we-roll-our-own].

Many strategies and protocols have been tried and tested over the years, and in order to discourage people from reinventing the wheel, cryptographers usually reference well-known implementations/ideas that have been proven to work - these concepts are known as (cryptographic primitives)[https://en.wikipedia.org/wiki/Cryptographic_primitive].

Here are some common cryptographic primitives, with links to simplified explanations:
(One-way hashing)[https://www.youtube.com/watch?v=b4b8ktEV4Bg]
(Symmetric key encryption)[https://youtu.be/ERp8420ucGs?t=53s]
(Public key cryptography)[https://medium.com/@vrypan/explaining-public-key-cryptography-to-non-geeks-f0994b3c2d5#.gaz3mnes8]
(Diffie-Hellman key exchange)[https://youtu.be/YEBfamv-_do?t=2m6s]
(Zero-knowledge proof)[https://youtu.be/0Sy6nb72gCk?t=3m41s]
(Secure random number generation)[http://diamond.boisestate.edu/~liljanab/ISAS/course_materials/BBSpresentation.pdf]

Apart from these basic primitives, there are also lesser-known, advanced cryptographic primitives. Many of them are composed of basic cryptographic primitives:
Sponge function
One-way compression function
Identity-based encryption
Functional encryption
Stream ciphers
Secure multi-party computation
Lattice based encryption
Group signatures
Paillier encryption
Oblivious transfer
Certificate transparency
Witnessing
Redactable Signatures
Sanitizable signatures
Chameleon hash functions
Fully homomorphic encryption
Oblivious RAM
Non-malleable codes
Attribute-based encryption
Order-revealing encryption
Physical Unclonable Functions

Several of these cryptographic primitives from the basis of the popular protocols / projects that are in use today. For example, (Monero)[https://en.wikipedia.org/wiki/Monero_(cryptocurrency)], a cryptocurrency that focuses on privacy, makes use of ring signatures to prevent identities from being revealed via big data analytics.
