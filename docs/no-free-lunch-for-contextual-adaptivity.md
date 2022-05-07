If you have an algorithm for nim, then necessarily any change to that algorithm either needs to increase complexity or decrease performance at nim.
I'm not claiming that any system that is functionaly similar to an algorithm must be implmenting the optimal version of that algorithm, the implementing system may have some capacity for increased complexity in its behaviour without reducing performance in any existing behaviours.

Contextual sensitivity requires that some stimuli which do not determine behaviour in one context will determine the behaviour in another.
Any system that exhibits contextual sensitivity must therefore either have all possible stimuli-response pairs available at all time, or have some kind of mechanism whereby sensitivity to certain stimuli and probabilities of certain behaviours are modified as a result of the changing situation.
I will name this context-free and stateful systems, where the behaviour of context-free systems is a function only of incoming stimuli and stateful systems respond to stimuli in a way which is, to some extent, modulated by some kind of context recognising super system.
An example of a context-free system is an algorithm for playing Nim, there is no state in the algorithm which needs to be maintained and respected outside of the number remaining at the time the algorithm gets to act. 
An example of a stateful system is an animal reacting differently to being presented with food depending on whether or not they have recently eaten.

Is is possible for a context-free system to exhibit context sensitivity? To a certain extent for sure.
A game of Nim may be won by being the player to reduce the number to zero, or to be the player to force the other player to reduce the number to zero, this is arguably an external state but one can easily imagine incorporating this as a part of the input stimuli, to keep the algorithm a 'pure' context-free system.
In this case the context-free Nim algorithm can act accordingly whether the aim is for it or for its opponent to reduce the number to 0.
The caveat is that the system requires the state to be presented at each step.
It is clear that for any context-free system it can be as adaptable as any computable algorithm as long as the entirity of relevant state is presented at all times, this precludes any form of memory or learning.
Furthermore, the algorithm inside needs to handle all input appropriately.
A context-free system can therefore only be as context-sensitive as it is possible to be as a response to immediately available information, and can only perform calculations while the responsive behaviour is relevant. There can be no pre-processing or partial-solutions.
A context-free system might include behaviour which ensures the relevant information is always available, imagine for example an android controlled by a purely context-free algorithm whose behaviour always includes printing all known information to a video screen that is in its vision.
This is something that would adhere to the strict letter of the definition of context-free but not the spirit, in that the system is manipulating an aspect of the world such that historical information is always available.
Neverthelss this might be an intersting example to keep in mind for the possibility of being the first-step towards stateful organisms which evolved.

Imagine then a stateful system, that has some context modulator.
It seems clear that there can be two forms of system, one in which the modulator is a completely distinct system, receiving no direct feedback from the behaviour system, or there is at least some interaction between the two systems up until they are meaningless to describe as two systems.
In the case of the first system, there must be some delay in detecting the context, and a complex detector may be so slow as to prohibit any behaviour actually taking place.
In the case of some level of integration, we must see that context-sensitivity comes at some cost, either all stimulii are always considered, or in the case of certain contexts some stimulii may be de-emphasised incorrectly.
Here we see the first indication that context sensitivity comes at a cost of always-correct behaviour.

How might an always correct, context sensitive system look?
I would need to take in all stimuli at once, in case anything was relevant.
And it must consider all simuli fully, at which point any heuristics for checking one thing over another become useless.
Why check certain things first if you are committed to checking all things?
You could imagine two systems in a box, with two separate inputs and two separate outputs.
A chess system and a route planning system, where one input can only recieve chess game states and the other input can only receive origin/destination pairs, this would be a system that seems to adapt correctly.
The two outputs could be unified as long as the input pattern for one was completely disjoint from the other, in which case the output could also be unified.
This would have the appearance of a system which could detect the context from the input alone, although notice this came at a cost, firstly twice the complexity in the box, this is unsurprising, but also the complexity in managing the input signals, keeping them separate and routing all input correctly, this is perhaps more surprising.

Imagine now, a not always perfect, context sensitive system. This is what we commonly see in GOFAI, some heuristics for detecting the situation and some heuristics for planning what to do in the detected situation given some current input and some current memory.
This is okay, but each context needs to be pre-programmed in.
If there are many contexts, the detection of the contexts becomes prohibitive.
Worse, if contexts can be proceduraly defined then there is a chance of a permanent halt in behaviour while the system interrogates all possible infinite contexts.
A heuristic for detecting the context saves some time, but if there is more than one heuristic then a further system is required to detect which heuristic to use.

Now to consider how a system might be context sensitive with some integration.

Where do neural networks fit in this taxonomy? Mostly as context-free systems, but some are integrated stateful systems.
