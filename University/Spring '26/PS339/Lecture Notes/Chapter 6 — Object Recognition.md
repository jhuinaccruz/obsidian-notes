Spatial resolution, timing resolution, causality, invasiveness, sensitivity to neurotransmitters, etc.__Ventral__: The what pathway of recognition (into the temporal lobe)
- Inferior longitudinal fasciculus into the inferior temporal cortex

__Dorsal__: The where/how pathway of recognition (into the parietal lobe)
- Superior longitudinal fasciculus into the posterior parietal cortex

__The main goal of object recognition is__: Object constancy; objects will be viewed the same way regardless of environmental conditions

__Object Recognition__: The rapid processing of objects to determine what something is
- Takes about 150ms to process what an object is
	- As little as 50ms of a stimulus presentation is required for this
	- Takes about 70-80ms for the stimulus to reach the visual cortex
- Considered to be both a typical ability in humans as well as a remarkable ability when comparing to non-human and non-animal alternatives
- Recogntion involves massive amounts of data stored (from memories experienced)
- Occurs primarily in the ventral pathway (Occipito-temporal cortex)

__Thorpe et. al.__ (1996) (Categorization of Novel Images): Participants were presented for 20ms with a novel image of a natural scene, and asked whether there was an animal present or not
- *Result*: Participants had a 94% success rate in determining whether an animal was present or not, most within 300ms of the presentation
	- EEG imaging shows that the brain distinguishes between target/distractor within 150ms of the stimulus presentation
- *Conclusion*: The brain processes images quickly and in parallel, such that their processing is almost instantaneous
	- Familiarity does not increase speed of processing
	- Superordinate advantages exist (determining whether there is an animal versus a subcategory of animal such as a dog)
	- People can generalize animals even if they have never seen the animal before
		- Works for people too
	- Most recognition is a bottom-up feedforward process
		- __Feedforward__ (Bottom-Up): Anticipate future outcomes from past experiences

__MIT AI Lab__ (1966): A summer project for students had people solving the problem of general visual object recognition
- *Conclusion*: Just because something is "simple" for humans does not mean that they will be computationally simple for computers

__Brain Storage__: Estimated to be around 2.5 petabytes
- Each synapse is upper bound by about 4.7kb

__Mental Module__: A set of specialized circuitry within the brain dedicated to the processing of specific things
- Since most neuroscience methods reveal only a single brain region related to a specific tasks, it begs the question of whether the methods are purely causal or if they simply reflect the limitations in experiments and their methods

__Fodor__ (1983): Proposed that the brain has some self-contained modular components.
- These components are
	- Respond to specific things like language, etc. (domain specific)
	- A bottom-up process (cognition does not affect operation)
	- Fast processing
	- Do not rely on other information for its output
	- Outputs are basic and shallow
	- Do not need to map onto an anatomically-specific module; can be multiple networks/regions working together

__Domain-Specific__: Processing only a specific kind of input
- Occurs very fast; outside of conscious cognition

__Domain-General__: Processing a general kind of input
- Occurs slower; results in attentionally-demanding processes

__Visual Agnosia__: Cannot recognize higher-level objects by sight
- Unlike memory loss, they can recognize the same object later with other cues subconsciously

__Shape Processing__: Occurs in the Lateral Occipital Complex
- From studies with lesion patient D.F.
- Familiar and novel objects drive the LOC
	- Scrambled objects, on the other hand, do not

__Bilateral Temporal Lobe Damage__: In an explicit matching task, patients cannot orient cards to match the mailbox, but can place the card in a mailbox when asked to do so
- Can even do it off of memory with an imaginary card and an imaginary mailbox

__Inferior Temporal Cortex Specificity__: Single neurons in a monkey's inferotemporal cortex responds specifically to complex images

__Hierarchical Coding Hypothesis__: Lower-level neurons respond to low-level (general) features, where the highest-level of neurons respond to the most complex features of a object
- Used in computer visual recognition programs (Deep Convolutional Neural Networks), where models are trained on classified large datasets

__Gnostic Unit__: Neuron that can recognize a complex object

__Grandmother Cell Hypothesis__: A more extreme form of neuron hierarchy; single cells at the top of a hierarchy that respond to specific people
- However, this hypothesis does not hold up for novel objects or neuron plasticity
- Studies show that certain neurons in the medial temporal lobe respond to specific people
	- However, the neurons responded to these specific people because the MTL responds to concepts rather than perception

>*MTL generally considered to be a memory region, not a visual region*

__Ensemble Coding Hypothesis__: A group of neurons codes high level features by working together like an "ensemble"
- Leads to a more flexible model where multiple neurons can fire together and rewire together when needed

>*Thorpe's conclusion about recognition being a bottom-up process must have some aspects of implicit memory/stored representation, implying some top-down processing as well, since recognition seems to require the use some previous memories, even if in a short period*

__Top-Down Feedback in Rapid Object Recognition__: In an MEG study, there is evidence that the left prefrontal cortex activates before the fusiform gyrus such that
```mermaid
---
title: Top-Down Feedback in Rapid Object Recognition
---
flowchart LR

	A[Early Visual Areas]
	B[Orbitofrontal Cortex]
	C[Fusiform Gyrus]
	A-->B-->C
	A-->|Ventral Visual Stream|C
```
- This leads to the idea that low spatial frequency information races ahead before the rest of information to guide the processes related to matching objects to memory

 __Face Inversion Effect__: Unlike other objects, face recognition is harder when the image is inverted/upside down

>*Face perception is very sensitive to orientation*

__Thatcher Illusion__: Face distortions are less obvious when the face is upside down

__Prosopagnosia__ (Faceblindness): Cannot recognize faces including their own
- Can still recognize standard objects as normal
- Usually associated with Ventral Temporal Lobe damage
- In double dissociation studies with agnosiacs, there is damage to lateral occipital cortices for agnosiacs, whereas prosopragnosiacs have more anterior damage
- Usually associated with ventral temporal lobe lesions
	- Can be congenital (Congenital Prosopagnosia); about 2% of the population

__Super Recognizer__: 1-2% of people can recognize more than 80 percent of faces that are seen
- Substantial differences across super-recognizers themselves

__Kanwisher, MCDermott, and Chun__ (1997): One of the most cited studies in neuroscience; shows evidence for a specialized face module in the right fusiform gyrus
- __Fusiform Face Area__: A part in the right fusiform gyrus that responds especially for faces

__N170__: Face-specific event-related potential that occurs at around 170ms after the presentation of faces
- Stronger variability occurs for emotional faces especially
- N170 is a neural marker for face recognition processes

__Schalk et. al.__ (2017): A patient had strips of electrodes implanted bilaterally along his fusiform gyri, stimulating both the fusiform gyri and the adjacent color processing areas (V4)
- The study itself is causal evidence of the face fusiform gyrus

__Face-Processing Network__: The fusiform face area (Ventral Temporal Lobe) with the occipital face area and the superior temporal sulcus

__Visual Word Form Area__: Localized in the left fusiform gyrus; works to support the sight reading of words
- Unlike the facial areas of the brain, literacy (reading and writing) is too recent of a development in human history to be an evolutionarily-driven feature unlike face processing
	- A theory suggests that the brain (during development) specializes this area of the brain (that would have otherwise been dedicated to something else) to focus on literacy

__Computational Models of Object Recognition__:
- Artificial Intelligence: Intelligence from a non-biological entity
- Encoding Model: Outputs modeled as brain activity are created based on an input(s) of stimulus
- Decoding Model: Outputs modeled as stimuli are modeled based on inputs of brain activity
	- Functions as a machine-learning model of data analysis through methods such as MVPA