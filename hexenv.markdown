# Hex environment
This set of environment is using isometric blocks to build spanning structures

{% include hexenv_largegap.html %}

Different environments (compatible with [gymnasium](https://gymnasium.farama.org/) for easy training) were created, and are available on [github](https://github.com/sycamore-lab-EPFL/StaticSimulatorEnvs/tree/master)

## State
The base state comprise the current structure and the robots currently holding it. This information is encoded in a multi-channel image. 

[![State example](./assets/images/OI.pdf "Example of a state, with the current structure and the robots holding it")]

It can be extended with information such as the blocks that are planned but not placed yet and their time of arrival.
## Action

## State transition

## Reward
The base reward is a simple binary {-1, 1} terminal reward, but helper rewards were manually designed to help the learning. 

An environment was also created to optimize the load bearing and pertubations during fabrication. This work, done by Marcel Garrobe, is detailed on [this page]()

## Specific environments


### Credits
* Lead: Gabriel Vallat
* Supervision: Maryam Kamgarpour and Stefana Parascho
* Contributions: Anna Maddux, Marcel Garrobe-Fontella
* Funding: ??
