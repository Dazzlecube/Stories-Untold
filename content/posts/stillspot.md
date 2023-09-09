---
title: Finding the still spot
date: 2022-06-01
description: "Fixed-point theorems have implications in the most unexpected places, from meteorology to cutting sandwiches."
math: true
tags:
   - extraordinaryphysics
---

Did you know that no matter how you stir a cup of coffee, at least one coffee particle will have come back to its original position once the liquid has come to rest?

This is quite an unexpected result. After all, there is no physical law imposing “a minimal-number-of-coffee-particles-returning-to-their-positions”.

It turns out that fixed-point theorems do impose such strong restrictions. Fixed-point theorems are parts of topology, a branch of mathematics that study shapes and their properties that don’t change under continuous transformations (i.e., you can bend, shrink, stretch, or twist them, but gluing or punching holes is not allowed).

Fixed-points theorems have non-trivial implications in various situations. For example:
- At any moment in time and on every meridian, there are two opposite (‘antipodal’) locations where the temperature is the same;
- You can’t comb the hair on a coconut;
- You can, in one knife stroke, cut a sandwich so that the bread, the butter, and the ham are equally distributed;

The demonstrations of some of these results require advanced mathematics. However, simpler, more intuitive demonstrations can be given for the low dimension cases.

Consider a continuous transformation $T$ from the interval [-1,1] into itself. We have $-1 \leq T(x) \leq 1$, so that
 $
-1-T(-1) \leq 0, \ 1-T(1) \geq 0.
$
The function $f = x-T(x)$ is continuous, negative at $x=-1$ and positive at $x=1$. It must therefore vanish at least in one point $x_0$ in [-1,1], leading to
$
x_0 = T(x_0).
$
This shows the existence of at least one fixed point for any continuous application from [-1,1] into itself.

More generally, we have the **Brouwer fixed-point theorem**: *“Every continuous function from a convex compact subset K of a finite dimensional Euclidean space to K itself has a fixed point.“*

Brouwer theorem is the reason why at least one coffee particle must return to its original position, no matter how much you stir your coffee (as long as you don’t create holes).

Let’s now look at an application from the unit circle $S^1$ to $R$. It doesn’t make sense to talk about fixed points in this case (since $S^1 \neq R$), but we can prove an interesting property of $T$ regarding antipodal points. 

$T$ can be seen as a periodic function of period $2\pi: T(\theta) = T(\theta+2\pi)$. Noting that two antipodal points differ by $\pi$, we define the function
 $
f(\theta) = T(\theta+\pi) - T(\theta)
$
As $f(\pi) = T(2\pi)-T(\pi) = T(0)-T(\pi) = -f(0)$, there exists at least one $θ* \in [0, \pi]$ such that $f(θ_0)=0$, i.e.
 $
T(\theta_0 + \pi) = T(\theta_0).
$
This shows that at least two antipodal points will take the same value. 

More generally, we have the **Borsuk–Ulam theorem**: *“If $T: S^n → R^n$ is continuous then there exists an $x$ in $S^n$ such that $T(-x) = T(x)$.”*

By assimilating the Earth to a sphere, the Borsuk-Ulam theorem reveals that there are at least two antipodal points where atmospheric fields like temperature and pressure take the same values at any instant of time.

Another related theorem is the Poincarré-Brouwer theorem, also known as the **“hairy ball” theorem**: *“There is no non-vanishing continuous tangent vector field on even-dimensional n-spheres.“*

For the ordinary sphere, or 2‑sphere, there is at least one point x where a tangent vector field vanishes. In other words, whenever one attempts to comb a hairy ball flat, like a coconut or a tennis ball, there will always be at least one tuft of hair at one point on the ball. Another example would be the horizontal wind on Earth, which, according to the Poincarré-Brouwer theorem, must vanish in at least one point.

The next result has deep cooking implications. The **ham sandwich theorem** states that: *“For any compact sets $A_1, …, A_n$ in $R^n$ we can always find a hyperplane dividing each of them into two subsets of equal measure.“*

In other words, you can always cut a ham sandwich, in one knife stroke, so that the bread, butter, and ham are equally divided (n=3). Same goes for two pancakes (n=2).

The other claims found at the beginning of this post can be derived using these theorems or variants thereof. Other applications include control theory, game theory, economy, biology and population dynamics. We have only scratched the surface of the many deep and beautiful results in topology and their implications.
 
**Further reading**
- V. I. Istrăţescu, “Fixed point theory”. Reidel (1981).
- R. B. Kellogg, T. Y. Li, and J. A. Yorke, “A constructive proof of the Brouwer fixed point theorem and computational results“. SIAM J. Numer. Anal.13, 473 (1976).
