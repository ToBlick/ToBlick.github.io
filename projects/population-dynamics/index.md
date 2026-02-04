---
title: "Population Dynamics Inference"
permalink: /projects/population-dynamics/
layout: single
author_profile: true
classes: wide
---

[📄 DICE on arXiv](https://arxiv.org/abs/2507.05107) | [📄 NeurIPS 2024 Paper](https://papers.nips.cc/paper_files/paper/2024/file/6782c18960808848174cfe60742b415a-Paper-Conference.pdf) | [💻 Code](https://github.com/julesberman/HOAM)

---

Stochastic dynamical systems present notorious challenges for model order reduction. We propose a change of perspective: instead of inferring governing dynamics of a single system $X_t$, we consider the evolution of a **population** of such systems—the distribution of states over many realizations: $X_t \sim \rho_t$.

This distribution evolves according to a deterministic equation: $\partial_t \rho(t) = \text{div}(\rho_t u_t)$, where $u_t$ is a velocity field.

The task is to infer the velocity field $u_t$ that governs this evolution. 

Different trajectory dynamics can give rise to the same population dynamics. This means there are infinitely many velocity fields $u_t$ that are *compatible* with observed data. We exploit this gauge freedom to find velocity fields that minimize kinetic energy or other selection criteria.

<p style="text-align: center;">
  <img src="/assets/images/projects/ngif-teaser.gif" alt="Population Evolution" style="height: 200px;">
</p>

This work is related to generative modeling algorithms like score-based diffusion models and stochastic interpolants. In generative modeling, only the beginning and end of the path $t \mapsto \rho_t$ are given. Our framework provides a more constrained setting where generated samples collectively adhere to a physically meaningful path.

---

## Papers

### DICE: Discrete Inverse Continuity Equation for Learning Population Dynamics

Tobias Blickhan, [Jules Berman](https://julesberman.github.io), [Andrew Stuart](https://www.cms.caltech.edu/people/astuart), [Benjamin Peherstorfer](https://cims.nyu.edu/~pehersto/)  
*Submitted to Journal of Machine Learning Research*

[📄 arXiv](https://arxiv.org/abs/2507.05107)

Previous approaches (e.g., Action Matching) have proven numerically unstable. We identify the root cause: a reliance on analytical properties that do not hold at the discrete level.

### Parametric Model Reduction of Mean-Field and Stochastic Systems via Higher-Order Action Matching

Tobias Blickhan, [Jules Berman](https://julesberman.github.io), [Benjamin Peherstorfer](https://cims.nyu.edu/~pehersto/)  
*NeurIPS 2024*

[📄 Paper](https://papers.nips.cc/paper_files/paper/2024/file/6782c18960808848174cfe60742b415a-Paper-Conference.pdf) | [📄 arXiv](https://arxiv.org/abs/2410.12000) | [📊 Poster](https://neurips.cc/media/neurips-2024/Slides/93463.pdf)

We present a method for parametric model reduction of mean-field and stochastic systems. Our higher-order formulation significantly improves numerical stability compared to previous action matching approaches.

---

## Acknowledgements

This work was supported by the National Science Foundation and the Air Force Office of Scientific Research.