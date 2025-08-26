# Walker2D-SAC-RL-Agent
A Walker2D Soft Actor-Critic (SAC) based RL  agent developed using MuJoCo, Gymnasium, and Stable-Baselines3. This is part of our ECE 590 Socially Cognizant Robotics project at Rutgers Univeristy. Please don't copy any part of the project. If you have any questions or need any help please feel free to contact.

To build and train our Walker2D agent, we first set up the environment in Google Colab. We installed MuJoCo,
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

<img width="578" height="425" alt="image" src="https://github.com/user-attachments/assets/ad665e66-0b33-4a27-a128-b019721cc2a6" />

The inconsistencies in the agent’s performance make it clear that some key hyperparameters need fine-tuning to improve
stability and generalization to different observation settings. While the agent has learned to move forward effectively in
certain episodes, its tendency to hop, lose balance, and fall suggests that it might be exploiting the reward function rather
than learning robust walking behavior. To address this we tried tuning different sets of hyperparameters. We evaluated
the models on the hyperparameter space with a maximum of 70000 steps and 2 episodes given some of the episodes
takes longer that 5000,000 steps which is time and resource consuming. Also, we evaluated the agents using the same
observation space for better evaluation. Figure 6 shows evaluation of the policies using different hyperparameters.

<img width="601" height="232" alt="image" src="https://github.com/user-attachments/assets/dc7b972f-eab4-4884-928f-1576a819a376" />


FEASIBLE APPLICATION: Designing a Socially Cognizant RL Agent with Theory of Mind for Autonomous Trash Collection
<img width="419" height="313" alt="image" src="https://github.com/user-attachments/assets/672e03bb-b8ea-4d9a-91b4-f85a631f89f3" />

