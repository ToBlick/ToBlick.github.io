---
title: "Optimal Transport Methods for Model Reduction"
permalink: /projects/optimal-transport/
layout: single
author_profile: true
classes: wide
---

## Overview

Reduced basis methods struggle with **advection-dominated problems** where solutions exhibit moving features (shocks, fronts, traveling waves). Standard linear approximation methods fail to capture these dynamics efficiently because the solution manifold has high Kolmogorov n-width.

We propose registration methods based on **Optimal Transport** that align solution snapshots before building the reduced basis, dramatically improving approximation quality.

<!-- Add before/after comparison when available -->
![Registration Effect](/assets/images/projects/optimal-transport-registration.jpg "Before and after optimal transport registration")

---

## The Problem

In advection-dominated PDEs:

- Linear subspaces approximate poorly
- Many basis functions needed for accuracy  
- Standard POD/RB methods are inefficient

The key insight is that while solutions *look* different due to translation/deformation, they share underlying structure that can be revealed through proper alignment.

---

## Method: Linear Optimal Transport

Given a reference measure $\mu_0$ and a family of measures $\{\mu_\theta\}_\theta$, the LOT embedding maps each $\mu_\theta$ to the optimal transport map $T_\theta$ pushing $\mu_0$ to $\mu_\theta$.

This embedding:
- **Linearizes** the Wasserstein space locally
- Enables **PCA-like** dimensionality reduction  
- Preserves **transport structure**

![LOT Method](/assets/images/projects/lot-method.jpg "Linear Optimal Transport embedding visualization")

---

## Papers

### A Registration Method for Reduced Basis Problems Using Linear Optimal Transport

**T. Blickhan**  
*SIAM Journal on Scientific Computing, 2024*

[📄 Paper](https://doi.org/10.1137/23M1570715) | [📄 arXiv](https://arxiv.org/abs/2303.07328)

**Linear Optimal Transport (LOT)** provides: (1) A principled way to "align" solution snapshots, (2) Linearization of the Wasserstein metric, and (3) Efficient computation via reference measures. After alignment, solutions become amenable to standard linear reduction techniques.

### Wasserstein Model Reduction Approach for Parametrized Flow Problems in Porous Media

B. Battisti, **T. Blickhan**, G. Enchery, V. Ehrlacher, D. Lombardi, O. Mula  
*ESAIM: Proceedings and Surveys, 2023*

[📄 Paper](https://doi.org/10.1051/proc/202373028) | [📄 arXiv](https://arxiv.org/abs/2205.02721)

We develop Wasserstein barycenters and displacement interpolation for parametric flow problems, enabling efficient model reduction for porous media applications.

---

## Applications

The method achieves significant improvements for:

- **Vlasov-Poisson equations** in plasma physics
- **Transport problems** with moving features
- **Parametric PDEs** with advection  
- **Porous media flows**

<!-- Add results comparison when available -->
![Results Comparison](/assets/images/projects/optimal-transport-results.jpg "Approximation quality comparison")

---

## PhD Thesis

This work was part of my doctoral thesis:

**Reduced Basis Methods for Problems with Moving Features**  
Technische Universität München, 2024

The thesis explores various approaches to handle moving features in model reduction, including optimal transport methods and nonlinear approximation spaces.

---

## Demo Videos

<!-- Add demo videos when available -->
<video width="600" controls>
  <source src="/assets/videos/lot-demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*Demonstration of LOT registration applied to traveling wave solutions*