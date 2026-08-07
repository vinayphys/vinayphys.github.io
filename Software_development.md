---
layout: default
title: Software Developments
---

# Software Developments

During my PhD and postdoctoral work, I have developed computational tools and simulation packages for complex soft-matter systems. These include large-scale molecular dynamics (MD), hybrid Monte Carlo–MD schemes, and continuum/lattice solvers for glasses, polymers, and active matter. I also maintain analysis suites for structural order, nonequilibrium dynamics, thermal transport, mechanical response, and topological defects.

---

## Active Matter Simulation Framework

LAMMPS extensions to simulate active dynamics, including Active Brownian Particles (ABP, with tunable persistence) and Active Ornstein–Uhlenbeck Processes (AOUP) in 2D and 3D. The framework also supports quasistatic activity limits such as Activity-Driven Dynamics (ADD) and Athermal Quasistatic Random Displacements (AQRD).

- **Language:** C++
- **Key features:**
  - Tested in multiple projects and used in ongoing studies
  - Drop-in integration with the standard LAMMPS source
  - Simple invocation in LAMMPS input scripts (activity type, persistence time, strength, etc.)

---

## Non-affine Lattice Dynamics (NALD)

Implementation of Non-affine Lattice Dynamics for coarse-grained and all-atom polymer models. It computes frequency-dependent viscoelastic moduli over many decades in frequency.

- **Repositories:**
  - [All-atom polymer system](https://github.com/ZacconeAlessio/NALD_atomistic)
  - [Coarse-grained polymer system](https://github.com/ZacconeAlessio/NALD_coarse-grained)
- **Language:** C++ / Python
- **Key features:**
  - Validated against analytical and numerical benchmarks
  - Efficient computation of non-affine mobility matrices and elastic constants
  - Direct integration into LAMMPS routines for high-throughput calculations

---

## Hybrid Swap Monte Carlo–Molecular Dynamics

LAMMPS extension implementing hybrid Swap MC–MD for polydisperse particle packings. Diameter swaps are attempted at user-defined MD intervals with Metropolis acceptance, accelerating equilibration in dense glassy states.

- **Language:** C++
- **Key features:**
  - Validated against standalone MC–MD solvers and used in published research
  - Fully integrated into the native LAMMPS framework
  - Significantly reduces equilibration times in polydisperse glasses

---

## Topological Defect Identification

Python tools to identify topological defects (charges) in 2D fields. Developed for normal-mode fields but applicable to generic scalar or vector fields.

- **Language:** Python
- **Key features:**
  - Efficient detection and classification of topological defects / charges
  - Multiscale coarse-graining to probe different length scales

---

## Custom Force Fields & Size Polydispersity in LAMMPS

Custom pair styles and fixes in LAMMPS for continuous size-polydispersity distributions and specialized pair potentials.

- **Language:** C++
- **Key features:**
  - Used in multiple peer-reviewed publications
  - Reads particle-diameter distributions from external files
  - Supported pair potentials include Hertzian, inverse power law (IPL), and Lennard-Jones-like interactions

---

## Normal Mode Analysis & Vibrational Spectra

Algorithms for vibrational analysis in glassy and polymeric materials via explicit construction of the dynamical matrix (Hessian) and eigen-decomposition to obtain eigenfrequencies and eigenmodes.

- **Languages:** C++, C, Python
- **Key features:**
  - Efficient construction and storage of large sparse Hessians for arbitrary pair potentials
  - Diagonalization via LAPACK (full spectra) and Spectra/Eigen (partial spectra)
  - Scales to millions of particles for short-range interactions and to ~20,000 particles for long-range / all-atom systems

---

## Analysis & Diagnostic Tools

Parallelized post-processing scripts for simulation trajectories and experimental datasets.

- **Languages:** C++, Python
- **Key features:**
  - **Structural order:** pair-correlation functions, static/dynamic structure factors, bond-orientational order in 2D/3D, spatial correlation functions, cluster identification
  - **Dynamics:** mean-squared displacement; two- and four-point space–time correlations (van Hove functions, overlap parameters, intermediate scattering functions); non-affine displacement analysis (D2min) under shear
  - **Thermal response:** heat flux; thermal conductivity
  - **Mechanics:** shear and bulk moduli via fluctuation formulas and stress–strain protocols; shear-band identification
  - **Visualization:** trajectory rendering and post-processing using **OVITO**, **VMD**, and **Matplotlib**

---

## High-Performance Computing (HPC) & Workflow Automation

Automated pipelines for high-throughput computing on supercomputing clusters and distributed infrastructure.

- **Languages:** Bash / Shell, Python
- **Key features:**
  - Experience with SLURM, PBS, and HTCondor
  - Automated job submission, checkpointing, parameter sweeps, and data aggregation
