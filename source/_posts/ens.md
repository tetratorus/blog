---
title: Ethereum Name Service
subtitle: 'human-readable names for everything'
tags: [ethereum, ens, icann60]
readtime: 3 min read
date: 2017-10-28 16:54:44
---

One of the problems of Ethereum, and blockchains in general, is that its identifiers are long hexadecimal strings like 0x6ce8df6c2c69c399ce020098f68f0944f8d12b23.

This makes them really hard to remember, and difficult to read. Something like the previous address of 0x6ce8DF6c2C69c399Ce002098F68F0944F8d12B23 could easily be mistaken for 0x6c38DF6c2C69c399Ce002098F68F0944F8d12B24.

\(Joke's on you, all three addresses are different.\)

In order to reduce the incidence of phishing attacks like these, and also to make life easier for everyone, Nick Johnson conceptualized and designed the Ethereum Name Service (ENS) - a system to address resources by name.

In many ways this is similar to the DNS system where we do domain lookups. However, there are several benefits to doing this on the blockchain:
- It is resistant to DDoS attacks. Theoretically, anyone can run a full Ethereum node and verify the lookups on their own, without relying on external servers.
- It is transparent. ENS operations are just Ethereum transactions, which can be seen by everyone.
- It was built to be upgradeable. The only part of the system that is difficult to upgrade is the ENS registry, which only maintains a mapping of names to owners and resolvers, and is so simple in terms of functionality that it is unlikely to need an upgrade.

Aside from addressing resources on the blockchain, ENS can also be used to assign names to other kinds of records like IPFS records, or even DNS records.

Learn more about ENS from their [official website](https://ens.domains), or download slides [here](/misc/slides.pdf)
