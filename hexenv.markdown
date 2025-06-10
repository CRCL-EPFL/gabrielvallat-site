# Hex environment
This set of environment is using isometric blocks to build spanning structures

{% include hexenv_largegap.html %}

Different environments (compatible with [gymnasium](https://gymnasium.farama.org/) for easy training) were created, and are available on [github](https://github.com/sycamore-lab-EPFL/StaticSimulatorEnvs/tree/master)

## State
The base state comprise the current structure and the robots currently holding it. This information is encoded in a multi-channel image. 

![State example](./assets/images/OI.png "Example of a state, with the current structure and the robots holding it")

It can be extended with information such as the blocks that are planned but not placed yet and their time of arrival, allowing parallel placing of blocks.
## Action

The available actions are:
* Place a block at a given position (with an optional mask, to not allow placing floating blocks)
* Wait for the other robots to finish their actions
## State transition
Each time a robot places a new block, the stability of the structure is checked, and the state is updated accordingly. If the structure is not stable, the environment is reset to its initial state.
## Reward
The base reward is a simple binary {-1, 1} terminal reward, but helper rewards were manually designed to help the learning. 

An environment was also created to optimize the load bearing and pertubations during fabrication. This work, done by Marcel Garrobe, is detailed on [this page]()

## Specific environments

Some specific environments, based on the previous core principles, were created to test different kind of tasks and structures:
* **Generic**: The aim is to span between two horizontal footings, leading to the construction of arches and bridge-like structures.
* **Obstacles**: The aim is still to span between two horizontal footings, but this time some obstacles are present, leading to constructions that can be more complex and taller.
![Structure with obstacles](./assets/images/structure_obstacles.png "Example of a structure with obstacles, where the robots have to avoid the red blocks while covering the yellow area")


### Credits
* Lead: Gabriel Vallat
* Supervision: Maryam Kamgarpour and Stefana Parascho
* Contributions: Anna Maddux, Marcel Garrobe-Fontella
* Funding: ??
