---
layout: tutorial
title: What is cryptographic hashing (used in blockchain)?
categories: ['tutorials', 'fundamentals']
description: Asymmetric (public-private-key encryption) is fundamental to the way our world operates and securing our communication, banking, email, etc. Let's learn more about it and how it differs from symmetric encryption. 
---

Cryptographic hashing is a fundamental concept that you should understand to work on blockchain, bitcoin, or any cryptocurrency. Hashing is a vast field of research and can . But, for the purposes of this tutorial, we will understand a few fundamentals that will help you get a grip on blockchain technology. Let’s get started!

### **Definition of Hashing**
Here’s a definition of hashing that I picked up from Wikipedia.

> Hashing means taking an input string of any length and giving out an output of a fixed length. This is the basic definition of hashing. Take some input data (of any length), process it, and produce an output which has a fixed, known number of characters.

### **Example of Hashing**
To fully understand the concept of hashing, let us look at two examples using the SHA-256 hashing scheme (the SHA-256 algorithm is a very popular hashing function which we will study later):

``` plaintext
input = blockchain  output = EF7797E13D3A75526946A3BCF00DAEC9FC9C9C4D51DDC7CC5DF888F74DD434D1
input = bitcoin     output = 6B88C087247AA2F07EE1C5956B8E1A9F4C7F892A70E324F1BB3D161E05CA107B
```
In the above example, we used an SHA-256 hash generator and gave it two input strings – “blockchain” and “bitcoin” and asked it to generate the SHA-256 output or hash (we generally refer to the output as the “hash” of the input). What you see above is the SHA-256 output containing 64 characters each and each character is made up of 4 bits (so that gives us 64×4 = 256 bits of information in the hash).

With this example, I hope you understand what a hashing function does. Now, let us take a look at the properties of a hashing function that make it interesting and usable for cryptocurrencies. In the next tutorial, we will see how to apply these properties to blockchains.

### **Fundamental properties of a hashing function**
So, let’s say you decide to create your own hashing function and you want everyone to use it. There are a few basic properties that your hashing function needs to satisfy in order for others to take it seriously. This is not an exhaustive list, but a few fundamental properties that should be satisfied. Let’s take a look!
- **Deterministic:** this means that if I use the hashing function on the same input  million of times, then the output will always be the same. The output should never vary and this is called deterministic.
- **Not invertible:** This is sometimes also called the “one-way requirement”. Simply put, if I cannot guess the input by looking at the output, then it is a non-invertible hash. In the worst case, it should require an impossible amount of computation to reverse-engineer or invert the hash. That is why it is also called the “one-way property”.
- **Fixed size / defined range:** It is desirable that the hash function creates a hash of a known, fixed, pre-determined length. For example, the popular SHA-256 hash produces a 256-bit long hash. Random numbered outputs require extra work for verification and might not make sense for cryptocurrencies.
- **Quick to compute:** this is an interesting property. To have a lot of people use your new hash function, it should be easy for them to compute. It should not need a powerful computer to compute, but, it should be incredibly difficult to reverse-engineer! Being easy to compute is why cryptographic hashes find uses in common uses cases like digitally signing documents (and doesn’t need any fancy hardware).
- **Small changes to the input make large changes to the hash:** What this means is that if I change one character in the input (maybe change an “x” to a “y”), then the output/hash should change drastically! Here is an example from SHA-256. You can see that by adding a single alphabet “x” to the input string “cryptochainery”, the hash completely changes. This is a very important property as it makes the hash incredibly hard to hack.
``` plaintext
input = cryptochainery     output = 0B8A51051650071F36D64ABC1DACB41FE52601B6E8B2C89BFBDCA129FA1650EF
input = cryptochaineryx    output = C8B79109CB23C3E218D8C37D0D787BD95362FA58DEBFE3145D4B469C3E00278F 
```
- **Uniformity:** A good hash function should map the expected inputs as evenly as possible over its output range. If this is not satisfied, then a hashing function might map all of its inputs to a particular range of possible hash values and this might lead to collisions. And, collisions (or two inputs giving the same output) is certainly something that we want to avoid.

### **A quick summary of hashing**
Okay! That was a lot of information – so let’s summarize it quickly before we forget:

> - the hashing function should produce an output/hash that has a fixed size.
> - you should not be able to guess the input by looking at the output (no recognizable patterns in the output hash).
> - two different input strings should not give the same output.
> - the hash should be extremely hard to reverse-engineer (computationally).
> - computing the hash should be computationally efficient.

Hope you understood how cryptographic hashing works. 

### Related Tutorials
1. [What is public/private key cryptography with an example.](https://mdcrypto512.github.io/tutorials/public-private-key-blockchain-bitcoin)
2. [How does a digital signature work?](https://mdcrypto512.github.io/tutorials/how-does-digital-signature-work)
