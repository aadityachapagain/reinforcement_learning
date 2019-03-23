# MDPs and Bellman Equations

## Learning Goals

* Understand the Agent-Environment Interface
* Understand what MDPs (Markov Decision Processes) are and how to interpret transition diagrams
* Understand Value Functions, Action-Value Functions, and Policy Functions
* Understand the Bellman Equations and Bellman Optimality Equations for value functions and action-value functions

## Summary

* Agent & Environment Interface: At each step t the agent receives a state S_t, performs an action A_t and receives a reward R_{t+1}. The action is chosen according to a policy function pi.
* he total return G_t is the sum of all rewards starting from time t . Future rewards are discounted at a discount rate gamma^k.
* Markov property: The environment's response at time t+1 depends only on the state and action representations at time t. The future is independent of the past given the present. Even if an environment doesn't fully satisfy the Markov property we still treat it as if it is and try to construct the state representation to be approximately Markov.
* Markov Decision Process (MDP): Defined by a state set S, action set A and one-step dynamics p(s',r | s,a). If we have complete knowledge of the environment we know the transition dynamic. In practice, we often don't know the full MDP (but we know that it's some MDP).
* The Value Function v(s) estimates how "good" it is for an agent to be in a particular state. More formally, it's the expected return G_t given that the agent is in state s. v(s) = Ex[G_t | S_t = s]. Note that the value function is specific to a given policy pi.
