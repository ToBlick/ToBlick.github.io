---
title: "Population Dynamics Inference"
permalink: /projects/population-dynamics/
layout: single
author_profile: true
classes: wide
---

[📄 TPF on arXiv](https://arxiv.org/abs/2605.26285) | [📄 Stochastic Lifting on arXiv](https://arxiv.org/abs/2605.29194) | [📄 NGIF on arXiv](https://arxiv.org/abs/2605.25107) | [📄 DICE on arXiv](https://arxiv.org/abs/2507.05107) | [📄 NeurIPS 2024 Paper](https://papers.nips.cc/paper_files/paper/2024/file/6782c18960808848174cfe60742b415a-Paper-Conference.pdf)

---

Instead of learning the dynamics of a single stochastic system $t \mapsto X_t$, we learn the evolution of a **population** of them: the distribution $\rho_t$ of states over many realizations. It follows the continuity equation $\partial_t \rho_t + \text{div}(\rho_t u_t) = 0$, and the task is to infer the velocity field $u_t$ from unlabeled samples at a few time points.

<p style="text-align: center;">
  <img src="/assets/images/projects/tpf-barotropic.png" alt="Barotropic turbulence" style="width: 100%; max-width: 800px;">
  <br><em>Barotropic turbulence with more than $10^4$ state dimensions. Top: ground truth. Middle: samples from a two-parameter flow. Bottom: pointwise trajectory fitting.</em>
</p>

Many velocity fields are compatible with the same population data. This gauge freedom lets us pick fields by a criterion of our choice, such as minimal kinetic energy. Population dynamics offer the potential for a massive complecity reduction in the learned field, if one is willing to give up the goal of following sample trajectories.

<p style="text-align: center;">
  <img src="/assets/images/projects/tpf-marginals.png" alt="TPF marginals" style="width: 100%; max-width: 700px;">
  <br><em>Snapshots of a curve $t \mapsto \rho_t$. Samples keep their color over time; the learned flow is similar to piecewise optimal transport, but more regular.</em>
</p>

---

## Papers

### Two-Parameter Flows for Learning Population Dynamics of Physical Systems

[Paul Schwerdtner](https://algopaul.github.io), Tobias Blickhan, [Benjamin Peherstorfer](https://cims.nyu.edu/~pehersto/)  
*ICML 2026*

[📄 OpenReview](https://openreview.net/forum?id=2Opz9uBYQT) | [📄 arXiv](https://arxiv.org/abs/2605.26285) | [📊 Poster](https://icml.cc/media/PosterPDFs/ICML%202026/66588.png?t=1782905152.1738322) | [💻 Code](https://github.com/Algopaul/tpf)

### Stochastic Lifting for Generating Trajectories of Stochastic Physical Systems

[Jules Berman](https://julesberman.github.io), Tobias Blickhan, [Benjamin Peherstorfer](https://cims.nyu.edu/~pehersto/)  
*ICML 2026*

[📄 OpenReview](https://openreview.net/forum?id=hmJdJLmwOY) | [📄 arXiv](https://arxiv.org/abs/2605.29194) | [📊 Poster](https://icml.cc/media/PosterPDFs/ICML%202026/62310.png?t=1782905316.1924145) | [💻 Code](https://github.com/julesberman/stochastic_lifting)

### Leveraging Gauge Freedom for Learning Non-Gradient Population Dynamics of Stochastic Systems

[Jules Berman](https://julesberman.github.io), Tobias Blickhan, [Benjamin Peherstorfer](https://cims.nyu.edu/~pehersto/)  
*arXiv preprint, 2026*

[📄 arXiv](https://arxiv.org/abs/2605.25107) | [💻 Code](https://github.com/julesberman/ngif)

### DICE: Discrete Inverse Continuity Equation for Learning Population Dynamics

Tobias Blickhan, [Jules Berman](https://julesberman.github.io), [Andrew Stuart](https://www.cms.caltech.edu/people/astuart), [Benjamin Peherstorfer](https://cims.nyu.edu/~pehersto/)  
*Submitted to Journal of Machine Learning Research*

[📄 arXiv](https://arxiv.org/abs/2507.05107)

### Parametric Model Reduction of Mean-Field and Stochastic Systems via Higher-Order Action Matching

Tobias Blickhan, [Jules Berman](https://julesberman.github.io), [Benjamin Peherstorfer](https://cims.nyu.edu/~pehersto/)  
*NeurIPS 2024*

[📄 Paper](https://papers.nips.cc/paper_files/paper/2024/file/6782c18960808848174cfe60742b415a-Paper-Conference.pdf) | [📄 arXiv](https://arxiv.org/abs/2410.12000) | [📊 Poster](https://neurips.cc/media/neurips-2024/Slides/93463.pdf) | [💻 Code](https://github.com/julesberman/HOAM)

---

## Acknowledgements

This work was supported by the National Science Foundation and the Air Force Office of Scientific Research.
