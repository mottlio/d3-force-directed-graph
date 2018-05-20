Force-directed graphs focus on the links between different nodes.

**d3.forceSimulation([nodes])**

- accepts an array of nodes
- begins to simulate the forces applied to those nodes
- method provides a range of new properties to the d3 nodes: vx, vy - depending on the force applied
- by default simulations have no forces

types of forces:

**d3.forceCenter([x, y])**
simulation.force(name - howyouwanttocallit, force - whetitdoes)

- need to specify how the position should be updated based on the velocities calculated in the simulation, then pass this function as a callback to the "on" function of the simulation:

**simulation.on(type, listener)**

type of event possible: tick (1 second) or end 

**d3.forceManyBody()**

- adds forces between all nodes in the simulation

**force.strength([newStrength])**

- accepts a value or callback to set a new strength, negative is repulsive, positive is attractive, default is -30

Nodes in this example are pulled to the center by the forceCenter() but pushed apart by forceManyBody()

**FORCE DIRECTED GRAPH**
- requires a link array with objects indicating a source and a target
- links may have different forces:

**d3.forceLink([links])**

**link.id([id])** 
alows a departure from d3's way of matching links (by index). We can specify how links should be matched to values.

Strength of the force of the link determined by 2 values: distance (how long the link wants to be), strength (proportionate to actual distance and original length - like a spring)

**distance()**

