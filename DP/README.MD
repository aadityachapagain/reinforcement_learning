# Policy and Value Iteration using Dynamic Programming

## Goals:
* Understand the difference between Policy Evaluation and Policy Improvement and how these processes interact
* Understand Policy Iteration algorithm
* Understand Value Iteration algorithm 
* Understand the Limitations of Dynamic Programming Approches

## Summary
* Dynamic Programming (DP) methods assume that we have a perfect model of the environment's Markov Decision Process (MDP). That's usually not the case in practice, but it's important to study DP anyway.
* Policy Evaluation: Calculates the state-value function V(s) for a given policy. In DP this is done using a "full backup". At each state, we look ahead one step at each possible action and next state. We can only do this because we have a perfect model of the environment.
* Full backups are basically the Bellman equations turned into updates.
* Policy Improvement: Given the correct state-value function for a policy we can act greedily with respect to it (i.e. pick the best action at each state). Then we are guaranteed to improve the policy or keep it fixed if it's already optimal.
* Policy Iteration: Iteratively perform Policy Evaluation and Policy Improvement until we reach the optimal policy.
* Value Iteration: Instead of doing multiple steps of Policy Evaluation to find the "correct" V(s) we only do a single step and improve the policy immediately. In practice, this converges faster.
* Generalized Policy Iteration: The process of iteratively doing policy evaluation and improvement. We can pick different algorithms for each of these steps but the basic idea stays the same.

## Lecture

* David Silver's RL Course Lecture 3 - Planning by Dynamic Programming ([video](https://www.youtube.com/watch?v=Nd1-UUMVfz4))

## Readings

* Chapter 4 of Reinforcement Learning of Sutton's Book