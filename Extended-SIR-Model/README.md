# Extended SIR Epidemiological Model

## Overview

A Python-based epidemiological simulation that extends the traditional **SIR (Susceptible-Infected-Recovered) model** by incorporating **healthcare pressure** and **nonlinear recovery rates**.

The model was developed to investigate how changes in disease transmission, hospitalisation, and healthcare capacity can influence epidemic dynamics, including scenarios where healthcare systems become overwhelmed.

## Objectives

* Simulate the spread of an infectious disease using an extended SIR model.
* Investigate the impact of different transmission and hospitalisation parameters.
* Model changes in recovery rates under healthcare pressure.
* Compare epidemic behaviour under different scenarios.
* Analyse the differences between discrete- and continuous-time simulations.

## Model

The extended model builds upon the standard SIR framework:

* **S — Susceptible:** Individuals who can become infected.
* **I — Infected:** Individuals currently infected and able to transmit the disease.
* **R — Recovered:** Individuals who have recovered from the infection.

Additional healthcare-related variables and nonlinear recovery behaviour are incorporated to represent the effects of increasing pressure on healthcare capacity.

## Methods

* Extended SIR epidemiological modelling
* Differential equations
* Discrete-time simulation
* Continuous-time simulation
* Runge-Kutta numerical methods
* Parameter sensitivity analysis
* Data visualisation

## Experiments

The simulation was conducted across different combinations of:

* Disease transmission rates
* Hospitalisation rates
* Healthcare capacity
* Recovery parameters

The resulting epidemic curves were analysed to understand how changes in these parameters affect infection peaks, recovery dynamics, and healthcare pressure.

## Results

The simulations demonstrate how healthcare capacity can influence epidemic dynamics. Under higher healthcare pressure, changes in recovery behaviour can affect the duration and severity of an outbreak.

Different parameter configurations were compared to observe how transmission and hospitalisation assumptions influence the resulting epidemic curves.

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
