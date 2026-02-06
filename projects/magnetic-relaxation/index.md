---
title: "Magnetic Relaxation for MHD Equilibria"
permalink: /projects/magnetic-relaxation/
layout: single
author_profile: true
classes: wide
---

[📄 MRX on arXiv](https://arxiv.org/abs/2510.26986) | [📊 Poster](/assets/pdfs/MRX_APS_DPP_2025.pdf) | [💻 Code](https://github.com/ToBlick/MRX)

---

In a fusion device operating near steady state, the plasma can be modeled as being in magnetohydrostatic (MHS) equilibrium. Finding such equilibria is crucial for designing and operating fusion devices. The equilibrium configuration determines properties such as stability and confinement, and reconstruction of equilibria from diagnostic measurements is essential for control.

In a domain $\Omega \subset \mathbb{R}^3$, the MHS equations are:

$$(\text{curl } B) \times B - \nabla p = 0 \quad \text{and} \quad \text{div } B = 0$$

together with appropriate boundary conditions. Here, $B$ is the magnetic field and $p$ the plasma pressure. This is inherently a three-dimensional problem, which makes it computationally challenging.

Most established methods (VMEC, DESC) simplify the search for equilibria to configurations with nested flux surfaces. However, relevant configurations in experiments feature magnetic islands and chaotic regions, violating this assumption.

Magnetic relaxation provides an opportunity to solve for very general equilibrium solutions. These methods rely on the observation that MHS states are stationary points of a constrained optimization process.

The MRX [code](https://github.com/ToBlick/MRX) is easy to use -- just clone and `pip install` it!

<p style="text-align: center;">
  <img src="/assets/images/projects/mrx-teaser.gif" alt="Magnetic relaxation with islands" style="height: 200px;">
</p>

---

## Paper

**MRX: A Differentiable 3D MHD Equilibrium Solver Without Nested Flux Surfaces**  
T. Blickhan, J. Stratton, [A. A. Kaptanoglu](https://wp.nyu.edu/courantinstituteofmathematicalsciences-alankaptanoglu/)  

[📄 Read on arXiv](https://arxiv.org/abs/2510.26986) | [📊 View Poster](/assets/pdfs/MRX_APS_DPP_2025.pdf)

---

## Acknowledgements

This work was supported by the Simons Collaboration on Hidden Symmetries and Fusion Energy.