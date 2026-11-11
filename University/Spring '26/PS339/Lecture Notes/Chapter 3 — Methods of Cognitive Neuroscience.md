__Cognitive Neuroscience Experiments__: Must combine
- A cognitive measure (such as performance, reaction time. recall, etc)
- A brain measure (such as anatomical or physiological measurements of the brain)

__Most experiments establish__: Correlation, not causation, due to the nature of the experiments
- Experiments must have a direct manipulation on the brain measure in order to have a causative relationship

__Causation__: When the brain measure is the cause and the cognition is the effect
__Correlation__: When the cognitive measure is the cause and the brain is the effect

__Tuskegee Syphilis Study__ (1932-1972): An unethical study by the US Public Health Service and CDC meant to study the natural history of untreated syphilis using 600 African-American men (most of whom were poor sharecroppers)
- Did not provide any treatment to them even after penicillin was discovered to be an effective treatment
- Told by the government they were getting free health care

__Ethical Principles and Guidelines for the Protection of Human Subjects of Research__: As an answer to the Belmont Report of 1979
- Respect of persons
- Beneficence
- Just selection of research participants

__Animal Subjects__: Usually in combination with behavioral studies, used as a model for human cognition study
- Assumes that the species possesses similar cognitive function within comparable and similar brain structures

>*Many animal neuroscience experiments are* not *cognitive*

__Institutional Animal Care and Use Committee__: (IACUC): Required for any institution using live vertebrate animals in research

## Cognitive Psychology Research Methods
__Research Methods__:
- Controlled laboratory experiments
- Self-reports
- Neuropsychological tests
- Case Studies
- Naturalistic Observations
- Computer models

__Patterns of Error__: Can be informative (rules are learned whole, whereas exceptions are learned individually)

__Dual Task Paradigm__: An experiment where two tasks are performed simultaneously, then performance is compared across single-task conditions
- Some tasks compete with one another (e.g. visualizing from memory and visual search)
- Other tasks are independent from one another (e.g. humming a tune from memory and visual search)

>*Cognitive resources are limited and shareable but divided into separate classes*

__Cognitive Subtraction__: A method of measuring the time for a process to occur by comparing the reaction time of a control vs the process of interest such that
$$
\text{Reaction Time} = \text{Target Time} - \text{Control Time}
$$

__Stages of Stimulus Transformation__:
1. Encode
2. Compare
3. Decide
4. Respond

__Parallel Processing__: Many-at-once (denoted by a zero slope line on a reaction time graph)
__Serial Processing__: One at a time (denoted by a non-zero positive slope line on a reaction time graph)

__Mental Rotation experiment__: Famously run by Shepard and Metzler in 1974, it involved asking people if two objects are identical or mirror images even if rotated.
- Concluded that objects were mentally rotated with a constant speed of about 60 degrees per second

__Ceiling Effect__: Compression at the top end of the response range
__Floor Effect__: Compression at the bottom end of a response range

>*Floor and ceiling effects can negatively impact accuracy, reaction times, and more*

__Resolution__: The smallest distinguishable difference, can be in time (temporal) or space (spatial)
__Field of View__: The extent of observations

__Resolution/Field of View Trade-Off__: HIgher resolution leads to a smaller field of view

__Electrode Recording__: Can be recorded from a single unit or multiple units, usually only from one specific brain area

__Calcium Imaging__ (in animals): A tool used for indirect imaging of electrical activity of cells using the fluctuations of fluorescent calcium-based transients through fiber photometry (a kind of microendoscopy)

__Optogenetics__: A causal methods that activates or shuts off sets of neurons in live mice by shining a light onto a portion of their brain

__Single Dissociation__: A research method of identifying a specific brain lesion impairs one function but leaves another intact

__Double Dissociation__: A research method of identifying two different lesions, where two groups have only one of either lesion, ideally resulting in people exhibiting opposite patterns of deficits

__Structural Imaging__: Using computer-based imaging to visualize changes in brain structures
- Computed Tomography (CT): Uses X-ray imaging to create cross-sectional detailed images of the structures within
- Magnetic Resonance Imaging (MRI): Uses the resonance of strong magnetic fields and radio waves to create images of structures within the brain
	- Magnetic fields within the machine causes proton alignments
	- Known as the best structural imaging technique of the brain
	- Non-invasive
- Diffusion Weighted Imaging (also known as Diffusion Tensor Imaging or Diffusion Spectrum Imaging): A technique used by mapping out the random movements of water throughout the brain to create high-contrast MRIs

__Human Functional Methods__:
- Scalp recording of evoked brain potentials
	- Electroencephalogram (EEG): Records the change in electrical potentials in the brain based on the changes in neural activity
		- Records populations of neurons rather than single ones
		- Negative signals reflect a positive change in neurons and vice-versa
		- Classically studied by the resulting waveforms
	- Magnetoencephalogram (MEG): Non-invasive high-resolution imaging that maps brain activity through measuring magnetic fields from neuronal electrical circuits
		- More expensive and spatially precise than EEG
	- Can be used in conjunction with an EEG
- Intracranial EEG (eCOG): Occurs when a sheet of electrodes are surgically implanted through an electro-cortigram
- Functional Neuroimaging
	- Positron Emission Tomography (PET): Measures metabolic brain activity via radioactive labels with a short half-life with a passive scanner of gamma ray sensors
		- Can also label neurotransmitters not just glucose or oxygen
	- Functional Magnetic Resonance Imaging (fMRI): Essentially a fast MRI, uses hemoglobin as the endogenous contrast agent
		- Is non-invasive and has a good spatial resolution (<1mm), but only works as an indirect measure with a modest temporal resolution
		- Hemoglobin carries oxygen to the brain
			- Oxy- and deoxy-hemoglobin have different magnetic states, such that bold signalings reflect the volume and concentration of hemoglobin

__Pyramidal Neurons__: Shaped like pyramids, has apical dendrites that go through the top and through the cortex

>*Biological natural signals have a pink noiseband*

__Pink Noiseband__: Denoted as
$$
(\text{Power} = P(f)) \propto \frac{1}{f}
$$
where `f` is frequency and `α` means the slope.
- In EEGs this equation is the baseline for the slope of an EEG graph, where its oscillations are specific rhythms on top of said slope. However, in practice the equation changes to
$$
P(f) \propto \frac{1}{f^\alpha}
$$
	where the slope is more variable based on `α`

__Noise band__: A specific frequency range containing mostly noise


| Brainwave Type  | Frequency Range | State of the Brain                                     |
| --------------- | --------------- | ------------------------------------------------------ |
| Delta           | 0.1Hz to 3Hz    | Deep, dreamless sleep                                  |
| Theta           | 4Hz to 7Hz      | Intuitive, creative, recall, fantasy, imaginary, dream |
| Alpha           | 8 to 12Hz       | Relaxed but not drowsy, tranquil, conscious            |
| Low-range beta  | 12 to 15 Hz     | Relaxed but focused                                    |
| Mid-range beta  | 16 to 20Hz      | Thinking, aware of self and surroundings               |
| High-range beta | 21 to 30Hz      | Alertness, agitation                                   |
| Gamma           | 30 to 100Hz     | Motor functions, higher mental activity                |
>*Parietal alpha activity is correlated strongly to inattention*

__Event-related potential__: Small amplitude signal in response to specific events; usually averaged over at least 70 trials

>*The fundamental limitation to spatial localization of EEG/MEG is that the results are in two dimensions when the brain is in three dimensions*

__Inverse Problems__: There is no unique solution to map surface data (in 2-D) to brain activity (in 3-D)
- Some assumptions can be made about the brain

>*The same subtractive principles used to analyze reaction time data are often applied to analyze fMRI and PET neuroimaging data*

__Voxel__: 3-D pixel

__Region of Interest__ (ROI): A defined cluster of voxels that are examined together

__Block Design__: Different conditions are presented in long alternating periods, where a task is performed for a long period, followed by a period of rest/different task
- Occurs because of the slower hemodynamic response

__ROI Analysis__: Focus on a predefined cluster of voxels

__Resting-State fMRI__: fMRI with no explicit task to perform
- Fluctuates together over time

__Subsequent Memory Task__: Posterior left inferior gyri and parahippocampal/fusiform gyri shows more activity remembering/forgetting

>*Does neural data contain predictive information about an aspect of cognition?*

__Multivoxel/Multivariate Pattern Analysis__: Uses machine learning to analyze ROIs

__fNIRS__: Functional Near Infrared Spectroscopy: Uses light through the skull/scalp to measure blood oxygenation
- Not very good; low brain signal, noise, spatial limitation like EEG, time limitations like fMRI
- Used in kids or for people who cannot tolerate more invasive methods

__Causal Methods__: 
- Invasive Methods
	- __Surgical Lesions
	- __Genetic Knockout__:
	- __Optogenetics__:
	- __Electrical Stimulation__:
	- __Pharmacology__:
- Non-invasive
	- Transcranial Magnetic Stimulation (TMS): A handheld wire coil in the shape of a figure eight is placed against the scalp, creating a powerful magnetic field. The magnetic field passes through the skull and induces a secondary current through the neurons, exciting or inhibiting the specific brain region, creating a transient lesion
		- __Transient Lesion__: A
	- __Transcranial Alternating Current Stimulation__ (TMS):