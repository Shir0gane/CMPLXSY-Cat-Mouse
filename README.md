# CMPLXSY-Cat-Mouse
An agent-based model simulating a predator-prey ecosystem. The cats act as the predator in the model while the mice act as the prey.


## Agents
The agents of the model are the cats and mice. Both agents move around the environment randomly. For each tick, each agent will perform 1 step in a random direction, consuming 1 energy unit. 

The number of initial cats and mice can be set by the `cat-count` and `mouse-count` sliders respectively. The default initial count for cats is 50 while 100 for mice. Each cat and mice are also given an initial energy value when they are created in the environment. These can be modified by the `cat-initial-energy` and `mouse-initial-energy` sliders.


### Eating Behavior
To replenish their energy, the agents must eat. Whenever a cat reaches a patch that contains mice, the cat will randomly pick a mouse from the patch and consume it. The energy consumed by the cat is equal to the current energy of the mice. 

As for the mice, the food that they consume are cheese that are randomly spawned throughout the environment. The current configuration of the model spawns 100 cheese per 20 ticks. Each cheese would give a mouse 50 energy.

The agents can only attain a maximum of 100 energy and dies once it reaches 0.


### Reproduction Behavior
Both agents are capable of reproducing. At each tick, there is a fixed probability that a cat or mouse will spawn another of its kind. The value of this probability can be modified by the sliders `cat-reproduction-probability` and `mouse-reproduction-probability`. The default value for both sliders is 10%. 

When an agent spawns another agent, the energy of the parent is divided equally among itself and the newly spawned child