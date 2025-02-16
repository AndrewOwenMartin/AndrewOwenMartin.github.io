Invertine the object model.
- Basic idea
- Can you do both at once?
- Why it might be important
- Hypotheses or how to test them.
- Examples, RE collision detection

Two things recur in my time researching AI.
1. that Cellular Automata are able to produce surprisingly "lifelike behaviour" from very simple rules.
2. that the philosophers who argue AI is on shakey philosophical ground point to the lack of importance of the environment in the models studied.

I have recently seen these statements as diferent aspects of the same concept sand will explore the feature of CA which allows the emergence of lifelike behaviour.

# Collision detection in continuous worlds vs grid worlds

> The next para is all about the idea of whether certain phenomena are/are not captured by grid/coninuous physics, wondering if we choose one just because it would be intractible to describe a situation in the other.

Imagine a 3D game with cellular physics. Why bother constructing a boundary in cellular detail? No interesting behavious depends on it. But matbe if we considered phenomena that exist at the boundary, peeling skin, aroma, or secreted oils reacting in the air. If we had tiny physical voxels maybe it would just be too slow. Is it simply the case that CA exist in small worlds and you need object physics to simulate complex environments.

Maybe consider gasses with object physics you can simulate each molecule. Or do whatever is in vogue, I guess an evolution function and a rendering function that works by sampling.

But if it was cellular physics you might just need to model the number of molecules in each voxel and have a simple evolution or diffusion function for each.

consider a hybrid model for collision detection. Could you maintain a record of objects and a record of occupuied cells?

Chaos suggests two odels would be unlikely to evolve in sync.

You could iterate one model then update the other but this might amount to calculating collision detection of each object against each voxel.

There's a chance the cellular physics model will work as such a powerful cache of precomputed info that it allows for some extreme optimisations, but it seems unlikely.

Intro to the idea: I learned physics programming for games which included collision detection, if you know the shape and location of every object how to tell which objects are touching?

The basic approach is to define the surface of each object and check every surface for intersection with each other surface. There are legion optimisation, the simplest of which is some kind of bounding boxes which are larger, but simpler than each object and only calculate collisions that occur between bounding boxes. Also octtrees. Also some concept of a maximum speed (or speed of light)
