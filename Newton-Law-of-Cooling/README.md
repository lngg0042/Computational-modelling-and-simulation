# Newton's Law of Cooling Simulation

## Overview
A Python-based simulation of Newton's Law of Cooling, developed as part of a Computational Modelling and Simulation project.

The project investigates how **ambient temperature** and **cooling rate** influence the temperature of an object over time. It also examines numerical accuracy in a restricted computing environment by using **Taylor series approximations** and analysing **floating-point errors** introduced when values are stored with only **3-digit precision**.

## Objectives
Build a numerical model for a client whose hardware is limited. The project sets out to:

1. **Model the phenomenon exactly**: simulate Newton's Law of Cooling and study how the cooling rate ($k$) and ambient temperature ($T_{env}$) change the system's behaviour.
2. **Measure modelling error**: see how much accuracy is lost when $e^{-kt}$ is replaced by a truncated Taylor series.
3. **Measure data error**: see how limited floating-point precision (chopping to 3 significant digits) affects the results.
4. **Assess total error**: combine both error sources to judge how reliable the model is under realistic hardware limits.
5. **Find where the model can be trusted**: use approximate and exact condition numbers to identify the well-conditioned and ill-conditioned regions, and advise users on when to trust the output.

## Methods
* Exponential modelling
* Taylor series approximation
* Numerical error analysis
* Computational simulation
* Data visualisation

## Technologies
* Python
* NumPy
* Matplotlib

## Key findings
- **Higher** $k$ or **lower** $T_{env}$ makes the object cool faster.
- The **Taylor approximation** works only for short time spans. Error grows with $t$ and with $k$.
- **3-digit chopping** adds small errors that accumulate and show up as visible fluctuations at larger $t$.
- **Combined errors** turn the smooth exponential decay into a roughly linear, noisy curve.
- The **condition number** is small at first, rises while the temperature is changing quickly, and then levels off. For $k = 0.1$ it peaks at about 12 minutes. Results are most reliable where $CN \le 1$.

## Files
```text
Newton-Law-of-Cooling/
├── README.md
├── cooling_simulation.ipynb
└── cooling_simulation_brief.pdf
```

## Academic Context
Developed as part of the **Computational Modelling and Simulation** unit.
