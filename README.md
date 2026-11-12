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

## Circuit modeling notebooks

Compact-model studies of the laser / BPW34 photodiode / 2N3904 / OPA380 feedback board. Each notebook runs
from a project root set by the `TWIN_PROJECT_ROOT` environment variable (defaulting to the current directory);
the raw experimental data they reference is not part of this public repository.

- **[`notebooks/two_loop_base_capacitor_study.ipynb`](notebooks/two_loop_base_capacitor_study.ipynb)** — two
  cross-coupled laser/photodiode boards with a 1 MΩ ∥ 100 nF feedback branch. The compact model gives
  alternating pulses near a 15.5 µs period (~64.5 kHz); an added base-ground capacitor is not required.
  Reported as a conditional, initial-condition-dependent model prediction, not experimental confirmation.
- **[`notebooks/nightlight_rc_equivalent_blocks.ipynb`](notebooks/nightlight_rc_equivalent_blocks.ipynb)** —
  exact nonlinear RC coordinate transformations that reproduce the reference thermal equation to ~1e-6 K,
  plus emitter-storage delay, DC/AC drive and sampling-artifact checks.
- **[`notebooks/EXPERIMENT_LOG.md`](notebooks/EXPERIMENT_LOG.md)** — consolidated log of the modeling
  attempts, retained and removed, with their main saved results and limitations.

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
