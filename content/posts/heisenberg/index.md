---
title: Uncertainty Principle in Classical Mechanics
date: 2017-10-01
description: "Classical mechanics satisfies an uncertainty principle reminiscent of the quantum Heisenberg uncertainty principle."
math: true
tags:
   - extraordinaryphysics
---

The Heisenberg uncertainty principle for the position and momenta of quantum particles asserts that
$$
\Delta x_i\Delta p_j\ge \frac{\hbar}{2} \delta_{ij}.
$$
These inequalities show that it is impossible to measure both the momentum and position of a quantum particle accurately.

Contrary to what is often believed, the Heisenberg inequalities are not statements about the accuracy of our measurements - their derivation actually assumes perfect instruments. These inequalities arise because individual particles are considered parts of a probability wave, in which many possible combinations of position and momentum exist simultaneously.

In contrast, both the positions and momenta of classical particles can be measured accurately and independently. 
In classical mechanics, given the positions and momenta of particles at one instant of time, the entire past and future of the system can, in principle, be determined.

Nonetheless, relations similar to the Heisenberg inequalities can be derived using only classical arguments!
 
{{< figure src="location_sharing.png" caption="*Location sharing* (Figure credit: XKCD 1473)" >}}

Consider a volume element in the phase space of a Hamiltonian system. As time evolves, it will distort and may take a very different shape. The fact that a Hamiltonian vector field is divergence free implies that its volume will remain constant (Liouville’s theorem). 

In addition of being volume-preserving, Hamiltonian flows have an unexpected additional property constraining the shape of phase space volumes. This property is a consequence of the symplectic **no-squeezing theorem**, also known as the symplectic camel, which was proven in 1985 by Mikhail Gromov[^1].

Gromov's no-squeezing theorem can be stated simply as follows. Make a circular "hole" with radius $r$ in any of the conjugate coordinate planes $(x_i, p_i)$ and choose a phase space ball with radius $R > r$. While it is to easy to find volume-preserving transformations that will move the ball from one side of the plane to the other, it is impossible to do it using canonical transformations (and, in particular, Hamiltonian flows). Notably, the no-squeezing theorem applies to conjugate coordinates only, i.e. there is no such constraint on coordinates $(x_i, p_j)$ with $i \neq j$.

Thus, the no-squeezing theorem tells us that, although symplectic transformations are volume-preserving, it is much more restrictive for a transformation to be symplectic than it is to be volume-preserving.

> *"This is a very powerful result, which is intimately tied to the Hamiltonian nature of the system, and is a completely different result than Liouville's theorem, which only interests the overall volume and does not pose any restriction on the shape.*" Andrea Censi

To derive the classical uncertainty relations, we consider an ensemble of joint position-momentum measurements. Due to measurement errors, these measurements will form a cloud of points in phase space.

To characterize the uncertainty in the state of the system we introduce the smallest ellipsoid $\Omega$ circumscribing this cloud of points (also called the John–Löwner ellipsoid). $\Omega$ provides a robust estimator of the variances and co-variances of the various positions and momenta.

We define the symplectic capacity $c(\Omega)$ as $\pi R^2$, where $R$ is the radius of the largest ball that can be sent inside $\Omega$ using canonical transformations. Then, the projections of that deformed ball on any plane of conjugate coordinates $(x_i,p_i)$ will never decrease below their original values. 
That is, if $h$ is a number such that $c(\Omega) \gt h/2$, we have 
$$
\Delta x_i(t)\Delta p_i(t)\ge \frac{h}{2}
$$
at all times $t$.

A stronger form of the uncertainty relations, the Robertson-Schrödinger inequalities, can even be derived. 
The Robertson-Schrödinger inequalities account for the co-variances between conjugate variables:
$$
(\Delta x_i)^2(\Delta p_i)^2\ge \textrm{Cov}^2(x_i,p_i)+\frac{h^2}{4}.
$$
The same relations hold in quantum mechanics, with $h$ taking the value $\hbar$.

This result changes our conception of Hamiltonian phase space mixing. According to conventional wisdom, a phase space volume can be stretched in all directions by Hamiltonian flows, and eventually get very thinly spread out over huge regions of phase space. Thus, after some (perhaps very long) time, the projections on any plane could a priori become arbitrary small. Gromov’s no-squeezing theorem reveals that Hamiltonian mechanics forbids this kind of chaotic spreading of phase space volumes.

Classical and quantum mechanics are thus formally much closer than they might appear at first sight. It is as if quantum mechanics has left a footprint in classical mechanics, here in the form of classical uncertainty relations. 
This begs the question: What other quantum effects are, unbeknownst to us, shaping classical dynamics?
 
**Further reading**:
- H. P. Robertson, "The uncertainty principle". Phys. Rev. 34, 163 (1929).
- M. de Gosson, "The Symplectic Camel and the Uncertainty Principle: The Tip of an Iceberg?" Found. Phys. 99, 194 (2009).
- I. Stewart, "The symplectic camel". Nature 329, 17 (1987).

[^1]: Why the "symplectic camel"? The expression comes from the following biblical parable: 
*"It is easier for a camel to go through the eye of a needle, than for a rich man to enter into the kingdom of God."* (Mark 10:25). In this context, the Biblical camel corresponds to the phase space ball and the eye of the needle to the hole in the $(x_i,p_i)$ plane. For this reason it is common to call Gromov’s theorem the principle of the symplectic camel.

