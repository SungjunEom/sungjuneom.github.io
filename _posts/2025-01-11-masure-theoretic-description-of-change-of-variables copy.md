---
layout: post
title: Measure theoretic description of change-of-variables
lead: 
use_math: true
---

# 1. Settings
Two measurable spaces:
$$(X,\mathcal{A},\mu)\quad\text{and}\quad (Y,\mathcal{B},\mu_T)$$
Consider a transform $\;T\;$ such that:
$$T:X\rightarrow Y$$
where $\;T\;$ is a measurable map. i.e., $T^{-1}(B)\in \mathcal{A}\quad \forall B\in\mathcal{B}$.

$T$ induces a pushforward measure $\mu_T$:

$$\mu_T(B)=\mu(T^{-1}(B))$$

# 2. Change-of-variables
Let $\nu$ and $\mu_T$ are measures defined on $Y$ and $\nu$ is dominated by $\mu_T$ ($\nu\ll\mu_T$). Then there exists a Radon-Nikodym derivative $\rho$ such that:

$$\forall B \in \mathcal{B},\quad \nu(B)=\int_B \rho(y)d\mu_T(y) $$

where $\rho:Y\rightarrow [0,\infty]$. (I missed this point before: the Radon-Nikodym assumes the measures are over the same measurable space.)

Let $f$ be a nonnegative measurable function on $Y$. Then,

$$\int_Y f(y)d\mu_T(y)=\int_Xf(T(x))d\mu(x)$$

$$\begin{aligned} \int_Y f(y)d\nu(y)&=\int_Y f(y)\frac{d\nu}{d\mu_T}d\mu_T(y)\\&=\int_Yf(y)\rho(y)d\mu_T(y)\\&=\int_X f(T(x))\rho(T(x))d\mu(x) \end{aligned}$$

# 3. Examples
- Random variable $Z: \Omega \rightarrow \mathbb{R}$
    - A random variable defines a pushforward measure $\mu_Z$ over the real number line. Assume that the pushforward measure $\mu_Z$ is dominated by Lebesgue measure$\lambda$ then $f=\frac{d\mu_Z}{d\lambda}$. The Radon-Nikodym theorem is applied between the measures $\mu_T, \lambda$ over the same measurable space $(\mathbb{R}, \mathcal{R})$
- Inverse transform sampling
- Normalizing flows