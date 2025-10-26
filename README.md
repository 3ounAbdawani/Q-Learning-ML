# Q-Learning Grid World

This Jupyter Notebook implements a Q-Learning algorithm to solve a grid world navigation problem with obstacles.

## Overview

The project demonstrates reinforcement learning concepts through a simple grid-based environment where an agent learns to navigate from a start position to a goal while avoiding obstacles.

## Features

- **5x5 Grid Environment** with customizable start, goal, and obstacle positions
- **Q-Learning Implementation** with configurable hyperparameters
- **Visualization** of agent movement and learning progress
- **Real-time Q-table updates** showing the learning process

## Environment Setup

- **Grid Size**: 5x5
- **Start State**: (0, 0)
- **Goal State**: (4, 4)
- **Obstacles**: (1,1), (2,2), (3,1), (1,3)
- **Actions**: Up, Down, Left, Right

## Algorithm Parameters

- **Learning Rate (α)**: 0.1
- **Discount Factor (γ)**: 0.9
- **Exploration Rate (ε)**: 0.3
- **Training Episodes**: 500

## Key Components

### 1. Q-Table Initialization
- 3D numpy array: 5 rows × 5 columns × 4 actions
- Initialized with zeros

### 2. Core Functions
- `choose_action()`: Implements ε-greedy policy
- `step()`: Handles state transitions and rewards
- `update_q_table()`: Performs Q-learning updates
- `plot_grid()`: Visualizes the grid world

### 3. Reward System
- **Goal reached**: +20 reward
- **Hit obstacle**: -5 reward
- **Normal move**: -1 reward

## Learning Process

The agent learns through:
- **Exploration**: Random actions (30% probability)
- **Exploitation**: Best known actions (70% probability)
- **Q-value updates**: Using the Bellman equation

## Visualization

The notebook includes color-coded grid visualization:
- **White**: Empty cells
- **Blue**: Start position (S)
- **Green**: Agent position (A)
- **Red**: Obstacles (X)
- **Yellow**: Goal (G)

## Usage

Run the notebook cells sequentially to:
1. Set up the environment and parameters
2. Train the Q-learning agent
3. Observe the learning process with detailed step-by-step outputs
4. View the final Q-table values

## Learning Outcomes

After training, the agent learns optimal paths from any position in the grid to the goal while efficiently avoiding obstacles, demonstrating the power of reinforcement learning for navigation problems.
