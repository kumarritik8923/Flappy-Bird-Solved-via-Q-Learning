# 🐦 Flappy Bird AI using Deep Q-Network (DQN)

## Project Overview

This project implements a Deep Q-Network (DQN) agent that learns to play Flappy Bird using Reinforcement Learning and PyTorch. The agent interacts with the game environment, stores experiences in a replay buffer, and learns an optimal policy through Q-learning. The model uses experience replay, target network synchronization, and epsilon-greedy exploration to improve training stability and performance.

## Working

1. The agent observes the current state of the Flappy Bird environment.
2. It selects an action (Flap or No Flap) using an epsilon-greedy strategy.
3. The environment returns the next state and reward.
4. The experience `(state, action, reward, next_state)` is stored in replay memory.
5. Random mini-batches are sampled from the replay buffer.
6. Target Q-values are calculated using the target network.
7. The policy network is updated through backpropagation.
8. The target network is periodically synchronized with the policy network.
9. The best-performing model is automatically saved during training.

## Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/flappy-bird-dqn.git
cd flappy-bird-dqn
```

### Create a Virtual Environment

```bash
python -m venv venv
```

### Activate the Virtual Environment

**Windows**

```bash
venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Usage

### Train the Agent

```bash
python agent.py flappybirdv0 --train
```

### Test the Trained Agent

```bash
python agent.py flappybirdv0
```

### Play Flappy Bird Manually

```bash
python game_flappy_bird.py
```

## Technologies Used

- Python
- PyTorch
- Gymnasium
- Flappy Bird Gymnasium
- PyYAML
- NumPy
