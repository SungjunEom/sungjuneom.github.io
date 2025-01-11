---
layout: post
title: Measure theoretic description of change-of-variables
lead: 
use_math: true
---

# 1. Settings
Two measurable spaces:
$$(X,\mathcal{A},\mu)\quad\text{and}\quad (Y,\mathcal{B},\nu)$$
Consider a transform $\;T\;$ such that:
$$T:X\rightarrow Y$$
where $\;T\;$ is a measurable map. i.e., $T^{-1}(B)\in \mathcal{A}\quad \forall B\in\mathcal{B}$.

$T$ induces a pushforward measure $\nu_T$:

$$\nu_T(B)=\mu(T^{-1}(B))$$

# 2. Change-of-variables
$$\int_Y f(y) d\nu_T(y)=\int_X f(T(x))d\mu(x)$$

The Radon-Nikodym derivative $\frac{d\nu}{d\mu}$ is:

$$\frac{d\nu}{d\mu}(x)=|\det J_T(x)|$$

In case of linear mapping, the Jacobian $J_T(x)$ is:

$$T(x)=Kx \Rightarrow J_T(x)=\frac{\partial T}{\partial x}=K$$

Finally, the change-of-variables formula is induced as below:

$$\begin{aligned}\int_Yf(y)d\nu(y)&=\int_Xf(T(x))\frac{d\nu}{d\mu}d\mu(x)\\&=\int_Xf(T(x))|\det J_T(x)|d\mu(x)\end{aligned}$$

# 3. Examples
- Random variable $Z: \Omega \rightarrow \mathbb{R}$
- Inverse transform sampling
- Normalizing flows