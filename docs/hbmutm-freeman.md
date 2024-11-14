Chapters
1. Self-control and intentionality
1. Meaning, representation and intentionality
1. Dynamics of neurons and neuron populations
1. Sensation and perception
1. Emotion and intentional action
1. Awareness, consciousness and causality
1. Knowledge and meaning in societies
# Self-control and intentionality
 We necessarily exist isolated, but have means of making ourselves understood.
 The brain is like a network of collaboration-by-consent networks. Each one choosing for itself whether to listen or ignore certain channels.

Meaning will always be uninterpretable from outside due to its uniqueness and complexity. To discover otherwise would be to have redefined meaning.
Meaning can be shared between those who participate in neuro-regulatory actions like dance, chant or hallucination.

Mental representation is distinct from a mental state.

Representations exist in the world but have no meanings, and meanings exist in the brain absent of representation.

Most actions are performed without being explicitely aware of them.

The big problem is making sense of the stimuli, and this can be done in one of two ways, i) full parsing of all signals, ii) context sensitive interpretation of a portion of the data.

# Meaning, representation and intentionality

all meaning is attached to the perseption, the odour, and not the stimukus, the odorant.

the internal is private, like a compiled binary for a unique architecture.

start with smell


how to be selective, selectively?

The neuron doctrine treats macroscopic activity as a meaningless epiphenomenon.

stimulus patterns are not fixed. learning a new pattern makes all other patterns change.

the response to a stimulus changes as the meaning of an experience changes, even for an individual.

1. plato. ideal forms to be accessed in the mind
1. Descartes. primacy of thought.
1. kant. we know only through categories. we know the world through mental representations.

Perception must not be just the passive reception of forms but a circular relationship between actions of the body and the modification of forms.
Perception is only *of* the altered surface of the self, never of any external forms themselves.
We can share an idea like Pythagoras's Theorem quite successfully, but what it means to each individual is totally unique. Meanings are internal and may as well be compiled binaries for a unique architecture.
The self 'assimilates' objects, that is it makes parts of itself similar to aspects of the world.

stimulii -> Anterior
motor -> lateral
association -> medial
All senses reach the Anterior via relays in the brainstem except smell, which is directly connected.

A hemisphere of the forebrain has three sections, roughly stimulii, motor, and association. Anterior, lateral, medial. All senses reach the Anterior via relays in the brainstem except smell, which is directly connected. In humans the association area is the hippocampus. These sections make up the limbic system.

Without a limbic system you can chew food placed in your mouth, walk when lead, and maintain homeostasis. But you don't do anything volitional. With only a limbic system in the forebrain you are severely incapacitatied but your actions are unmistakably intentional.

How might you implement preafference in an ANN? This is when you pass detail about the intended action to the ann which is reciving input, so it can anticipate the volitional changes, and separate them from any external changes.

"The assembled activity is unified, whole and purposive". This quote is a nice contrast to the idea of activity being abstract and only theoretically applicable.

You can destroy parts of the brain, such as the left lateral hemisphere for language, the ventral frontal lovbes for social behaviour, and so on for blindness, deafness, paralysis, aphasia, but remain intentional, albeit with less meaning. Advanced Alzheimers can sever that final link. Destruction of the medial temporal lobes in both hemispheres, means you retain intentionality, but lose "episodic memory" the ability to take experiences as a meaningful whole, the whole "integration" part is gone.

# Chapter 3

Each cell is like a person in a society, infinitiely complex and unable to function outside of the whole.

A neuron has dendrites which look like a bush or a tree, splitting multiple times. Each neuron has exactly one axon. In the language of Python type hinting `dentrites: Tree[Position], axon: Position`

In the cerebral cortex there are two types of neuron, projection neurons and local neurons. Projection neurons have dendrites which spread over up to 1mm, the main trunk will point to the surface of the cortex, and three or four other branches point "sideways". The Axon can be up to 1 meter! Each axon has "side branches" called Axon Collaterals. Local Neurons has dendrites over an area up to 0.1mm (25-50 cell body widths) evenly spread in all directions.

Neurons mostly have all excitatory or inhibitory synapses. Projection neurons are mostly excitatory.

"several thousand" synapses on each neuron.

Most important state variables for a neuron, i) potential across the membrane (indicating an axon), ii) potential across the tissue around it (indicating a dendrite). 

Neurons have dendrites which have switches at their membranes, turned on at synapses, which causes current to flow. This current is integrated in the cell body which determines the frequency of the output from the axon. The axon has an output train of pulses, which can increase in frequency, but cannot be superimposed due to the refractory period of a neuron.

The movement of current from the synapse to the cell body causes a potential across the membrane. The current flows to the cell body, which then flows in the opposite direction, outside of the neuron back to the synapse at the dendrite. The current flowing within a single neuron can be detected with two probes on the membrane, and represents the activity of a neuron. The current flowing outside of a neuron can be detected with two neurons in the "neuropil" which surrounds the neurons and represents the activity of a population of neurons.

There is no attentuation in the pulse train. There is loss of power with dendritic synapses which are further away from the cell body. But there is room for more synapses at a larger distance.

The minimum pulse rate for a healthy neuron is 1 per second.

Neurons are stimulated like an S-curve by pulses, the first few are highly stimulating, then there is a linear relation, following that pulses become less stimulating.

A population of interconnected inhibitory neurons will maintain a steady state of pulses as one neuron inhibits the other and in doing so reduces the inhibition onto other neurons, this brings those other neurons into activity, and they start inhibiting the original neuron. Similarly positive neurons lead to a steady state as each neuron stimulated more activity out of each other neuron until they are all firing at the maximum rate a neuron can achieve. Given a mix of stimulatory and inhibitory neurons a steady state will be achieved but with a rate somewhere between the maximum and minimum firing rates, ideally at the rate where there is a linear relation between pulse trains.

Autofeedback (one neuron stimulating itself) need not be considered as each neuron has around ten thousand outputs and around ten thousand inputs, so a neuron train from one more neuron will not make a significant difference.

Sensory neurons don't have any interconnections, rather they transmit in parallel.

One thousandth of a second is a reasonable temporal resolution for a neuron state space.

In populations, wave-pulse conversion is always nearly linear.
