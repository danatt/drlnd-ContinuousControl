# drlnd-ContinuousControl

### Udacity RL-ContinuousControl Project

This is a project from the **Deep Reinforcement Learning Nanodegree** @Udacity. 

_The task is to solve the Unity [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) Environment._
You can watch the final result by using the `watch_a_trained_agent.ipynb`.

![](/pictures/reacher.png)


### Project Overview
In this environment, a double-jointed arm :muscle: can move to target locations. A reward of +0.04 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The **observation space consists of 33 variables** corresponding to position, rotation, velocity, and angular velocities of the arm. Each **action is a vector with 4 numbers**, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

The task is episodic, and in order to solve the environment, your agent must get an average score of 30 over 100 consecutive episodes.

### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - **_Version 1: One (1) Agent_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

2. Place the file in the repository folder, and unzip (or decompress) the file. 

3. Open the `Continuous_Control.ipynb` notebook and follow instructions there.


### Dependencies
For more information on how to run the environment please read the Dependencies section in this [repo](https://github.com/udacity/deep-reinforcement-learning#dependencies).

### Resources

- [CONTINUOUS CONTROL WITH DEEP REINFORCEMENT LEARNING](https://arxiv.org/pdf/1509.02971.pdf)
