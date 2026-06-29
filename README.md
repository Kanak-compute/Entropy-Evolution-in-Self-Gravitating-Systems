# Self-Gravitating-Systems-Entropy
Python implementation of a 2D N-body simulation investigating entropy evolution, gravitational collapse, and phase-space dynamics in self-gravitating systems.# Entropy and the Emergence of Structure in Self-Gravitating Systems

## Overview

Self-gravitating systems present an interesting challenge to our intuition about thermodynamics. In many physical systems, increasing entropy is associated with increasing disorder. A gas, for example, naturally spreads out to occupy all available space.

Gravitational systems appear to behave differently. Under gravity, particles attract one another and form dense structures such as stars, galaxies, and galaxy clusters. From a spatial perspective, this evolution appears to increase order rather than disorder.

This project investigates that apparent contradiction through numerical simulation of a self-gravitating N-body system. By tracking multiple entropy measures simultaneously, the simulation explores how entropy evolves during gravitational collapse and whether the Second Law of Thermodynamics remains valid.

---

## The Physical Question

The central question explored in this project is:

**If entropy must increase, why do self-gravitating systems spontaneously form ordered structures?**

The answer lies in distinguishing between spatial order and thermodynamic entropy.

While particles become more concentrated in space during gravitational collapse, entropy is not determined solely by position. A complete thermodynamic description requires consideration of both positions and velocities within phase space.

To investigate this behavior, the simulation tracks:

* Spatial Entropy
* Velocity Entropy
* Phase-Space Entropy

simultaneously throughout the evolution of the system.

---

## Simulation Methodology

### System Initialization

The simulation begins with particles randomly distributed in two-dimensional space with small initial velocities.

This represents an initially diffuse gravitational system with no preferred structure.

The average velocity is adjusted to zero so that the system has no net motion.

---

### Gravitational Interaction

Each particle interacts gravitationally with every other particle in the system.

Because close particle encounters can generate extremely large forces and numerical instabilities, a gravitational softening parameter is introduced. This modifies short-range interactions while preserving large-scale gravitational behavior.

---

### Time Evolution

The evolution of the system is computed using the Velocity Verlet integration method.

Velocity Verlet was chosen because it:

* Provides good numerical stability
* Conserves energy effectively
* Accurately captures long-term dynamical behavior

At every time step, particle positions and velocities are updated according to the gravitational forces acting on the system.

---

## Entropy Analysis

Three independent entropy measures are calculated during the simulation.

### Spatial Entropy

Spatial entropy measures how particles are distributed throughout physical space.

As particles cluster together under gravity, spatial entropy decreases because the distribution becomes less uniform.

---

### Velocity Entropy

Velocity entropy measures the distribution of particle speeds.

During gravitational collapse, potential energy is converted into kinetic energy. Some particles gain significant velocity while others remain slower, broadening the velocity distribution.

This causes velocity entropy to increase.

---

### Phase-Space Entropy

Phase-space entropy combines both position and velocity information.

A system may appear increasingly ordered in physical space while simultaneously becoming more complex in velocity space.

Phase-space analysis provides a more complete description of the thermodynamic evolution of the system.

---

## Energy Analysis

The simulation continuously tracks:

* Kinetic Energy
* Potential Energy
* Total Energy

As collapse proceeds:

* Potential energy decreases
* Kinetic energy increases
* Total energy remains approximately conserved

Monitoring energy conservation provides validation of the numerical integration scheme and confirms the physical consistency of the simulation.

---

## Results

The simulation demonstrates several important behaviors:

### Gravitational Clustering

Particles evolve from an initially diffuse configuration into dense gravitational structures.

### Entropy Redistribution

Spatial entropy decreases as clustering occurs.

At the same time, velocity entropy increases because particle motions become increasingly diverse.

### Stable Phase-Space Evolution

Phase-space entropy remains relatively stable throughout the evolution of the system.

### Energy Conservation

Total energy exhibits only minor fluctuations and remains approximately conserved over the duration of the simulation.

---

## Key Conclusion

The formation of ordered structures in self-gravitating systems does not violate the Second Law of Thermodynamics.

Although particles become more organized spatially, entropy is not destroyed. Instead, entropy is redistributed between spatial and velocity degrees of freedom.

The simulation demonstrates how gravitational dynamics and statistical mechanics remain fully consistent when the system is analyzed in phase space rather than position space alone.

---

## Technologies Used

* Python
* NumPy
* Matplotlib
* Jupyter Notebook

---

## Topics

Computational Physics • Statistical Mechanics • Gravitation • N-Body Dynamics • Entropy • Phase-Space Analysis • Astrophysics

---

## References

* Schroeder, *An Introduction to Thermal Physics*
* Pathria & Beale, *Statistical Mechanics*
* Binney & Tremaine, *Galactic Dynamics*
* Padmanabhan, *Statistical Mechanics of Gravitating Systems*
* Goldstein, *Classical Mechanics*
