# Typed-Logical-Interface-for-Quantum

Companion repository for **A Typed Logical Interface for Quantum-Oracular k-Center**.

## Repository roles

This repository is intentionally split into three layers.

1. **Lean (`lean/`)** — proof-oriented artifact  
   This directory contains the Lean 4 formalization scaffold for the typed calculus, typing rules,
   trace semantics, compilation layer, and farthest-first case-study structure.

2. **Python (`python/`)** — reproducibility artifact  
   This directory contains scripts that generate the paper's illustrative figures such as the
   radius sweep curve and the oracle-trace heatmap.

3. **Quantum simulation (`quantum_sim/`)** — backend illustration  
   This directory contains lightweight simulation scripts that illustrate bounded-error distance
   estimation and candidate-search ideas at the backend layer. These scripts are demonstrations,
   not the formal proof artifact.

## Suggested citation text for the paper

> A companion artifact is available at this repository. It contains the Lean 4 formalization of
> the core typed calculus, typing rules, trace semantics, compilation layer, and proof-oriented
> case-study files. It also contains Python code for figure generation and supplementary
> quantum-backend simulation scripts used for reproducible demonstrations.

## Directory layout

```text
Typed-Logical-Interface-for-Quantum/
├── README.md
├── paper/
├── lean/
│   ├── lakefile.toml
│   ├── lean-toolchain
│   └── TypedKCenter/
├── python/
├── quantum_sim/
├── figures/
└── docs/
```

## Quick start

### Lean
```bash
cd lean
lake build
```

### Python figures
```bash
cd python
python generate_all_figures.py
```

Generated figures are written to `../figures/`.

### Quantum simulations
```bash
cd quantum_sim
python backend_demo.py
python inner_product_estimation_demo.py
python minimum_finding_toy_demo.py
```

## Notes

- The Lean files are organized as a clean proof-development scaffold matching the paper's formal sections.
- The Python figure scripts are meant to reproduce illustrations, not to serve as empirical evidence.
- The quantum simulation scripts are backend-oriented demos that illustrate contract-style bounded-error behavior.
