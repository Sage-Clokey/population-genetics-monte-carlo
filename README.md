# Population Genetics Monte Carlo Simulator

A Wright-Fisher population genetics simulator using Monte Carlo methods to model allele frequency dynamics across thousands of generations. Explores the interplay between **genetic drift**, **selection pressure**, and **initial allele frequency** across different population sizes.

## What This Does

Simulates allele frequency trajectories across 10,000 generations under the Wright-Fisher model — the standard framework for modeling how gene variants spread or disappear in finite populations.

Two population sizes are compared:
- **N = 10,000 individuals** — large population where selection dominates
- **N = 500 individuals** — small population where genetic drift dominates

Three initial allele frequencies are tested at each population size:
- **p₀ = 0.1** — rare allele, starting from low frequency
- **p₀ = 0.5** — neutral start, equal frequency
- **p₀ = 0.9** — common allele, starting from high frequency

## Key Biological Insight

At small population sizes (N=500), **random genetic drift overwhelms selection pressure**. Alleles fix or go extinct not because of fitness — but because of chance. At large population sizes (N=10,000), trajectories are smoother and selection has room to act.

This demonstrates one of the most counterintuitive results in evolutionary biology: **evolution is not purely optimization**. It is optimization plus noise, weighted by population size.

## Repository Contents

| File Pattern | Description |
|---|---|
| `*AF_rawdata.csv` | Raw allele frequency trajectory data per simulation run |
| `*.pdf` | Visualization plots of allele frequency over 10,000 generations |
| `*.html` | Interactive visualization (500 individuals, p₀ = 0.5) |

File naming convention: `{N}ind_{G}gen_{p0}AF`
- `10Kind` = N of 10,000 individuals
- `500ind` = N of 500 individuals
- `10Kgen` = 10,000 generations
- `0p1` / `0p5` / `0p9` = initial allele frequency (0.1, 0.5, 0.9)

## Background

The **Wright-Fisher model** assumes:
- Discrete, non-overlapping generations
- Fixed population size N
- Random sampling of 2N alleles each generation
- No mutation, migration, or recombination (unless specified)

**Genetic drift** is the random fluctuation in allele frequency due to finite population size. Its strength is inversely proportional to N — the smaller the population, the more powerful the drift.

## Related Projects

- [genetic-drift-simulator](https://github.com/sage-clokey/genetic-drift-simulator) — Interactive Python simulator with real-time visualization
- [spiral-steward-website](https://github.com/sage-clokey/spiral-steward-website) — Broader living systems research platform

## Author

**Sage Clokey** — [sage-clokey.github.io](https://sage-clokey.github.io)
