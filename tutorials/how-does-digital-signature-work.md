---
layout: tutorial
title: How does a digital signature work?
categories: ['tutorials', 'fundamentals']
description: Let us take a look at how digital signatures work in this tutorial and how they are used in enuring the identity of the signer and that the data has not been altered/tampered.
---

You must  be familiar with a hand-written signatures that you might have used on contracts, wills, legal documents, etc. Each person creates a unique signature (his style!) which is then used as an unique identifier that proves that he has read and signed a document.

There are two big problems with handwritten signatures:-
- it can be forged (copied, duplicated)
- it is the same on every document - a will, or a bank slip, or a contract

### Digital Signature
> A digital signature on the other hand, 
- is hard to forge/replicate,
- is unique to an individual, 
- and the signature varies based on the content of the document being signed. 

Each of these proerties is important and let's study why. 

### Underlying technology of digital signatures
Digital signatures depend on two technologies (tutorial links below):
1. [cryptographic hashes](https://mdcrypto512.github.io/tutorials/what-is-cryptographic-hashing-blockchain-bitcoin)
2. [public/private key cryptography](https://mdcrypto512.github.io/tutorials/public-private-key-blockchain-bitcoin)
*(please visit the tutorials linked above to understand these concepts. It will make the rest of this tutorial simple to follow).*

### Steps to creating a digital signature (signing)
1. Given a message, create a cryptographic hash from it. [As we've already studied](https://mdcrypto512.github.io/tutorials/what-is-cryptographic-hashing-blockchain-bitcoin), the output hash/digest is of known size and even the smallest change to the message/document will change the hash drastically.
2. Encrypt the hash with the signer's private key. Note: This step is a little different compared to what we've studied in the past. We know that a public key is used for encrypting and the private key is used for decrypting. But in algorithms like [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)), the private key's mathematical properties allow it to be used for encrypting and the public key for decrypting. 
3. Combine the encrypted hash and the signer's public key and send it along with the message to the receiver.


### What happens at the receiver's end?
1. The receiver will decrypt the hash using the provided public key - the output of this step is the hash computed by the signer (hash of the original message). Let's call this **H1**.
2. He will recreate the hash using the received message (using the same hashing algorithm used by the signer). Let's call the resultant hash as **H2**.  
3. If **H1** = **H2**, then the original message is the same as the received message and it has not been tampered with. Else, the receiver knows that someone has modified the message.

### Advantages of using a digital signature
Coming back to the first point in this tutorial, we said that there are advantages to using digital signatures. Let's look at the reasons as well. 
- *it is hard to forge/replicate:* the signature can be forged only if the private key is lost/stolen and this is rare as the signer is expected to keep it very carefully. 
- *is unique to an individual:* the signature is created using a signer's private key which is known only to him. So this makes it unique to an individual. It also ensures that after the document has been signed using the private key, a person cannot deny that he signed it (unless his private key hsa been lost). This is called non-repudiation.
- *and the signature varies based on the content of the document being signed:* this is because the signature is created by encrypting the hash of the message. Everytime the message changes, so does the signature making it unique and hard to forge. 
- *cannot tamper with the public key as well:* if someone tampers with the public key which is transmitted from the signer's side, then the message cannot be decrypted which is an indication of an hacking attack. It is also extremely difficult to guess the the public key by just looking at the encrypted message. 

Hope this tutorial helped you understand digital signatures.

### Related Tutorials
1. [What is cryptographic hashing and what are it’s properties?](https://mdcrypto512.github.io/tutorials/what-is-cryptographic-hashing-blockchain-bitcoin)
2. [What is public/private key cryptography with an example.](https://mdcrypto512.github.io/tutorials/public-private-key-blockchain-bitcoin)
