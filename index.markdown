---
layout: default
---
# Multi-agent reinforcement learning applied to construction 
The aim of this research is to train robots to build structures by simply imputing some specifications, such as an area to cover or obstacles to avoid.
![Robots task](./assets/images/intermediate2.png "The robots have to place blocks in a way that is covering the yellow area while avoiding the red one")

To achieve this task, two main building blocks are designed in parallel: training environments and algorithms. 
## Training environment pages
To train robots to build structures, we developed two suites of environments. Each of these environments can be modeled as MDP, and out of the box RL algorithms can be used to solve them.

[Hex environment suite](./hexenv.markdown)

[3D environment suite](./3Denv.markdown)

## Algorithms

The aim of the algorithmic part of this research is to find how complex structures can be represented and simplified to get tractable solutions, while maximizing the variety of shapes created. To provide solid baselines, RL algorithms such as Soft Actor-Critic and AlphaZero, and search algorithms such as A* are used. 

### Coordination between agent
As a close collaboration is needed between each robot, a centralized and asynchronous approach was chosen. 

