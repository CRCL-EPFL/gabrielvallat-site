---
layout: default
---
# Multi-agent reinforcement learning applied to construction 
The aim of this research is to train robots to build structures by simply imputing some specifications, such as an area to cover or obstacles to avoid.
![Robots task](./assets/images/intermediate2.png "The robots have to place blocks in a way that is covering the yellow area while avoiding the red one")

To achieve this task, two main building blocks are designed in parallel: training environments and algorithms. 
## Training environment pages
To train robots to build structures, we developed two suites of environments. Each of these environments can be modeled as Markov decision processes (MDP), and out of the box RL algorithms can be used to solve them. The first suite, using a discrete action space and a 2D grid representation, is designed for simpler tasks, while the second suite, using a continuous action space and a 3D representation, is aimed at more realistic scenarios. The 2D environmentst are descibed in more detail in the [Hex environment suite](./hexenv.markdown), while the 3D environments, still under development, are described here.

### 3D environment suite
The idea behind these environments is to represent the world as a typed graph, where nodes are blocks, forces, contact points and objectives, and edges are relations between them.
![FTGraph](./assets/images/FTgraph.jpg "The FTGraph is a graph representation of the world, where nodes are blocks, forces and contact points, and edges are relations between them")

In the future, we aim to add other types of nodes, such as robots, to embed robotic path planning in the algorithms directly. 
## Algorithms

The aim of the algorithmic part of this research is to find how complex structures can be represented and simplified to get tractable solutions, while maximizing the variety of shapes created. To provide solid baselines, RL algorithms such as PPO and AlphaZero, and search algorithms such as A* are used. 

By representing a set of structures using a policy from a trained RL agent, we hope to by able to easily generate new structures by sampling from it, and to add new constraints to fit with the designer's needs seamlessly.

### Coordination between agents
In the current development stage, the robots are simply acting sequentially, but we plan to use a a centralized and asynchronous approach in the future. This approach would allow the robots to coordinate their actions effectively, while still being able to act independently when needed.

### Credits
* Lead: Gabriel Vallat
* Supervision: Maryam Kamgarpour and Stefana Parascho
* Contributions: Ziqi Wang
* Funding: ??