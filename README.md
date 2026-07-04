# Primordial Black Hole Evolution Simulator

A Python project for studying the mass evolution of primordial black holes (PBHs) under Hawking evaporation and cosmological accretion.

The goal is to start from a simple toy model and progressively incorporate more realistic physics.

---

# Motivation

Primordial black holes may have formed in the early universe from the collapse of large density fluctuations.

Once formed, they evolve through two competing processes:

1. Hawking evaporation (mass loss)
2. Accretion of surrounding matter and radiation (mass gain)

The balance between these mechanisms determines:

- PBH lifetime
- Present-day mass distribution
- Contribution to dark matter
- Cosmological constraints

This project aims to build a simulator capable of tracking that evolution.

---

# Physics Background

The evolution equation is

dM/dt = Accretion - Evaporation

where:

M = black hole mass

The simplest possible model is

dM/dt = A M² ρ(t) - B/M²

where

A = accretion coefficient
B = evaporation coefficient
ρ(t) = cosmic energy density

The first term increases mass.

The second term decreases mass.

---

# Project Roadmap

## Phase 1 - Hawking Evaporation Only

### Goal

Simulate a black hole losing mass through Hawking radiation.

### Equation

dM/dt = -B/M²

### Tasks

- Create PBH class
- Solve differential equation numerically
- Plot mass versus time
- Determine evaporation time

### Deliverables

- Single PBH evolution
- Mass history plot
- Lifetime calculation

### Questions

- Which initial masses survive until today?
- Which masses evaporate before BBN?
- Which masses evaporate before recombination?

---

## Phase 2 - Add Cosmological Accretion

### Goal

Include mass growth from the surrounding universe.

### Equation

dM/dt = A M² ρ(t) - B/M²

### Tasks

Implement:

```python
rho_radiation(t)
rho_matter(t)
