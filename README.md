# 🌊 2D Rayleigh–Bénard Convection (Boussinesq) — Interactive Web Demo

An interactive, browser-based simulation of **2D Rayleigh–Bénard convection** under the **Boussinesq approximation**, implemented in vanilla **HTML, CSS, and JavaScript**.

This project visualizes buoyancy-driven convection using a **streamfunction–vorticity formulation**, allowing real-time exploration of key physical and numerical parameters.

🔗 **Live Demo:**  
https://kavyaagarwal2001.github.io/rb-convection/

## Overview

Rayleigh–Bénard convection describes the instability that develops when a fluid layer is heated from below and cooled from above. When the **Rayleigh number (Ra)** exceeds a critical threshold, buoyancy overcomes thermal diffusion and organized convection rolls emerge.

This demo numerically evolves a simplified 2D Boussinesq system and renders both the **temperature field** and **velocity vectors** in real time.

The goal is to provide an intuitive, interactive visualization of convection dynamics while preserving the structure of the governing equations.

## Governing Equations (Streamfunction–Vorticity Formulation)

The simulation uses a 2D streamfunction–vorticity representation:

**Poisson equation for streamfunction**

$$
\nabla^2 \psi = -\omega
$$

**Buoyancy-forced vorticity relation (simplified form)**

$$
\nabla^2 \omega \propto Ra \frac{\partial T}{\partial x}
$$

**Temperature advection–diffusion**

$$
\frac{\partial T}{\partial t} + \mathbf{u}\cdot\nabla T = \nabla^2 T
$$

Velocity components are recovered from the streamfunction:

$$
u = -\frac{\partial \psi}{\partial z}, \qquad
w = \frac{\partial \psi}{\partial x}
$$

## Numerical Approach

- Finite-difference spatial discretization
- Explicit time stepping for temperature
- Iterative Poisson solver (fixed iteration count for interactivity)
- Dirichlet temperature boundary conditions (hot bottom, cold top)
- Zero streamfunction boundary conditions

This implementation prioritizes **conceptual clarity and interactivity** rather than high-accuracy CFD convergence.

## Possible Extensions

- Convergence-based Poisson solver
- Periodic boundary conditions in x
- Kinetic energy diagnostics
- Critical Rayleigh number validation
- WebGL acceleration
- Snapshot export / animation recording

## Motivation

This project demonstrates how core geophysical fluid dynamics equations can be translated into a lightweight browser-based solver.

It bridges:
- Partial differential equations
- Numerical methods
- Scientific visualization
- Interactive communication of physical intuition

---

## License

MIT License