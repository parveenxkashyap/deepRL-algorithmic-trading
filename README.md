# DeepRL-trade

Algorithmic Trading Using Deep Reinforcement Learning Algorithms (PPO and DQN)

---

## Introduction:

In quantitative finance, stock trading is essentially a dynamic decision problem—deciding where, at what price, and how much to trade in a highly stochastic, dynamic, and complex stock market. With recent advances in deep reinforcement learning (DRL) methods, sequential dynamic decision problems can be modeled and solved in a human-like way.

<br>

In this project, I explore the potential and performance of deep reinforcement learning to optimize stock trading strategies and maximize investment returns. I selected Google stock as the target asset and used daily opening and closing prices, trading volume, and several technical indicators to construct the training environment and trading simulation.

<br>

I developed two trading agents based on deep reinforcement learning—one using the Proximal Policy Optimization (PPO) algorithm and the other based on Deep Q-Learning (DQN). These agents autonomously make trading decisions and aim to generate returns in dynamic financial markets. Their performance is compared to the traditional buy-and-hold strategy, showing that the deep reinforcement learning approach achieves better results in terms of risk-adjusted returns and portfolio performance.

---

## Project Description:

I trained two deep RL agents using Google stock data (**GOOG**) from **01-01-2014** to **01-08-2022**, implementing **Proximal Policy Optimization (PPO)** and **Deep Q-Learning (DQN)**.

I used the stable-baselines3 implementations for both agents. Both `ppo_agent` (PPO) and `dqn_agent` (DQN) use discrete action spaces:

- **1** for a full **Long** position
- **0** for a complete **Cash** position
- **-1** for a **Short** position equivalent to the agent’s current asset value.

The trading environments are implemented using the OpenAI Gym interface. At each timestep (day), the agent selects an action (1, 0, or -1), moves to the next trading day, and receives a reward equal to the percentage change in its total asset value.

**All implementation details are documented in the `notebook.ipynb` notebook.**

---

## References:

- Human-level control through deep reinforcement learning (Deep Q-Learning): [paper](https://www.nature.com/articles/nature14236)
- Proximal Policy Optimization: [paper](https://arxiv.org/abs/1707.06347), [blog](https://openai.com/blog/openai-baselines-ppo/), [spinning-up](https://spinningup.openai.com/en/latest/algorithms/ppo.html)
