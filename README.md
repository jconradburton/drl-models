# Deep Reinforcement Learning – Homework Assignments  
**Ben-Gurion University of the Negev – Department of Software and Information Systems Engineering**  
**Course: Deep Reinforcement Learning (DRL)**  

## Overview  
This repository contains my solutions and experiments for the course assignments in Deep Reinforcement Learning. Each assignment explores a key topic in reinforcement learning, ranging from classic tabular Q-learning to more advanced deep learning techniques such as DQN and its improvements.

---

## 📁 Repository Structure

- `From_Q_Learning_to_Deep_Q_Learning.ipynb`  
  Covers the full Assignment 1:  
  - Tabular Q-learning on FrozenLake  
  - Deep Q-Learning (DQN) on CartPole-v1  
  - Improved DQN
  Includes code, explanations, hyperparameter tuning, plots, and performance results.

- `hw2/` *(coming soon)*  
  [Placeholder for Assignment 2]

- `hw3/` *(coming soon)*  
  [Placeholder for Assignment 3]

---

## 🧠 Assignment 1 – From Q-learning to Deep Q-learning

### Section 1 – Tabular Q-Learning
- Environment: `FrozenLake-v0`
- Implemented from scratch using a Q-table
- Uses epsilon-greedy with decay
- Includes:
  - Optimized hyperparameters  
  - Reward and step plots  
  - Q-value table snapshots and visualizations  


### Section 2 – Deep Q-Learning (DQN)
- Environment: `CartPole-v1`
- Uses a neural network to approximate Q-values
- Techniques:
  - Experience Replay  
  - Target Network  
- Includes:
  - Two tested NN architectures  
  - Training plots and loss metrics  
  - Evaluation results  

### Section 3 – Improved DQN
- Extends DQN with a state-of-the-art improvement
- Includes:
  - Explanation of the improvement  
  - Results comparison with basic DQN  
  - Plots and performance summary  

---
