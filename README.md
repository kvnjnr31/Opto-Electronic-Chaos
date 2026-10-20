# opto-electronic-chaos

This repository contains modeling code and documentation for nonlinear dynamics and feedback control in bistable optoelectronic systems. Our focus is on:

- Real-time voltage data acquisition and hysteresis detection
- AI-enhanced feedback systems
- Circuit stability analysis through numerical modeling
- Integration of experimental data and predictive models
- Visualization of feedback-induced chaos and attractor transitions

## Featured analysis

**[`notebooks/optoelectronic_dynamics.ipynb`](notebooks/optoelectronic_dynamics.ipynb)** — a self-contained
analysis of the oscillator's two operating regimes from audio recordings. Builds an envelope feature table
with **pandas**/**scipy**, recovers the Period-1 vs Period-2 regimes by **unsupervised** PCA + KMeans
(scikit-learn, clean separation), and reconstructs the phase-space attractors by delay embedding. Based on
[Joiner, Palmero & Carretero-González, *Int. J. Bifurcation and Chaos* 26(05), 2016](https://doi.org/10.1142/S0218127416500802).

## Contents

- `notebooks/` – Jupyter notebooks for modeling and analysis
- `circuits/` – Circuit schematics and SPICE simulations
- `data/` – Raw and processed experimental data
- `docs/` – Documentation and research notes
- `models/` – Python models for hysteresis, resonance, and feedback dynamics

## Goals

1. Understand bistability in photodiode-laser feedback loops
2. Map hysteresis regions and switching thresholds
3. Simulate attractor evolution under parameter variation
4. Develop AI models for control and stabilization
5. Publish results and offer open research access

## License

This project is licensed under the MIT License.

---

For real-time visualizations and project status, visit: [AI Low Voltage Innovations](http://192.168.0.46:5000/)
