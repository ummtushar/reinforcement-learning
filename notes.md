# Reinforcement Learning

- Goal: get the max reward possible

- Difference: from supervised (labels), unsupervised (find patterns) - RL doesnt use predefined data and make decisions that maximise reward from the environment (Trial & Error)

- For: decision making tasks - sequential decision making (decisions influence future observations), learning through rewards and penalties with no direct supervision

- Ex, player in game learns to make seq. decisions and AI receives points and loses lives depending on actions.

- Not for: image recognition in games. Shooter games like CSGO - doesnt require seq. decision making and no interaction with an environment. Use supervised learning instead.

- RL apps: Robotics (walking, object manipulation), Finance (optimising trading and investment to maximise profit), Autonomous Vehicles (safety and efficiency, minimise accident and risks), Chatbot (enhance conversation skills to improve UX)

## RL Framework

add image here

## Tasks in RL - Episodic vs. continuous

- Episodic - tasks segmented in episodes; episodes has beginning and end; ex - agent playing chess

- Continuous - continuous actions without episodes; ex - adjusting traffic lights

## Return

Actions have long term consequences; agents aim to maximise the total reward over time; return - sum of all expected awards

## Discounted Return

Immidiate rewards are more valuable than future ones; discounted return - gives more weight to nearer rewards; Uses discount factor (γ, between 0 to 1) to discount future rewards; γ=0 favours only immidiate gains and γ=1 favours future gains without discount

- lower γ -> immidiate gains
- higher γ -> long-term benefits

## OpenAI Gymnasium

- Standard library for RL tasks

- Abstracts complexity of RL problems

- Provides environments like CartPole, MountainCar, FrozenLake & Taxi

- Unified for all environments

- Includes functions and methods to:
  - initilise env
  - visually represent environment
  - execute actions
  - observes outcomes

## Why Extract a Policy?

- **Deployment**: In production, you want deterministic behavior (no randomness)
- **Efficiency**: No need to compute epsilon-greedy during execution
- **Interpretability**: You can inspect what the agent learned
- **Testing**: Consistent behavior for evaluation
