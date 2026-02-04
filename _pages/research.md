---
title: "Research"
permalink: /research/
layout: single
author_profile: true
classes: wide
---

<style>
.project-card {
  display: flex;
  margin-bottom: 2.5em;
  padding-bottom: 2em;
  border-bottom: 1px solid #eee;
}
.project-thumb {
  flex: 0 0 250px;
  margin-right: 2em;
}
.project-thumb img {
  width: 250px;
  height: 160px;
  object-fit: cover;
  border: 1px solid #ddd;
  border-radius: 6px;
}
.project-thumb a {
  display: block;
}
.project-info {
  flex: 1;
}
.project-title {
  font-size: 1.3em;
  font-weight: bold;
  margin-bottom: 0.4em;
}
.project-title a {
  text-decoration: none;
  color: #333;
}
.project-title a:hover {
  color: #0066cc;
}
.project-collab {
  font-size: 0.95em;
  color: #666;
  margin-bottom: 0.8em;
  font-style: italic;
}
.project-desc {
  line-height: 1.6;
  margin-bottom: 1em;
}
.project-links a {
  display: inline-block;
  padding: 0.4em 0.8em;
  margin-right: 0.4em;
  background: #0066cc;
  color: white;
  border-radius: 4px;
  font-size: 0.9em;
  text-decoration: none;
}
.project-links a:hover {
  background: #0055aa;
}
.placeholder-img {
  width: 250px;
  height: 160px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 1em;
  text-align: center;
  border-radius: 6px;
  font-weight: bold;
}
.placeholder-img.plasma {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}
.placeholder-img.ml {
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
}
.placeholder-img.mor {
  background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
}

@media (max-width: 700px) {
  .project-card {
    flex-direction: column;
  }
  .project-thumb {
    margin-bottom: 1em;
    margin-right: 0;
  }
}
</style>

# Current Research Projects
* * *

<div class="project-card">
  <div class="project-thumb">
    <a href="/projects/magnetic-relaxation/">
      <img src="/assets/images/projects/mrx-teaser.png" alt="Magnetic Relaxation">
    </a>
  </div>
  <div class="project-info">
    <div class="project-title"><a href="/projects/magnetic-relaxation/">Magnetic Relaxation for MHD Equilibria</a></div>
    <div class="project-collab">with A. Kaptanoglu (NYU) and J. Stratton (PhD student, NYU)</div>
    <div class="project-desc">
      In fusion devices, finding magnetohydrostatic equilibria is crucial for design and operation. Standard methods assume nested flux surfaces, but real configurations feature magnetic islands and chaotic regions. We developed <strong>MRX</strong>, a magnetic relaxation code using structure-preserving finite elements in JAX that can compute general equilibria on GPUs—enabling PDE-constrained optimization for stellarator design.
    </div>
    <div class="project-links">
      <a href="/projects/magnetic-relaxation/">Project page</a>
      <a href="https://arxiv.org/abs/2510.26986">MRX preprint</a>
    </div>
  </div>
</div>

<div class="project-card">
  <div class="project-thumb">
    <a href="/projects/population-dynamics/">
      <img src="/assets/images/projects/ngif-teaser.gif" alt="Population Dynamics">
    </a>
  </div>
  <div class="project-info">
    <div class="project-title"><a href="/projects/population-dynamics/">Population Dynamics Inference</a></div>
    <div class="project-collab">with J. Berman, B. Peherstorfer, and A. Stuart</div>
    <div class="project-desc">
      Instead of inferring dynamics of individual stochastic trajectories, we consider the evolution of <em>populations</em>—distributions over many realizations. This leads to deterministic continuity equations. We exploit gauge freedom to find velocity fields minimizing kinetic energy, with connections to optimal transport. Our methods <strong>DICE</strong> and <strong>Higher-Order Action Matching</strong> (NeurIPS 2024) dramatically improve training stability.
    </div>
    <div class="project-links">
      <a href="/projects/population-dynamics/">Project page</a>
      <a href="https://arxiv.org/abs/2507.05107">DICE preprint</a>
      <a href="https://proceedings.neurips.cc/paper_files/paper/2024/file/6782c18960808848174cfe60742b415a-Paper-Conference.pdf">NeurIPS paper</a>
    </div>
  </div>
</div>

<div class="project-card">
  <div class="project-thumb">
    <a href="/projects/optimal-transport/">
      <div class="placeholder-img mor">Optimal Transport<br>Registration</div>
    </a>
  </div>
  <div class="project-info">
    <div class="project-title"><a href="/projects/optimal-transport/">Optimal Transport Registration for Model Reduction</a></div>
    <div class="project-collab">PhD research at Max Planck Institute for Plasma Physics</div>
    <div class="project-desc">
      Reduced basis methods struggle with advection-dominated problems where solutions exhibit moving features. We propose registration methods using <strong>Linear Optimal Transport</strong> and <strong>Wasserstein barycenters</strong> to align solution snapshots before building reduced bases. This dramatically improves approximation quality for Vlasov-Poisson equations and porous media flows.
    </div>
    <div class="project-links">
      <a href="/projects/optimal-transport/">Project page</a>
      <a href="https://doi.org/10.1137/23M1570715">SISC Paper</a>
    </div>
  </div>
</div>

---

# Research Interests
* * *

### Computational Plasma Physics
- Magnetohydrodynamic equilibrium solvers
- Stellarator optimization and design
- Structure-preserving discretizations using Finite Element Exterior Calculus

### Model Order Reduction
- Reduced basis methods for advection-dominated problems
- Optimal transport and Wasserstein methods
- Parametric model reduction for kinetic equations

### Scientific Machine Learning
- Generative models for dynamical systems
- Population dynamics inference
- Differentiable programming for physics simulations
