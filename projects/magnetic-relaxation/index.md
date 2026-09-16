---
title: "Magnetic Relaxation for MHD Equilibria"
permalink: /projects/magnetic-relaxation/
layout: single
author_profile: true
classes: wide
---

[📄 MRX paper (PDF)](/assets/pdfs/MRX_paper.pdf) | [📄 Boundary preprint](https://arxiv.org/abs/2605.01652) | [💻 Code](https://github.com/ToBlick/MRX)
<!-- [📄 MRX on arXiv](https://arxiv.org/abs/2510.26986) -->

---

A fusion plasma near steady state is in magnetohydrostatic (MHS) equilibrium: $(\text{curl } B) \times B = \nabla p$,  $\text{div } B = 0$. MRX is able to compute configurations have magnetic islands and chaotic regions.

<p style="text-align: center;">
  <img src="/assets/images/projects/mrx-ncsx-islands.png" alt="NCSX equilibrium with a 3/5 island chain" style="width: 100%; max-width: 800px;">
  <br><em>A non-nested NCSX equilibrium computed with MRX, colored by rotational transform (left) and pressure (right). A 3/5 island chain has formed through magnetic reconnection.</em>
</p>

## Relaxation

MHS states are minima of the magnetic energy along *admissible variations* $\delta B = \text{curl}(v \times B)$, which preserve field topology. MRX follows these orbits. 

<div style="display: flex; flex-wrap: wrap; justify-content: center; align-items: center; gap: 1.5em;">
  <img src="/assets/images/projects/mrx-energy-landscape.png" alt="Magnetic energy landscape" style="height: 260px;">
</div>
<p style="text-align: center;"><em>Magnetic energy landscape with constant-helicity sheets and the orbit of admissible variations.</em></p>

Targeted resistive steps can be used to change the topology in a controlled way.

<div style="display: flex; flex-wrap: wrap; justify-content: center; align-items: center; gap: 1.5em;">
  <img src="/assets/images/projects/mrx-reconnection-before-after.png" alt="Poincaré sections before and after reconnection" style="height: 260px;">
</div>
<p style="text-align: center;"><em>Poincaré sections of a NCSX equilibrium before and after reconnection.</em></p>

## The code

MRX is written in JAX, using Finite Element Exterior Calculus. An inexact Newton method computes high-resolution finite-$\beta$ equilibria in minutes on a single GPU. Just clone and `pip install`!

<div style="display: flex; flex-wrap: wrap; justify-content: center; align-items: center; gap: 1.5em;">
  <img src="/assets/images/projects/mrx-meshes.png" alt="Meshes in MRX" style="height: 300px;">
</div>
<p style="text-align: center;"><em>Different meshes on a poloidal plane with their equilibria configurations.</em></p>

---

## Papers

### MRX: A Differentiable 3D MHD Equilibrium Solver Without Nested Flux Surfaces

Tobias Blickhan, Julianne Stratton, [Alan A. Kaptanoglu](https://wp.nyu.edu/courantinstituteofmathematicalsciences-alankaptanoglu/)  
*arXiv preprint, 2025*

[📄 PDF](/assets/pdfs/MRX_paper.pdf) | [💻 Code](https://github.com/ToBlick/MRX)
<!-- [📄 arXiv](https://arxiv.org/abs/2510.26986) -->

### Computational Boundary Specification in 3D Fixed-Boundary Magnetohydrodynamic Equilibrium Modeling

[Alan A. Kaptanoglu](https://wp.nyu.edu/courantinstituteofmathematicalsciences-alankaptanoglu/), Tobias Blickhan  
*arXiv preprint, 2026*

[📄 arXiv](https://arxiv.org/abs/2605.01652)

---

## Acknowledgements

This work was supported by the Simons Collaboration on Hidden Symmetries and Fusion Energy and a Google TPU Research Award.
