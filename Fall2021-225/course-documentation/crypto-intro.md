---
tags: mth225, crypto
---

# Very Short Introduction to Cryptography 




## What is cryptography?

**Cryptography** is the study of secure communications in the presence of an adversary. It involves taking information (an email for example, or your credit card number, or your Banner password) and sending it to a person or to a computer in such a way that only the people you intend to read it, can actually read it. Someone who has access to the message that you send should *not* be able to discern any information from the message unless you allow them to. 

Cryptography is a fundamental tool of life in a digitally connected world. We may not have deep secrets to hide, but we do have information that changes hands that we would not want to leak out to the general public --- your credit card number, your email password, and so on. We need to be able to communicate this information to another person in a digital format without some third person being able to read it. This is the problem that cryptography deals with. 

Although the technology behind cryptography [is getting very advanced very rapidly](https://quantumxc.com/quantum-cryptography-explained) these days, most cryptographic systems we use today boil down to applications of mathematical ideas that you're learning about right now. 

## The basic elements of cryptography

Cryptography begins with one person (or a computer) attempting to send information to another person (or a computer). We often refer to these people as **Alice** (the sender) and **Bob** (the recipient). Alice wants to send Bob some information over a channel that isn't necessarily secure, and she only wants Bob to be able to read it. 

The information or message Alice wants to send is called the **plaintext**. Before she sends the plaintext to Bob, Alice will **encrypt** the message so that it's unreadable to an outsider. The encryption process is done using some kind of mathematical process that turns the plaintext into an encrypted message that we call the **ciphertext**. 

There are countless ways to encrypt a given plaintext, but they all work the same: They take the plaintext and an additional piece of information called the **key**, and through mathematical processes, the key and the plaintext are combined to produce the ciphertext. That ciphertext is sent to Bob. 

Bob also has a key, and when he receives the ciphertext, he can **decrypt** the message using his key. Some cryptographic processes have Alice and Bob using the same key, while others have Alice using a different key than Bob. The first kind of systems are called **symmetric key systems** while the second kind are called **asymmetric**. When Bob receives the ciphertext and uses his key to decrypt, then if everything was done correctly he will have the exact same plaintext that Alice started with. 

We do *not* assume that the channel used to communicate the information is secure. That is, an eavesdropper --- who we often refer to as **Eve** --- can intercept or listen in on our communications at will. However, we want our encryption to be strong enough that even if Eve intercepts the message, then **without the key, no information can be obtained from the ciphertext**. This should be the case *even if Eve knows the method we used to encrypt the message*. That's known as **Kerckhoffs's principle**: A cryptographic system should remain secure even if every part of it --- except the key --- is public knowledge. 

This diagram shows the basic idea: 

![](https://i.imgur.com/w6cGsbo.png)

## Super simple example

Alice wants to tell Bob to meet her at Starbucks immediately. So she writes down the message, "MEET AT STARBUCKS NOW". She doesn't want any Eves out there to be able to know what she's telling Bob. So she chooses a small number, say the number 3, and **shifts each letter forward in the alphabet by that many places**. The number 3 is the *key*. The letter "M" shifts forward and becomes a "P"; the letter "E" becomes "H" and so on. The *ciphertext* is the result: 

>PHHW DW VWDUEXFNV QRZ

This is the message she sends to Bob, who is also using a key of 3. (How to communicate a shared key securely is a real issue. They may have some agreed-upon rule for what key to use; for now just assume Bob has the same key Alice has, and it hasn't been compromised.)

So Bob receives this ciphertext message. He knows that it was shifted by 3 units. So he shifts each letter of the ciphertext *backwards* three places, and ends up with 

>MEET AT STARBUCKS NOW

which is the original plaintext. 

Eve, on the other hand, intercepts the message `PHHW DW VWDUEXFNV QRZ` but it looks like random text. On the surface, this string of letters contains no information --- and that's the goal. 

However, this cryptographic system of shifting the characters of a message forward by a certain amount has a lot of security problems, and Eve won't have to work terribly hard to crack the code and find the message. If you assume that Eve knows that the ciphertext was obtained by shifting, but that Eve does not know the amount by which it was shifted, can you think of some ways Eve could still get information out of this message? If so, you've engaged in **cryptanalysis**, the science of breaking cryptographic systems. 


[![hackmd-github-sync-badge](https://hackmd.io/HIom2Po5RNiscLfUYC6qCw/badge)](https://hackmd.io/HIom2Po5RNiscLfUYC6qCw)