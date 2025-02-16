# AI
# if NFL is true, there can not be GAI.

# Your own mind is doing the heavy lifting

If you see an image that claims to he the output of some computer vision system remember that what you're experiencing is the result of your own act of perception and experience on top of whatever the computer output.
It's easy to see the output of an edge detector and say to yourself "yeah, that looks like the edges are highlighted in white" but then you're doing your own "edge detection" and checking that the result is more or less plausible.
The real output of an edge detector will look like a list, an easily interpretable JSON object, a binary string that in a conventional format for listing edges, or ultimately some intelligent behavior.

# goodhart's law

# there is no true autonomy

You may draw a line which defines autonomy, or an agent, in a system, but there is no objective way to draw the one true line.

# Anticipation is more important to study than prediction

Anticipation is a solution os the commonsense problem, as the commonsense is already built-in to the anticipation.

It's the (attention) Economy, stupid!

# Meaning

Meaning never 'objectively' "bottoms out" only 'subjectively' and in a undefined number of routes to "the bottom".

# Swarm Intelligence + NFL theorems

All is a trade off, and swarm intelligence can be seen as a mix between connectionist architectures (lots of dumb units) and symbolic AI (one large algorithm) as it is a modestly large number of agents controlled by modestly complex algorithm.

A swarm Intelligence analogue of computing should be 'willing' to sacrifice one of the features of Turing Computation in order to gain a new and unique feature.
Maybe this feature could be that it doesn't always give the same result. Or that it is less expressive. Maybe that it can't handle NP Hard problems.
Alternatively, if it could be shown that swarms were Turing equivalent, what gain would that give?

A more 'natural' behaviour than computing an output might be to assume the structure whereby the dynamical system does not end up in a known trivial steady state.
This is not something that can be computed because it will have to be "played out", like there's no algoruthm for "predicting" what the steady state of a Game of Life will be. But maybe that's unsurprising maybe that's most algorithms, that we don't know a quicker way to compute the output.

In what way could the environment of a computeration be taken meaningfully into account?
Maybe in "summers of plenty" the system would perform error checking, redundant calculations, exact methods to high accuracy, and explorative optimisations quickly expiring caches. In "winters of discontent" ever more crude heuristics broad approximations, rash branch predictions, fat caching. This could be written as standard computation, but the principle remains.

# Are Swarms equivalent to Freeman Neurodynamic modules?

Could swarms be analogous to Freeman Neurodynamic modules? A module can "more of less" be defined by some neurons and different models can overlap with other modules, swarms can do this too. WE would have to work at the agent level else we will lose that overlapping property. But how essential is that? Conceptually they're different, no?

# Swarms/ANNs computing

No one has demonstrated that a swarm can compute. Why is that interesting? Segelman Neural Net like stimulation to executre algorithms.
Vegner, P shared interation more powerful than computation. Can a Neural Network solve sequential programming tasks? Community of people working on this. Can I do it with one swarm? A robust demo on its own is paper worthy. Could we use an evolutionary type algorithm?

# Swarms/SDS, using the algorithm while you train it.

Certainly the use of the algorithm as it trains could be seen as a tradeoff.

# Failure of AI startups without domain knowledge

Notice the lack of 'boom' in businesses replacing humans with AI. If you get a dataset without domain knowledge, you can't do anything with it.

There aren't many, could you perform a Chinese Room-style test?

I was thinking about how just doing "a machine learning" on a dataset isn't easy without domain knowledge. You need to know which columns are irrelevant, which columns to represent as categorical, which correlations are likely spurious, and other things about how the data is collected and how it will be used. So on and so on.

This made me imagine what might happen if you took an existing dataset (or collected a new one) and anonymised the semantics, such a hiding column names and mangling any text. Would you still be able to use the data to train a neural network?

We could call this a Chinese Room dataset as it would appear as meaningless squiggles and squoggles to the Data Scientist, but should be functionally identical to the AI itself.

Before looking into this idea any further, I wonder if you've ever heard of an experiment like this?

It would seem to me to be a good indication of how much of the "semantic heavy lifting" is done by the human operator, and cannot be attributed to the algorithm itself.

# Modelling the environment is essential for 'natural behaviour'

Cellular Automata can often be seen to produce "natural" or "lifelike" behaviour because they model the environment space rather than just the objects represented.
I.e. they consider each cell of space to be an entity worth modelling.

Is it possible to marry the two thoughts: "Modelling the environment is essential for 'natural behaviour'" and "Swarm Intelligence + NFL theorems". I.e. What could Swarm Intelligence sacrifice of Turing Computation in order to gain a new interesting behaviour, is the presence of the environment beneficial? It could certainly been seen as a computational cost.

## Next Level AI Notes

# Defining Intelligence

- Doung the task to a commercial degree
- Adaptable agency
- The things which the culture defined as intelligent. Not taht we don't say "raising a child well" or "dance" but we do say "word puzzles, logic, math and chess". (The passtimes of those defining intelligence)

# Nothing new under the sun in AI or Comp. Sci.

"If AI is 1) handcrafted, 2) statistic, 3) adaptable". Note that we're 'nowhere' on 3.

The first sentence is stupid. Reeks of naivety.

Autonomous Driving long before Computer Vision. Trains, autopilot.

# 'vision' is more than just 'eyes'

We attribute to 'vision' what we should describe as 'feel'.

# AI is not a thing

AI is not a thing to focus a business on, you may as well focus on 'maths'. It's inarguably useful, often the basic stuff is the most important, and you still need practical knowledge + domain experience to make a business.

# Heidegger's philosophy science nexus

Scinece gets complex then cumbersome until the philosophy radically changes.

# Brain claims

- The brain is not a 'kludge' how dare they?
- Neurons are always firing, not just on a signal
- Neurons are not information processing units. (info is subjective, see 5V or/and)
- It's not true to say information is stored in weights, the previsout experience influences the weights, but also the 'current state'. It's like saying the story is stored in the typewriter, the weights determine the range of situations and behaviours.
- A random network is not a blank slate, it's a very specific type of network.
> In the days when Sussman was a novice, Minsky once came to him as he sat hacking at the PDP-6.
> 
>     "What are you doing?", asked Minsky.
>     "I am training a randomly wired neural net to play Tic-tac-toe", Sussman replied.
>     "Why is the net wired randomly?", asked Minsky.
>     "I do not want it to have any preconceptions of how to play", Sussman said.
> 
>     Minsky then shut his eyes.
>     "Why do you close your eyes?" Sussman asked his teacher.
>     "So that the room will be empty."
>     At that moment, Sussman was enlightened.

Humans also exist in time and bring their STM with them + prejudices. (i.e. intelligent action doesn't rise from a blank slate of stimulus->action)

In a photo, lighting and the Background isn't noise to be ignored but contextual information.

A convolutional neural network means to "step" or "march" a window

Error is not reduced by the cost function, but evaluated by it.

"million training examples per category" is not always true, XOR is 4 examples for 2 categories.

Even a transparent "white box" algorithm is objscure if there are any weights or thresholds. E.g. 18yr age restriction is very clear but why 18? Also points based immigration or 24 points is politically motivated.

Brains don't forget, but smoosh ideas together.

"Some world model is needed", this is debatable. See animats.

"Geometry is important" - Add sensorimotor effects, such as how geometry changes as you take specific actions. Indeed shapes can be 'defined' by their unique pattern of distortions in response to various actions.

Episodic memory - No anticipation in ANNs

The brain isn't "henerating hypotheses about upcoming events" It's 'in a state' and anticipating all characteristic events.  Attention emerges from this state.

Is General AI a perpetual motion machine? If you make it you'd never turn it off.

There is a recurring assumptions that we infer context from objects. It's more natural to posit that we infer objects from context. Context is prior as it is always essential knowledge. Objects are only relevant depending on context.

Internal Representations are the entire problem. What aspects do you choose to represent? If it's context specific then how to detect context? Especially without objects? If it's a cycle "objects <==> context" then how to bootstrap?

# Role of memory
- Traditionally seen like a "film archive" or a database
- McKergow says it's to "re-member". To piece together a "what must have happened" or "what I feel happened"
- Freeman sees it as an invisible background to what you anticipate

"As babies we learn how the world works largely through observations" Suspect this was written by a man. Consider Feminist AI. Contextual + responsive. Anticipates what we meant to do, it corrects, and praises, but also does what you wanted.

# "Dench" "Bench" example

Can the AI even know how close it was?

There's no "removing bias", consider Dennett's Frame Problem. Knowing what is relevant that's bias. Else you die.

# high dimenstionality

A high dimensional orange has most of its volume in the skin. High dimensional spaces are 'large' and unintuitive.

# test/train cross-valuidate

XOR has a training set, then we introduced a test set, now we use a cross-valudation set. Why not a super duper final v3 set?

