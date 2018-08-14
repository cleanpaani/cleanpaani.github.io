---
layout: tutorial
title: What is the 51% attack?
categories: ['tutorials', 'fundamentals']
description: 51% attack states that if someone has 51% of the nodes in the blockchain, then he can control which blocks become canonical. Let's learn more about this. 
---

Everyone talks about how secure a distributed ledger technology (DLT) is and we’ve covered this topic in our tutorial on DLT as well. But, there is a potential attack that can bring down the trust in the entire network and its called the 51% attack.

### **51% attack defined**
> The 51% attack states that if someone controls 51% of the nodes in the blockchain or bitcoin network, then he can control which blocks are validated or become canonical and thus start double-spending or simply invalidate the entire currency.

### **Distributed Ledger Technology and Consensus**
We’ve studied in our tutorial on distributed ledger technology (DLT) that the strength of decentralization lies in replicating the data across several independent nodes which individually validate transactions and decide which transactions are genuine, based on a consensus policy. This consensus policy is where the 51% attack begins.

Let’s understand it with an example.

### **Example of the 51% attack**
Suppose I have 100 computers on my cryptocurrency and all of them are miners. After a transaction has been validated by one of the machines, it broadcasts it to all the computers on the network for validation. If 10 of them say it is invalid and 89 say it is valid, then I’ll assume it is valid (majority wins!).


So now if I am a hacker and I want to control the network (and allow my fraudulent transactions to enter the chain), then all I have to do is capture 51 computers and ensure that they all approve my fraudulent block. The remaining 49 (actually, 48) will give a different result (disapproved), but by consensus (majority vote), I will win and my fraudulent transaction can enter the blockchain.

**In reality, though, a public cryptocurrency like bitcoin will have 1000s of miners and it is hard to capture 51% of the voting power.**

Additionally, if this fraud goes on for a while and it is detected, then nobody will trust the blockchain and the value of the currency will drop. Result? the hacker's coins will be rendered useless (unless he already encashed them!) and everybody loses!

Hope you understood how the 51% attack works!