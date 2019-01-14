[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/43851646-d899bf20-9b00-11e8-858c-29b5c2c94ccc.png "Crawler"


# Udacity Deep Reinforcement Learning Nanodegree - Project 2: Continuous Control

### Introduction

For this Udacity project, I used a single DDPG agent to solve the Unity's [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment which includes 20 parallel robotic arms movements.

![Trained Agent][image1]

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

Agents must get an average score of +30 (over 100 consecutive episodes, and over all agents).  Specifically,
- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent.  This yields 20 (potentially different) scores.  We then take the average of these 20 scores.
- This yields an **average score** for each episode (where the average is over all 20 agents).

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30.

### Getting Started
Codes were written using Python3.6.2, run this to install necessary packages:

`pip install -r requirements.txt`

The Unity environment `Reacher_20.app` only runs on Macs, for Windows users, download the Windows 32-bit version [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip).

Please follow the instruction in the [Udacity DRLND Instructions](https://github.com/udacity/deep-reinforcement-learning#dependencies) on setting up the environment.

### Instructions

- Run all the block cells `Report.ipynb` to initiate the environment and go through the trainings.
- `model.py` defines the DDPG agent's actor and critic neural network architectures.
- `ddpy_agent.py` defines the DDPG agent class.
- `checkpoint_actor.pth` and `checkpoint_critic.pth` are the weights of the best model's actor and critic networks.

### Sources
- [Continuous control with deep reinforcement learning](https://arxiv.org/pdf/1509.02971.pdf)
- Udacity Learning Materials
