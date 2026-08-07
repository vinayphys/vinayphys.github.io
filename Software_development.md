---
layout: default
title: Software Developments
---

# Software Developments

During my PhD and postdoctoral work, I have developed specialized computational tools and simulation packages for complex soft-matter systems. My software spans large-scale molecular dynamics (MD), hybrid Monte Carlo–MD schemes, and customized continuum/lattice solvers for glasses, polymers, and active matter. I also maintain analysis suites for structural order, nonequilibrium dynamics, thermal transport, mechanical response, and topological defects.

---

### Active Matter Simulation Framework
A set of LAMMPS extensions to simulate active dynamics, including Active Brownian Particles (ABP, with tunable persistence) and Active Ornstein–Uhlenbeck Processes (AOUP) in 2D and 3D. It also covers quasistatic activity limits such as Activity-Driven Dynamics (ADD) and Athermal Quasistatic Random Displacements (AQRD).

- **Language:** C++
- **Key Features:**
  - Production-tested across multiple projects and currently deployed in ongoing studies.
  - Drop-in integration with the standard LAMMPS source for straightforward compilation.
  - One-line invocation in LAMMPS input scripts (activity type, persistence time, strength, etc.).

---

### Non-affine Lattice Dynamics (NALD)
An implementation of Non-affine Lattice Dynamics for coarse-grained and all-atom polymer models. It computes frequency-dependent viscoelastic moduli over many decades in frequency.

- **Repositories:**
  - [All-Atom Polymer System](https://github.com/ZacconeAlessio/NALD_atomistic)
  - [Coarse-Grained Polymer System](https://github.com/ZacconeAlessio/NALD_coarse-grained)
- **Language:** C++/Python
- **Key Features:**
  - Validated against analytical and numerical benchmarks.
  - Efficient computation of non-affine mobility matrices and elastic constants.
  - Direct integration into LAMMPS routines for high-throughput calculations.

---

### Hybrid Swap Monte Carlo–Molecular Dynamics
A specialized LAMMPS extension implementing hybrid Swap MC–MD for polydisperse particle packings. Diameter swaps are attempted at user-defined MD intervals with Metropolis acceptance, accelerating equilibration in dense glassy states.

- **Language:** C++
- **Key Features:**
  - Rigorously validated against standalone MC–MD solvers and used in published research.
  - Fully integrated into the native LAMMPS framework.
  - Significantly reduces equilibration times in polydisperse glasses.

---

### Topological Defect Identification
Python tools to identify topological defects (charges) in 2D fields. Developed for normal-mode fields but applicable to generic scalar or vector fields.

- **Language:** Python
- **Key Features:**
  - Efficient detection and classification of topological defects/charges.
  - Multiscale coarse-graining to probe different length scales.

---

### Custom Force Fields & Size Polydispersity in LAMMPS
Custom pair styles and fixes in LAMMPS for arbitrary continuous size-polydispersity distributions and specialized pair potentials.

- **Language:** C++
- **Key Features:**
  - Production-tested and used in multiple peer-reviewed publications.
  - Reads arbitrary particle-diameter distributions directly from external files.
  - Supported pair potentials include Hertzian, inverse power law (IPL), and Lennard-Jones-like (e.g., LP) interactions.

---

### Normal Mode Analysis & Vibrational Spectra
Algorithms for vibrational analysis in glassy and polymeric materials via explicit construction of the dynamical matrix (Hessian) and eigen-decomposition to obtain eigenfrequencies and eigenmodes.

- **Languages:** C++, C, Python
- **Key Features:**
  - Efficient construction and storage of large sparse Hessians for arbitrary pair potentials.
  - Diagonalization via LAPACK (full spectra) and Spectra with the Eigen headers (targeted partial spectra).
  - Scales to millions of particles for short-range interactions (sparse Hessians) and up to ~20,000 particles for long-range/all-atom systems.

---

### Analysis & Diagnostic Tools
A comprehensive suite of parallelized post-processing scripts for simulation trajectories and experimental datasets.

- **Languages:** C++, Python
- **Key Features:**
  - **Structural order:** partial pair-correlation functions $g_{ij}(r)$, static/dynamic structure factors $S(q)$, bond-orientational order parameters ($\psi_6$), spatial correlation functions, and cluster identification.
  - **Dynamics:** mean-squared displacement (MSD), two- and four-point space–time correlations (van Hove functions, overlap parameters, intermediate scattering functions), and non-affine displacement analysis ($D^2_{\min}$) under sheared periodic boundaries.
  - **Thermal response:** heat-flux autocorrelation and thermal conductivity.
  - **Mechanics:** shear and bulk moduli via fluctuation formulas and stress–strain protocols; shear-band identification.

---

### High-Performance Computing (HPC) & Workflow Automation
Automated pipelines for high-throughput computing across supercomputing clusters and distributed infrastructure.

- **Languages:** Bash/Shell, Python
- **Key Features:**
  - Experience with SLURM, PBS, and HTCondor.
  - Automated job submission, checkpointing, parameter sweeps, and data aggregation.
