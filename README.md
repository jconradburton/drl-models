# Deep Reinforcement Learning – Assignments  
**Ben-Gurion University of the Negev – Department of Software and Information Systems Engineering**  
**Course: Deep Reinforcement Learning (DRL)**  

## Overview  
This repository contains my solutions and experiments for the course assignments in Deep Reinforcement Learning. Each assignment explores a key topic in reinforcement learning, ranging from classic tabular Q-learning to more advanced deep learning techniques such as DQN and its improvements.

---

## Repository Structure

- `hw1/From_Q_Learning_to_Deep_Q_Learning.ipynb`  
  Tabular Q-Learning, DQN, and Improved DQN (Assignment 1)

- `hw2/Monte_Carlo_Policy_Gradients.ipynb`  
  REINFORCE and REINFORCE with baseline algorithms (Assignment 2)

- `hw2/Advantage_Actor_Critic.ipynb`  
  Advantage Actor-Critic (Assignment 2)

- `hw3/Training_Individual_Networks.ipynb`  
  Actor-Critic on additional environments (Assignment 3)

- `hw3/` (coming soon)
  
- `hw3/` (coming soon)


---

## Assignment 1 – From Q-learning to Deep Q-learning

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

## Assignment 2 – Policy Gradient Methods

### Section 1 – Monte Carlo Policy Gradient (REINFORCE)
- Environment: `CartPole-v1`
- Implements the REINFORCE algorithm for direct policy optimization
- Two versions developed:
  - Basic REINFORCE using the return from each episode
  - REINFORCE with a baseline (value function approximation) to compute the advantage
- Includes:
  - Policy network with softmax output
  - Value function network for baseline estimation
  - Gradient ascent updates with variance reduction
  - Evaluation and comparison of both versions in terms of convergence speed and stability

### Section 2 – Advantage Actor-Critic (A2C)
- Environment: `CartPole-v1`
- Implements the Actor-Critic algorithm using:
  - Actor network to model the policy
  - Critic network to approximate state-value function
- Uses the TD error as an approximation for the advantage estimate, enabling online updates
- Includes:
  - Modified training loop with TD target
  - Shared and separate network structures explored
  - Performance comparison with both REINFORCE variants
  - Plots of training rewards and value function estimates

---

## Assignment 3 – Meta and Transfer Learning

### Section 1 – Training Individual Networks
- Environments: `CartPole-v1`, `Acrobot-v1`, `MountainCarContinuous-v0`
- Extended the actor-critic architecture from HW2 to each environment individually
- Standardized input and output dimensions across tasks using:
  - Input padding (with zeros)
  - Output padding (with unused "dummy" actions)
- Includes:
  - Separate networks with at least one hidden layer each
  - Training time and convergence statistics for each environment

### Section 2 – Fine-Tuning a Pretrained Model
- Performed transfer learning by fine-tuning a model trained on one task for another
- Pairs: `Acrobot → CartPole`, `CartPole → MountainCar`
- Method:
  - Reused pretrained weights from the source model
  - Reinitialized output layer for the target environment
- Includes:
  - Training stats and comparison to training from scratch
  - Analysis of whether fine-tuning led to faster convergence

### Section 3 – Progressive Networks for Transfer Learning
- Implemented a simplified version of Progressive Networks
- Transfer learning settings:
  - `{Acrobot, MountainCar} → CartPole`
  - `{CartPole, Acrobot} → MountainCar`
- Used frozen source networks and connected them to a fresh target network
- Includes:
  - Training architecture and layer-matching explanation
  - Statistics on training iterations and time
  - Evaluation of whether transfer learning improved convergence

---
