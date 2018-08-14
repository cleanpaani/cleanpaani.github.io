---
layout: tutorial
title: What is proof-of-stake and how is it different from proof-of-work?
categories: ['tutorials', 'fundamentals']
description: Proof-of-stake protocol involves people depositing coins with a cryptocurrency in order to get the right to mine or forge a coin. It is faster, more efficient than proof-of-work.
---

Proof-of-stake and proof-of-work are protocols aimed at securing and preventing attacks on the blockchain and cryptocurrency infrastructure. Both aim at the same goal but from very different directions. Let's find out what proof-of-stake tries to achieve and how it differs from the proof-of-work protocol.

### **What is proof-of-work?**
In another tutorial, we give an in-depth explanation of the proof-of-work system. Let us summarize that tutorial here.

> What's proof-of-work? In the proof-of-work protocol, the user has to solve an extremely hard problem and the process of solving it very resource intensive.

Essentially, the problem serves as a deterrent to anyone who wishes to hack into the system (or capture the blockchain). Though the proof-of-work protocol was published by Cynthia Dwork and Moni Naor in 1993, it formed the basis of Satoshi Nakamoto’s path-breaking white paper and found its way into Bitcoin when it was actually created.

Using a proof-of-work model that needs heavy computation resources has essentially prevented attacks, increased trust, and allowed for a distributed ledger architecture to flourish.

### **A quick introduction to mining**
Every time a few transactions are conducted in bitcoin, these transactions are sent out to miners who check if these are bonafide transactions. The verification process is called mining and the people who perform them are called miners.

**Mining bitcoins is extremely resource-intensive (essentially it is a proof-of-work system) and it is quite common to see several people pool their resources and mine bitcoins as a group of miners.**

After a miner has successfully mined a block, he informs this to all his peers and they verify that his calculations are correct. If it is correct, then,
- the verified transactions are added to the blockchain (as a new block),
- and, the miner is rewarded with some bitcoins.

With this understanding of mining, let's see what are the short-comings of the proof-of-work system.

### **Drawbacks of proof-of-work**
If we consider bitcoin as an example, each miner is given a few bitcoins every time he successfully mines a block.

> The Bitcoin block mining reward halves every 210,000 blocks, and currently as it stands (in mid-2018), the coin reward will decrease from 12.5 to 6.25 coins.

For detailed information, check out https://www.bitcoinblockhalf.com/

Over time, the number of blocks will reach zero and so will the rewards for mining a block. After the reward reaches zero, then the miners will be paid a small transaction fee for each of the transactions in a block.

**The big question is - will the transaction fee be sufficient to retain existing miners and attract new miners?**

If miners start dropping out of bitcoin, then the system becomes vulnerable to a 51% attack, where a hacker or group of hackers can control more than 51% of the network and start manipulating the blockchain. So - if there are few miners, then the system is vulnerable to 51% attacks.

In a bid to counter these problems, new protocols such as the proof-of-stake system are being proposed. Let's learn more about it!

### **What is proof-of-stake?**
According to the definition on Wikipedia,

> in the proof-of-stake system, the creator of the next block is chosen via various combinations of random selection and wealth or age (i.e., the stake).

The ethereum FAQs define it as follows: **proof of Stake (PoS) is a category of consensus algorithms for public blockchains that depend on a validator's economic stake in the network.**

That is, in the proof-of-stake system, instead of sending the transactions to all the miners in the network for validation, one miner is chosen based on some formula and only he will mine and validate the transactions. This chosen miner is paid a small transaction fee if he is successful.

And, in the proof-of-stake system, a miner is called a "forger".

### **Proof-of-stake system and its environmental impact**
The first implication of the proof-of-stake system is that it is more environmentally friendly than the proof-of-work system.

In the PoW system, if there are 1000 miners, it is possible that all 1000 miners will start mining a particular block of transactions. In the end, only one will succeed and the efforts of 999 will be wasted. This system causes a huge waste of electricity - something our planet cannot afford.

However, in proof-of-stake systems, only one forger works on a transaction and this conserves electricity and is a less wasteful system.

### **How are forgers chosen in proof-of-stake?**
As Vitalik Bueterin puts it beautifully when he says in [[1]](https://medium.com/@VitalikButerin/a-proof-of-stake-design-philosophy-506585978d51)

> The “one-sentence philosophy” of proof of stake is thus not “security comes from burning energy”, but rather “security comes from putting up economic value-at-loss”

Let's try to understand what the above quote means. For an altcoin that wants to use proof-of-stake, it maintains a pool of validators. This pool consists of people who want to validate or forge blocks and they have to have a stake in the system. They should lock up or deposit their coins into a "bank" to prove that they are serious validators. This is why it is called a proof-of-stake.

After you have a pool of validators, you need a way to choose who validates or forges a block. There are different ways to do this, but in practice, there are two major types: chain-based proof of stake and BFT-style proof of stake.

- In **chain-based proof of stake**, the algorithm selects a validator and assigns that validator the right to create a single block. The algorithm is a pseudo-random one and the block has to point to a previous block, and this block must point to some previous block, and this ensures that over a period of time, most of the blocks converge to a single constantly growing chain. (reference)
- In **BFT-style proof of stake**, validators are randomly assigned the right to propose blocks (i.e. forge blocks), but, this is followed up by a voting process where every validator has to vote on whether a block ends up in the chain or not. This provides additional security. (reference).

In either case, if a chosen validator tries to be dishonest with the system, then his stake is confiscated and he is penalized. This is a huge financial loss and serves as a deterrent.

### **The advantage of proof-of-work systems is that**
- it is energy efficient and far fewer people have to process the blocks in order to validate it.
- it is tolerant to 51% attacks as it assumes that the pool of validators who have a stake in the process is honest. And, the ability to penalize a dishonest validator discourages bad elements.

There are several cryptocurrencies that use proof of stake (like NEO, PeerCoin, GridCoin, NXT) and Ethereum might be switching to it as well. So, its something to look out for and understand well.