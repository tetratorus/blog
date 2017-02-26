---
title: Bitcoin Transactions Explained
subtitle: inputs and outputs
date: 2017-01-02 23:38:23
readtime: 5 min read
tags: [bitcoin, short]
---
I've seen many (complicated) explanations of bitcoin transactions, but in short:
<h3>**A transaction is a record that contains _inputs_ and _outputs_.**</h3>

An input references a previous transaction's output. The correct key has to be provided in order to spend this output.

That's really all there is, the rest are just details.
<br>
<hr>
**Q:** How do I know how many bitcoins I own?
**A:** Sum up the value of transaction outputs that can be unlocked by your private key. Wallets do that for you automatically.

**Q:** How do I send bitcoins to someone else?
**A:** Create a transaction where the input references some bitcoin that you own. Wallets do that for you automatically.

**Q:** How do I send a partial amount to someone if my input is too large?
**A:** Create a transaction with a large input and two outputs: a small output to your payee, and a large output back to yourself. Wallets do that for you automatically.

**Q:** What about miner fees? Are those an output?
**A:** No. Just set your outputs to be smaller than your inputs. The difference is implicitly taken as the miner's fee. ... Wallets do that for you automatically.

**Q:** But, if all transactions reference another transaction, where did the first transaction come from?
**A:** Ok you got me. The first transaction of a block is a [special transaction](https://bitcoin.org/en/glossary/coinbase-transaction) that is created when the block is mined.
