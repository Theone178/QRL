# Quantum Reinforcement Learning: "The Wall Drop"

## Overview
This project extends Dong et al.'s Quantum Reinforcement Learning (QRL) framework by introducing "The Wall Drop"-a dynamic 5x5 gridworld environment that shifts mid-training. The primary objective is to evaluate the agent's resistance to catastrophic forgetting when the optimal path suddenly changes. 

## Tech Stack
* **Language:** Python
* **Quantum Framework:** Google Cirq
* **Domain:** Reinforcement Learning (RL)

## Key Algorithmic Upgrades
To optimize the quantum agent's adaptability and training stability, the baseline framework was upgraded with several enhancements:
* **Prioritised Experience Replay (PER):** Improves sample efficiency by prioritizing significant transitions.
* **N-Step Returns (n=3):** Bootstraps multi-step rewards for faster credit assignment.
* **Adaptive Grover $\beta$ Decay:** Dynamically scales the quantum operator for optimal amplitude amplification.
* **Amplitude Warm-Start:** Blends partial knowledge during resets to accelerate recovery.
* **Double-Q Updates:** Prevents overestimation bias during action selection.
* **Annealed Reward Shaping & Vectorised Penalties:** Fades shaping weights as the policy matures to avoid sub-optimal fixation, alongside vectorized penalties for wall collisions.

## Performance Benchmarking
The upgraded QRL agent was rigorously benchmarked against a classical Q-learning baseline across **25 runs x 150 episodes** 

* **QRL Post-Shift Win Rate:** 96.6%
* **Classical Post-Shift Win Rate:** 94.8%
* **Result:** The quantum agent demonstrated a **1.9 percentage point higher win rate**, indicating superior robustness against catastrophic forgetting in dynamic environments.

## Repository Structure
* `RL.ipynb`: Main Google Colab notebook containing the environment transition logic (`env_step`), agent architecture, and training loop.

## Getting Started
1. Clone this repository:
   ```bash
   git clone [https://github.com/Theone178/QRL.git](https://github.com/Theone178/QRL.git)
