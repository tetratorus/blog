---
title: Intel Secure Guard Extensions (SGX)
subtitle: secure computing + DLT
tags: [corda, secure computation]
readtime: 5 min read
date: 2017-04-16 14:57:22
---

So if you have been keeping an eye on R3 and their "distributed ledger" solution, Corda, you will have realized that a particular piece of technology called Intel SGX does a lot of the heavy-lifting for Corda.

If you are interested in an in-depth (and very long) review of what Intel SGX is about, refer to this paper [here.](https://eprint.iacr.org/2016/086.pdf)

For the rest of the us, the basic idea behind Intel SGX is that it allows any Intel SGX enabled CPU (introduced in Skylake) to perform remote attestations of the software that is being run on the CPU. This basically means that your CPU can now run instructions in a manner such that you, the owner, cannot tamper with its execution.

This is done by having low-level sensors that monitor and report on the state of the processor when it is executing a particular piece of software inside of an "enclave". The information is signed via a platform key that is unique to each CPU.

The benefit of this limitation is that developers are now able to securely rely on computations that are done remotely. In the context of Corda, this removes the need for a distributed consensus protocol (i.e. blockchain), because every node can be trusted to follow the rules of Corda's transaction verification software.

Of course, there are many limitations, including the fact that Intel could potentially ship malicious instruction sets, but considering the fact that most Bitcoin mining rigs run on Intel chips, and most computers in the world all run on Intel CPUs too, it's really a non-issue. Some vulnerabilities have also been discovered [here](https://arxiv.org/abs/1702.08719), and [here](https://www.blackhat.com/docs/us-17/thursday/us-17-Swami-SGX-Remote-Attestation-Is-Not-Sufficient-wp.pdf), but as with all experimental technology, we are certain to see improvements as Intel SGX matures.

For anyone who has an Intel SGX enabled chip, feel free to check out Intel's [SDK](https://software.intel.com/en-us/sgx).
