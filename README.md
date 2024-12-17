# Turbulent Flow Simulation using the Navier-Stokes Equations

## Overview

This repository provides a high-performance Python implementation for solving the **Navier-Stokes equations** to simulate **2D incompressible flow**. The project focuses on creating **turbulent flow** using numerical methods such as the **finite difference method (FDM)**. It demonstrates optimization techniques for high-performance computing, including:

1. **Baseline CPU implementation**  
2. **Numba-optimized parallel CPU version**  
3. **GPU-accelerated version using Numba CUDA**

The results include performance comparisons, stability analysis, and visualizations of the velocity fields to highlight the development of turbulence.

---

## Key Features

- **Navier-Stokes Solver**: Simulates incompressible flow using finite differences.
- **High-Performance Computation**:
  - Pure NumPy implementation for the baseline solver.
  - Numba-accelerated CPU solver for parallel computations.
  - GPU-based solver using Numba's CUDA for massive parallelism.
- **Turbulence Creation**: Localized velocity disturbances and low viscosity to trigger turbulence.
- **Visualization**: Streamline and quiver plots to observe velocity fields and turbulent structures.

---

## Problem Description

The Navier-Stokes equations describe the motion of viscous fluids. For incompressible flow, the equations are:

$$
\frac{\partial u}{\partial t} + u \frac{\partial u}{\partial x} + v \frac{\partial u}{\partial y} = -\frac{1}{\rho} \frac{\partial p}{\partial x} + \nu \left( \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} \right)
$$
$$
\frac{\partial v}{\partial t} + u \frac{\partial v}{\partial x} + v \frac{\partial v}{\partial y} = -\frac{1}{\rho} \frac{\partial p}{\partial y} + \nu \left( \frac{\partial^2 v}{\partial x^2} + \frac{\partial^2 v}{\partial y^2} \right)
$$

Where:  

- $ u, v $ are the velocity components in $ x $ and $ y $ directions.  
- $ p $ is the pressure field.  
- $ \nu $ is the kinematic viscosity.  
- $ \rho $ is the fluid density.  

This solver uses numerical methods to approximate these equations on a **2D grid** and explores how turbulence develops.

---

## Requirements

To run this project, ensure the following dependencies are installed:

- Python 3.8+
- NumPy
- Matplotlib
- Numba
- CUDA-capable GPU (for GPU acceleration)

Install dependencies using:

```bash
pip install numpy matplotlib numba
