# 🎮 Vision-Based Deep Q-Learning Agent for Atari Pac-Man

A deep reinforcement learning project implementing a Convolutional Deep Q-Network (DQN) to train an agent to play Atari Pac-Man using raw pixel input.

The project focuses on understanding how Deep Q-Learning scales from low-dimensional state spaces to high-dimensional image-based environments, emphasizing core stabilization techniques rather than hyperparameter tuning.


---

## 🔍 Overview

This project demonstrates how an agent can learn optimal behavior through interaction with a visually complex environment using Deep Reinforcement Learning.

Unlike environments with small numeric state vectors, Pac-Man provides raw image frames.  
To handle this, the agent uses convolutional neural networks to extract spatial features before estimating Q-values.

Key goals of the project:

- Understand how Deep Q-Learning works with image inputs  
- Implement experience replay for decorrelated learning  
- Use target networks to stabilize Q-value estimation  
- Observe how exploration–exploitation trade-offs affect training  


---

## 🧠 Core Concepts Implemented

- Deep Q-Learning (DQN)
- Convolutional Neural Networks (CNNs)
- Experience Replay
- Target Networks
- ε-greedy Exploration Strategy
- Mini-batch Training
- Temporal Difference Learning

These techniques are essential for stabilizing deep reinforcement learning in high-dimensional environments.


---

## 🌍 Environment

Environment: Atari Pac-Man (Gymnasium / ALE)

### State Space:
- Raw RGB game frames  
- Preprocessed (resized / grayscale if applied)  
- Stacked consecutive frames to capture motion  

### Action Space:
Discrete actions such as:
- Move Up  
- Move Down  
- Move Left  
- Move Right  
- No-op (depending on configuration)  

### Goal:
Maximize cumulative reward by:
- Eating pellets  
- Avoiding ghosts  
- Surviving longer  


---

## 🏗️ Architecture Overview

### Q-Network:
Convolutional neural network followed by fully connected layers.

### Convolutional Layers:
Extract spatial features from stacked game frames.

### Fully Connected Layers:
Map extracted features to Q-values.

### Output Layer:
Predicts Q(s, a) for all possible actions.

### Local Network:
Learns from sampled experiences.

### Target Network:
Provides stable Q-value targets and is updated periodically or via soft updates.

### Replay Buffer:
Stores and samples past experiences uniformly to break correlation between sequential frames.

### Optimizer:
Adam

### Loss Function:
Mean Squared Error (MSE)


---

## 🛠 Tech Stack

- Python  
- PyTorch  
- NumPy  
- Gymnasium  
- OpenCV (for frame preprocessing if applied)  
- Google Colab  


---

## ▶️ Getting Started

1. Clone the repository

```bash
git clone https://github.com/harshinikailasam/pacman_dcqn.git
cd pacman_dcqn
```


2. Install dependencies

```bash
pip install -r requirements.txt
```


### 3. Run the notebook

Open:

notebooks/Deep_Convolutional_Q_Learning_for_Pac_Man.ipynb


---
