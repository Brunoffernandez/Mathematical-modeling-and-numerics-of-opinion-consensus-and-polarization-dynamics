# Opinion Consensus and Polarization Dynamics: Mathematical Modeling and Numerics

## Overview
This repository contains the Bachelor's Degree Thesis, presentation slides, and simulation code for the project **"Mathematical modeling and numerics of opinion consensus and polarization dynamics"** by Bruno Fernández Carballo (2026), supervised by Gissell Estrada-Rodriguez at UPC FME. The project investigates the application of kinetic theory, specifically the Boltzmann equation, to model social opinion dynamics. It utilizes the Direct Simulation Monte Carlo (DSMC) method, specifically the Nanbu-Babovsky scheme, to simulate opinion exchanges among interacting agents.

## Repository Contents

### 1. `TFG_Bruno_MCMC_for_opinions (3).pdf`
The main Bachelor's Degree Thesis document. It provides a comprehensive theoretical analysis and numerical exploration of opinion models built upon classical kinetic gas theory. Key elements include:
* **Theoretical Framework:** Application of the Boltzmann equation to opinion consensus and polarization dynamics.
* **Model Variables:** Formulation of opinion models that incorporate agent-specific variables, such as external diffusion and compromise propensity, to describe social interactions.
* **Numerical Methods:** Development and implementation of Direct Simulation Monte Carlo (DSMC) algorithms for the homogeneous Boltzmann equation.

### 2. `TFG_Bruno_MCMC_for_opinions (4).pdf`
The presentation slides for the thesis defense. The slides outline the project's structure and summarize key concepts:
* **Motivation:** Connecting the microscopic, mesoscopic, and macroscopic scales of dynamics.
* **Theory:** An overview of the kinetic theory of gases and its translation to opinion dynamics.
* **Numerics:** Introduction to the Kac equation and the step-by-step logic of the Nanbu-Babovsky algorithm.
* **Summary:** Key findings from the mathematical modeling and simulations.

### 3. `MCMC(NB).ipynb`
A Jupyter Notebook designed to validate the numerical methods used in the project.
* **Goal:** Validate the Nanbu-Babovsky (NB) numerical scheme by applying it to the Kac equation.
* **Methodology:** Implements the NB scheme in Python and compares the Monte Carlo simulation solutions against exact analytical solutions across different time steps.
* **Evaluation:** Plots the simulation results for different values of $\epsilon$ alongside the asymptotic/analytical solution to demonstrate the algorithm's convergence and accuracy.

### 4. `MCMC(NB)_Opinions.ipynb`
A Jupyter Notebook simulating a kinetic model of opinion formation based on the During model.
* **System Setup:** A population of $N$ agents, each with a continuous opinion value bounded between $v \in [-1, 1]$, exchanges opinions through binary interactions.
* **Microscopic Rules:** Updates opinions based on a compromise parameter ($\gamma$), a Bounded Confidence indicator function ($P$), stochastic noise ($\eta$), and an opinion diffusion function ($D(v)$).
* **Numerical Implementation:** Uses the Nanbu-Babovsky DSMC scheme featuring specific time discretization ($\Delta t$), random pairing of agents at each step, and boundary condition clipping to ensure opinions remain bounded.
* **Experiments:** Simulates the system across varying Confidence Radii ($r$) to observe phase transitions in the social dynamics:
  * **Fragmentation:** (Small $r$) Emergence of multiple isolated clusters.
  * **Polarization:** (Medium $r$) Formation of two opposing groups.
  * **Consensus:** (Large $r$) Convergence of the population to a single shared opinion.

## Requirements
To run the Jupyter Notebooks locally, you will need **Python 3** and the following libraries installed:
* `numpy`
* `matplotlib`
* `scipy`

You can install the dependencies using pip:
```bash
pip install numpy matplotlib scipy
