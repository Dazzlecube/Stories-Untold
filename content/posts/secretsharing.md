---
title: How to share a secret
date: 2022-05-01
description: "A secret S can be divided into n pieces in such a way that even complete knowledge of n – 1 pieces reveals no information about S."
math: true
tags:
   - extraordinaryphysics
---

Suppose you need to share nuclear activation codes. For obvious reasons, no single individual should be able to activate the nuclear protocol on his own. Only when a majority of the operators combine their code parts can a nuclear weapon be launched.

This situation is an example of secret sharing, where a secret is divided into parts and each participant is given a unique part.  Some or all of the parts are then necessary to reconstruct the secret.

Simply dividing a secret and distributing the parts is not secure enough. Consider for example the scheme in which the 4-digit code “1234” is divided into the parts “1”, “2”, “3” and “4”. An attacker would have to guess the password from 104 = 10000 possible combinations. A person with one share, however, would have to guess only three digits, from 103 = 1000 combinations, and so on as more persons collude.
 
A **secure secret sharing scheme** divides a secret *S* into *n* pieces of data in such a way that:
1. Knowledge of *any k* or more pieces makes *S* easily computable.
2. Knowledge of *any k-1* or fewer pieces leaves *S* completely undetermined (in the sense that all its possible values are equally likely). 
 
This scheme is called a *(k, n)* threshold scheme. 
If *k = n* then all participants are required to reconstruct the secret.
 
**Shamir’s secret sharing** algorithm provides an elegant solution. The essential idea of Shamir’s scheme is that it takes *k* points to define a polynomial of degree *k-1*. For instance, an infinite number of polynomials of degree 2 can be drawn through 1 or 2 points, whereas 3 points define a unique polynomial of degree 2.


Suppose we want to use a *(k, n)* threshold scheme. We can encode a secret and shares in the values of a random polynomial in a finite field $F$ of size $P>S$. Working with a *finite* field allows generating elements with a uniform probability distribution for perfect security. 
 
To encode the secret, we choose $k-1$ positive integers $a_i$ at random in $F$. We then construct the polynomial
$$
q(x) = S + a_1 x + a_2 x^2 + … + a_{k-1} x^{k-1},
$$
which encodes the secret in the constant term $q(0) = S$.
 
To divide the secret into pieces $S_i$, we evaluate this polynomial at n points $x_i$ to retrieve $n$ pieces  $S_i = q(x_i)$. Every participant is then given a pair $(x_i, S_i)$, i.e. an integer input to the polynomial and the corresponding integer output.

Given any subset of $k$ of these pairs, we can find the coefficients of the polynomial using interpolation. In fact, the polynomial can be immediately written down in terms of [Lagrange polynomials](https://mathworld.wolfram.com/LagrangeInterpolatingPolynomial.html). The secret can then be recovered by retrieving the constant term $q(0) = S$.
 
Now let's see what happens when $k-1$ of the $n$ pieces are revealed to an opponent. For each candidate value $S’$ they can construct only one polynomial $q'(x)$ of degree $k- 1$ such that $q'(0) = S'$ and $q'(x_i) = S_i$ for the $k- 1$ given arguments. 

By construction, these $P$ possible polynomials are equally likely, and thus there is absolutely nothing the opponent can deduce about the real value of $S$.
  
Shamir’s threshold scheme possesses several useful properties, including being:
1. **Secure**: Less than the requisite number of shares of the secret provides no information about the secret.

2. **Minimal**: The size of each piece does not exceed the size of the original data.

3. **Flexible**: We can supply participants a different number of pieces according to their needs (for instance, a president can unlock the safe alone, whereas three secretaries are required together to unlock it).
 
Note that a minimal scheme is still somewhat space inefficient: Each share of the secret is as large as the secret itself. Storing and transmitting the shares requires an amount of storage and bandwidth resources equivalent to the size of the secret times the number of shares. More space efficient schemes based on data partitioning have been devised.

Threshold schemes are ideally suited to applications in which a group of mutually suspicious individuals with conflicting interests must cooperate. The fact that the secret sharing problem can be solved in an optimal and elegant way is one of the key achievements in the field of cryptography.
