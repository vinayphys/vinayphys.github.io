---
layout: default
title: Software Developments
---

# Software Developments

Over the years as a part of my PhD research and postdoctoral employment, I have developed a number of codes to simulate a variety of systems, from glasses to polymers to active matter, for large-scale simulations and analysis tools to investigate structure, dynamics, thermal response, mechanical properties, topological defects, etc.

---

### Active Matter Simulation Framework  
A specialized custom implementation in [LAMMPS](https://www.lammps.org/) (Large-scale Atomic/Molecular Massively Parallel Simulator) to simulate different activity dynamics, like ABP (finite or infinite persistence) or AOUP in 2D or 3D, along with the quasistaic activity limits ADD (Activity Driven Dynamics) and AQRD (Athermal Quasistaic Random Displacement).

* **Language:** C++
* **Key Features:**
  * Tried and tested against various benchmark studies and presently being used in different research projects
  * Integrates with the default LAMMPS package, making easier to implement for existing users
  * Can be used by adding a single line in the input script specifying the parameters like, type of activity, persistence time, activity strength, etc

### Non-affine Lattice Dynamics  
Implemented NALD (Non-affine Lattice Dynamics) for coarse-grained and full atom polymer models to calculate frequency dependent modulus as a function of external frequency across multiple decades.   

Please have a look at the following dedicated Github repositories to which I fundamentally contributed:
[Full atom polymer system]()
[Coarse-grained polymer system]()

* **Language:** C++
* **Key Features:**
  * Tried and tested against various benchmark studies and presently being used in different research projects
  * Integrates with the default LAMMPS package, making easier to implement for existing users
  * Can be used by adding a single line in the input script specifying the parameters like, type of activity, persistence time, activity strength, etc

### Hybrid Swap Monte-Carlo Molecular Dynamics   
A specialized custom implementation in [LAMMPS](https://www.lammps.org/) to simulate Hybrid Swap Monte-Carlo Molecular Dynamics that performs a number of diameter swap attempts among the polydisperse particles based on Metropolis criterion at a given interval of MD steps.  

* **Language:** C++
* **Key Features:**
  * Tried and tested against various benchmark studies including a homegrown MC-MD code; used this feature in various published research
  * Integrates with the default LAMMPS package, making easier to implement for existing users   


### Custom implementation of various force fields, diameter polydispersityin LAMMPS
I have developed a custom implementation in [LAMMPS](https://www.lammps.org/) to simulate different size polydispersity and pair-potentials 

* **Language:** C++
* **Key Features:**
  * Tried and tested against various benchmark studies; used in various published research
  * Integrates with the default LAMMPS package, making easier to implement for existing users  
  * For size polydispersit, a list of diameters of particles written in a file is required
  * Some example pair-potential implementations: Hertzian, Inverse power law (including LP potential)


### Normal Mode Analysis
In different research projects, I have performed normal mode (frequency) analysis in glassy and polymeric systems that requires creation of dynamical matrix (Hessian) and its diagonalization to get eigenfrequencies and eigenmodes.

* **Language:** C/C++/Python
* **Key Features:**
  * First principle implementation to construct the dynamical matrix for different pair-potentials and its efficient storage in sparse format
  * C/C++ implementation to diagonalise the matrix; Via LAPACK if full spectrum is required; For partial spectrum, via SPECTRA with EIGEN package 
  * Tested for short-range potential (sparse Hessian) for a few million particles; for long-range potential (for example, full atom polymer models) upto 20 thousand particles


### Analysis Tools
Developed and implemented various analysis tools, many of them to run in a parallel. I have also worked with experimental data in some reserach projects that involve specialized tools different from those used in simulations.

* **Language:** C/C++/Python
* **Key Features:**
  * Structure: Pair-correlation function (g11(r), g22(r), etc), Structure factor (Static, Dynamical), Bond orientational order parameter including Hexatic order parameter and its spatial correlation, Cluster analysis 
  * Dynamics: Mean-squared displacement, Various two-point and four-point correlation functions in real and Fourier's space (von-Hove, Ovrelap, Intermediate scattering, etc), Non-affine displacement (D2min) in deformed periodic boundary condition
  * Thermal response: Heat-flux, Thermal conductivity, etc
  * Mechanics: Shear/Bulk modulus, 


### High Performance Computing
.... 

* **Language:** Shell/Python
* **Key Features:**
  * Job Scheduler: SLURM, PBS, CONDOR
  * Efficient management computing jobs 

