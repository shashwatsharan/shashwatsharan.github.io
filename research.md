---
layout: default
title: Research
---

My research in applied mathematics centres on nonlinear waves, dispersive partial differential equations and dynamical systems, motivated by problems in ultra-cold atomic physics, fluid dynamics and engineering. I combine asymptotic analysis with large-scale numerical computation, and I am especially drawn to problems at the intersection of mathematical theory, computation and experiment.

## Dispersive hydrodynamics and Bose–Einstein condensates

### Dam-break dynamics of confined Bose–Einstein condensates

When a confined fluid is suddenly released (the classical dam-break problem), it expands as a rarefaction wave. In ultra-cold atomic gases this expansion happens inside a trapping potential that holds the gas together, and the theory of such confined dam-breaks was, until recently, largely undeveloped. Working closely with experimental collaborators, I studied dam-break expansion in harmonically confined Bose–Einstein condensates, governed by a nonlinear Schrödinger equation with a harmonic potential:

$$
i\hbar\,\Psi_t = -\frac{\hbar^2}{2m}\nabla^2\Psi
+ \frac{m}{2}\left(\omega_x^2x^2+\omega_y^2y^2+\omega_z^2z^2\right)\Psi
+ g_{3D}\,\lvert\Psi\rvert^2\Psi .
$$

I derived and validated a reduced quasi-one-dimensional model of the full three-dimensional dynamics, identifying the effective coupling $$g_{1D} = \tfrac{2}{3}\,\mu/R_{TF}$$ that makes the reduction faithful, and described the flow through its Riemann invariants. To test the theory I ran GPU-accelerated three-dimensional simulations and compared the predicted invariants directly against experiment, finding excellent agreement. These results appeared in [*Physical Review Letters*](https://journals.aps.org/prl/abstract/10.1103/38f7-ym2v).

<!-- To add a figure: upload the image to assets/img/ and uncomment this block.
<figure>
  <img src="/assets/img/dambreak-3d.png" alt="3D dam-break simulation">
  <figcaption>3D simulation of dam-break expansion in a confined condensate, alongside experimental density images.</figcaption>
</figure>
-->

### Exact solutions for confined rarefaction waves

A natural follow-up is whether confined rarefaction flows can be described exactly, rather than only numerically. I developed a perturbative framework in which the confinement enters as a series of corrections to the classical unconfined simple-wave solution, and the full series can be summed in closed form. This yields what is, to my knowledge, the first exact closed-form solution of the nonlinear Schrödinger equation with harmonic confinement, capturing the flow near the vacuum edge of a dam-break. A manuscript presenting this framework and its higher-order corrections is in preparation.

### Effective dissipation in turbulent superfluids

Piston-like experiments in condensates produce turbulent structures and shock-like fronts that strongly resemble classical viscous shocks, even though the underlying model is conservative and has no dissipation. How does effective dissipation emerge from a dispersive, dissipationless system? I study this in the dam-break reflection configuration, where the flow generates its own shock front upon reflecting off a wall. By running high-resolution simulations of the higher-dimensional nonlinear Schrödinger equation alongside the inviscid compressible Euler equations, I aim to quantify this effective dissipation and connect it to classical viscous-shock theory.

<!-- To add a video: upload an .mp4 to assets/video/ and uncomment this block.
<figure>
  <video controls muted loop playsinline src="/assets/video/reflection.mp4"></video>
  <figcaption>2D simulation of dam-break reflection; a shock-like front forms after reflection from the wall.</figcaption>
</figure>
-->

### A scalar formulation for irrotational Euler flows

While studying the dispersionless limit of the nonlinear Schrödinger equation, I derived a scalar, complex-valued formulation that is equivalent to the compressible Euler equations for irrotational flow and, as a special case, the shallow-water equations. This formulation is, to my knowledge, new, and it brings practical advantages: fast split-step pseudospectral methods carry over almost unchanged, giving an efficient spectral scheme for irrotational Euler flows in any dimension. I am developing criteria for handling dry regions and shock formation, and extending the approach to broader classes of fluid systems.

## Nonlinear dynamical systems

### Oscillations and bifurcations in feedforward networks

My earlier work concerned feedforward networks of unidirectionally coupled nonlinear oscillators, systems that arise in engineering settings such as antenna arrays, where controlling the collective output is essential. I mapped out, in closed form, the regions of parameter space giving qualitatively different collective behaviour: phase and amplitude synchronisation, phase locking and signal amplification. In the amplification regime I showed that unidirectional coupling fundamentally changes the classical Hopf scaling, producing a hierarchical amplitude growth across the network with its own scaling law. This work appeared as a pair of papers in the *International Journal of Bifurcation and Chaos*.
