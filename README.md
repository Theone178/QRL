# Quantum Reinforcement Learning: "The Wall Drop"

## Overview
This project extends Dong et al.'s Quantum Reinforcement Learning (QRL) framework by introducing "The Wall Drop"—a dynamic 5x5 gridworld environment that shifts mid-training[cite: 1, 3, 6]. The primary objective is to evaluate the agent's resistance to catastrophic forgetting when the optimal path suddenly changes[cite: 1, 3]. 

## Tech Stack
* **Language:** Python[cite: 1, 3]
* **Quantum Framework:** Google Cirq[cite: 1, 3]
* **Domain:** Reinforcement Learning (RL)[cite: 1, 3]

## Key Algorithmic Upgrades
To optimize the quantum agent's adaptability and training stability, the baseline framework was upgraded with several enhancements[cite: 1, 3, 6]:
* **Prioritised Experience Replay (PER):** Improves sample efficiency by prioritizing significant transitions[cite: 1, 3, 6].
* **N-Step Returns (n=3):** Bootstraps multi-step rewards for faster credit assignment[cite: 1, 3, 6].
* **Adaptive Grover $\beta$ Decay:** Dynamically scales the quantum operator for optimal amplitude amplification[cite: 1, 3, 6].
* **Amplitude Warm-Start:** Blends partial knowledge during resets to accelerate recovery[cite: 1, 3, 6].
* **Double-Q Updates:** Prevents overestimation bias during action selection[cite: 1, 3, 6].
* **Annealed Reward Shaping & Vectorised Penalties:** Fades shaping weights as the policy matures to avoid sub-optimal fixation, alongside vectorized penalties for wall collisions[cite: 1, 3, 6].

## Performance Benchmarking
The upgraded QRL agent was rigorously benchmarked against a classical Q-learning baseline across **25 runs x 150 episodes**[cite: 1, 3]. 

* **QRL Post-Shift Win Rate:** 96.6%[cite: 1, 3]
* **Classical Post-Shift Win Rate:** 94.8%[cite: 1, 3]
* **Result:** The quantum agent demonstrated a **1.9 percentage point higher win rate**, indicating superior robustness against catastrophic forgetting in dynamic environments[cite: 1, 3].

## Repository Structure
* `RL.ipynb`: Main Google Colab notebook containing the environment transition logic (`env_step`), agent architecture, and training loop[cite: 4, 6].

## Getting Started
1. Clone this repository:
   ```bash
   git clone [https://github.com/Theone178/QRL.git](https://github.com/Theone178/QRL.git)
