# Playing Atari's Pong with Reinforcement Learning

## Deep Q Learning (DQN)

![](/Images/dqn_atari_pong.gif)

## Results
Hardware: Google Colab T4

| Model Type | Average Reward | Training Time | Total Training Steps |
|------------|----------------|---------------|----------------------|
| PPO        |                |               |                      |
| SAC        |                |               |                      |
| DQN        | 20.6           |  11:56:00     | 10,000,000           | 

## Training Notes
- When training with Google Colab Notebooks with high memory option enabled, try not to exceed the buffer size `850,000` as you can run into memory issues
- When training in more complex environments or using multiple simulated environments (`n_evn` > 1), DQN is very sensitive to the hyperparameter settings
  
## Blog Post
- [Mastering Atari's Pong with Reinforcement Learning: Overcoming Sparse Rewards and Optimizing Performance](https://www.findingtheta.com/blog/mastering-ataris-pong-with-reinforcement-learning-overcoming-sparse-rewards-and-optimizing-performance)
