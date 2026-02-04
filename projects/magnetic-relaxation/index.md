---
title: "Magnetic Relaxation for MHD Equilibria"
permalink: /projects/magnetic-relaxation/
layout: single
author_profile: true
classes: wide
---

[📄 MRX on arXiv](https://arxiv.org/abs/2510.26986) | [📊 Poster](/assets/pdfs/MRX_APS_DPP_2025.pdf) | [💻 Code](https://github.com/ToBlick/MRX)

---

## Overview

In a fusion device operating near steady state, the plasma can be modeled as being in magnetohydrostatic (MHS) equilibrium. Finding such equilibria is crucial for designing and operating fusion devices. The equilibrium configuration determines properties such as stability and confinement, and reconstruction of equilibria from diagnostic measurements is essential for control.

![MHS Equilibrium](/assets/images/projects/mrx-teaser.png "Magnetic equilibrium with islands")

---

## The MHS Equations

In a domain $\Omega \subset \mathbb{R}^3$, the MHS equations are:

$$(\text{curl } B) \times B - \nabla p = 0 \quad \text{and} \quad \text{div } B = 0$$

together with appropriate boundary conditions. Here, $B$ is the magnetic field and $p$ the plasma pressure.

This is inherently a **three-dimensional problem**, which makes it computationally challenging.

---

## Breaking Nested Flux Surfaces

Standard methods (VMEC, DESC) simplify the search for equilibria to configurations with **nested flux surfaces**. However, relevant configurations in experiments feature magnetic islands and chaotic regions, violating this assumption.

**Magnetic relaxation** provides an opportunity to solve for very general equilibrium solutions. These methods rely on the observation that MHS states are stationary points of a constrained optimization process, in principle allowing for computation of very general equilibria.

---

## Key Features

- **Structure-preserving discretization**: Modern finite element methods using Finite Element Exterior Calculus preserve geometric properties at the discrete level
- **Spline basis functions**: Accurate representation of complex stellarator geometries with high-order convergence (common in isogeometric analysis)  
- **Automatic differentiation**: JAX-based implementation enables efficient gradient computation for PDE-constrained optimization
- **Accessible**: Simple installation via `pip install` — runs on laptops or GPU/TPU nodes

---

## Results

Our method can compute equilibria with:

- **Magnetic island chains** at resonant surfaces
- **Complex 3D stellarator geometries** (e.g., Heliotron with 19-fold symmetry)
- **Preservation of constraints**: Magnetic helicity and divergence-free condition maintained to desired precision

<!-- Add results images/videos when available -->
<!-- ![Results Gallery](/assets/images/projects/mrx-results.jpg "Stellarator equilibrium examples")-->

---

## Differentiation and Outer Loop Optimization

In the context of building a fusion power plant, the MHS equations are a constraint in the **design optimization** of the device. This constitutes a PDE-constrained optimization problem. 

By implementing our solver in JAX, we leverage automatic differentiation to compute gradients of functionals that depend on the MHS solution efficiently. This opens up possibilities for:

- Design optimization problems
- Real-time equilibrium reconstruction  
- Sensitivity analysis

---

## Paper

**MRX: A Differentiable 3D MHD Equilibrium Solver Without Nested Flux Surfaces**  
T. Blickhan, J. Stratton, [A. A. Kaptanoglu](https://wp.nyu.edu/courantinstituteofmathematicalsciences-alankaptanoglu/)  
*Submitted to Physical Review X*

[📄 Read on arXiv](https://arxiv.org/abs/2510.26986) | [📊 View Poster](/assets/pdfs/MRX_APS_DPP_2025.pdf)

---

## Acknowledgements

This work was supported by the Simons Collaboration on Hidden Symmetries and Fusion Energy.