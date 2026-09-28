# Extended SIR Epidemiological Model

## Overview

A Python-based epidemiological simulation that extends the traditional **SIR (Susceptible-Infected-Recovered) model** by incorporating **healthcare pressure** and **nonlinear recovery rates**.

The model was developed to investigate one question: *What happens when hospitals are overwhelmed and recovery slows down?* By varying disease transmission, hospitalisation, and healthcare capacity, the model shows how an overloaded healthcare system changes the course of an outbreak.

## Objectives

1. **Extend the SIR model** by adding a hospital population \(H\), where recovery rates decrease as hospital occupancy increases.
2. **Simulate the model in discrete time** to study how hospital strain, admission rates, and key parameters affect the outbreak.
3. **Simulate the model in continuous time** across small, medium, and severe outbreaks and different parameter settings.
4. **Analyse the long-term behaviour of the epidemic**, including its steady states and stability, to determine whether the outbreak dies out or can persist over time.

## Model

$$
\begin{aligned}
\frac{dS}{dt} &= -\beta S I \\
\frac{dI}{dt} &= \beta S I - \gamma(H)\, I \\
\frac{dR}{dt} &= \gamma(H)\, I \\
\frac{dH}{dt} &= \rho I - \eta H \\
\gamma(H) &= \frac{\gamma_0}{1 + \alpha H}
\end{aligned}
$$

| Symbol | Meaning |
|---|---|
| $S, I, R$ | Susceptible, infected, recovered fractions |
| $H$ | Hospitalised fraction (hospital load) |
| $\beta$ | Transmission rate |
| $\gamma_0$ | Baseline recovery rate |
| $\alpha$ | Hospital pressure sensitivity (higher means faster healthcare collapse) |
| $\rho$ | Fraction of infected who are hospitalised |
| $\eta$ | Hospital discharge rate |

**Assumptions:** closed population, fixed hospitalisation fraction $\rho$, constant discharge rate $\eta$, recovery depends only on $H$, and recovered individuals are permanently immune.

---

## Methods

* Extended SIR epidemiological modelling
* Differential equations
* Discrete-time simulation
* Continuous-time simulation
* Runge-Kutta numerical methods
* Parameter sensitivity analysis
* Data visualisation

## Key Findings

- **Higher $\alpha$** (hospitals collapse faster) gives higher infection peaks and a longer epidemic.
- **Higher $\rho$** sends more people to hospital, which spikes $H$ and slows recovery.
- Strong hospital feedback can **delay and amplify** the infection peak and even cause second waves.
- The only realistic equilibrium is **disease-free**. It is stable when $\beta S < \gamma_0$ and unstable when $\beta S > \gamma_0$, where a small infection can restart an outbreak.
- **Takeaway:** hospital capacity is critical in large outbreaks. An overloaded "lifeboat" makes the whole epidemic worse.

## Technologies

* Python
* NumPy
* SciPy
* Matplotlib

## Files

```text
Extended-SIR-Model/
├── README.md
├── FIT3139_Assignment2.ipynb
├── FIT3139_Assignment2_Brief.pdf
```

## Academic Context

Developed as part of the **Computational Modelling and Simulation** unit.
