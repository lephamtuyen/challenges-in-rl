# Challenges in Reinforcement Learning and Research Trending
A curated list of [9 Challenges in Reinforcement Learning](https://arxiv.org/pdf/1904.12901.pdf) and theirs Research Trending (collected from 2018~present)

I'm looking for more contributors!

![](images/cover.jpeg)

## Table of Contents

### Challenges in Reinforcement Learning and Research Trending
<!-- MarkdownTOC depth=4 -->

- [Off-line training and evaluating](#offline)
    - [Intuition](#offline-intuition)
    - [Examples](#offline-examples)
    - [Researches](#offline-trending)
- [Learning from Limited Samples](#sample)
    - [Intuition](#sample-intuition)
    - [Examples](#sample-examples)
    - [Researches](#sample-trending)
- [High-dimensional state and action spaces](#dimensional)
    - [Intuition](#dimensional-intuition)
    - [Examples](#dimensional-examples)
    - [Researches](#dimensional-trending)
- [Satisfying Safety Constraints](#safety)
    - [Intuition](#safety-intuition)
    - [Researches](#safety-trending)
- [Partial observability](#partial)
    - [Intuition](#partial-intuition)
    - [Examples](#partial-examples)
    - [Researches](#partial-trending)
- [Reward functions](#reward)
    - [Intuition](#reward-intuition)
    - [Examples](#reward-examples)
    - [Researches](#reward-trending)
- [Explainability](#explain)
    - [Intuition](#explain-intuition)
    - [Examples](#explain-examples)
    - [Researches](#explain-trending)  
- [Real-Time Inference](#realtime)
    - [Intuition](#realtime-intuition)
    - [Examples](#realtime-examples)
    - [Researches](#realtime-trending)
- [System Delays](#delay)
    - [Intuition](#delay-intuition)
    - [Examples](#delay-examples)
    - [Researches](#delay-trending)  


<!-- /MarkdownTOC -->

<a name="offline"></a>
## Off-line training and evaluating

<a name="offline-intuition"></a>
#### Intuition

Training and evaluating can't be performed online directly.
The only way is using offline training and evaluating methods
that train agent based on the collected data of previous controllers 
(e.g., human, canonical controller).

<a name="offline-examples"></a>
#### Examples

- Big systems deployed from the past, 
want to replace its controller (e.g., human, classical controller) by an AI model. 
For examples, water distributed systems, eletrical systems, HVAC systems
  
<a name="offline-trending"></a>
#### Researches

- [BCQ](https://arxiv.org/abs/1812.02900) - Off-Policy Deep Reinforcement Learning without Exploration
- [BEAR](https://arxiv.org/abs/1906.00949) - Stabilizing Off-Policy Q-Learning via Bootstrapping Error Reduction
- [Offline REM](https://arxiv.org/abs/1907.04543) - An Optimistic Perspective on Offline Reinforcement Learning

<a name="sample"></a>
## Learning from Limited Samples

<a name="sample-intuition"></a>
#### Intuition

In case the agent can be trained from the real systems directly. 
However, because of the high cost when exploring the state-action space, the agent is only
learned from limited dataset that is only cover a small space of state and action
space.

<a name="sample-examples"></a>
#### Examples

- In a robotics system, an agent exploring random actions can be harmful 
to the systems; or a live trading agent can lose much money if it takes random actions.

<a name="sample-trending"></a>
#### Researches
The researches for this challenge aim to improving sample efficiency.

- Meta reinforcement learning: Learning how to learn
    * [MAML](https://arxiv.org/abs/1703.03400)
    * [SNAIL](https://arxiv.org/abs/1707.03141)
- Learning from demonstration:
The agent initializes from expert demonstration rather than learning from scratch
    * 
    *
- Model-based Reinforcement Learning: agent is planned based on 
a transition model of environment. It means the agent can learn from both real system 
and transition model.
    * [Ensembles of transition models](https://arxiv.org/abs/1805.12114)

<a name="dimensional"></a>
## High-dimensional state and action spaces

<a name="dimensional-intuition"></a>
#### Intuition

Many practical real world problems have large and continuous state and action spaces

<a name="dimensional-examples"></a>
#### Examples

- In recommender systems (number of items for recommends)
- Question Answering system (number of answer)

<a name="dimensional-trending"></a>
#### Researches (not too much active topic ?)
- [AE-DQN](https://arxiv.org/abs/1809.02121) Action Elimination Deep Q Network

<a name="safety"></a>
## Satisfying Safety Constraints

<a name="safety-intuition"></a>
#### Intuition

Each environment existed its own constraints that the agent should be followed 
to avoid damages during exploration

<a name="safety-examples"></a>

<a name="safety-trending"></a>
#### Researches (applicable)
- [CPO](https://arxiv.org/abs/1705.10528) Constrained Policy Optimization
- [DDPG+Safety Layer](https://arxiv.org/abs/1801.08757) Safe Exploration in Continuous Action Spaces

<a name="partial"></a>
## Partial observability

<a name="partial-intuition"></a>
#### Intuition

- Partial observability can be understand in two ways:
    + Some states are missing due to hard to collect or cannot collect
    + States/actions are noisy in the real world (uncertainty)
<a name="partial-examples"></a>

<a name="partial-trending"></a>
#### Researches (Hard problem and still challenged)
- Stack of history observations. [DQN](https://arxiv.org/abs/1312.5602) is one example
- Using [RNN](https://arxiv.org/abs/1507.06527) to memory the past

<a name="partial"></a>
## Reward functions

<a name="reward-intuition"></a>
#### Intuition

- Design reward function sometimes is infeasible or difficult
- Learning a reward function that combines of multiple sub-reward 
(sub-objective) is difficult

<a name="reward-trending"></a>
#### Researches
- Inverse Reinforcement Learning: don't design reward function but learn a reward model
    + [GAIL](https://arxiv.org/abs/1606.03476)

<a name="partial"></a>
## Explainability

<a name="explain-intuition"></a>
#### Intuition

- Similar to problem of AI model, an RL agent also need to interpret for its decisions

<a name="explain-trending"></a>
#### Researches
- `not investigated yet`

<a name="realtime"></a>
## Real-Time Inference

<a name="realtime-intuition"></a>
#### Intuition

- For some domains such as robotics, control systems, 
real-time inference is very importance. The time from 
collected the data to making decision should less than a limited runtime.

<a name="realtime-trending"></a>
#### Researches (still challenge)
- `in research topic`

<a name="realtime"></a>
## System Delays

<a name="delay-intuition"></a>
#### Intuition

- most real systems have delays in either states, or rewards

<a name="sample-examples"></a>
#### Examples

- In a robotics system, states (sensor data) need to be 
collected and transferred over IoT infrastructure

- In recommendation system, reward values are only 
received after the user click/buy products

<a name="delay-trending"></a>
#### Researches (still challenge)
- Optimizing agent behavior over long time scales by transporting value [Nature](https://www.nature.com/articles/s41467-019-13073-w)

