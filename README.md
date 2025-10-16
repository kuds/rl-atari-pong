# Playing Atari's Pong with Reinforcement Learning

## Deep Q Learning (DQN)

![](/Images/atari_pong_dqn.gif)

## Proximal Policy Optimization (PPO)

![](/Images/atari_pong_ppo.gif)

## Results
Hardware: Google Colab L4

| Model Type | Environment Version | Average Reward | Training Steps | HuggingFace                                           |
|------------|---------------------|----------------|----------------| ------------------------------------------------------|
| PPO        | PongNoFrameskip-v4  | 21.0           | 4,000,000      | [Link](https://huggingface.co/kuds/atari-pong-v4-ppo) |
| DQN        | PongNoFrameskip-v4  | 20.6           | 4,000,000      | [Link](https://huggingface.co/kuds/atari-pong-v4-dqn) |
| PPO        | ALE/Pong-v5         |                |                |                                                       |
| DQN        | ALE/Pong-v5         |                |                |                                                       |

## Training Notes
- When training with Google Colab Notebooks with high memory option enabled, try not to exceed the buffer size `850,000` as you can run into memory issues
- When training in more complex environments or using multiple simulated environments (`n_evn` > 1), DQN is very sensitive to the hyperparameter settings
- Stable Baselines3 implementation of Soft Actor-Critic (SAC) only supports continuous action spaces and can not be used with Atari's Pong as it uses discrete actions
- When using rllib, be mindful of your resources, as the training jobs might not start (always in pending status) if there are not enough CPUs or GPUs allocated
  
## Finding Theta Blog Posts
- [Mastering Atari's Pong with Reinforcement Learning: Overcoming Sparse Rewards and Optimizing Performance](https://www.findingtheta.com/blog/mastering-ataris-pong-with-reinforcement-learning-overcoming-sparse-rewards-and-optimizing-performance)
