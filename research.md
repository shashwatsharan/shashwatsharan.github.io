---
layout: default
title: Research
---

My research in applied mathematics centres on nonlinear waves, dispersive partial differential equations and dynamical systems, motivated by problems in ultra-cold atomic physics, fluid dynamics and engineering. I combine asymptotic analysis with large-scale numerical computation, and I am especially drawn to problems at the intersection of mathematical theory, computation and experiment.

Below I present some results and simulations from my research. Click a topic to expand it.

## Dispersive hydrodynamics and Bose–Einstein condensates

<details class="topic" markdown="1">
<summary>Confined expansive waves in Bose–Einstein condensates</summary>

A condensate released from one half of a harmonic trap expands into vacuum as a rarefaction wave, a dry dam break against the confining potential.

<details class="result" markdown="1">
<summary>An exact rarefaction wave solution in a harmonic trap</summary>

An elongated condensate obeys the one dimensional NLS equation with a harmonic potential

$$
i\hbar\,\psi_t = -\frac{\hbar^2}{2m}\,\psi_{xx} + \frac{1}{2}\,m\,\omega^2x^2\,\psi + g\,\lvert\psi\rvert^2\psi .
$$

With sound speed $$c = \sqrt{g\lvert\psi\rvert^2/m}$$, superfluid velocity $$u$$ and initial sound speed $$c_0$$, I found the exact solution near the vacuum edge

$$
\begin{aligned}
c^2 &= \frac{\omega^2}{4}\csc^2\!\Big(\frac{3\omega t}{2}\Big)\big(X(t)-x\big)^2, \\[4pt]
u &= \frac{2c_0 + \omega x\cos\!\big(\frac{3\omega t}{2}\big)\csc\!\big(\frac{\omega t}{2}\big)}{1+2\cos(\omega t)},
\end{aligned}
\qquad
X(t) = \frac{2c_0}{\omega}\sin(\omega t).
$$

Since $$c$$ is linear in $$x$$, the quantum pressure vanishes and the same pair solves the Euler equations with parabolic forcing, where $$h = c^2$$

$$
h_t + (hu)_x = 0,
\qquad
u_t + u\,u_x + h_x = -\,\omega^2 x .
$$

As $$\omega \to 0$$ it reduces to the classical simple wave

$$
c^2 = \frac{1}{9}\Big(2c_0 - \frac{x}{t}\Big)^2,
\qquad
u = \frac{2}{3}\Big(\frac{x}{t} + c_0\Big),
\qquad
X = 2c_0\,t .
$$

Details are in [arXiv:2607.13050](https://arxiv.org/abs/2607.13050).

</details>

<details class="result" markdown="1">
<summary>Experiment and simulations</summary>

GPU accelerated three dimensional simulations of the confined dam break, compared directly with experiment. Published in [*Physical Review Letters*](https://journals.aps.org/prl/abstract/10.1103/38f7-ym2v).

</details>

<!-- Experiment (to be added). Earlier text kept here for reference:
When a confined fluid is suddenly released (the classical dam-break problem), it expands as a rarefaction wave. In ultra-cold atomic gases this expansion happens inside a trapping potential that holds the gas together, and the theory of such confined dam-breaks was, until recently, largely undeveloped. Working closely with experimental collaborators, I studied dam-break expansion in harmonically confined Bose–Einstein condensates, governed by a nonlinear Schrödinger equation with a harmonic potential:

$$
i\hbar\,\Psi_t = -\frac{\hbar^2}{2m}\nabla^2\Psi
+ \frac{m}{2}\left(\omega_x^2x^2+\omega_y^2y^2+\omega_z^2z^2\right)\Psi
+ g_{3D}\,\lvert\Psi\rvert^2\Psi .
$$

I derived and validated a reduced quasi-one-dimensional model of the full three-dimensional dynamics, identifying the effective coupling $$g_{1D} = \tfrac{2}{3}\,\mu/R_{TF}$$ that makes the reduction faithful, and described the flow through its Riemann invariants. To test the theory I ran GPU-accelerated three-dimensional simulations and compared the predicted invariants directly against experiment, finding excellent agreement. These results appeared in [*Physical Review Letters*](https://journals.aps.org/prl/abstract/10.1103/38f7-ym2v).

 To add a figure: upload the image to assets/img/ and uncomment this block.
<figure>
  <img src="/assets/img/dambreak-3d.png" alt="3D dam-break simulation">
  <figcaption>3D simulation of dam-break expansion in a confined condensate, alongside experimental density images.</figcaption>
</figure>


### Exact solutions for confined rarefaction waves

A natural follow-up is whether confined rarefaction flows can be described exactly, rather than only numerically. I developed a perturbative framework in which the confinement enters as a series of corrections to the classical unconfined simple-wave solution, and the full series can be summed in closed form. This yields what is, to my knowledge, the first exact closed-form solution of the nonlinear Schrödinger equation with harmonic confinement, capturing the flow near the vacuum edge of a dam-break. A manuscript presenting this framework and its higher-order corrections is in preparation.
-->

</details>

<details class="topic" markdown="1">
<summary>Effective dissipation in turbulent superfluids</summary>

In dam break reflection experiments on condensates, the reflected flow forms a shock front that looks like a classical viscous shock, even though the underlying model has no dissipation. A transverse snake instability breaks the dispersive shock wave into vortices, and on the macroscopic scale this vortex dynamics acts as an effective viscosity. The resulting shock is described by the Rankine–Hugoniot jump conditions of the compressible Euler equations. I study this with high resolution simulations of the three dimensional nonlinear Schrödinger equation and the inviscid compressible Euler equations, compared directly with experiment.

<details class="result" markdown="1">
<summary>Experiment and 3D simulation of a dam-break flow</summary>

<figure>
  <video controls muted loop playsinline preload="none" poster="/assets/video/bec-dambreak-exp-vs-sim-poster.jpg" src="/assets/video/bec-dambreak-exp-vs-sim.mp4"></video>
  <figcaption>Dam-break flow of a Bose–Einstein condensate: measured column density (top) vs. a 3D simulation (middle), with line densities below. The simulation is integrated along the imaging direction, stretched transversely to match the time-of-flight expansion, and smoothed to the imaging resolution of the camera.</figcaption>
</figure>

</details>

<!-- To add a video: upload an .mp4 to assets/video/ and uncomment this block.
<figure>
  <video controls muted loop playsinline src="/assets/video/reflection.mp4"></video>
  <figcaption>2D simulation of dam-break reflection; a shock-like front forms after reflection from the wall.</figcaption>
</figure>
-->

</details>

<details class="topic" markdown="1">
<summary>A scalar formulation for irrotational Euler flows</summary>

While studying the dispersionless limit of the nonlinear Schrödinger equation, I derived a scalar, complex-valued formulation that is equivalent to the compressible Euler equations for irrotational flow and, as a special case, the shallow-water equations. This formulation is, to my knowledge, new, and it brings practical advantages: fast split-step pseudospectral methods carry over almost unchanged, giving an efficient spectral scheme for irrotational Euler flows in any dimension. I am developing criteria for handling dry regions and shock formation, and extending the approach to broader classes of fluid systems.

</details>

## Nonlinear dynamical systems

<details class="topic" markdown="1">
<summary>Oscillations and bifurcations in feedforward networks</summary>

My earlier work concerned feedforward networks of unidirectionally coupled nonlinear oscillators, systems that arise in engineering settings such as antenna arrays, where controlling the collective output is essential. I mapped out, in closed form, the regions of parameter space giving qualitatively different collective behaviour: phase and amplitude synchronisation, phase locking and signal amplification. In the amplification regime I showed that unidirectional coupling fundamentally changes the classical Hopf scaling, producing a hierarchical amplitude growth across the network with its own scaling law. This work appeared as a pair of papers in the *International Journal of Bifurcation and Chaos*.

</details>
