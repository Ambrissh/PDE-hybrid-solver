# PDE Specifications - Burgers' Equation

## Governing Equation

The 1D viscous Burgers' equation:

$$
\frac{\partial u}{\partial t} + u \frac{\partial u}{\partial x} = \nu \frac{\partial^2 u}{\partial x^2}, \quad x \in [0, 2\pi], \ t \in [0, 1]
$$

## Physical Description

The Burgers' equation models nonlinear advection and diffusion of a velocity field $u(x,t)$.

## Domain and Parameters

- **Spatial domain**: $x \in [0, 2\pi]$ (periodic)
- **Time domain**: $t \in [0, 1]$
- **Viscosity**: $\nu \in [0.001, 0.02]$

## Initial Condition

$$
u_0(x) = \sum_{k=1}^{N} A_k \sin(kx + \phi_k)
$$

## Purpose

- **Neural Operator**: $(u_0, \nu) \mapsto u_T$
- **PINN**: $\mathcal{R}(u) = \frac{\partial u}{\partial t} + u \frac{\partial u}{\partial x} - \nu \frac{\partial^2 u}{\partial x^2}$
