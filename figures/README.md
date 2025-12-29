# StructOpt — Stability Layer for First-Order Optimization

StructOpt is a trajectory-based stability module designed to improve the robustness
of first-order optimization methods under challenging curvature and learning-rate regimes.

Rather than optimizing for speed, StructOpt focuses on stabilizing optimization dynamics
by reacting to how gradients change along the actual optimization trajectory.

## What is demonstrated here

This repository presents a stability stress-test on an ill-conditioned quadratic objective.
The test evaluates optimizer behavior across several orders of magnitude of learning rates.

![Stability stress-test](myplot8.png)

An optimizer is marked as stable if it converges without divergence or sustained oscillations.

StructOpt remains stable across the entire tested learning-rate range, while standard
first-order methods (SGD, Adam) diverge outside narrow tuning intervals.



## Intended use

StructOpt is intended to function as a modular stability layer that can be integrated
into existing first-order optimizers to widen their stable operating regime.

## Status

This repository focuses on illustrating the stability property.
Code and extended benchmarks may be released separately.
