---
layout: post
title: Measure theoretic description of KL divergence
lead: 
use_math: true
---
In this writing, I consider the KL divergence with measure theoretic approach.



Suppose $P$ and $Q$ are probability measures on a measurable space $(\Omega, \mathcal{F})$, and $P\ll Q$. That is, $P$ is absolutely continuous with respect to $Q$. (Or, equivalently, $Q$ dominates $P$)



KL divergence is defined as below:

$$\begin{aligned} \mathcal{D}_{KL}(P||Q)&:=E_P\left[\log \frac{dP}{dQ}\right] \\ &= \int_{\Omega}\log \frac{dP}{dQ} dP \end{aligned}$$

If we have density functions for $P$ and $Q$ with respect to Lebesgue measure:

$$\begin{aligned} \frac{dP}{d\lambda}&=f \\ \frac{dQ}{d\lambda} &=g \end{aligned}$$

then the KL divergence can be expressed in the familiar form.

$$\begin{aligned} \mathcal{D}_{KL}(P||Q) &= \int_{\Omega}\log \frac{dP}{dQ} dP \\ &= \int_{\Omega}\log \frac{\frac{dP}{d\lambda}}{\frac{dQ}{d\lambda}} \frac{dP}{d\lambda}d\lambda \\ &= \int_{\Omega} \left(\log \frac{f}{g}\right) f d\lambda \end{aligned} $$

Just to be clear, $dP=P(d\omega)$, $dQ=Q(d\omega)$, and $d\lambda=\lambda(d\omega)$.

Since the Lebesgue measure is defined over a real interval, for the last expression, $\Omega=\mathbb{R}\cap[\text{some interval}]$.