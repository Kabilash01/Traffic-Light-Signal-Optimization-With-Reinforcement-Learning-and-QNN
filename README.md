
# 🚦 Traffic Light Optimization with Reinforcement Learning

This project provides a reinforcement learning-based framework for optimizing traffic flow at complex urban intersections. A Deep Q-Learning agent is trained to intelligently control traffic signal phases in order to minimize congestion and waiting times, ultimately improving traffic efficiency.

---

## 🧠 Deep Q-Learning Agent

### ⚙️ Framework
- **Algorithm**: Q-Learning with a Deep Neural Network
- **Objective**: Optimize traffic light phases to reduce cumulative waiting time

### 🧭 Environment
- **Intersection**: 4-way, with 4 incoming and outgoing lanes per arm (each 750 meters long)
- **Traffic Lights**: Dedicated lanes for specific movement directions (left, straight, right)

### 🚘 Traffic Generation
- Each episode simulates **1000 vehicles**
- Traffic patterns vary dynamically across episodes

### 🎯 Agent (Traffic Light Control System - TLCS)
- **State**: Discretized vehicle positions on lanes (80-cell binary vector)
- **Action**: Selection from 4 pre-defined traffic light phases, each lasting 10 seconds
- **Reward**: Based on the **reduction in cumulative vehicle waiting time**
- **Learning**: Q-learning with a neural network to approximate Q-values for state-action pairs

---

## 🚀 Getting Started

### ✅ Prerequisites
Ensure the following dependencies are installed on your system:

| Tool               | Version        |
|--------------------|----------------|
| Python             | 3.11           |
| SUMO Simulator     | 1.2.0          |
| TensorFlow         | 2.16.1         |
| TensorFlow GPU     | 2.5.0 (optional) |
| NumPy              | 1.19.5         |
| Matplotlib         | 3.6.0          |

### 📦 Setup Instructions

1. **Install Anaconda**  
   [Download Anaconda](https://www.anaconda.com/products/distribution)

2. **Install SUMO**  
   [Download SUMO](https://www.eclipse.dev/sumo/)

3. **Clone the Repository**
```bash
git clone https://github.com/yourusername/traffic-light-optimization.git
cd traffic-light-optimization
```

4. **Install Dependencies**
```bash
pip install -r requirements.txt
```

5. **Set SUMO Environment Variable**
```bash
export SUMO_HOME="/path/to/sumo"
```

---

## 🏃 Running the Algorithm

Start the training process:
```bash
python training_main.py
```

For testing:
```bash
python testing_main.py
```

---

## 📂 Code Structure

| Component        | Description                                                 |
|------------------|-------------------------------------------------------------|
| Model            | Defines the neural network architecture                    |
| Memory           | Handles experience replay buffer                           |
| Simulation       | Manages the traffic environment and interaction with SUMO  |
| Traffic Generator| Generates vehicle routes for each episode                  |
| Visualization    | Plots performance metrics (reward, delay, queue length)    |
| Utils            | Manages configuration, file handling, and SUMO setup       |

---

## ⚙️ Settings

All training and testing parameters are specified in:
- `training_settings.ini`
- `testing_settings.ini`

These include:
- Simulation duration
- Number of episodes
- Vehicle generation count
- Neural network layers and learning rate
- Traffic light durations (green/yellow)

---

## 📊 Results Summary

| Metric     | Value   |
|------------|---------|
| Accuracy   | 80%     |
| Precision  | 85.83%  |
| Recall     | 80%     |
| F1 Score   | 79.05%  |

Visualizations for reward trends, queue lengths, and waiting times are generated and saved automatically during training and testing.

---

##contact
KABILASH S -kabilash0108@gmail.com
## 📜 License

This project is licensed under the MIT License.
```

---

Let me know if you want this saved as a file or embedded in your GitHub repository structure.
