# Walker2D-SAC-RL-Agent
A Walker2D Soft Actor-Critic (SAC) based RL  agent developed using MuJoCo, Gymnasium, and Stable-Baselines3. To build and train our Walker2D agent, we first set up the environment in Google Colab. We installed MuJoCo,
Gymnasium, and Stable-Baselines3. MuJoCo is the physics simulation engine required for Walker2d-v4, Gymnasium is
the OpenAI Gym environment wrapper and Stable-Baselines3 is a library that provides preimplemented RL algorithms,
including SAC.
The walker in the Walker2D-v4 environment is a two dimensional two-legged agent figure consisting of four main body
parts: a single torso at the top with two legs splitting after the torso, two thighs in the middle below the torso, two legs
in the bottom below the thighs, and two feet attached to the legs on which the entire body rests. The environment is
build on top of the hopper environment Durrant-Whyte et al. (2012) allowing the robot to work forward using a new set
of legs in MuJoCo (Gymnasium). The goal of the walker is to move in the forward (right) direction by coordinating
both sets of feet, legs, and thighs and by applying torques on the six hinges connecting the six body parts.

To train our Walker2D agent we used the Soft Actor-Critic (SAC) reinforcement learning algorithm to optimize its
policy through interaction with the environment. Soft actor-critic (SAC) is a model-free off-policy maximum entropy
actor-critic algorithm that avoids the complexity and potential instability associated with approximate inference in prior
off-policy maximum entropy algorithms based on soft Q-learning Haarnoja et al. (2018).

FEASIBLE APPLICATION: Designing a Socially Cognizant RL Agent with Theory of Mind for Autonomous Trash Collection
<img width="419" height="313" alt="image" src="https://github.com/user-attachments/assets/672e03bb-b8ea-4d9a-91b4-f85a631f89f3" />

