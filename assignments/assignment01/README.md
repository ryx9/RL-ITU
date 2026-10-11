# Homework 1 - Multi-Armed Bandit

Reinforcement Learning, Fall 2025

## Overview

Implementation and comparison of seven exploration strategies on a 10-armed bandit problem. Each bandit arm has a true mean reward sampled from N(0,1), and rewards are sampled from N(mean, 1) at each step.

## Strategies Implemented

- **Greedy** - always picks the arm with the highest estimated value
- **Epsilon-Greedy (constant)** - explores randomly with fixed epsilon = 0.2
- **Epsilon-Greedy (linear decay)** - epsilon decreases linearly from 0.2 to 0.01
- **Epsilon-Greedy (exponential decay)** - epsilon decays multiplicatively each step
- **Optimistic Initialization** - initializes Q values to 5.0 to force early exploration
- **UCB** - picks arms using an upper confidence bound on estimated value
- **Thompson Sampling** - samples from a Gaussian posterior for each arm

## Experiment Setup

- 100 independent bandit instances per strategy
- 1000 time steps per run
- Results averaged across all runs with standard error bands

## Results

Two plots are generated inside the notebook:

1. Average reward vs time steps
2. Percentage of optimal arm selections vs time steps



## Dependencies

- numpy
- matplotlib