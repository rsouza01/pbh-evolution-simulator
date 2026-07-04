# Primordial Black Hole Evolution Simulator

A modular Python framework for studying the formation, evolution, evaporation, accretion, clustering, merger history, and cosmological consequences of primordial black holes (PBHs).

The project begins with a single primordial black hole and gradually evolves into a complete research-oriented sandbox for exploring the PBH dark matter hypothesis.

---

# Scientific Goals

This project aims to answer questions such as:

- Which primordial black holes survive until today?
- How important is Hawking evaporation?
- Can accretion significantly increase PBH masses?
- Could PBHs account for all dark matter?
- How do PBH mass distributions evolve with time?
- What observational constraints exclude specific models?
- What inflationary scenarios produce PBHs?
- What gravitational-wave signatures emerge from PBH populations?

---

# Development Philosophy

Every phase introduces exactly one new piece of physics.

At the end of each phase:

- results must be reproducible
- numerical solutions should be validated
- visualizations should be produced
- tests should pass

The goal is scientific software, not merely a coding exercise.

---

# Phase 1 — Hawking Evaporation

## Physics

A black hole loses mass through Hawking radiation:

dM/dt = -B/M²

where:

- M = black hole mass
- B = evaporation coefficient

---

## Objectives

Implement:

```python
PBH(mass)
```

Numerically solve:

```python
pbh.evolve()
```

Generate:

- mass vs time
- remaining lifetime
- evaporation event

---

## Validation

Compare numerical results to the exact solution:

M(t)³ = M₀³ - 3Bt

---

# Phase 2 — Accretion

## Physics

Add mass growth from the surrounding universe:

dM/dt = A M² ρ(t) - B/M²

---

## Objectives

Implement:

- radiation accretion
- matter accretion
- configurable efficiencies

Compare:

- evaporation dominated cases
- accretion dominated cases

---

# Phase 3 — Cosmological Background

## Physics

Model universe expansion.

Introduce:

- scale factor a(t)
- Hubble parameter H(t)
- energy density evolution

Radiation:

ρ ∝ a⁻⁴

Matter:

ρ ∝ a⁻³

---

## Objectives

Implement:

```python
Universe()
```

with functions:

```python
rho(t)
a(t)
H(t)
```

PBHs should evolve inside a realistic cosmological background.

---

# Phase 4 — Multiple PBHs

## Physics

Move beyond single objects.

Create populations of PBHs.

---

## Objectives

Generate:

- monochromatic distributions
- log-normal distributions
- power-law distributions

Example:

```python
population = Population(...)
```

Compute:

- mean mass
- surviving mass fraction
- population statistics

---

# Phase 5 — Dark Matter Fraction

## Physics

Determine how much dark matter is composed of PBHs.

Define:

fPBH = ΩPBH / ΩDM

---

## Objectives

Track:

- initial abundance
- evolving abundance
- present abundance

Visualize:

- fPBH(t)
- total surviving density

---

# Phase 6 — Constraint Engine

## Physics

Many observations constrain PBHs.

---

## Objectives

Implement exclusion regions from:

### Evaporation

- gamma rays
- neutrinos
- cosmic rays

### Microlensing

- MACHO
- EROS
- OGLE

### CMB

- accretion signatures
- ionization history

### Dynamical Constraints

- globular clusters
- dwarf galaxies

Output:

```python
constraint_plot()
```

Generate PBH exclusion diagrams.

---

# Phase 7 — PBH Formation

## Physics

Connect inflation to PBHs.

Start from:

P(k)

the primordial power spectrum.

---

## Objectives

Implement:

- horizon crossing
- density perturbations
- collapse threshold

Compute:

β(M)

initial PBH abundance.

---

# Phase 8 — Critical Collapse

## Physics

PBH masses are not necessarily equal to horizon mass.

Near collapse threshold:

M ∝ (δ-δc)^γ

---

## Objectives

Generate realistic PBH mass spectra.

Explore:

- threshold behavior
- critical exponents

Compare with monochromatic approximations.

---

# Phase 9 — Non-Gaussian Fluctuations

## Physics

Primordial perturbations may not follow Gaussian statistics.

---

## Objectives

Implement:

- skewness
- kurtosis
- local fNL

Explore impact on:

- PBH abundance
- mass spectra

---

# Phase 10 — PBH Clustering

## Physics

PBHs may not be uniformly distributed.

---

## Objectives

Implement:

- two-point correlation functions
- clustered populations
- density maps

Study effects on:

- mergers
- observability

---

# Phase 11 — PBH Binary Formation

## Physics

Nearby PBHs may form gravitationally bound binaries.

---

## Objectives

Implement:

```python
Binary(pbh1, pbh2)
```

Compute:

- orbital parameters
- merger times

Generate merger-rate predictions.

---

# Phase 12 — Gravitational Waves

## Physics

PBH binaries produce gravitational waves.

---

## Objectives

Predict distributions of:

- chirp masses
- merger rates
- redshift evolution

Compare with:

- LIGO
- Virgo
- KAGRA

Generate synthetic catalogs.

---

# Phase 13 — N-Body Dynamics

## Physics

Model gravitational interactions among many PBHs.

---

## Objectives

Implement:

- direct N-body
- Barnes-Hut tree method

Study:

- clustering
- halo formation
- binary creation

---

# Phase 14 — Early Matter Domination

## Physics

Some models predict a temporary matter-dominated era before BBN.

---

## Objectives

Implement alternative expansion histories.

Study effects on:

- PBH formation
- accretion
- merger rates

---

# Phase 15 — Extended Evaporation Physics

## Physics

Move beyond the simplest Hawking model.

---

## Objectives

Include:

- particle species thresholds
- greybody factors
- spin dependence
- charged PBHs

---

# Phase 16 — Rotating PBHs

## Physics

Real PBHs may possess angular momentum.

---

## Objectives

Implement Kerr black holes.

Track:

- mass
- spin

Model spin evolution.

---

# Phase 17 — Alternative Cosmologies

## Objectives

Allow exploration of:

- modified gravity
- scalar-tensor theories
- extra dimensions
- bouncing cosmologies

---

# Phase 18 — Research Pipeline

## Final Goal

The framework should support:

Inflation Model
↓
Power Spectrum
↓
PBH Formation
↓
Population Evolution
↓
Accretion
↓
Evaporation
↓
Clustering
↓
Mergers
↓
Observational Constraints

---

# Suggested Repository Structure

project/

├── pbh/

│   ├── blackhole.py

│   ├── evaporation.py

│   ├── accretion.py

│   ├── formation.py

│   ├── binaries.py

│   ├── mergers.py

│   ├── clustering.py

│   ├── constraints.py

│   ├── gravitational_waves.py

│   └── cosmology.py

├── notebooks/

├── figures/

├── tests/

├── docs/

└── examples/

---

# Minimum Viable Product

The first usable release should support:

✅ Hawking evaporation

✅ Cosmological accretion

✅ Multiple PBHs

✅ Dark matter fraction calculation

✅ Publication-quality plots

Everything beyond this can be viewed as progressively turning the project into a genuine computational cosmology laboratory.
