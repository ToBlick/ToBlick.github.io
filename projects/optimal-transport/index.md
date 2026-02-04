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


Given a reference measure $\mu_0$ and a family of measures $\{\mu_\theta\}_\theta$, the Monge embedding maps each $\mu_\theta$ to the optimal transport map $T_\theta$ pushing $\mu_0$ to $\mu_\theta$.

This embedding:
- **Linearizes** the Wasserstein space locally
- Enables **PCA-like** dimensionality reduction  
- Preserves **transport structure**

![Monge Embedding Method](/assets/images/projects/ot-tangentspace.png "Linear Optimal Transport embedding visualization")

---

## Papers

### A Registration Method for Reduced Basis Problems Using Linear Optimal Transport

**T. Blickhan**  
*SIAM Journal on Scientific Computing, 2024*

[📄 Paper](https://doi.org/10.1137/23M1570715) | [📄 arXiv](https://arxiv.org/abs/2303.07328)

We provide a principled way to "align" solution snapshots, making them amenable to standard linear reduction techniques.

### Wasserstein Model Reduction Approach for Parametrized Flow Problems in Porous Media

B. Battisti, **T. Blickhan**, G. Enchery, V. Ehrlacher, D. Lombardi, O. Mula  
*ESAIM: Proceedings and Surveys, 2023*

[📄 Paper](https://doi.org/10.1051/proc/202373028) | [📄 arXiv](https://arxiv.org/abs/2205.02721)

We develop Wasserstein barycenters and displacement interpolation for parametric flow problems.