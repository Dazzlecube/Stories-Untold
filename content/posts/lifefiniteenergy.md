---
title: Life in an ever-cooling universe
date: 2018-01-01
description: "In an eternally expanding universe life might, at least in principle, endure forever."
math: true
tags:
   - extraordinaryphysics
---

Our universe could end in one of two ways. The observed expansion could either terminate and be followed by collapse and a Big Crunch (closed universe), or the expansion could continue forever (open universe). At present, the evidence strongly suggests the latter. Could life endure until the end of time?

In a closed universe, there is little hope for life to escape from frying. Gravity eventually stops the expansion of the Universe, after which the Universe starts to contract until all matter collapses to a final singularity.

The case of an open universe appears equally dismal. As the Universe expands indefinitely in space and time, temperature, as well the energy available for life, will be ever-decreasing. Yet, physicist Freeman Dyson proposes a scenario in which life could survive in an open universe.

In an open universe, any survival strategy of a society must comply with two requirements:
1. An infinite (possibly subjective) lifetime,
2. A total use of energy that is finite.

An acceptable strategy also requires that a society maintains its complexity over time.
To make the discussion quantitative, Dyson introduced a *'Biological Scaling Hypothesis'* that relates the speed of metabolism of a creature to its temperature[^1].
The first consequence of this scaling hypothesis is that the appropriate measure of time as experienced by a living creature is not the physical time $t$, but the 'subjective time'
$$
u(t)=f\int\limits_{0}^t \theta(t')dt'
$$
where $\theta(t)$ is the temperature of the creature and $f = (300 K s)^{-1}$ is a scale factor that is introduced to make $u$ dimensionless. The value of $f$ reflects that humans operate at approximately 300 K and that a 'moment of consciousness' lasts about 1 second.

A second consequence of the biological scaling hypothesis is that any structure is characterized by a quantity $Q$ that measures its rate of entropy production per unit of subjective time. For example, a human being dissipates about 200 W of power at a temperature of 300 K, so that $Q \sim 10^{23}$ bits. For the human species as a whole $Q ~ 10^{33}$ bits.
A creature or society with a given $Q$ and a given temperature will therefore dissipate energy at a rate 
$$
m=kfQ\ \theta^2,
$$
where $m$ is the metabolic rate and $k$ is Boltzmann's constant. Importantly, the dissipation rate varies with the square of the temperature, one factor $\theta$ coming from the relationship between energy and entropy, the other factor $\theta$ coming from the assumed temperature dependence of the rate of vital processes.

We now assume that life is free to change its temperature so as to maximize its chances of survival. There are two physical constraints on $\theta(t)$.
The first constraint is that $\theta(t)$ must be greater than the universal background radiation, which is the lowest temperature available as a heat sink. In a simple model of an open universe, this leads to $\theta (t) > a R^{-1}(t)$, where $a$ is a constant and $R(t)$ is the radius of the universe. As the radius of an open universe is constantly expanding, this bound becomes less and less constraining with time.

The second constraint is that the rate of energy dissipation must not exceed the power that can be radiated away into space. Assuming that the disposal of waste heat is by electromagnetic radiation, this constraint imposes a lower bound for the temperature,
$$
\theta>b \ (Q/N)
$$
where $b$ is a constant and $N$ the number of electrons available to the society. As the ratio $(Q/N)$ cannot be made arbitrarily small, this leads to a lower bound on the rate of energy dissipation of a society of a given complexity. Since the total energy available to a society is finite, its lifetime is also finite. The slowing down of metabolism with temperature is not enough to allow a society to survive indefinitely.

However, life has another strategy to escape from this impasse: hibernation.
Suppose a fraction $g(t)$ of society spends of its time in the active phase and a fraction $[1-g(t)]$ in hibernation. The constraint on radiated power becomes
$$
\theta(t)>g(t)b\ (Q/N)
$$
so that life can keep in step with this limit by lowering its duty cycle in proportion to its temperature.
A society can thus survive if it can find profiles $\theta(t)$ and $g(t)$ such that its total energy dissipated over all time, $\int\limits_{0}^\infty m(t)dt,$ is finite while its subjective time $u(t)$ grows indefinitely.

A possible strategy is to take
$$
g(t)=\theta(t)/\theta_0=(t/t_0)^{-\alpha},
$$
where $\theta_0$ and $t_0$ are the present temperature of life and the present age of the universe, respectively. If the exponent $\alpha$ lies in the range $1/3 < \alpha< 1/2$, the total energy dissipated will be finite, while the subjective time will be infinite. Life could thus endure indefinitely with finite resources.

>*"I have found a universe growing without limit in richness and complexity, a universe of life surviving forever and making itself known to its neighbors across unimaginable gulfs of space and time".* Freeman Dyson

Dyson's discussion entails a series of subtle implications. In particular, life eventually must take an analog form.
An example of an analog form of life is the Black Cloud described by Fred Hoyle in his eponymous science-fiction novel. The Black Cloud lives in the vacuum of space and is composed of dust-grains held together by electric and magnetic interactions. Instead of having a nervous or wiring system, it has a network of long-range electromagnetic signals that transmit information and coordinate its activities.

An analog form of life can better adapt to low temperatures. Any finite system, living or dead, will have only a finite set of accessible quantum states. Therefore, once the temperature goes below the lowest energy gap, a digital system of this kind would be permanently frozen in its ground states. It could no longer emit or absorb energy and would be incapable of processing any information. It would be, in essence, dead.

In contrast, an analog form of life like the Black Cloud would expand as the temperature goes down, increasing the number of quantum states accessible with the three halves power of the size of the cloud. In an analog system of this kind there is no ground state and no energy gap. The quantized-energy argument does not apply.

Whether life is mostly analog or digital is an important and fascinating question. This, and the fundamental differences between analog and digital capabilities, will be discussed in a forthcoming post.
 
**Further reading**:
- F. J. Dyson, "Time without end: Physics and biology in an open universe". Rev. Mod. Phys. 51, 447 (1979).
- M. J. Rees, "The collapse of the universe: An eschatological study". Observatory 89, 193 (1969).
- L. M. Krauss and G. D. Starkman, "Life, the Universe, and Nothing: Life and death in an ever-expanding Universe". The Astrophysical Journal, 531, 22, (2000).  

 
[^1]: Dyson's Biological Scaling Hypothesis reads: *"If we copy a living creature so that the Hamiltonian of the copy is $H' = λ U H U^{-1}$, where H is the Hamiltonian of the creature, U is a unitary operator, and λ is a positive scaling factor, and if the environment of the creature is similarly copied so that the temperatures of the environments of the creature and the copy are respectively T and λT, then the copy is alive, subjectively identical to the original creature, with all its vital functions reduced in speed by the same factor λ"*. The structure of Schrodinger's equation, with time and energy as conjugate variables, makes this scaling plausible.
