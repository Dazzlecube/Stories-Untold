---
title: The Banach-Tarski paradox of infinite cookies
date: 2018-03-01
description: "One of the strangest results in mathematics suggests you can create something out of nothing."
tags:
   - extraordinaryphysics
---

It is common sense that if you cut an object into pieces, the recomposed object will be the same volume as the original object, no matter how you rearrange the pieces. Yet, the following theorem reveals that this is not necessarily the case:

**Banach-Tarski Theorem**: *A solid ball may be separated into a finite number of pieces and reassembled in such a way so as to create two solid balls, each identical in shape and volume to the original.* 

That is, you can take a cookie, cut it in pieces, and reassemble those pieces to create two cookies identical in shape and volume to the original. Repeat the process and you have created a factory capable of producing an infinite amount of cookies from a finite amount of matter.
In a variant of the theorem, you can take a small sphere, for example of the size of a pea, and transform it into a far bigger sphere, for example of the size of the Sun:

**Banach-Tarski Theorem (second form)**: *A solid ball can be cut into as few as five pieces which can then be reassembled so as to make a ball of arbitrary size.*

This theorem is not a trick or an optical illusion, contrary to some puzzles. Only cutting, rotations, and translations are used in the demonstration, with no hidden stretching or gaps. So what can lead to such a counter-intuitive result?

{{< youtube liI7rm5o1Rc >}}

<br>
  
   
The theorem uses a key ingredient, the so-called "**Axiom of Choice**". Informally put, the Axiom of Choice says that given any collection of bins, each containing at least one object, it is possible to make a selection of exactly one object from each bin.

This is an intuitive and reasonable statement in many cases, in particular if the number of bins is finite. For an infinite collection of bins, however, such a selection can be obtained only by invoking the Axiom of Choice (assuming the objects to have no distinguishing features).
With the Axiom of Choice, it becomes possible to construct and manipulate *non-measurable sets*. A non-measurable set is a set which cannot be assigned a meaningful "size".

A first indication that there might be a problem in defining length for an arbitrary set came from the **Vitali theorem**, which also uses the Axiom of Choice. Vitali showed that a subset of [0,1] can be partitioned in such a way that the pieces can be translated so that their union is the entire real number line - without any stretching involved. This set is thus not measurable[^1].
 
A similar set is required in the Banach-Tarski construction, where at least one of the pieces must be a non-measurable set. The Banach–Tarski paradox thus shows that there is no way to define volume in three dimensions unless one of the following four concessions is made:
1. The volume of a set might change when it is rotated.
2. The volume of the union of two disjoint sets might be different from the sum of their volumes.
3. Some sets might be tagged "non-measurable", and one needs to check whether a set is "measurable" before talking about its volume.
4. The standard axioms of set theory might have to be altered.

Standard measure theory takes the third option, while the fourth option is still being debated. In particular, some view the Banach-Tarski paradox as evidence that the Axiom of Choice is false, despite being logically consistent[^2].

Similar paradoxes and mind-bending results have been derived over the years and challenge our intuition on sets and their volumes.
A first example is the existence of one-to-one correspondences between sets of different dimensions. Cantor obtained a bijection between the unit segment [0,1] and the unit square [0,1]x[0,1], but also with the unit "cube" of arbitrary dimension. Peano, Hilbert and others then constructed bijections that are in addition continuous, i.e. true **space-filling curves** (Figure 1). These results show that dimension has nothing to do with the cardinality of a continuous point set.

{{< figure src="hilbert1.png" caption="*Figure 1: The first six iterations of the Hilbert curve. [Image credit](https://discspace.org/hilbert-curves-are-cool/)*" >}}

Another example is the so-called "Cantor set". Starting from a unit line segment, the Cantor ternary set is created by iteratively deleting the open middle third from a set of line segments (Figure 3). What will remain after an infinite number of steps?

At each iteration, a third of the set is removed, so that whatever remains at the end will be "small". Supporting this is the fact that the total length of the removed interval is one, the length of the original segment (as can be verified by summing the corresponding series).
At this stage, we might suspect that the Cantor set will consist in a countable number of points of which the total measure is zero. But the truth is that once we remove all of the intervals, what remains is an uncountable set of points, no less that the number of points with which we started! That is, the Cantor set, of measure zero, can be put in one-to-one correspondence with the points of the original and complete unit line segment.

{{< figure src="cantor_set.png" caption="*Figure 2: The first seven iterations of the Cantor set's construction are illustrated.*" >}}


> *"Je le vois mais je ne le crois pas! (I can see it but I don't believe it)"* George Cantor, upon discovering the one-to-one correspondence between sets of different dimensions

So, can we use these results in practice? Unfortunately, building an infinite number of cookies (or an infinite amount of gold for that matter) out of thin air is not within our foreseeable reach unless we acquire the ability to manipulate non-measurable sets composed of an infinity of disjoint elements.

That said, non-Euclidean geometries can sustain such paradoxes with lighter logical requirements. Specifically, a type of Banach-Tarski paradox can be derived in the hyperbolic plane without using the Axiom of Choice. In this version of the paradox, the hyperbolic plane can be decomposed into three simple sets such that each is a third of the space, but also each is a half of the space.

Some researchers have suggested that the Banach-Tarski mechanism of magnification without stretching could be at the basis of some physical phenomena. For example, the creation of particles from the void by quantum fluctuations could also be the result of such a Banach-Tarski mechanism. 
In any case, the Banach-Tarski paradox provides a forceful illustration of the sometimes highly counter-intuitive nature of sets, and as such, it has greatly strengthened our understanding of mathematics.

**Further reading**
- S. Banach and A Tarski, "Sur la décomposition des ensembles de points en parties respectivement congruentes". Fundamenta Mathematicae 6, 244 (1924).
- Leonard M. Wapner, "The Pea and the Sun: A mathematical paradox", A K Peters/CRC Press (2007).
- Grzegorz Tomkowicz and Stan Wagon, "The Banach–Tarski Paradox", Cambridge University Press (2016).
 

[^1]: To construct the Vitali set, we partition [0,1] into equivalence classes. 
We say that two numbers a and b are equivalent if a-b is a rational number. Consequently, all rational numbers in [0,1] are equivalent and the interval [0,1] consists of uncountably many classes, each consisting of a countable number of members. 
Using the Axiom of Choice, the Vitali set is then a subset of [0,1] formed by selecting one and only one number from each equivalence class.
 
[^2]: The Zermelo–Fraenkel set theory is one of several axiomatic systems that were proposed in the early twentieth century to formulate a theory of sets free of paradoxes. The Zermelo–Fraenkel set theory, combined with the Axiom of Choice, is the standard form of axiomatic set theory and as such is the most common foundation of mathematics. 
Kurt Gödel showed that the ZFC axiomatic system is logically consistent. Assuming ZF is consistent, Paul Cohen then showed that the Axiom of Choice is not a theorem of ZF. Together these results establish that the Axiom of Choice is logically independent of ZF.
