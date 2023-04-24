---
title: The Answer to (almost) Everything
date: 2018-02-01
description: "A well-defined, yet uncomputable number encodes the solutions of all finitely refutable mathematical conjectures (and it's not 42)."
math: true
tags:
   - extraordinaryphysics
---

Most of the famous unproved conjectures of mathematics, such as Goldbach’s conjecture, the extended Riemann hypothesis, and, until recently, Fermat’s theorem, are conjectures of the nonexistence of something, and would be refuted by a single counterexample. Riemann’s hypothesis, for example, would be refuted by finding a misplaced zero of the zeta function. Such conjectures are equivalent to the assertion that some program, which searches systematically for the allegedly nonexistent object, will never halt.

A possible approach to the quest for mathematical truths is thus to determine whether a given program with a given input will eventually halt. Simply running the program for some number of steps and checking if it halts is not enough however. If the program does not halt, it remains unknown whether the program will eventually halt or run forever.

Alan Turing actually proved that no algorithm exists that always correctly decides whether an arbitrary program halts when run with an arbitrary input. The essence of Turing’s proof is that any such algorithm can be made to contradict itself, and therefore cannot be correct. This result has profound implications on our understanding of logic and mathematics by showing that some mathematical questions are undecidable.
Even if we cannot determine whether a program will halt, what is the probability that a universal computer $U$ halts if its program is provided by a sequence of fair coin flips? The **halting probability** is the real number defined by
$$
\Omega = \sum_{U(p) < \infty} 2^{-l(p)}
$$
Here $l(p)$ is the length of program $p$ and the sum is taken over all inputs $p$ for which the reference machine $U$ halts (for technical reasons, we require $U$ to be a prefix-free Turing machine).
 
> *" $\Omega$ embodies an enormous amount of wisdom in a very small space… inasmuch as its first few thousands digits, which could be written on a small piece of paper, contain the answers to more mathematical questions than could be written down in the entire universe."* C. H. BENNETT
 
$\Omega$ is perfectly well defined and has a value between $0$ and $1$ (which depends on the choice of the Turing machine). This number turns out to possess remarkable properties:
- It cannot be computed by any finite computer program (in contrast to numbers such as $\pi$ or e).
- Its binary expansion is a random, incompressible sequence.
- It encodes the halting problem in a very compact form. Knowing, say, its first 10,000 bits enables us to solve the halting of all programs of fewer than 10,000 bits.

This last point covers programs looking for counterexamples to the Goldbach conjecture, the Riemann hypothesis, and most other conjectures in mathematics that can be refuted by single finite counterexamples.
Interesting conjectures of this sort are generally sufficiently simple to describe that they can be encoded in the halting of small programs, a few thousands or tens of thousands of bits long. Thus only the first few thousand digits of $\Omega$ would be needed in principle to solve these outstanding “finitely refutable” conjectures as well as any others of comparable simplicity that might be thought of in the future.
Moreover, for all axiomatic mathematical theories that can be expressed compactly enough to be conceivably interesting to human beings, say in fewer than 10,000 bits, the first 10,000 bits of $\Omega$ can be used to decide whether every statement in the theory is true, false, or independent.

Some well-known conjectures, e.g. that there are infinitely many twin primes, are not in principle decidable one way or the other by any finite amount of evidence. Such high-level conjectures involve multiple quantifiers such as "for infinitely many", while finitely refutable conjectures, i.e. those equivalent to the statement that that a certain program will not halt, involve only a single quantifier "for all".
Although higher level conjectures cannot be directly decided by $\Omega$, there is good reason to believe that many of them could be decided indirectly as logical consequences of stronger, finitely refutable conjectures.
 
{{< figure src="medallion.jpeg" caption="*The first 40 bits of Chaitin’s constant (for a certain prefix-free universal Turing machine) are engraved on the medallion presented to Gregory Chaitin for his 60th birthday by Stephen Wolfram.*" >}}

It is actually possible to determine the first couple of bits of the halting probability $\Omega$. This is because many short strings are either not syntactically correct programs for the given universal machine, or they halt quickly, or looping is easily detected. However, because of the undecidability of the halting problem such methods are not scalable and only finitely many digits of $\Omega$ can ever be computed.
It is worth noting that even if we get, by some kind of miracle, the first 10,000 digits of $\Omega$, the task of solving the problems whose answers are embodied in these bits is unrealistically difficult: The time it takes to find all halting programs of length less than n from the first n digits of $\Omega$ grows faster than any computable function.

In a sense, $\Omega$ is similar to an oracle that cannot be consulted, or whose prophecies are undecipherable. As C. H. Bennett aptly puts it: *“$\Omega$ is in many senses a cabalistic number. It can be known of, but not known, through human reason. To know it in detail, one would have to accept its uncomputable digit sequence on faith, like words of a sacred text.”*

Kurt Gödel demonstrated that mathematics is necessarily incomplete, containing true statements that cannot be formally proved (more details in a forthcoming post). $\Omega$ reveals even greater incompleteness by providing an infinite number of theorems that cannot be proved by any finite system of axioms.

**Further reading**
- C. H. Bennett and M. Gardner, “The random number omega bids fair to hold the mysteries of the universe“. Scientific American 241, 20 (1979).
- C. S. Calude, M. J. Dinneen, and C-K. Shu, “Computing a Glimpse of Randomness“. Experimental Mathematics 11, 361 (2002).
G. Chaitin, “Omega and why maths has no TOEs“.
