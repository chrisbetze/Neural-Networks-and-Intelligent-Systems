# Deep Reinforcement Learning
The aim of the exercise is to optimize deep reinforcement learning algorithms in "MsPacman" Atari game.<br>
![220px-Mspacman](https://user-images.githubusercontent.com/50949470/111311155-8ae54700-8666-11eb-82b0-22a60935f21d.png)

## Game Description
This game is similar to the classic Pac-Man. The agent earns points by eating "fruits" and avoiding some monsters. 
In addition to the classic fruits, there are more specialized ones, which enable the player to eat even the monsters and win even more points (blue mode).
Ιn the course of time, gameplay speed increases and duration of blue mode decreases.

## Environments
We use [Atari environments](https://gym.openai.com/envs/#atari) of OpenAI gym with the Stable Baselines3 ([SB3](https://github.com/DLR-RM/stable-baselines3)) library.
We study four different environments:
* Deterministic-v4: Same action for 4 frames (Without thoughtfulness)
* Deterministic-v0: Same action for 4 frames (With thoughtfulness)
* NoFrameskip-v4: The action is decided for each frame (Without thoughtfulness)
* Empty-v4: The action is randomly selected every 2 or 4 frames (Without thoughtfulness)

## Algorithms
We study three deep reinforcement learning algorithms that are implemented in the Stable Baselines3 project and support discrete actions:
* A2C: Advantage Actor Critic
* DQN: Deep Q-Networks
* PPO: Proximal Policy Optimization

## Description - Steps
* We start with a random agent (without learning).
* We continue applying the above algorithms in all different environments.
* We use the "TensorBoard" with the "ngrok" service to keep track of mean episode length and mean reward.
* We choose the environment and the algoithm that achieve the best evaluation reward.
* We optimize the best pair (env-algo), by modifying some parameteres of the [SB3 documentation](https://stable-baselines3.readthedocs.io/en/master/modules/dqn.html).
* We record a video with the optimal agent.

## Results
The best evaluation reward, achieved with DQN algorithm in Deterministic-v4 environment, is 4396 (±963).

## Video
To watch the video with the optimal agent click [here](Lab4/MsPacman_DQN.mp4)
