# Extended Schelling's Segregation Model

## Overview

A Python-based **agent-based simulation** that extends Schelling's Segregation Model to investigate how individual location preferences and stochastic relocation can produce emergent patterns of segregation. The project extends the original model in two ways: agents also care about where they live (a desirable location, like a city centre), and they sometimes move at random.

The model incorporates **Markov Chains** and **Monte Carlo simulation** to study how different parameters and relocation behaviours influence the evolution of segregation over time.

<img width="977" height="486" alt="image" src="https://github.com/user-attachments/assets/9f348e00-0ff8-4cc1-878f-3207a117a4b1" />

## Objectives

1. **Recreate** the original Schelling model and see how segregation emerges.
2. **Add a location preference**, so agents are drawn towards a desirable spot on the grid.
3. **Incorporate stochastic relocation (random moves)** so agents sometimes relocate for reasons unrelated to their neighbours.
4. **Run many simulations** to see how randomness and location preference affect segregation and happiness.

## The Model

The simulation places individuals as agents on a **30 × 30 grid**, split into two types (A and B), with some cells left empty. Each agent looks at its **8 surrounding neighbours** and at how close it is to a desirable location, and combines the two into a happiness score:

$$
\text{happiness} = \underbrace{\frac{\text{similar neighbours}}{\text{total neighbours}}}_{\text{neighbourhood}} + \underbrace{\frac{\alpha}{1 + d}}_{\text{location}}
$$

  where $d$ is the distance to the desirable location (grid centre) and $\alpha$ controls how much location matters.
- If happiness falls below the **threshold** (0.3), or a random move is triggered with probability $p$, the agent moves to a random empty cell.
- The **segregation index** is the average fraction of same-type neighbours across all agents (higher means more segregated).

| Parameter | Meaning | Value(s) |
|---|---|---|
| Threshold | Minimum happiness to stay put | 0.3 |
| $\alpha$ | Weight of location preference | 0, 0.3 |
| $p$ | Probability of a random move | 0, 0.01, 0.05, 0.10, 0.20 |
| Trials | Monte Carlo repetitions | 20–50 |


## Methods

* Agent-Based Modelling
* Schelling's Segregation Model
* Markov Chains
* Monte Carlo Simulation
* Stochastic Modelling
* Parameter Sensitivity Analysis
* Statistical Analysis

## Key Findings

- **Segregation emerges quickly.** Even with a low threshold of 0.3, the segregation index roughly doubles (about 0.35 to 0.69) within about 20 steps.
<img width="790" height="490" alt="image" src="https://github.com/user-attachments/assets/44cfb337-e63b-4eab-a384-fc6416239648" />
- **Randomness breaks up segregation.** As the random-move probability rises from 0.01 to 0.20, segregation falls from about 0.69 to 0.37, close to the random starting level.
- **Randomness also adds uncertainty.** With random moves, results vary more between runs and never fully settle.
- **Location preference raises happiness.** With $\alpha = 0.3$, agents' happiness scores shift higher and spread out, because living near the desirable spot adds a bonus.
  <img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/7044579e-103a-48a8-95fc-4cf9d290798e" />


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
├── Schelling-Segregation-Model.ipynb
├── Schelling-Segregation-Model-Slides.pdf
└── Schelling-Segregation-Model-Report.pdf/
```

## Academic Context

Developed as part of the **Computational Modelling and Simulation** unit.
