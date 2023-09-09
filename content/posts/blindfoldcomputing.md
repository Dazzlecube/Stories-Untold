---
title: Blindfold computing
date: 2022-09-01
description: "A new form of encryption allows you to compute with data you cannot read."
tags:
   - extraordinaryphysics
---

Encryption is used every day to transfer and store data securely. Encryption secures data by making them unreadable to those who don’t possess the decryption key. You cannot, however, search, sort, or make any useful operation on encrypted data. They have to be decrypted first, so that any data processing must therefore be done by you or someone you trust. Encryption thus works great for transferring and storing data securely, but cannot easily be generalized beyond that.

Now, imagine running your most computationally intensive programs on your large datasets on a cluster of remote computers (“in the Cloud”), while keeping both your programs, data, and results encrypted and confidential.

This sounds like magic. Yet, such magic trick is indeed possible thanks to homomorphic encryption. Homomorphic encryption was first proposed in the late 1970s, but for many years it was viewed as a fantasy that would never come true. That changed in 2009 with Craig Gentry’s breakthrough discovery of a fully homomorphic cryptosystem.

> "*Gentry’s work is clearly a landmark achievement. Before Gentry’s discovery many members of the cryptography research community thought fully homomorphic encryption was impossible to achieve."* 
> Daniele Micciancio, UCSD

Homomorphic encryption is a special kind of encryption that allows operating on encrypted texts without decrypting them.
 
To achieve this remarkable feat, an encryption scheme must satisfy two requirements. First, it must support arbitrarily complex computations on the encrypted data. In practice, supporting the addition and multiplication (or the *AND* and *XOR* operations) is enough if you can perform those operations an unlimited number of times. Second, the scheme must be secured, meaning that it must thoroughly randomize the bits of the encoded data.
 
These two requirements appear contradictory. Strong encryption implies a strong randomization of the bits whereas algorithms for arithmetic are extremely sensitive and give correct results only if all the bits are in the right places.
Gentry was experimenting with an encryption scheme that could support both addition and multiplication. However, it was limited to a few arithmetic operations before the data were corrupted due to the accumulation of small errors in the encrypted data.

Indeed, modern encryption schemes add a layer of security by randomly choosing among a multitude of possible encodings. This probabilistic step introduces small amounts of error at every arithmetic step. Performing just a dozen or so computations corrupts the data to the degree that it can no longer be accurately decrypted.
Gentry’s insight was to double-encrypt the data in such a way that the errors could be removed, so to speak, in the dark. By periodically unlocking the inner layer of encryption (using the encrypted version of the secret key!) underneath an outer layer of scrambling, the computer would correct errors as it went along, without ever seeing the secret data.

> In effect, homomorphic encryption allows someone to work on something he cannot look at, and without knowing anything about it.

Applications are multiple, especially with regards to privacy. For instance, you could encrypt your queries before sending them to your favorite search engine, and receive the encryption of the result without the search engine even knowing what the query was.

A medical institute could encrypt its entire database of patient records and upload it to a cloud. Then it could use the cloud-stored data as desired – for example, to detect patterns of health hazards or conduct large scale genetic analyses. The results would be downloaded and decrypted without ever exposing the details of a single medical record.

Another idea is to build a cryptographic privacy fence between online advertisers and consumers. A service based on homomorphic encryption could match ads to targeted consumers while ensuring that advertisers learn nothing about the people selected.

Program obfuscation, i.e. disguising the operational details of a computer program so that it can’t be reverse-engineered, is another possible application. Program obfuscation is used when there is a strong proprietary interest not only in the data but also in the program itself – like Wall Street’s trading and investment algorithms. With homomorphic encryption, both data and the algorithm could be cryptographically secured.

Homomorphic encryption is, however, not quite ready for everyday use. The methods have been shown to work in principle, but they're still very inefficiency. On the other hand, in the six years since its invention, people have been shaving off many orders of magnitude in performance improvements.

In short, homomorphic encryption promises to make cloud computing perfectly secure. While still too computationally intensive to be practical, it offers a very general paradigm. And like many landmark achievements, it will certainly open the door to many unforeseen possibilities.
 
**Further reading**
- D. Micciancio, “A First Glimpse of Cryptography’s Holy Grail“. Communications of the ACM 53, 96 (2010).
- C. Gentry, “Computing Arbitrary Functions of Encrypted Data“. Communications of the ACM 53, 97 (2010).
- B. Hayes, “Alice and Bob in Cipherspace“, American Scientist 100, 362 (2012).


