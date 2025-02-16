# Reinforcement Learning-Based Surge Pricing Simulation

## Overview
This repository contains a **Reinforcement Learning (Q-learning)** based simulation for modeling **surge pricing** and driver allocation in a multi-route transportation network. The project simulates how **drivers (agents) choose routes**, how **surge pricing adjusts dynamically**, and how **drivers learn over time** to maximize their earnings.

The key objective is to analyze the **emergent pricing patterns, driver distribution, and reward optimization** in a dynamic transportation system.

## Features
- **Multi-Agent Reinforcement Learning**: Each driver (agent) uses **Q-learning** to optimize their route selection based on historical earnings.
- **Dynamic Surge Pricing**: Fares adjust based on supply-demand imbalances, simulating real-world surge pricing.
- **Exploration-Exploitation Tradeoff**: Uses **epsilon-greedy policy** to balance **exploration** (trying new routes) and **exploitation** (choosing the most profitable routes).
- **Data Visualization**: Generates insights through plots on:
  - Driver distribution across routes.
  - Evolution of Q-values (profitability estimates).
  - Surge pricing trends.
  - Average earnings per route.

## Simulation Parameters
The following parameters can be adjusted to explore different scenarios:

| Parameter       | Description                                         | Default Value |
|----------------|-----------------------------------------------------|--------------|
| `num_routes`   | Number of available routes                         | 10           |
| `num_drivers`  | Number of drivers (RL agents)                      | 20,000       |
| `total_riders` | Total number of riders across all routes           | 300          |
| `iterations`   | Number of simulation iterations                    | 100          |
| `base_price`   | Base fare for a route                              | 10.0         |
| `k`           | Surge sensitivity parameter                         | 0.1          |
| `alpha`        | Learning rate for Q-value updates                  | 0.1          |
| `epsilon`      | Exploration rate (epsilon-greedy policy)           | 0.1          |

## How It Works
1. **Initialize Q-values:** Each driver starts with zero knowledge about route profitability.
2. **Driver Route Selection:** Each driver selects a route based on an **epsilon-greedy strategy**.
3. **Supply and Demand Calculation:** The simulation calculates the **number of drivers per route**.
4. **Surge Pricing Calculation:** If demand exceeds supply, fares increase using a **surge multiplier**.
5. **Reward Calculation:** Driver earnings are updated based on route price and competition.
6. **Q-Learning Update:** Drivers update their Q-values using the **reward feedback**.
7. **Iteration & Learning:** The process repeats, allowing drivers to **learn profitable strategies** over time.
8. **Data Visualization:** Key metrics are plotted to understand learning dynamics.

## Installation & Usage
### **Prerequisites**
- Python 3.x
- NumPy
- Matplotlib

### **Installation**
Clone the repository:
```sh
git clone https://github.com/viznuv/Pricing_models_dynamic.git
cd Pricing_models_dynamic
