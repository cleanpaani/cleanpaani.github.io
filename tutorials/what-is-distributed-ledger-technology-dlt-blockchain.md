---
layout: tutorial
title: What is Distributed Ledger Technology (DLT) used in blockchain?
categories: ['tutorials', 'fundamentals']
description: Proof-of-work is an important concept and underlying principle for blockchains and any cryptocurrency like bitcoin, ethereum, etc. 
---

In this tutorial, let us get a good understanding of Distributed Ledger Technology which is fundamental to the world of cryptocurrencies.

As the name suggests,
> distributed ledger technology refers to a system where the data (the ledger) is distributed to different entities on a network; where each of these entities independently holds and verifies the data and the entire network votes to decide which entries in the ledger is genuine or fraudulent.

However, before we dive into distributed ledgers, let us first take a look at the definition of a ledger. In most dictionaries,
> a ledger is defined as a book or collection of financial accounts.

If we break down this definition, it basically tells us that every transaction that takes place in a company, business, or a bank is recorded into a book or a database called a ledger.

A ledger has records that describe how much money came in, how much money went out, people’s names who were involved in the transactions, bank accounts, the overall balance (which keeps changing with time).

As you can see, **a lot of critical information is stored in a ledger and it has to be protected.**

### **Centralized Ledger**
Generally, there is an accountant or an accounting software which maintains this ledger. That is there is a single entity who is responsible for the accuracy and integrity of this ledger. Since the power is centralized – this method can be referred to as centralized ledger technology.

### **Drawbacks of a centralized ledger scheme**
Centralizing the power in the hands of one person, or one server creates a single-point-of-failure and it exposes the ledger to a lot of attacks. A hacker can go in and change the dollar numbers in his account, or a corrupt employee of the bank can change numbers to favor someone else, or the bank can go down if someone erases the ledger!  Most banking institutions have safeguarded against such issues, but, we’re highlighting some drawbacks of a centralized system.

### **So do we decentralize and distribute the ledger?**
Let’s say there is a bank and it has a central ledger stored in Chicago. Suppose the bank manager decides that he will create two ledgers – one in Chicago and one in New York. And he creates a policy that stipulates,
- both ledgers are maintained independently on different servers with different employees managing them.
- every transaction goes to both ledgers for independent verification.
- at the end of each hour, the ledgers are tallied to see if they match. If there is a mismatch, there are audited to see where the mismatch happened to catch any wrong-doing.

This ensures that transactions are verified independently with interference from the other branch. So if there is one corrupt employee at one branch, he will be caught when the transactions are cross-verified. This is an example of decentralization.

**Do you see how this improves reliability and trust?**

But, this solution can be hacked too. The bank manager only created two servers .. right? It’s pretty easy to hack and take control of both of them and manipulate the records, rendering the system useless. So what do we do next?

### **Distributed Ledger Technology**
Let’s use the principle of scale to solve this problem. Instead of two servers, let us suppose that the ledger is now on 500 different servers in different parts of the country. Now a hacker has to attack and capture a lot more machines which makes it an unattractive idea.

> So, to distribute the process of validation and consensus over a large number of interconnected nodes is a fundamental property of distributed ledgers.

However, there are some problems with DLT as well. If I hack 251 servers and ensure that they all give the same wrong ledger, then the system will be in doubt whether to favor the majority or minority. Fyi, this is called the 51% attack.

In real-life, DLT is used along with other concepts like cryptographic hashing, public-private keys, proof-of-work, proof-of-stake, timeservers, etc. to harden and secure the system.

Let’s study these in other tutorials.

### **Summary of DLT**
To summarize, in distributed ledger technology (DLT), the ledger/database of records is replicated on several distributed nodes. Each of these nodes work on the new transactions to verify them and then based on a consensus, the nodes collectively decide which transactions are genuine and can be added to the blockchain.

### **Advantages of using DLT**
- distributed implies a lower security risk as it eliminates the single-point-of-failure.
- DLT uses a consensus algorithm to decide which transactions are genuine and fraudulent and this improves trust in the system.
- in DLT, every node has a complete history of all the records, and so even if one or more nodes go offline, the transaction history is not lost.

Hope you understood how distributed ledger technology works!