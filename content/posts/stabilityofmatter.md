---
title: The Stability of Matter
date: 2017-10-01
description: "Pauli Exclusion Principle prevents matter from collapsing - and exploding."
math: true
tags:
   - extraordinaryphysics
---

The term ‘stability of matter’ summarizes the simple observation that all material objects occupy a volume proportional to the mass of the object. While obvious at first glance, this observation is actually nontrivial. Classical mechanics is unable to explain this elementary fact.

To get a better sense of the problem, bear in mind that matter is mostly empty space. And yet, if we pour two separate liters of water together we still have two liters rather than, say, one liter of "compact" water that is twice as dense. It is not obvious why, since twice as many molecules now interact with each other. 
So how do all these molecules conspire to give matter its bulkiness?

Molecules, as well their constitutive electrons and nuclei, interact with each other via electrostatic forces. The electrostatic energy is not just additive; it grows with the square of the numbers of particles.

Assume for now that the energy content of matter consisting of N particles follows its electrostatic energy and is proportional to $N^2$. The pouring of water would then have dramatic consequences. The energy difference before and after the pouring is proportional to $(2N)^2−2N^2=2N^2$. Since $N \sim 10^{26}$ for a liter of water, the energy liberated is comparable to the energy released in a big explosion. Such "matter" would be very unpleasant stuff to have lying around.

The only way to avoid such a catastrophe is if the energy of bulk matter is proportional to the total number of particles. Thus, there must be a mechanism that somehow beats the quadratic dependence on the number of particles of the Coulomb energy. Quantum mechanics and the Pauli Exclusion Principle are the missing ingredients to explain the observed stability of matter.

The Pauli Exclusion Principle states that two identical fermions (particles with half-integer spin such as electrons) cannot occupy the same quantum state.
Bosons (integer spin particles such as protons), on the other hand, are not subject to the Pauli Exclusion Principle. Any number of identical bosons can occupy the same quantum state. 
 
Every elementary particle is either a boson or a fermion. Pauli’s Exclusion Principle (and, more generally, the spin-statistics theorem) follows from the combination of special relativity with quantum mechanics.

Consider a system of $N$ electrons interacting with $K$ nuclei with charges $\underline{Z}=(Z_1, \cdots, Z_K)$. 
The *absolute ground state energy* $E_0(N,K,\underline{Z})$ represents the lowest possible energy configuration of the system, and is obtained by minimizing the Hamiltonian over all normalized wave functions and nuclei locations. 
That is, it is the ground state energy when the nuclei are placed in the most favorable locations.

A first fundamental result is that the absolute ground state energy $E_0(N,K,\underline{Z})$ is finite for every $N, K$, and $Z$. The finiteness of the ground state energy (**'stability of the first kind'**) accounts for the stability and spatial extension of matter.
 
This first form of stability comes from the uncertainty principle in quantum mechanics, which implies that localizing an electron costs kinetic energy. Effectively electrons behave like a rubber ball, or a fluid, which limits the compression caused by the attractive electrostatic forces. This is why matter is extended in space and does not collapse despite the attractive interaction between electrons and nuclei.

We now turn to the dependence of the energy on the number of particles. 
For simplicity, we assume that all the Z's have the same value and that $N = K Z$, i.e., that the system is electrically neutral. 
Minimizing over all possible wave functions, the absolute ground state energy is reached for a symmetric wave function, i.e. for bosons. We obtain the bound
$$
E_0(N, K=N/Z, Z)\le-A(Z) N^{5/3}
$$
with some constant $A(Z)$. 
As discussed earlier, such a non-linear scaling with $N$ implies that bosonic matter is unstable.

Since we are dealing with electrons, imposing the Pauli Exclusion Principle raises the energy by restricting the range of admissible wave functions. 
Remarkably, this raises it just enough so that matter is stable. 
More precisely, there exists a constant $B(Z)$ such that
$$
E_0(N, K=N/Z, Z)\le-B(Z) N.
$$
This linear law ('**stability of the second kind**') is not just a lower bound. It is, indeed, the correct asymptotic law: There is a number C(Z) such that
$$
\lim\limits_{N\rightarrow\infty}\frac{1}{N} E_0(N,K=N/Z,Z)=-C(Z).
$$
This theorem demonstrates the existence of the thermodynamic limit and is part of the foundation of thermodynamics. If this limit did not exist, matter would not behave the way we expect it to behave - even if stability of the second kind is assumed to hold.

> Without Pauli's Exclusion Principle, matter would collapse into a dense state, creating a situation in which the assembly of any two macroscopic objects would release energy comparable to that of an atomic bomb.

Summarizing, bulk matter is stable, and has a volume proportional to the number of particles, because of the Pauli Exclusion Principle. The total energy of a system of $N$ particles has a negative lower bound proportional to $N^{5/3}$ when no assumption is made on the statistics of the particles. When all particles belong to a fixed number of fermion species, a lower bound exists proportional to $N$.

These results hold for 'ordinary' matter. The Pauli Principle still leads to stability even in more extreme conditions. In white dwarfs and neutron stars for example, the constituents are supported by 'degeneracy pressure' alone despite the large gravitational forces and intense magnetic fields. However, even this internal pressure can be overcome by large enough gravitational fields, leading to the formation of a black hole.
 
**Further reading**
- E. H. Lieb, "The stability of matter: From atoms to stars". Bull. Amer. Math. Soc. 22, 1 (1990).
- F. J. Dyson and A. Lenard, "Stability of Matter. I". J. Math. Phys. 8, 423 (1967).
- E. H. Lieb and J. L. Lebowitz, "The constitution of matter: existence of thermodynamics for systems composed of electrons and nuclei". Adv. in Math. 9, 316 (1972).
