---
title: Analog is more powerful than Digital
date: 2018-02-01
description: "Computable physical equations can possess non-computable solutions."
math: true
tags:
   - extraordinaryphysics
---

An analog computer deals with continuous variables whereas a digital computer deals only with discrete variables like zeroes and ones. Marian Pour-El and Ian Richards, two mathematicians at the University of Minnesota, proved that analog computers are more powerful than digital computers.

Pour-El and Richards gave examples of numbers that are non-computable with digital computers but are computable with a simple kind of analog computer. Their analog computer is a classical field propagating though space and time and obeying a linear wave equation, such as the classical electromagnetic field obeying the Maxwell equations.  They showed that the field can be focused on a point in such a way that the strength of the field at that point is not computable by any digital computer, but it can be measured by an analog device[^1].

As an archetype of an analog system, El-Pour and Richards considered the three-dimensional wave equation
$$
\frac{ \partial^2 u}{\partial t^2} = \frac{ \partial^2 u}{\partial x^2} + \frac{ \partial^2 u}{\partial y^2} + \frac{ \partial^2 u}{\partial z^2}
$$
with the initial conditions $u(x, y, z, 0) = f(x, y, z)$ and $\partial u/ \partial t (x,y,z,0) = 0$.
The wave equation arises in various fields like acoustics, electromagnetism and fluid dynamics. Solutions of the wave equation travel with finite velocity (here made equal to one).

The question is now: can computable initial conditions f give rise to non-computable solutions? Remarkably the answer is “yes,” and two quite different types of non-computability can occur.

In the first case, the solution $u(x, y, z, t)$ takes a non-computable real value at a computable point in space-time. More precisely, “there exists a computable – and hence continuous function $f (x, y, z)$ such that $u(x, y, z, t)$ is continuous but not computable, and furthermore the value $u(0, 0, 0, 1)$ is a non-computable real number.”
 
In the second case, the solution maps each computable sequence of points in space-time into a computable sequence; nevertheless $u(x, y, z, t)$ is not a computable function. More precisely, “there exists a computable function $f (x, y, z)$ such that $u(x,y,z,t)$ is continuous and sequentially computable, but $u(x, y, z, 1)$ is not a computable function of $(x, y, z)$.”

These non-computable solutions of the wave equation are of the type commonly referred to as “weak solutions” – i.e., although continuous, they are not twice differentiable at all points. Weak solutions describe creases, cusps and other non-differentiable patterns that frequently appear in models of wave phenomena. The use of weak solutions is required as twice differentiable solutions are always computable.

> Physical theories – e.g., classical mechanics or quantum mechanics – cannot predict the existence of a physical constant that is not a computable real
 
A similar discussion can be given for other linear differential and integral equations that occur regularly in analysis and in physical theory. For example, there exists a computable – and hence continuous – function $F$ such that $dx/dt= F(x, t)$ has no computable solution in any rectangle however small within its domain. More generally, (non)-computability is tightly linked to the (non)-bounded nature of evolution operators.
 
These examples show that physical theories, which are often expressed in terms of differential equations, can lead to non-computable results. This suggests that physical theories – e.g., classical mechanics or quantum mechanics – cannot predict the existence of a physical constant that is not a computable real.

Another implication is that analog devices are - at least in principle - more powerful than digital ones. This conclusion is unexpected. In the development of our human technology during the last fifty years, analog devices such as vinyl records and film cameras appear to be primitive and feeble, while digital devices are overwhelmingly more convenient and powerful. In the modern information-based economy, digital wins every time. Assuming we can take advantage of the non-smoothness of the initial conditions, how can we unlock the full potential of analog devices?

The difference between analog and digital also ties back to a discussion by Freeman Dyson on the nature of life. Dyson argued that, under very general conditions, analog life has a better chance of surviving than digital life. Perhaps this implies that some very exotic forms of life like the Black Cloud, which use an analog form of information processing, will prevail when the time comes?
 
**Further reading**
- M. B. Pour-El and I. Richards, “A computable ordinary differential equation which possesses no computable solution“. Annals of Mathematical Logic 17, 61 (1979).
- M. B. Pour-El and I. Richards, “The wave equation with computable initial data such that its unique solution is not computable“. Advances in Mathematics 39, 215 (1981).
- M. B. Pour-El and I. Richards, “Computability in analysis and physics”. Springer Verlag (1989).
 

[^1]: What do we mean by computability? Roughly speaking, an object is computable if it can be constructed to within any desired precision by a finite, terminating algorithm. For example, a real number $x$ is computable if it is the effective limit of a computable sequence of rationals $r_n$, i.e. there is a recursive function $e(n)$ such that $k \geq e(n)$ implies $|x-rk | \leq 10^{-n} $. Thus the number $\pi$ is computable, since there exist finite recipes for computing it. When more precision is desired the computation may take longer, but the recipe itself does not change. Computable functions are defined similarly.
