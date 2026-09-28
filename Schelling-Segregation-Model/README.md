# Extended Schelling's Segregation Model

## Overview

A Python-based **agent-based simulation** that extends Schelling's Segregation Model to investigate how individual location preferences and stochastic relocation can produce emergent patterns of segregation.

The model incorporates **Markov Chains** and **Monte Carlo simulation** to study how different parameters and relocation behaviours influence the evolution of segregation over time.

## Objectives

* Simulate residential segregation using an agent-based model.
* Investigate how individual location preferences influence overall segregation.
* Incorporate stochastic relocation into the simulation.
* Analyse how different parameter settings affect emergent patterns.
* Evaluate the consistency of simulation results across multiple trials.

## Model

The simulation represents individuals as agents located within a grid-based environment.

Each agent evaluates its surrounding neighbourhood based on its location preferences. Agents that are dissatisfied with their current environment may relocate to another available location.

The extended model introduces stochastic behaviour to capture the uncertainty involved in relocation decisions and the resulting emergence of segregation patterns.

## Methods

* Agent-Based Modelling
* Schelling's Segregation Model
* Markov Chains
* Monte Carlo Simulation
* Stochastic Modelling
* Parameter Sensitivity Analysis
* Statistical Analysis

## Experiments

More than **50 simulation trials** were conducted using different parameter configurations.

The experiments investigated the effects of factors such as:

* Agent location preferences
* Relocation behaviour
* Neighbourhood composition
* Simulation parameters
* Randomness in agent movement

Simulation outputs were compared across different parameter settings to identify changes in segregation patterns and system behaviour.

## Results

The simulations demonstrate how relatively simple individual preferences and relocation decisions can produce **emergent segregation patterns** at the population level.

Results were analysed using time-series plots, heatmaps, and distribution visualisations to examine how segregation evolved throughout the simulations.

## Visualisation

The simulation results were visualised using:

* Time-series plots
* Heatmaps
* Histograms
* KDE-based distribution plots

## Technologies

* Python
* NumPy
* Matplotlib
* Seaborn

## Files

```text
Schelling-Segregation-Model/
├── README.md
├── 33986010_FIT3139_Final_Project.ipynb
├── 33986010_FIT3139_Final_Project_Report.pdf
└── 33986010_FIT3139_Final_Project_Slides.pdf/
```

## Academic Context

Developed as part of the **Computational Modelling and Simulation** unit.
