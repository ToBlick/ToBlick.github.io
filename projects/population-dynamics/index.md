---
title: "Population Dynamics Inference"
permalink: /projects/population-dynamics/
layout: single
author_profile: true
classes: wide
---

# Population Dynamics Inference for Stochastic Systems

**Authors:** [Tobias Blickhan](https://toblick.github.io), Jules Berman, [Andrew Stuart](https://www.cms.caltech.edu/people/astuart), [Benjamin Peherstorfer](https://cims.nyu.edu/~pehersto/)  
**Affiliations:** New York University, Caltech

---

## Overview

Stochastic dynamical systems present notorious challenges for model order reduction. We propose a change of perspective: instead of inferring governing dynamics of a single system $X_t$, we consider the evolution of a **population** of such systems—the distribution of states over many realizations:

$$X_t \sim \rho_t$$

This distribution evolves according to a deterministic equation:

$$\partial_t \rho(t) = \text{div}(\rho_t u_t)$$

The task is to infer the velocity field $u_t$ that governs this evolution.

<!-- Add conceptual diagram when available -->
![Population Evolution](/assets/images/projects/population-dynamics-concept.jpg "From individual trajectories to population evolution")

---

## Key Insight: Gauge Freedom

Different trajectory dynamics can give rise to the same population dynamics. This means there are infinitely many velocity fields $u_t$ that are *compatible* with observed data.

We exploit this gauge freedom to find velocity fields that **minimize kinetic energy**, leading to a well-posed problem with deep connections to optimal transport theory.

---

## Papers

### DICE: Discrete Inverse Continuity Equation for Learning Population Dynamics

**T. Blickhan**, J. Berman, A. Stuart, B. Peherstorfer  
*Submitted to Journal of Machine Learning Research*

[📄 arXiv](https://arxiv.org/abs/2507.05107)

Previous approaches (e.g., Action Matching) have proven numerically unstable. We identify the root cause: naive formulations rely on analytical properties that do not hold at the discrete level. **DICE** provides solutions to drastically improve training stability through careful structure preservation during discretization.

### Parametric Model Reduction of Mean-Field and Stochastic Systems via Higher-Order Action Matching

**T. Blickhan**, J. Berman, B. Peherstorfer  
*NeurIPS 2024*

[📄 Paper](https://papers.nips.cc/paper_files/paper/2024/file/6782c18960808848174cfe60742b415a-Paper-Conference.pdf) | [📄 arXiv](https://arxiv.org/abs/2410.12000) | [📊 Poster](https://neurips.cc/media/neurips-2024/Slides/93463.pdf)

We present a method for parametric model reduction of mean-field and stochastic systems. Our higher-order formulation significantly improves numerical stability compared to previous action matching approaches.

---

## Applications

Our method works directly on **particle data** without requiring grid-based discretization:

- **Vlasov-Poisson equations** for charged particle dynamics
- **Inertial particles** in turbulent flow  
- **Ocean drifter data** analysis
- Connections to **generative modeling** and diffusion models

<!-- Add application examples when available -->
![Applications](/assets/images/projects/population-dynamics-apps.jpg "Particle simulations and ocean drifter data")

---

## Connection to Generative Modeling

This work is related to generative modeling algorithms like score-based diffusion models and stochastic interpolants. In generative modeling, only the beginning and end of the path $t \mapsto \rho_t$ are given. Our framework provides a more constrained setting where we adhere to a physically meaningful path.

---

## Acknowledgements

This work was supported by the National Science Foundation and the Air Force Office of Scientific Research.