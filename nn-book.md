
AN INTRODUCTION TO NEUROSCIENCE AND NEURAL NETWORKS
---------------------------------------------------

INSERT QUOTE HERE
- from Frankenstein by Mary Shelley

We are the inheritors of the Frankenstein myth, pressing beyond AI, towards the
synthetic a priori. Computers and robots: programs and expert systems aren't
enough.  After forty years of AI, it seems the procedural-declarative if you
can describe it, you can program it dictum of von Neumann is insufficient to let
us create intelligence. The problems so easy for us, and so difficult for a
computer - perceiving speech, recognizing shapes - are not necessarily
describable in precise a implies b language. On the other hand, the neural
processes underlying talking and moving and blinking and hearing, and the
interactions of the neural processes, are conceivably describable (even if only
probabilistically). And, if the underlying processes are describable in precise
enough language, we can simulate them on our machines. And so, let's seize
the gauntlet hurled in the face of Nature - the Medieval alchemist's homunculus,
the Golem, Shelley's Frankenstein, modern computers, robotics. Let's truck with
Devils, and build ourselves a Brain.

This book presents an overview of how the nervous system does its processing -
the retina and vision, the cochlea and hearing, and so on. It describes the
work of many researchers: the historical work that led to our present day
understanding of neural networks, and modern neuron and neural network models.
It describes the results of a few experiments and explains how to do them, and
it presents a few observations and hypotheses just for the fun of it.

This is the book that I wished existed when I began researching neural networks
in 1987. My background is in systems analysis, software engineering, and
robotics, as well as the softer sciences of art and music. These betray my
interests, and consequently, the tone of this book.

In 1987, the field was still young. Neural nets were being hyped in a way
reminiscent of the Perceptron excitement of the 1960's, only this time people
were claiming breakthroughs that went beyond the problems which had almost killed
neural net research twenty years earlier. In 1987, there had been few major
conferences on neural networks, and there weren't all that many researchers.
The reference works were research papers sprinkled through a variety of
academic and trade journals and a few textbooks, and certain common themes were
just beginning to emerge.

The trouble was, I couldn't find an introduction that gave a broad,
multi-sided view - a view detailing physiology and computation and evolution and
all the little details that when taken as a whole give a view as to how the brain
does its processing in relation to how brain-like processing could be implemented
on a machine. I wanted a do-it-yourselfer's guide, and particularly one that
gave an overview with cross-disciplinary peeks, instead of a tunnel-vision look at
a single paradigm or set of ideas.

Everyone has a different tack, a different focus; yet, certain common themes
appear over and over again - the physical distribution of memory and behaviour
through the brain, self organization, the minimization of energy, principles of
lateral inhibition and information focussing.

It began as a hobby - reading through a mountain of papers and texts, trying to
grasp the common thread - but as I began collating and sifting, my notes gradually
began to look less like a random collection of thoughts from here and there, and
more and more like a book.

I hope I have tied the many threads together in a coherent fashion, and that this
book will provide both an easy start into the field of neural networks, and a
useful reference work later.

Build a scaffold, flesh it out, discard what no longer fits - a theory emerges.
- paraphrasing Marvin Minsky (1987)

Stephen Grossberg (1980) suggests that researchers "respect the wisdom of
evolution by trying to imitate it." When the environment shapes the theory,
oversights caused by the researcher's biases are more likely to be avoided.
Observation of natural phenomenon can lead to thought experiments which can help
to define how natural mechanisms can account for particular behaviours. When the
hypothesized mechanisms can predict real behaviours, mathematical analyses can
show how they work together. Synergisms between simple mechanisms result in
more complex behaviours, and possibly will lead one day to intelligence.

With the goal in mind of eventually developing autonomous synthetic
intelligences, a carefully thought out plan is required. The plan could take the
form of a conceptual map, with a very concrete departure point in the body of
neurophysiological and neuroethological data.

The first step is to make general diagrams delineating functional demarcations;
and of course, most systems will be black boxes. Black boxes can be elaborated
as theory and technology allow. At first the diagrams will be vague, but as
subsystems are developed and subsequently improved, functionality of the model
systems will become more precisely defined and characterized. Along the way,
many practical applications will result in a variety of areas.


HERE IS A NEURON

DIAGRAM NEURON

Neurons are the basic processing elements of any nervous system. Input arrives
at the neuron through the synapses which are located all over the cell, and the
principal output is from the axon. From the axon through subsequent synapses,
a single neuron can affect a great many others. There are so many connections
going in and out of every neuron (anywhere from 100 to 100,000), that some theorists
suggest that no neuron is ever more than four neurons away from any other.

This diagram shows the activity of a neuron over time, in terms of electrical
potential. A neuron carries a small electrical potential, caused by the difference
of ion concentrations inside and outside the cell. This potential is maintained
and controlled by ion channels which pump molecules such as Sodium and Potassium
across the cell membrane.

The fluid that surrounds neurons is filtered blood. The neuron's soma (body)
takes glucose from the surrounding fluid and synthesizes adenosine triphosphate (ATP).
ATP is the fuel which drives the ion pumps and all the cell's activity.

Signals from other neurons are transmitted via the synapses. Neurotransmitters
are released at the synapses and taken up by the dendrites of other cells. As
neurotransmitters are released and received, the potential within the soma changes.
As signals arrive at the neuron, and through the regular functioning of the cell, the
potential inside the cell body builds up until finally the cell will fire, propagating a
spike down the axon, guided by the opening and closing of ion channels within the
axon. This propagating spike is called the neuron's action potential.
The cell's internal potential then falls below the resting level, and the neuron
undergoes a refractory period when it is inhibited from firing again. The action
potential is an all-or-none signal, and can thus be considered digital. The
outputs of interneurons are analog or graded, because interneurons often have no
axons, having output synapses on the dendrites instead.


NEURON                 INTERNEURON

Because each arriving signal at a neuron tends to increase or decrease the 
likelihood of that neuron firing, a neuron is generally considered to perform some
sort of weighted summation of signals arriving at the synapses, and to produce an 
all-or-none response, the action potential, at the junction of the cell body and 
the axon when that sum crosses some particular threshold. This vastly simplified 
view of the neuron is the basis of most models today. It describes everything from 
Threshold Logic Units which were the precursors of modern digital electronics, to 
Adaptive Filters which permeate every aspect of the communications industry. High 
speed digital modems, for example, use an adaptive filter to achieve speeds that 
wouldn't be otherwise possible due to noise and distortion that are always present 
on telephone lines.

In comparison to these models, real neurons are frighteningly complex. The usual 
model of the neuron assumes all input arrives via the synapses on the dendrite 
tree, but a real neuron has synaptic inputs everywhere: on the dendrites, on the 
cell body, and on the axon. Sometimes synapses form connections onto other 
synapses. Every synapse makes some contribution to the performance of the neuron.

Models usually assume very simple synapses; they are either excitatory (predisposing 
a neuron to fire) or inhibitory (discouraging it). Sometimes a model will have 
two different types of synapses, one for each behavior. In reality, synapses do 
tend to be either excitatory or inhibitory, but a great many variations exist. 
Recent research suggests that synapses can change their character rapidly over the 
course of time, being predominantly excitatory or predominantly inhibitory, but 
capable of switching to the other mode at any time. (cf. von der Marlsburg's 
transient cell assemblies.)

Communication between neurons is principally electrical. The axon is like a wire 
conducting impulses, and in many places, the axons are organized in parallel 
bundles. Naturally, current flowing through a conductor evokes an electromagnetic 
field, and the neurons in that field will be affected by it. If many axons are 
bundled together, it is natural that their fields would interact, perhaps 
causing the axons to share similar behaviour. This is called cellular field 
coupling. Other significant field effects are provided by hormones, the 
availability of neuro-modulators, and so on.

Further complicating attempts at modeling neuronal systems is the matter of 
cell type diversity. Here is a small sampling:

Basket Cells

DIAGRAM BASKET CELL

Named for its shape, the basket cell tends to inhibit or veto a great number of 
neighbouring cells. This function could conceivably help to organize the brain 
into functional columns. Columnar organizations play important roles in most sensory 
processing. In the cerebellum, basket cells generally synapse with a half dozen 
Purkinje cells.

Purkinje Cells

DIAGRAM

Purkinje cells are the only cells whose axons leave the cerebellum, and are 
therefore the only way the cerebellum has of influencing other brain structures. 
The Purkinje cell axons terminate in the deep cerebellar nuclei which lie under 
the cortex. Because the Purkinje cells are GABAergic, and therefore inhibitory, 
the cerebellum can only exert an inhibitory influence on other parts of the 
brain (Gottlieb, 1988). The principle of controlling behaviour through inhibitory 
influence is a common one in Nature; as an example, the insect brain influences 
various ganglia mainly through inhibition (see Chapter 9).

Golgi Cells

DIAGRAM

Glial Cells

DIAGRAM

Glial means glue in Latin, and that points to the function of the glial cells. 
Glial cells occupy the space surrounding other neurons; in fact, they comprise 
up to half the mass of the brain. Depicted here are astrocytes, named for their 
star shape. During ontogenesis, astrocytes serve as a scaffolding over which 
neurons can migrate to their places during early nervous system development. 
Astrocytes are also involved in neurotransmitter metabolism.

Glutamate (GLU), an excitatory neurotransmitter, and Gamma aminobutyric acid (GABA), 
an inhibitory neurotransmitter, are released in the synaptic cleft when a signal 
is transmitted, and then taken up by the astrocyte, converted to glutamine (GLN) 
by glutamine synthetase (GS), and then returned to the neurons where it is used 
to make new neurotransmitters. Ammonia (which is toxic) is consumed by this 
process, and the toxicity of the brain is controlled. (diagram and description 
adapted from Kimelberg and Norenberg, 1989)

Motor Cells

DIAGRAM

Pyramid Cells

DIAGRAM

Pyramid cells are relatively large cells found in the cortex, named for their 
shape. The axon of the pyramid cell extends from the neuron's apical surface and 
branches out into a cone-like volume. The dendrites are extended as a sphere 
around the neuron. Some eighty percent of the neurons in cortex are pyramid cells, 
interconnected mostly by excitatory synapses (Braitenburg, 1990).

Sensory Cells

DIAGRAM

Pictured here from left to right are auditory sensors, smell sensors, stretch 
receptors, and touch receptors. The auditory cells receive stimulation from hair 
cells in the basilar membrane.  The touch receptor has inputs in amongst the 
epiphelium layer of skin cells.  The stretch receptor has inputs entwined around 
muscle fibres.

Stellate Cells

DIAGRAM

Stellate cells are named for their star-like shape.


THE NERVOUS SYSTEM
------------------

The complexity of nervous systems run a gamut from the almost random arrangement 
of the lowest animals to the highly organized nervous systems of the primates and 
cetacea. It is a smooth gradation, one level of organization shades smoothly into 
the next higher, and the capacity for learning and intelligence increases ever so 
slightly at each step.

DIAGRAM THE VARIOUS NERVOUS SYSTEMS

	At the very lowest level are animals like sponges which don't have a nervous network, but rather have neurons scattered randomly throughout the body. The nervous system of the starfish has a simple ring organization, which is an order of magnitude improvement over the sponge. There is no central control in the starfish, but it is capable of much more complex behaviour.  Rodney Brooks’ “subsumption architecture” demonstrates that useful and interesting behaviour can emerge from a completely decentralized system (Brooks, 1989).

	The next step is the ladder structure found in the protocordates. They have a simple nerve cord studded with large ganglia (groups of cells ).  Examples of this class are the leeches and worms. There is a ganglia dedicated to the control of each segment of the animal, and a thickening in the head of the animal called the cerebral ganglia, which moderates the activity of the nerve cord through selective inhibition.

	The next step above the protocordate is the insect. As the structure of the insect becomes more complex, the ganglia along the nerve cord migrate towards the head of the insect, until a primitive brain is found in the most sophisticated insects. The insect's brain is called the corpora pedunculata, or mushroom body. As an aside, it is an interesting point that there is a direct correspondance between the level of social behaviour of certain insects and brain size: in termites for example, the most sophisticated termite hill architecture is produced by the species with the smallest brains, and therefore the simplest individual behaviour. Building termite hills is a parallel distributed process...

	The cephalopods - the squid, octopus, and so on - are the next level. The cephalopod nervous system reaches its highest development in the octopus. Cephalopod tentacles have somewhat independent nervous systems because there is too much information to be handled by the central nervous system. Each tentacle is roughly as intelligent as a worm. The major improvement made by the cephalopod brain is the functional subsystem: specialized cortexes and nuclei exist for motor control, sensory integration, and so on.

	Above the cephalopods are the vertebrates, where the highest development is found in the primates and cetacea. Association cortex is larger, there are more functional subsystems, the resultant behaviour is far more complex. The vertebrate brain is stereotypical from species to species with specializations to suit an organism's particular niche. As an example, the bat has an extremely well developed auditory cortex. A curious exception to the usual plan is the brain of the cetacean, which in addition to left and right hemispheres also has a third lobe called the paralimbic lobe. Due to the difficulty of studying aquatic species, little is known about its function.
	The human brain has billions of cells, commonly estimated to number on the order of ten to the tenth. The nervous system is comprised of hundreds of systems - nervous networks - organized by function.



	The cerebral cortex is where we imagine thinking and memory take place. It is subdivided into many different functional subsystems, from the visual cortex at the back of the had, to the motor cortex on top, to association cortex or frontal lobes.

DIAGRAM LIMBIC SYSTEM AND BASAL GANGLIA

	The limbic system is comprised of hippocampus, cingulate gyrus, septum, and amygdala. Hippocampus appears to be associated with conditioning, and the limbic system in general is concerned with behavioural strategy.
	The hypothalamus and pituitary are involved with the control and production of hormones.

	Sitting on top of the brain stem is the thalamus, which is often called the gateway to the brain because all sensory information (except for smell) goes through it.  Cells of the Red Nucleus have forward connections via the thalamus to the cortex, and also posterial connections with spinal motor neurons through the rubro-spinal tract. The cerebellum is at the base of the skull, and helps coordinate movement commands from the motor cortex. The spinal chord routes information from all over the body through to the cerebellum and the thalamus, and also governs many reflex actions such as jerking away from fire.
	Other major nerve centers not located in the brain itself are the solar plexus and the spinal ganglia which have a great deal to do with how we feel at any particular time. Of course, there are an incredible variety of systems not even mentioned here, and we'll go into a few of them later.

DIAGRAM CNS

	The cerebral cortex is divided into two parts (the so-called left and right brains) connected by the corpus callosum, a vast bundle of nerves connecting the two halves of the brain in a symmetrical fashion - the connections are essentially mirrored from left to right.  The cortex is essentially flat, organized into functional columns. As a space saving measure, the cortex is very wrinkled, and has an approximate fractal dimension of 2.5. For comparison, a wadded ball of paper has a fractal dimension of about 2.3, and if you really pack it tight, it has a dimension of 2.7 because it almost fills the 3 dimensional space it occupies. A fractal dimension of 2.5 describes an object half way between flat (2-space filling) and a 3-space solid, and in fact, if the grey matter of the cortex could be flattened out into two sheets, each would be several millimeters thick (connected by the corpus callosum), and about a hundred centimeters square each. Half the thickness is wiring (the white matter), the rest is processing (the grey matter) (Mead, 1987).
	If we look closely at the organization of neurons in the cortex, we would find a highly regular and general structure. Cells are organized into small functional units called cortical columns. Each column is composed of many hundreds of neurons, all highly interconnected, and every column is highly interconnected with its neighbours. It is interesting to note that not only is the organization of the brain general and regular, it is also most probably self-similar (or fractal) on both micro and macro scales.

DIAGRAM CORTICAL COLUMNS

	When we study large numbers of neurons, close up like this, we are studying neural networks.



.c21.3: HERE ARE NEURAL NETS


	This diagram shows the instantaneous potential between a number of neurons arranged in a one-dimensional network. The pattern extant in a network at any time is probably unique to that nervous system at that particular time and will never be repeated, but the pattern of activation in a network represents information. In a two-dimensional array, we could show the instantaneous potential by assigning shades or colors or sizes to the units representing neurons.

	When studying neural networks, methods of showing the activity of the network are vitally important, because the sheer volume of information in anything larger than a trivial network can be difficult to grasp.  It's all very well to show a particular activation or an individual neuron, but does the representation show the relationships between the different neurons? In a system with normalized weights, for example, a useful display might show vectors, one for each neuron, radiating out from the origin.






This picture shows a Hinton diagram, named for Professor Geoffrey Hinton of the University of Toronto. The sizes of the squares represents the level of activation of each neuron, and the colour of the square represents the sign of the activation: positive or negative.

	This diagram shows a way to represent the weights and activities in a three layer neural network. This type of representation is a result of work by (GET REF HERE, 1989). The size of a unit represents the level of activation, and the length of the vectors extending between units represents weights.

DIAGRAM BACKPROP NET

DEFINITION OF NEURAL NETWORK FROM HECHT-NIELSEN 1989, WITH CAVEATS.

	There are several varieties of neural networks:

m	Autoassociators -which can perform pattern recognition and pattern completion.
m	Associative Networks - which can associate one vector with another, and can also perform 	categorization and generalization.
m	Mapping Networks - which map input space onto output space. Back Propagation is a
 	member of the mapping network class.

m	Optimization Networks - of which class the Hopfield network is a member.

m	Topographic Networks -The body, for example, is mapped onto the cortex and this mapping
 	is often shown in psychology textbooks as the sensory homunculus.




	This diagram shows the sensory cortex of the raccoon (adapted from Welker and Seidenstein, 1959). The numbers correspond to the raccoon's fingers, from thumb to little finger, and the letters correspond to the pads on the palm of the hand.

DIAGRAM A HOMUNCULUS

	Of course, there is no homunculus, no disembodied observer, lurking inside the brain, but the diagram gives a useful impression of exactly how a topographic mapping works: neurons are assigned according to the topology and statistical distribution of the input. Two dimensional topographic maps are used extensively throughout the nervous system: the homunculus diagram maps the somatosensory system, the retina is mapped (many times in retinotopic maps), and there are even two dimensional maps in the audio cortex for perceived frequency.
DIAGRAM FREQUENCY MAP


.c21.4: COMMON USES FOR NEURAL NETWORKS

	Neural networks are used wherever an analysis must be done of a complicated nonlinear environment. They can easily perform nonlinear statistical analysis, and often exceed the performance of traditional classification and analytical methods.
.c
ROBOTICS:
m	Automation Control
m	System Control Dynamics
m	Path Planning
m 	Navigation and Obstacle Avoidance
m	Multiple Sensor/Actuator Integration, eg: 	   vision-manipulator coordination
m 	Adaptive Platform and Effector Dynamics
m 	Goal Seeking Behaviour
m 	Autopilot
m	 Microrobotics
m	 Emergency Response Behaviour




ENGINEERING:
m 	Circuit & VLSI Design and Layout
m 	Opposing force and relaxation models

SIGNAL PROCESSING:
m 	Adaptive Filtering and Gain Control
m 	Signal Extraction, Enhancement and 	  Classification
m 	Noise Suppression
m 	Pattern Recognition
m 	Error Detection and Correction
m 	Significant Feature Analysis, Data 	  	  Compression, Data Reconstruction


KEY:
m 	Well studied
m 	Current research
m	Future investigation



VISION:
m 	Edge Detection
m 	Elimination of shading gradients across 	  curved objects
m 	Pattern Recognition
m 	Character Recognition
m 	Image Enhancement
m 	Image Reconstruction and Restoration
m 	Image Segmentation
m 	Image Understanding
m 	Target Acquisition and Tracking
m 	Surveillance and Security Systems
m 	Acoustic Imaging
m	2D and 3D Graphics Entry and 	  	  Manipulation

DATA PROCESSING AND BUSINESS:
m 	Statistical Analysis
m 	Pattern Recognition
m 	Voronoi tessellation
m 	Fleet vehicle scheduling
m 	Airline seat booking
m 	Securities Analysis
m 	Loan Risk Analysis
m 	Trend Analysis and Prediction
m 	Expert Systems
m	Social and Geopolitik Simulators
m	Data Abstraction and Generalization
m	Security Systems


SPEECH:
m 	Identification of Phonemes
m 	Speech Production and Recognition
m 	Speech Transcription
m	Identification of a Speaker
m	User Independent Speech Recognition

ENTERTAINMENT:
m 	Image Compression and 	  	  	  Decompression for ISDN and HDTV
m 	Video Games and Toys
m 	Image Enhancement for Home Video 	  and Digital Photography





KEY:
m 	Well studied
m 	Current research
m	Future investigation




 Chapter 4 discusses how these systems determine behaviour and govern processing in the central nervous system.

Section 7.5 describes back propagation, and section 7.8 describes the Cerebellar Model of Arithmetic Memory (CMAC).

Section 7.2 discusses the Hopfield network.

Section 5.6 discusses the organizational principals of topographic mappings. Section 7.5 describes Kohonen's self organizing feature maps. Section 2.1 describes retinotopic maps, and Section 3.2 describes tonotopic maps.



.cTHE PHYSIOLOGICAL BASIS OF COMPUTATION 										- VISION

2




DIAGRAM THE EYE

.c22.1: THE RETINA

	The retina is composed of a layer of light detecting cells underlaid by a layer of ganglia which performs higher order processing such as contrast detection and local rate of change of illumination. By the time signals reach the optic nerve, a great deal of preprocessing has taken place. A variety of low level feature have been extracted and conditioned in preparation for the more complex processing that takes place in the various ganglia on the way to the visual cortex.

	Detail vision takes place in the central area of the retina, termed the fovea. The same type of processing takes place everywhere in the retina, but the cells concerned with detail have a complex-log distribution, being nearly linearly dispersed in the fovea, and becoming rapidly sparser as the edge of the retina is approached.
	Second order processing, the processing of image motion takes place uniformly across the entire field of vision: consider how readily we spot motion at the edge of vision: a flash of light, or a bird.  One function of the higher order processing is to initiate the saccadic reflex to center a moving image in the fovea. On the other hand, merging of an image doesn't occur at the edge of the retina. This is demonstrated simply by looking at a television at the very edge of the field of vision: flicker is quite obvious.  The human eye will merge images presented at thirty Hertz or greater. By contrast, the eye of the bee will not allow merging until the flicker rate goes over one hundred Hertz.

 Detail Vision Cells and Motion Detecting Cells

	Retinal cells habituate or “get used to” a constant level of light, and the signal returned by a habituated cell gradually decreases to nothing. That's why we can see afterimages. For the same reason, the complicated network of blood vessels on the surface of the human retina can't be perceived: the blood vessels are stationary with respect to the retina. To prevent habituation to an image, the eye moves constantly, as a microscopic jitter is all that is needed to keep the retinal cells reacting. A crab's eyes, which are at the end of stalks, tremor constantly to prevent habituation.
	The following diagram illustrates a retinal rod cell. The Lamellae are the light detecting part of the cell. The signals from the rod are input directly to the layer of amacrine cells under the retina. Before the image even leaves the eye, it has been enhanced, and many types of features extracted.




DIAGRAM NEUROPIL OF THE RETINA

	The ommatidium, or simple eye, of the invertebrates is an interesting eye: it responds to shorter wavelengths of light, polarized light, and fast moving targets. DESCRIBE OPERATION OF OMMATIDIA


	The compound eye's ommatidia are not distributed uniformly over the eye. Close observation of an insect eye reveals a small black spot. This spot is caused by ommotidia that are faced directly towards the viewer... Light is absorbed in this direction rather than reflected, and the black spot, called a pseudopupil, is formed. At one place on the compound eye the pseudopupil will be larger than in most other spots because more ommatidia are pointed in this particular direction. Detail vision is most acute in this area and it is termed the fovea by analogy to the pupil of the vertebrate eye.
	DESCRIBE FLY'S RETINA (Braitenburg and Encyclopedia of Neuroscience)

	The retina of the horseshoe crab, Limulus, consists of about a thousand ommotidia, each with a field of view of about six degrees, covering a total area of about two hundred degrees. The network underlying the retina embodies the very important principle of lateral inhibition, whereby neighbouring neurons inhibit each other and feed back to themselves, causing hyperacuity, image sharpening, self organization and various other useful phenomenon to occur. The retinal circuit of Limulus has been extensively studied since the 1930's, and was one of the first neural networks to be completely characterized owing to its extreme simplicity. By 1978, the circuit underlying the eye of Limulus had been modelled reliably as a linear system (Brodie, Knight, & Ratliff, 1978). The following diagram shows the circuitry of the Limulus retina:

DIAGRAM LIMULUS CIRCUIT

	Brodie and his colleagues conducted a series of experiments where they presented computer generated images to the horseshoe crab via an optic fiber cable glued to the eye. A small hole was cut behind the eye, the optic nerve was transected and dissected free, and a single firing axon was obtained.  Once readings from many crabs were obtained and analyzed, there were several interesting results.
	Maxima or minima of activity in the axon was detected just before a test ommotidium was crossed by a moving edge, a kind of anticipatory effect. The magnitude of the anticipation was directly proportional to the speed of the edge: a fast edge gave a large response, a slow edge, almost none. The retina's response characteristics (lateral inhibition) are such that contours and movements are accentuated, providing useful detail to the brain, even though the number of cells is small.





.c22.2: ORIENTATION SENSITIVE CELLS:

	Long before an image reaches the association cortex, the visual (striate) cortex has begun the process of abstracting useful data from the image. 	Through a long series of well known experiments Hubel and Weisel found two important types of neurons in the visual cortex.  These two types of cells are characterized by their receptive fields. One type of cells has circular receptive fields arranged in concentric, mutually antagonistic sub-regions : these are the on-center off-surround cells, and the off-center on-surround cells.



	These cells are sensitive to changes in contrast (Wiesel & Hubel, 1966). Hubel and Wiesel found the other type of cell in experiments with kittens. The activity of individual striate cortex cells were monitored as bars of light of various orientations were swept across a screen. Individual neurons responded strongly only to edges at particular angles (Hubel & Wiesel, 1962). Example receptive fields of orientation sensitive cells are shown below.
BRIEF NOTE ON LINSKER'S EIGENVECTOR RECEPTIVE FIELD RESULTS



	They found that as a probe went deeper and deeper through the cortex, the preferred orientations of the cells would change slightly. They deduced that neurons are organized in columns, and within these columns, all the neurons are sensitive to the same orientation. Neighbouring columns tend to respond to similar orientations.  This demonstrates an important organizing principle: neighbouring cells in a network have similar behaviour. In other words, the activity of neighbouring neurons is almost the same.

      PROGRESSIVE ROTATION

	Christoph von der Marlsburg (1982) argued that it would be impossible for every detail of that organization to be programmed genetically, and that consequently, the cortex must be able to organize itself. The constraint that neighbouring columns tend to respond to similar orientations was the key to developing an organizing rule. The experiments with the kittens demonstrated that there was a period when the structure of the cortex was plastic (changeable). It was therefore the function of intracortical connectivity and the adaptive abilities of the neurons to organize the cortex during that period of plasticity.
	Von der Marlsburg developed a computer model that self-organized: units tended to fire in clusters, a large proportion of the cells exhibited orientational preferences, and preferred direction varied gradually from neighbouring cell to neighbouring cell, matching the physiological observations of Hubel and Wiesel. The system was also robust: if the values in particular synapses were destroyed, the synapses would relearn their old values, and the system would thus repair itself.
	The cells in von der Marlsburg's model were simple summing thresholding units, below the threshold, the output would be zero, above, one. Because a simple linear system has no bounds on activities of the weights, inhibitory neurons were put in, to keep the values reasonable. As a simplification, only on-cells with no center-surround organization were used in the model. Excitatory and inhibitory cells were arranged in a two dimensional hexagonal matrix, and they interacted via a bell-shaped function of distance. The bell-shaped interaction function caused reinforcement of most active cells, and inhibition of cells outside the immediate neighbourhood of the most active cells. The system learned using a modified Hebb rule: weights at a given cell were normalized so that they all added to a constant, thus, one weight would gain at the expense of the others. Even with all the simplifying assumptions, this arrangement was enough to effect self-organization.

	Bienenstock, Cooper, and Munro (1982) extended von der Marlsburg's model to include inputs from the left and right eyes, so that binocular results obtained from experiments with kittens could be modelled. With their model, they found that if the system is allowed to develop normally, the cells become orientationally selective, and binocular.
	A single cell will develop so that it responds to the same orientation coming from both eyes. If, however, the system develops in a state of light deprivation, the cells never choose a particular orientation preference, instead exhibiting low selectivity, and random orientational preferences. If input to one eye is suppressed, cells become orientationally selective, and monocular, not responding at all to input from the other eye. In the case of uncorrelated input, binocular as well as monocular equilibria exist, and the preferred orientations from the left and right inputs don't necessarily coincide in binocular cells.


DIAGRAM OCCULUAR DOMINANCE STRIPES IN VISUAL CORTEX
DESCRIBE MACAQUE MAPS AND THREE EYED FROGS AND POSSIBLE MECHANISMS FOR BINOCULAR FUSION



The processing performed by the retina of the frog is described in detail in Section 2.3.

Section 4.5 describes edge sharpening through lateral inhibition.

Section 5.1 describes Hebbian learning

Predators are more likely than prey organisms to have eyes on the front of the head with overlapping visual fields. Prey organisms tend to have eyes located on the sides of the head, giving rearward vision, but little depth perception. This is probably related to the tendency to form herds. This idea is elaborated on in Section 5.9 which discusses flocks and herds as a type of distributed processing.

.c22.3: FROG'S EYES

	The classic paper “What the Frog's Eye Tells the Frog's Brain” by Lettvin, Matturana, McCulloch and Pitts in 1959 illuminates a way in which progressive stages of processing can do most of the signal processing and abstraction of a scene before an image reaches the cortex.	The frog's visual system was studied because it is very simple. Signals from the retina travel directly to the collicus. The frog has no fovea, therefore a uniform amount of information is available from across the retina. The frog's eyes don't move except to stabilize an image on the retina. 	The old view of visual perception would have a pattern of light and dark arriving in the visual cortex, ready to be interpreted. The results of these experiments was to demonstrate that this is not the case, but rather that the image is highly organized and interpreted by the time it reaches the cortex. As it turns out, the frog does not receive much information about the stationary world - in fact, it will starve to death if surrounded by unmoving food.
	To perform the experiment, a frog was placed inside a spherical globe. Inside the globe were various objects which the experimenters could manipulate from outside using magnets. Various stimuli were presented - dots, bars, fields of moving dots, scenery, etc. Readings were obtained from the optic nerve and from the optic tectum.
	The frog's retina has about a million receptors (rods & cones), about three million connecting neurons (bipolars, horizontals, and amacrines), and about a half million ganglion cells. The receptors feed out to many different ganglion cells, and the ganglion cells receive synapses from thousands of receptors. The following diagram shows a section of the frog's retina (after Ramon y Cajal).

DIAGRAM CAJAL'S FROG RETINA

	The optic nerve fibres are disordered within the optic nerve, but after the nerves cross and enter the opposite tectum, they disperse amongst four layers of cells in the optic tectum, each layer containing a retinotopic map. These four maps are in register with each other.
	Each layer has a different purpose. The outermost layer, containing contrast detectors, had the slowest fibres. The next layer contained convex edge detectors, though the cells for the first two layers were somewhat intermixed. The next layer contains the moving-edge detectors, and deepest were the dimming detectors. In general, the layers were quite distinct. The depth of the layer and the speed of nerve fibre conduction were intimately related. Deep fibres conducted faster than superficial ones. This would have the net effect of causing the images in each retinotopic mapping to arrive synchronously.
	The layers self organize. As noted above, within the optic nerve, there is no particular ordering. If the optic nerve is severed and moved (essentially randomizing the connections) and allowed to grow back, after some time has passed, the connections will restore themselves, and the organization will be the same as before.



	The sustained contrast detectors had small receptive fields (one to three degrees) and began to respond strongly when a moving edge was moved into their receptive fields. They responded if the moving edge was stopped, and continued to respond until the edge was removed. If the scene was darkened then relit, the cells would begin responding again if the edge was still present, although they lost their memory after about a minute of darkness. These cells respond independently of image brightness: they respond the same to a dark image as to a light one.
	A layer of convex edge and sustained edge detectors was hypothesized to function as a bug perceiving layer. These are on-center off-surround cells with receptive fields of two to five degrees. They respond best to dark spots smaller than their receptive fields. Movement of a field of dots has no effect on these cells, however a dot moving independently of the field caused a strong response. Moving a photograph causes no response, however a moving dot over the photograph does. The colour and shape of the dot is not important - a response will occur so long as a perceptable convex edge is present. The response of these cells vanishes as soon as a moving edge moves out of the receptive field. Because of the small receptive fields of the sustained edge and convex edge detectors, these cells are useful for locating prey. These cells sometimes exhibit directional sensitivity, responding to edges moving in one direction, but not another.
	Moving edge detectors (seven to twelve degrees) respond to any distinguishable moving edge. The output of the cells is fairly independent of illumination. To a certain degree, these cells fire faster for faster moving edges.
	Dimming detectors could detect moving shadows. They have receptive fields of seven to fifteen degrees, and have no response to stopped edges. These cells are always active, but their activity increases as dimming occurs within their receptive fields. They respond most strongly to dimming in the center of their receptive fields, and less for dimming on their edges. This suggests a Gaussian sensitivity distribution. The behavioural significance of these cells is perhaps that they are looming shadow detectors, as a frog is able to distinguish between objects coming directly towards it and objects which will narrowly miss hitting it.
	There is a small group of cells which respond to the overall illumination of the retina, having no distinct receptive field. They fire faster as the general illumination gets dimmer, perhaps indicating that night has fallen.




.c22.4: IMAGE SEGMENTATION

The full description of human object recognition facilities might be more complex than the network that implements it.
- John von Neumann

	An important mechanism commonly used to segment an image is motion data, because for a particular object, every part of the image moves together. In other words, local motion is uniform. Motion data is readily available from the eye, because one of the main functions of sensory neurons is to detect change. A tiger lying in wait blends with its background, essentially invisible until it moves. Squirrels freeze, hoping to avoid detection. A flashing light catches our attention immediately.
	To see how motion helps segment an image, flip this page rapidly back and forth, and observe the dot patterns in the upper corner. The image imbedded in the pattern should jump out, thus demonstrating the segmentation effect.
DIAGRAM AT TOP OF THIS PAGE, AND TOP OF NEXT
	Optical systems with small depth of field provide a curiously overlooked mechanism for the separation of figure from ground, and to a limited extent for getting range data. The value of depth of field is easy to demonstrate with a camera. If a photograph is made through a chainlink fence or a dirty window, odds are the links or the dirt will not appear in the picture, or if they do, they will appear only as vague blurs or smears. A subject in the distance will appear clear and unobscured.
	If, through the use of a regenerative feedback loop, a system were to enhance areas with sharp image boundaries and inhibit areas where colors blur softly into one another, figure would emerge automatically from ground, and many of the problems of perception of three dimensional figures would be resolved. It would be a simple matter to get range information from the focusing mechanism of a lense. This system would be particularly useful at close ranges where depth of field is small, being therefore useful for hand-eye (manipulator-vision system) coordination.
	INSERT DESCRIPTION OF HIGH LEVEL FEATURE EXTRACTION AND RECOGNITION, IN PARTICULAR MIT WORK ON BLOB DETECTION AND HOW IT RELATES TO GAUSSIAN RECEPTIVE FIELDS.
	It appears that human pattern recognition is somewhat dependent on the orientation of the image. One must learn to read a page upside down, or at strange angles. James Anderson (1972) reported that snakes will move their heads to keep their slit pupils upright.
	It is important to bear in mind that only a tiny area of the retina, the fovea, is involved in actual detail vision. A naive observer may assume that everything in the field of vision is available at maximum resolution, but this is incorrect. The mind builds up an image, a model, of the environment, and it is this model which fools us into believing we actually see everything in detail in the field of vision (Crick, 1977).



.c22.5: SACCADES

	A saccade is a short ballistic movement of the eyeball to orient the eye towards an object of interest, or to keep an object of interest centered in the field of vision.
	INSERT DESCRIPTION OF V.O.R. AND SOME APPROACHES TO MODELLING IT, INCLUDING PELLIONISZ TENSORIAL TRANSFORMATIONS.
	The frog offers a unique opportunity to study visual saccades because of the simplicity of its nervous system. Churchland (1988) has analyzed the problem quite nicely. Specific behaviours of the frog appear to have specific command centers. One area controls orienting towards prey, another snapping, another avoiding a predator. The frog's avoidance behaviour is quite simple: it jumps towards large dark patches, which in its normal environment are usually ponds.
	The superior collicus and the frontal eye fields together have been identified as the locations of visuomotor maps for eye movements (Stein, Clamann, & Goldberg, 1980). The cells within the collicus and the frontal eye fields are organized in an orderly fashion according to both amplitude and direction of a saccade. The collicus is implicated in orienting the entire body. Visual, auditory, somatic and auditory stimuli are all represented within the collicus, and any of them can initiate eye movements by interacting with the same motor outputs.
	Stimulating the collicus or the frontal eye fields in a particular place yields a particular saccade whose size and direction depends on the site of the stimulation. Both fields are vital for the reflex as demonstrated by the fact that ablating either structure causes a small performance deficit, however, ablating both disrupts the saccade completely. (Schiller, True, & Conway, 1979)
	Since cells in the intermediate and deeper layers of the superior colliculus are responsive to tactile stimuli at birth and after 5 days to auditory stimuli as well, these stimuli might serve to initiate eye movements. Neonatal eye movements are very small and uncoordinated when compared to adult eye movements. There seems to be some correlation between identical stimuli, and the angles moved by the eyes during repeated trials, possibly indicating plasticity of the system. These tentative eye movements set the stage for later visual-motor associations (Stein, Clamann, & Goldberg, 1980).
INSERT DETAIL OF CHURCHLAND'S MODEL, AND DESCRIBE THE OPERATION OF THE KOHONEN SELF ORGANIZING FEATURE NET>



.cTHE PHYSIOLOGICAL BASIS OF COMPUTATION - 									    SOUND

3




.c23.1: FROM THE COCHLEA TO THE CORTEX

.c2	The simplest system in nature for detecting sound is the insect ear. It consists of a taut membrane behind which are sensory cells. If connected to an audio amplifier, a probe inserted into the axon of a sensory cell coming from the ear will allow an experimenter to hear what an insect can hear. In general, the insect ear detects only very specific behaviourally significant sounds, such as the characteristic sound of another conspecific insect. In many cases, it is very difficult to detect any behavioural correlation to the information coming from the ear. Study of this system should yield simple systems for small robots, but it is the concept of extremely specialized detectors that is interesting here, rather than the actual physical details.

	The mammilian system is far more complex and interesting from a signal processing point of view. The cochlea is a complex resonant structure, whose job is to condition and detect sound in preparation for processing by higher levels of the brain. The basilar membrane is a sensitive strip on the inside of the cochlea covered with cilia. Different points along the membrane resonate at different frequencies, and so the cilia on the membrane can decompose an arriving signal into its frequency components. The basilar membrane thus performs much the same function as a Fourier transform. This step of decomposing the sound signal into its frequency components essentially converts an analog signal into a digital one.
	At the apex of the cochlea are the cells which detect low frequencies, and at the base are the cells which detect high frequencies. There are many cells at the low frequency end, and fewer and fewer as the high end is approached, which is one reason why we have more difficulty hearing high frequencies.


This diagram shows the basilar membrane. The length of the membrane is covered with sensory hair cells which detect sound of particular frequencies.

	The numbers on the diagram refer to the maximally resonant frequencies (in kilohertz) at particular spots along the membrane, and hence the frequency that particular hair cells respond to most strongly. The base of the basilar membrane is located near the oval window, and the apex is about 40 millimeters away.
	Within the cochlea, the first step in processing sound is the detection of sound by the hair cells.  The frequency response of the hair cells is bell shaped. Sound is highpass filtered by fluid-cilia coupling. Transduction at the apical membrane of the hair cell compresses the signal, through the familiar sigmoid input-output relation, and finally the signal is lowpass filtered by the relatively slow response of the output of the cell.

DIAGRAM PROCESSING BY THE COCHLEA
	After the cochlea, the signal then gets preprocessed and organized by the lower auditory nuclei. Spectral decomposition and time domain information about the sound signal is measured here, and then the information is sent to the Medial Geniculate Nucleus (MGN). The MGN is involved in selective attention, and it sends inhibitory signals to the Inferior Collicus.

DIAGRAM AUDITORY PROCESSING STATIONS
	The Inferior Collicus is implicated in the topographic mapping of auditory space, and echolocation in bats. Some cells in the inferior collicus become phase locked to the beat frequency arising from the mixture of binaural signals, and some respond selectively to particular relationships between the signals, and to changes in the relationships between the binaural signals (Kuwada, Yin, & Wickesberg, 1979).

DIAGRAM PHASE RELATIONSHIPS

	It has long been recognized that tonotopic maps exist to map frequency in a highly organized structure through the auditory nuclei, but it was thought that the Medial Geniculate Nucleus mapped randomly to the auditory cortex. Measurements reported by Bryan Travis (1987) showed that the mapping is not random. Rather, at least four maps exist, butted end to end in a symmetrical fashion and extensively cross-connected - cells in each map responding to particular frequencies are connected together.

DIAGRAM TONOTOPIC MAPS IN AUDIO CORTEX

	As in visual cortex, on and off response cells exist. ELABORATE - WHAT ARE THE IMPLICATIONS OF THESE FACTS? WHAT IS A LIKELY ARCHITECTURE FOR A NEURALLY INSPIRED AUDIO SIGNAL PROCESSING SYSTEM?



.c23.2: THE CASE FOR THREE EARS

	Why don't we have more than two ears, or conversely, only one?
	One ear would allow detection and analysis of all kinds of sounds, but little directional information. Two ears allows determination of the direction of the source of a sound within the plane of the ears. Minimizing phase difference between sound signals arriving from both ears orients the head towards the source of a sound. Three ears would tell whether the sound arrived from the front or the rear, and a fourth ear would tell the elevation of the sound source in space.
	For an organism operating on a plane, two ears is really all that is necessary, as the front-rear ambiguity of a sound source would be minimized by directional sensitivity provided by the ear's structure. Organisms which have three dimensional mobility usually have other mechanisms available to ascertain elevation. Some owls, for example, have feathers arranged around the ear which are sensitive to sound sources at different elevations.



.c23.2.1: ECHOLOCATION AND THE BAT

	Bats use ultrasonic echolocation to detect and avoid objects. Due to ultrasound's short wavelength, it reflects well from small objects, allowing the bat to detect objects as small as wires a third of a millimeter in diameter. Of course, the strength of a high frequency sound diminishes rapidly with distance, making the system most useful at close ranges.
	To keep information about the nearby environment accurate, the bat increases the rate of its crys dramatically when it approaches within a meter or two of an obstacle. Typically, the emitted pulse rate increases from a normal rate of 10 to 30 pulses per second to a far more informative pulse rate between 50 and 200 pulses per second). Bats can discriminate shape and accurately range an object. They can tell the difference between objects of similar shape, but different make up, for example they can discriminate between mealworms and similarly shaped plastic discs (Camhi 1984, p. 174-177).
	The audio cortex of the bat can compensate for Döppler shift in the echo from large stationary objects. The ear of Rhinolophus, for example, is especially sensitive to tones of 83 kHz. When Rhinolophus detects an approach to a stationary object, signalled by a positive Döppler shift, it will start lowering the frequency of its emitted pulses to keep the return in the ears' most sensitive range. This acoustic analysis is done in the frequency domain rather than the time domain. Time domain information - the length of time that elapses between a cry and its echo return - is used to detect the range to an object (Camhi 1984, p. 183). It is time domain information as well that tells the bat to step up its pulse rate for close objects.
	The cry of the bat reduces the sensitivity of the ear to the return echo. During a cry the stapedius and tensor tympani muscles tense the stapes and malleus bones in the ear to damp the sound. As shown in the diagram below the sensitivity of the ear is attenuated during the cry. Immediately after the cry, the ear is hypersensitive in order to catch any returning echoes.


	Cells in the audio cortex are especially sensitive to quiet sounds following loud ones: after a loud sound, the sensitivity of the ear is enhanced. Many bats issue a frequency modulated sweep, and particular cells in these bats' brains are sensitive to particular frequencies. Other cells are sensitive to particular directions of sound. Resolution can approach one degree of arc in the forward direction where the most detailed processing takes place. Cells are found which respond to particular time delays from which range and directional information can be extracted.
	The cortex of the bat is relatively small and unfissured compared to other mammals, but the auditory subnuclei are very highly developed . The sophistication of the nuclei suggests that most of the processing of audio signals is done before the signals reach the cerebral cortex.



.c23.2.2: SPATIAL LOCALIZATION


	A variety of localization information is available from the ears. Some of the possibilities are summarized in the following table.

m		The phase difference between the signal arriving at the two ears tells what angle a sound is coming from relative to the head.
m		The interaural intensity difference will indicate where a signal is coming from. This method is usefull for nearby continuous sound sources.
m		The interaural time delay also tells where a signal is coming from. This method is useful for transient sounds such as clicks and pops.
m		The rate of change of relative phasing between the ears, or Doppler shift of the signal, tells how fast an object is moving relative to the head.
m		The loudness of the sound as compared to an expected volume indicates how far away an object is.

	Analysis of phase difference is probably the most generally useful. To orient the head towards a sound, for example, the head could be swung around until the phase difference was minimized. Wavelengths approximately twice as long as the distance between the ears are the best for determining location, and in fact it is difficult (or impossible) to localize very high frequency and very low frequency sounds. The best frequencies for humans are less than approximately 1500 Hertz, a frequency whose wavelength corresponds to the distance between human ears. This is the same frequency range that most human speech falls into.




Number of spikes CAT'S BINAURAL RESPONSE CELLS
      		       0.0         0.5          1.0
			       Interaural phase f

	This diagram, adapted from Kuwada, Yin, and Wickesburg 1979, shows the response of a single neuron to a binaural beat frequency as the frequency is stepped through one complete cycle of the beat. The f=0 and f=1 marks correspond to no phase difference. Note that the gradually increasing and then decreasing response of the neuron shows that the sound locating system is coarse-coded. Direction sensitive neurons show a strong response like this when the signal is strongest on their favoured side, and they show a very diminished response on the other.
	The Inferior Collicus is implicated in echolocation in bats, and the topographic mapping of auditory space. Subserving this mechanism, some cells in the inferior collicus become phase locked to the beat frequency arising from the mixture of binaural signals, and some respond selectively to particular relationships between the signals, and to changes in the relationships between the signals. Some cells in the collicus are directionally sensitive, becoming phase locked to particular beat frequencies, but responding strongest when the signal to one ear is stronger than the signal to the other. (Kuwada, Yin, & Wickesberg, 1979)
	The work of Knudsen and Konishi (1978) shows a step above the phase detecting cells: they found that a topographic map of auditory space exists in the mesencephalicus lateralis dorsalis (MLD) nucleus of the barn owl. (The MLD is the avian homologue of the mammalian inferior collicus.) Helping the owl obtain its three dimensional map are a set of feathers arranged around the ears which focus sounds into the ear. The feathers at the top are best for reflecting high frequency sound, and the feathers at the bottom are best for low frequency sound. Presumably, information from this arrangement helps the MLD form its map. In the MLD mapping, most processing is directed towards signals coming from the front, and all neurons have the typical on-center off-surround response.

DESCRIBE KONISHI'S MODEL OF ITD ORIENTATION DETECTION - SIMULTANEOUS L/R SIGNAL INPUT LEADING TO CORRELATION DETECTION.

	The brains of bat, cat, and barn owl are all quite different, but they follow the same general plan. As in the bat, specialized processing substations on the pathway from the cochlea to the cortex are found in both the owl and the cat. Because the vertebrate brain's architecture remains similar from species to species, we can hypothesize that extensive sound preprocessing occurs before cortex in all vertebrates. The generality of the plan suggests that it would form a useful model for manmade signal processing systems.



.c23.3: THE PERCEPTION OF MUSIC

	Rhythm: When we walk, why do we take steps that conform to a rhythm, rather than taking steps of varying duration? The answer is Minimization of Energy. Walking in strange patterns requires extra effort; it is necessary to overcome the inertia that wants to keep the body and legs moving along at the same velocity.
	Perhaps rhythm perceptors exist in the brain, in one of the processing stations between the cochlea and the cortex. In the postulated system, the maintenance of a steady oscillatory rate entrained to audio input would be the minimization function.
DETAIL MORE RECENT RYTHM LEARNING RESULTS, and MAYBE SHIBATA'S HUMMING TRANSCRIBER



	Multiple “rhythm catchers” could exist, organized into cortical columns in a manner reminiscent of the orientation selective cells in the LGN.
	Rhythms certainly insinuate every aspect of day to day existence, and every culture since the beginning of time. Maybe because energies are being minimized, rhythms are perceived as being pleasurable.


.c23.4: SUPPRESSING NOISE

	The audio processing stages of the brain seem to habituate to repetitive or recurrent sounds, for example the humming of a noisy computer monitor, or the low thunder of traffic on the road just outside the window.
	If rhythm catchers could pick up more sophisticated patterns than just a simple beat, they could learn, or perhaps habituate to, a characteristic sound, and thereafter subtract it from the total signal going into the audio cortex.
	For the suppression of noise noise, there is always the recurrent on-center off-surround architecture to eliminate the clicks and pops and scratches that are a constant impingement on our ears.

	A MORE DETAILED ANALYSIS IS REQUIRED HERE



.c23.5: SPEECH PERCEPTION AND GENERATION

What we believe we hear, we in fact reconstruct in our minds from pieces of received information.
- Teuvo Kohonen (1988a)

DESCRIPTION WHAT IS INVOLVED IN SPEECH PRODUCTION? NOTE ON BROCA'S AREA AND WERNICKE'S AREA
	Counting in your head does not involve the brain's speech centers. Reading out loud, on the other hand, uses almost every area of the brain - from speech areas to somatosensory areas to visual.
	A deaf person has difficulty speaking clearly, being unable to listen to speech and correct it as it is produced. It is easily observable that speech generation is heavily influenced by listening - people shout to be heard over a portable cassette player, because they think they are speaking quietly.  Speech perception and generation by the brain are absolutely interrelated, to the extent that it is very difficult to have one without the other. It has been suggested that speech perception occurs in terms of articulemes which are the speech to muscle combinations that actually produce speech. This theory is called the “motor theory” of speech perception.
	Internal speech, or even the intention to speak, primes the speech perceiving mechanisms of the brain before the words are spoken, affecting an anticipation of the correct sounds. The production centers can match the anticipation against the perception areas in a kind of feedback loop which will dynamically alter speech production as necessary to produce the desired sounds.
	After (and even as) a word is spoken and simultaneously perceived, it will excite memory associations and anticipations in memory which the language centers of the brain will use to decide what the next thing to say is, or that it is time to listen to the other person, or even that it forgot what it was trying to say.
	Luria (1977) developed an elaborate model describing the production of speech from intention to articulation.
	Stephen Grossberg and ? (1987 XXX) are in the process of developing a model based on the Adaptive Resonance Theory. In this system, the expected sound of the speech generated is matched against the sounds that are actually produced, and thus, through a feedback mechanism, the speech production mechanism regulates itself.




.c23.5.1: A PHONETIC TYPEWRITER

	Teuvo Kohonen at the University of Helsinki has created an interesting speech recognizer. (Kohonen 1988a). Based on the principles of the self organizing feature net, the network will recognize isolated phonemes, and when the output of the network is passed through a later symbolic processing stage, it will recognize speech.

	The system will produce a phonetic transcription of Finnish or Japanese with good accuracy. Finnish and Japanese were chosen because Finnish is written the way it sounds as is Japanese which has two phonetic alphabets.
	The neurons were arranged in a hexagonal matrix, and the same input arrived at every neuron. The network was constructed in hardware, and the equations were implemented using digital signal processing chips, and thus could be evaluated in real time. The speech signal is sampled and quantized into fifteen channels. Subsequent samples are averaged together to preserve some time domain information. The fifteen dimensional input vector is normalized to unit length and presented to the neural network.
	As input arrives, the net self organizes, forming a continuous map of the input space. The net organizes into a Voronoi tessellation which approximates theoretical Bayesian decision surfaces. The net performs an accurate nonlinear statistical analysis of the speech signal.
	Individual neurons learn to respond to characteristic input patterns - some neurons respond to particular vowels, others to particular consonants.

DIAGRAM PHONEME MAPPING

	These characteristic learned patterns are the neurons' internal representations. Sounds which are transient in nature, such as plosives (t or p for example) aren't recognized by the network, because it is their evolution through time which contains the information rather than instantaneous spectral content. In Kohonen's model, an auxiliary network specifically designed to handle these sounds was designed (but not described in the paper).
	It is difficult to determine where exactly phonemes start and end, and in this model, a heuristic was used: if a particular neuron (or group of neurons) responds consistently for a particular time period, then a phoneme is considered identified.
DESCRIPTION HIDDEN MARKOV MODELS
DESCRIPTION SPEAKER INVARIANT PERCEPTION
DESCRIPTION RECOGNITION OF VARIOUS SPEAKERS


See sections 4.1 and 4.2 for a discussion of noise suppression by on-center off-surround cells.

Section 7.5 describes the Kohonen self organizing feature net.


THE PHYSIOLOGICAL BASIS OF COMPUTATION



4




What do we mean by self conscious? If we will realize that all spontaneous life, desire, impulse and firsthand individual desire arises and is effective at the great nerve centers of the body, and not in the brain, we shall begin to understand.
- D.H. Lawrence, in What is Education?




.c24.1: TOPOGRAPHIC MAPPINGS

	One of the most common data processing principles used by the nervous system is the two dimensional topographic mapping. Maps of the retina in the intermediate processing stages preserve the spatial relationships between adjacent image elements. The sensory and motor cortex are physically organized in a manner commonly represented in psychology textbooks as the homunculus. Sound is organized into a variety of maps which are organized on the basis of frequency and some other dimension. Cristoph von der Marlsburg showed that retinotopic maps can self organize and repair themselves (von der Marlsburg, 198x. Many experiments have shown conclusively that the homunculus reorganizes on the basis of incoming sensory information. What are the principles of self organization? How does the nervous system form a map?

	The Perceptron suffered because the lesson of the nervous system was ignored.  The Perceptron randomly mapped the input space to the processing elements, thus destroying the physical, topological relationships between all the input signals.

DIAGRAM MOTOR CORTEX - HAND

	This diagram shows the portion of the sensory map in motor cortex which represents the hand. Topographic mappings reflect the statistical distribution of input space by devoting more processing units to features that are important. In the sensory homunculus, for example, notice how large the representation of a finger is, as compared to the entire back of the body!

DIAGRAM REORGANIZED HAND IN SENSORY CORTEX

	This diagram shows how the area of the cortex mapped out in the previous diagram reorganized itself after sensory input from the little finger was cut off by deafferentiation. Much less information comes from that finger, so its representation occupies less space in the map. Notice as well, the areas devoted to other fingers have expanded to use the extra neurons now available. (ref XXX)
	Typical self organizing maps are arranged in cortical columns. Each column tends to recognize a particular feature of the input, coming from a particular sensory location. This principle is illustrated by the retinotopic maps: each column recognizes edges of light rotated to a different angle. When orientation sensitive cells like these are available at all image locations, processing of an entire image can occur. Different sensory modalities would require different feature detecting cells. The auditory cortex for example uses frequency tuned cells.
	A mechanism common to all these sensory maps is lateral inhibition. Columns which strongly match a particular input feature tend to suppress nearby competing cells. This sort of winner-take-all mechanism can cause self organization.

LATERAL INHIBITION CURVE

	This curve shows lateral inhibition as a function of distance, derived from experimental measurements in cortex. The central peak is excitatory, and extends in cortex for a range of 50 to 100 micrometers. The inhibitory surround extends out from there to 200 to 500 micrometers, and beyond that, there is a weak excitatory area (Kohonen, 1988). This type of response function is the typical “on-center, off-surround” receptive field.



.c24.2: ON-CENTER, OFF-SURROUND CELLS

	Many cells in the visual cortex have receptive fields which are biased towards detecting light areas surrounded by dark, or dark areas surrounded by light. These cells are called on-center, off-surround cells and off-center on-surround cells. Many of these cells working together in a competitive network can perform edge detection and noise suppression. Noise suppression is easily accomplished by these cells, because noise tends to average to a uniform level, especially at a small scale, like that of the receptive fields of individual cells.

  Original signal, noisy signal, and averaged noise.

	In the field of image processing, the Laplacian operator takes advantage of this fact to smooth pixel images.

 LAPLACIAN OPERATOR AND BEFORE AFTER IMAGES

	An image is convolved with the Laplacian - the operator is used on every pixel. When every pixel is averaged with its neighbours, noise in the image blurs away. An alternative to the Laplacian kernel is the Gaussian kernel, which operates in much the same way, but has different receptive field properties.

DIAGRAM LAPLACIAN KERNEL AND BEFORE/AFTER IMAGES

	The receptive field of a cell with concentric mutually antagonistic receptive fields is conceptually similar to the Laplacian and Gaussian operators. These cells reinforce their output when the center of their receptive field is bright, and they tend to inhibit themselves if the area surrounding that central section is bright. For that reason, the uniform light levels of a noisy image would tend to suppress output, due to the contrary excitation and inhibition across the receptive field.

DIAGRAM ON-CENTER OFF-SURROUND CELL AND MEXICAN HAT

The “Mexican hat” curve is described by the function:
F(sin r,|r|)  where r is radius from the center of the curve.

DESCRIBE HOW ON CENTER OFF SURROUND CELLS PERFORM FIRST ORDER IMAGE PROCESSING, AND HOW 2nd ORDER PROCESSING IS CARRIED OUT BY ORIENTATION SENSITIVE CELLS, AND RELATE 2nd ORDER PROCESSING TO SELF ORGANIZATION.

	In an image processing network, every cell is connected to its neighbours in a similar fashion. Inhibition is greater farther away from the active cell to aid self-organization in the system.
	On-center, off-surround cells can also perform edge detection.



	Cells one and three are subject to uniform levels all across their receptive fields, and thus, they have low outputs. Cell two, on the other hand has a gradient light level across it, so the inhibitory effects cancel, and its output is boosted. Since any cells with a strong gradient reinforce, and cells receiving a uniform light level are suppressed, edges are detected.



.c24.3: THE SEARCHLIGHT HYPOTHESIS:

If the thalamus is the gateway to the cortex, perhaps the reticular complex is the guardian of the gateway.
- Francis Crick



	It is a simple matter to find the o mixed in with all the s's.
	Finding the italicized s in the picture takes a little longer, almost as if finding the o was done by a parallel search, and finding the s was done serially, by checking each s...
	Francis Crick (1984) suggests the idea of an attentional spotlight, akin to a searchlight at dusk illuminating and intensifying part of a scene that is already somewhat visible. Due to its structure and location, the thalamus is hypothesized to be the location of the attentional spotlight.
	With the exception of olfactory input, the senses pass through the thalamus on the way to the cortex. Most of the thalamic cells are relay cells, projecting excitatory synapses to the cortex. Efferent (from the cortex) projections don't necessarily pass through the thalamus on their way out, but from thalamus to cortex, there are reciprocal pathways.
	The reticular complex is a thin sheet of cells, often only a few cells thick, which partially surrounding the thalamus. All connections between the cortex and the thalamus pass through the reticular complex. The cells of the reticular complex are GABAergic, which is to say, they are inhibitory. In this layer, the cells all share extensive lateral interconnections. (In contrast, the cells within the thalamus have few, if any, collaterals.) Because the reticular cells are almost all inhibitory, it follows that excitation within this layer must come from the axons that pass through it.
	A lateral inhibitory net (which is what the reticular complex must be) will perform edge enhancement, noise suppression, and feature detection, as detailed in the previous section. These nets are characteristic of all topographic mappings such as the sensory homunculus, or the Kohonen self organizing feature net.

	Perhaps a map of the cortex exists in the reticular complex. The searchlight could play upon the reticular complex, and should be able to sample the cortex, and thus determine “where the action is.” The searchlight itself would be expressed by an increase in firing rate in a subset of the thalamic neurons. Higher firing rates correspond to increased attention.*

	The number of searchlights would depend upon the range and strengths of the reticular neuron's inhibitory connections. The number could perhaps be dynamic, flickering, spawning and fusing across the reticular surface, like the turbulent wanderings of a stream of thought. Conversely, the number of searchlights - the number of things that can be attended at one time - could be fixed.  Every topographically mapped section of the brain could have its own set of searchlights...
	There is evidence that we can know the number of only six things at one time. We can look at a group of objects, and know: there is one, there are three, there are six. For seven things and higher, we must rely on symmetry, or we must count the objects.

DIAGRAM ONE OBJECT THREE OBJECTS EIGHT OBJECTS




.c24.4: SYMMETRY:

DIAGRAM SLASHY SYMMETRY DIAGRAM ALA BRAITENBURG

	We like symmetry, because we are symmetrically designed. Consider a wrist watch that must be wound: It's an easy task, right? You hold the watch in your left hand, and wind it with your right. Now, quickly imagine, what if you wind the watch with your left hand? Maybe a first impulse is to wind it in the exactly opposite way: holding it in the left hand and winding with the right. But, this is impossible...
	Consider also left and right handed scissors. Why are there two different types? (Try cutting a piece of paper with the wrong hand, and observe why the scissors don't cut.)
	Perhaps motor patterns are generalized symmetrically, and hence, we like symmetry... On the other hand, motor patterns can't generalize left to right too readily, otherwise, we would all be ambidextrous.
	Perception of symmetry is a different problem. An example back propagation network cited in Rumelhart and McClelland's book “Parallel Distributed Processing” solves the problem of determining if a binary input pattern is symmetric.
 That solution is reconstructed here:



	If symmetry is broken, the hidden units will detect the fact... The sum of the weighted inputs arriving at the hidden units will not be zero, and asymmetry will thus be detected. This arrangement can be criticized as being biologically impossible for the simple reason that the weights are increasing by powers of two, and therefore recognizing the symmetry of a larger problem might be quite impossible. An argument for plausibility could be made by considering the limited number of items that can be attended at one time, as discussed at the end of Section 4.2.
	In the epilogue to the revised edition of “Perceptrons” by Minsky and Papert it is suggested that the problem is in fact biologically plausible, because humans have difficulty perceiving symmetry in some cases:
HL4SD7NKf3fKN7DS4LH

	Unfortunately for this argument, extra processing is involved in this example, because we must first read the characters before we can check for symmetry, and when we check the pattern, we must do it serially, a character at a time, rather than all at once.
	I offer two intriguing clues to the perception of symmetry, and no conclusion:
	Left-right visual symmetry, for example two half-photographs of a face juxtaposed, are perceived as being normal, even if the halves don't match... Random dot patterns with several prominent dots symmetrically placed, but with most randomly located, will be perceived as symmetric.

DIAGRAM "DOTS"





.c24.5: RHYTHMS OF BEHAVIOUR:

	The pineal gland, located under the cerebellum, plays a large part in establishing the body's rhythms, being implicated in the regulation of estrus and menstrual cycles, for example. In some animals, such as the salamander or tuatara reptiles of New Zealand, the pineal is near the surface of the body, and shows a response to light. XREF SALAMANDER POLARIZATION SENSITIVE CELLS. In humans, however it is buried quite deep. Melanotonin is released by the pineal and interacts with the suprachiasmatic nuclei area in the hypothalamus (Hyde, 1988).
	The pituitary of the salamander has about 175 photoreceptors similar to vertebrate rod structures. These are oriented perpendicular to light arriving through the skull, and each is rotated to a particular angle. Assuming the photoreceptors within the receptor cells lie flat within the lamellar membranes, they would be sensitive to particular polarizations of light. Experiments in which salamanders were trained to swim towards a shore in an aquarium which lay along the axis of polarized light showed that the pineal gland did indeed make that information available to the salamander. The salamanders would swim in correspondence with the rotation of the light (Camhi 1984, p143-145). Insects as well are sensitive to phase orientation of light.
	The hypothalamus is located very near the pituitary, and seems to control production of hormones.
	The sun's electromagnetic field oscillates at 10 Hz, as does the human alpha rhythm. Cellular clocks. Pacemaker cells. Acetylcholine or various peptides might mediate sleep. The hippocampus appears to be involved with learning and conditioning. The limbic system has a lot to do with behavioural strategy - in particular, emotions. Feeding behaviour is controlled by the balance of hormones in the bloodstream.



.c24.6: FREQUENCY AND ALERTNESS:

	High heart rate implies high frequency implies higher alertness. The mammalian startle response consists of increased alertness. (Someone bangs the table, my heart rate increases, I pay attention.) XREF - INVERTEBRATE STARTLE RESPONSES

DESCRIBE WORK AT ORNL USING FREQUENCY CODED NETWORKS



.c24.7: B-BRAINS AND FRONTAL LOBES:


	Self awareness is perhaps nothing more than the sum total of activation in the nervous system, with some prodding from a B-Brain.


DESCRIBE, WHERE DOES THIS MODEL COME FROM?


	The main brain, or A-Brain, is most intimately connected to the outside world, it is also where decisions and intentions are made.  It processes sensory data, relates it to experience, mulls over problems. In contrast, the B-Brain (proposed by Marvin Minsky, in Minsky, 1987) is completely isolated from the outside world. In fact, the B-Brain's world is the A-Brain. The B-Brain watches the A-Brain, providing a kind of self-awareness, interfering with the A-Brain if the A-Brain seems to be stuck in one particular mode of thought: the B-Brain gets bored.
	The function of the B-Brain, then is to provide self-programming: frustration, elation, boredom; all the things necessary to keep the A-Brain from doing nothing or getting locked up in a non-productive mode. It could dampen overly emotional behaviour, or amplify relatively quiet activity. In this way, the B-Brain is reminiscent of Adaptive Heuristic Elements, or even the Automatic Gain Control on radios and TVs.
	The concept of the B-Brain establishes a powerful new paradigm for network design, as it provides a way for networks to monitor and evaluate their actions. As networks become more and more complex, this ability will become more important. There is already a trend favouring this type of design, as demonstrated by the Adaptive Critic of Barto, Sutton and Anderson (1984), and the “consciences” being designed for Kohonen Self Organizing Feature Nets.



.c24.8: COMPUTERS AND BRAINS:


REWORK THIS SECTION WITH NEW FIGURES FROM MEAD 1990 IN NETWORKS MAGAZINE

	Neurons occupy a volume of approximately one litre.  If we assume that there are on the order of ten billion neurons, each neuron would occupy about 10-7 cm. The packing density of neurons is therefore at least a hundred times greater than that possible for transistors.
	In terms of power consumption, the brain radiates about 10 Watts, or about 10-9 Watts per neuron.  A neuron leads a transistor by a factor of about a hundred million.
	A neuron can react in a time between 10-2 seconds to about 10-4 seconds, a speed at least a hundred thousand times slower than a transistor. (Quantities are from “The Computer and The Brain,” by John von Neumann, 1958.)
	Neurons are energy efficient, small, and have an incredibly high connectivity, but they are very slow. Their extreme connectivity lets them implement inherently parallel processing; the term massively parallel is currently in vogue.
	Digital circuitry is very fast, but inherently serial, and this is the tradeoff. This is what allows us to model nervous systems on computers.
	Long range connections in the nervous system are digital, conveyed as all-or-nothing axonal impulses. Locally, processing can be either analog or digital, conversion taking place freely between the two modes. The amacrine interneurons of the retina are strictly analog; and, they have no axons. The interface between motor neurons and muscle fibres is an example of a location where digital to analog conversion takes place.


Section 1.3 introduces the sensory homunculus and tonotopic mapping.  Section 5.11 contains a general discussion of self organizing systems. Section 6.4.3 discusses the problems of the Perceptron.

See section 4.1 for a discussion of topographic mappings, and section 7.4 for the Kohonen self organizing feature net which uses the principle.

See section 4.6 for the importance of firing rate to attention.

Section 7.3 is all about back propagation.


cBEHAVIOUR, MEMORY, & SELF-ORGANIZATION
5





.c25.1: LEARNING IN REAL SYSTEMS

It is hard to justify the term ‘learning’ for a machine that relentlessly ignores its experience.
- Marvin Minsky & Seymour Papert in Perceptrons


	No single neuron is aware of the functioning of an entire nervous system, yet nervous systems self-organize, global learning occurs on the basis of local interactions.  Neuronal memory is achieved through morphological adaptation of the soma, and through the size of the synaptic junctions. Synaptic development is attenuated (synaptic spines are elongated increasing internal resistance to conduction of action potentials) if fish are raised in an socially isolated environment, demonstrating that learning affects cell morphology (Coss & Globus 1978). Connections, connection characteristics, cell shape - all these affect the behaviour of a neuron. The manner in which all these factors interact could be considered the “device physics of the brain” (Stevens 1985).

DIAGRAM OF GOLDFISH NEURONS

	The simplest type of learning is association learning, where a particular stimulus comes to be associated with a particular response. Habituation is the lessening of sensitivity of an organism to a particular stimulus. Adaptation is .<DEFN> Negative reinforcement is the cessation of an aversive stimulus.
DIAGRAM ASSOCIATION LEARNING SYSTEM + DESCRIPTION

	Classical conditioning is an elaboration of association learning, possibly having the same underlying mechanism, but several more complex effects. Classical conditioning can be observed in organisms as complex as a human, or as simple as an earthworm. In fact, it can be observed at the level of individual neurons, as is the case in the gill withdrawal reflex of the sea slug Aplysia.

DIAGRAM APLYSIA AND EXPERIMENT DESCRIPTION

	There are many familiar examples of classical conditioning. Typically, an unconditioned stimulus (UCS), such as an electric shock, yields an unconditioned response (UCR), like a startle reflex. If a conditioning stimulus (CS), such as a ringing bell, is paired with the electric shock, eventually the bell will be all that is needed to evoke the startle response, the conditioned response (CR).

	CS + UCS	fi UCR...	training
	CS	fi CR... 	result

	In an elaboration of the previous paradigm, if two CS's are presented simultaneously with an UCS, for example, if a ringing bell and a flashing light are presented at the same time as an electric shock, eventually either the bell or the light will be enough to evoke the CR.

	(CS1 + CS2) + UCS	fi UCR... 	training
 	CS1	fi CR
	CS2	fi CR... 	result

	Another phenomenon is called blocking. To begin, simple classical conditioning is completed: for example a bell is paired with a shock. Then, if a second stimulus is presented in conjunction with the first, for example, a bell and a light and a shock all together, conditioning to the second stimulus will never occur. Perhaps the flashing light contains no extra informational value, so it is never associated with the shock.

	CS1 + UCS	fi UCR...	training1
	(CS1 + CS2) + UCS	fi UC...	training2
	CS1	fi CR
	CS2	πfi CR...	result

	Classical conditioning demonstrates that feedback is vital to the learning process. In other words, an action must generate a perceptible response for learning to occur (Grossberg, 1980). DESCRIBE WHY THIS IS SO & IMPLICATIONS

.c25.2: PLASTIC MEMORY

	Hubel and Wiesel established that there is a certain amount of localization of function in the nervous system: some cells in the striate cortex respond preferentially to bars of light at particular orientations. Certainly it would be impossible to genetically encode the preferences of these cells, therefore, they must learn their behaviour. Hubel and Wiesel further established that there is a period of plasticity (or changeablity) during which the cells self-organize and learn to respond to particular stimuli. For a long time, it was assumed that the cells keep their memory fixed after the initial period of plasticity has passed.

	Whether or not learning shuts down at some point is a problem Stephen Grossberg calls the stability-plasticity dilemma. In model neural networks there are two almost paradoxical elements to be balanced. If the memories become fixed, they could become ultimately meaningless as the environment changes and the old memories no longer apply. On the other hand, if the codes never stop changing, meaningful generalization may never occur. Feedback is necessary to provide information about whether something is valid or not. (Non-linear feedback is generally used because linear feedback tends to amplify noise and send signals off to infinity.)
	Experiments done later than Hubel and Wiesel's pioneering work, reported by Creutzfeldt and Huggelund (1975, cited in Fair, 1988), showed that orientation cells in cortex are still plastic in mature adults. Adult cats were kept in darkness, except for brief periods of light (one hour twice a day) for two weeks. While the light was on, the visual environment consisted only of vertical lines. They discovered that the number of neurons sensitive to orientations around the vertical actually decreased relative to the number of neurons responding to horizontal orientations, thus demonstrating plasticity.
	Charles Fair (1988) suggests that the decrease was due to “mismatch overshooting,” a kind of over-sensitivity to “forgotten” orientations. He also suggests that the brain needs a constant level of “miscellaneously patterned input to maintain normal efficiency.”
	Heron et al, (19xx, cited in Fair 1988) reported a study wherein human subjects underwent sensory deprivation for 48 hours, through partial immobilization and unpatterned sound and visual stimuli. The subjects wore translucent goggles so that the subjects could see only vague blurs rather than dark or light. When the goggles were removed, various visual abnormalities were observed: walls appeared to move in and out, “abnormally strong” afterimages were seen. Opaque goggles were then placed on some of the subjects who were still hallucinating. Within two hours, the hallucinations were gone or reduced, suggesting that nonpatterned input has more of a “destructuring effect” than simple darkness. (This observation has important implications for artificial neural networks, as well as for natural ones.)
	Dreams could help prevent this destructuring effect during sleep. Slow wave, dreamless sleep is the time when the cells of the central nervous system ‘recharge’: the metabolic processes go into full swing. This process could be destructive to memory, however. About every ninety minutes therefore, slow wave sleep is interrupted by REM sleep which could serve to keep memory structured.
DESCRIPTION IMPLICATIONS OF DREAMING FROM LITERATURE



.c25.3: DISTRIBUTED MEMORY


Memory traces survive any cortical lesion, provided some portion of cortex remains intact.
- Karl S. Lashley


	Donald Hebb argued for distributed memory in his famous book “The Organization of Behaviour,” (1949) and his lasting contribution in this area was the concept of cell assemblies. His idea was that

“any frequently repeated stimulation will lead to the slow development of a cell assembly, a diffuse structure comprising cells in the cortex... capable of acting briefly as a closed system, delivering facilitation to other such systems and usually having a specific motor facilitation.  A series of such events constitutes a phase sequence - the thought process. Each assembly action may be aroused by a preceding assembly, by a sensory event, or - normally by both. The central facilitation from one of these activities on the next is the process of attention.”

DESCRIPTION RELATING CELL ASSEMBLIES TO DISTRIBUTED MEMORIES
	The concept of a cell assembly is a powerful one, and the idea that specific patterns lead to others in sequence is termed association.
	Rumelhart and McClelland (1986) argue that a distributed memory is more robust than a localized memory where one cell corresponds to one concept, because the distributed memory survives the loss of individual units, and noise in the memory traces.  As cells fail, the degradation of system performance is gradual, rather than immediate and total. If a concept is represented by the joint action of one hundred cells, and one of those cells fails, the pattern will still be 99% accurate.
	In the 1960s Bernard Widrow and his student Marcian Hoff were building the first adaptive filters, which were very much like neuron models. They had a working model, a huge box covered with potentiometers and meters that demonstrated learning using the Least Means Square (LMS) algorithm. They demonstrated it successfully to the people with the money. Later, when they stripped the unit down, they discovered cold solder joints, short circuits, even damaged components. Yet, due to the distributed nature of the design and feedback in the algorithm, the unit worked as if nothing was wrong (Widrow, 1988).
	In the first half of this century, Lashley argued for full distribution of memories, thoughts, and mental patterns (engrams), based on the observation that destroying portions of cortex results in a gradual degradation of performance, rather than piecemeal loss of conceptual ability and memory. In a series of experiments involving lesions in the brains of various animals, he demonstrated that specific memories don't reside in any one particular spot in the cortex. Once a rat, for example, learns to solve a maze, it retains the ability to solve the maze until the entire cortex is destroyed, although performance slowly degrades and the rat makes more and more wrong turns. Summarizing thirty years of research in the paper “In Search of the Engram,” Lashley found that “memory traces survive any cortical lesion, provided some portion of cortex remains intact.” He reached the ultimate conclusion that every area of the brain was involved in storing every memory, and every area of the brain was in some way involved in every thought. This would be total distribution of brain functionality.
	The opposite point of view, that an individual cell holds the complete representation of a single concept (for example, the activation of one cell represents the concept of ‘grandmother’) has been championed equally vociferously by the ‘connectionists.’
	Memories are likely stored in terms of what already exists in memory. Understanding only occurs in terms of previous understanding. Imagine therefore a cell embodying the concept of ‘pen,’ connected to related cells such as ‘long,’ ‘thin,’ ‘ink,’ ‘writing,’ and so on. If the ‘pen’ cell were destroyed in that kind of grandmother cell based memory system, would not the concept of ‘pen’ still exist as an emergent property of the net, a consequence of the web of relations between all the other cells?
	In that type of formulation, rather than having knowledge embodied in individual cells, concepts and generalizations could be stored in terms of connection strength and direction between ‘grandmother cells.’ This would result in a connected and weighted graph very similar in concept to Minsky's K-Lines (Minsky, 1988). Knowledge would be distributed between the cells, therefore the system would be robust.
	Related to these ideas is the question of temporal ordering. How can a mind associate a memory with a particular time? Is the when of an event available as part of a memory, or is it remembered as an association? “What else was I doing then? Where was I? What time of year? Hmmm... Must have been the spring of 1983; or was it 1984?”

	It seems after due contemplation of the literature, that both systems have merit, but neither paradigm alone can explain observable phenomenon.  Some sort of amalgam is necessary. In both vertebrate and higher invertebrate nervous systems, a high degree of differentiation and specialization of tissue is apparent, yet within the functional subsystems, there is a certain uniformity of structure (perhaps sometimes even self similar or fractal) and distribution of memories.
	Obviously, the differentiation of the macrostructure points to a particular reconceptualization of the ‘grandmother cell’ concept, and the homogeneity of the microstructure naturally suggests the distribution of the engram.



.c25.4: LONG AND SHORT TERM MEMORY

	Long Term Memory and Short Term Memory are frequently theorized to exist as completely different subsystems. This could simply be an old simplifying assumption devised by psychologists in order to explain observable phenomenon.
	In actual fact, it could be that LTM is the physical representation of the memory trace and STM is the pattern of activation across that engram. The two conceptualizations therefore describe different aspects of the same system.
	Perhaps every sensation that comes in is stored to some degree or another in short term memory. Retrieval of very recent experiences is easy, and, experiences that caused a strong association are also easy to get.
	Perhaps a model of short term memory could be based upon a topological space. We could visualize it as a big white room with percepts forming the walls... Thoughts, sights, sounds, body feelings, and so on, forming a topological space. T he space would undergo continuous transformation, much as the view changes as the eyes are shifted.
	In this model of short term memory, association strength is dependent upon the attention given to a particular percept - either external (a sensation) or internal (an association or thought).  The more unique a stimuli, the more likely it is to receive attention, the less unique, the more likely it is to fade, and be replaced by a different pattern of activation.
	Percepts could undergo decay as time passes. Focussing the attentional spotlight on a percept would renew its strength, giving it time to form long term memory traces. Repeatedly focussing on a percept would therefore lead to learning.
	“That reminds me of...” All aspects of the topological space excite long term memory stores (and each other), and if a strong enough resonance occurs, a new focus of attention is generated. “Hey! That reminds me of...”



.c25.5: ALICE IN WONDERLAND

‘Am I who I was this morning?’
asked Alice.


.c25.6: PRINCIPLES OF SELF ORGANIZATION


Perhaps [the most puzzling aspect of the overall motion of a flock] is the strong impression of intentional, centralized control. Yet, all the evidence suggests that flock motion is merely the aggregate results of the actions of individual animals, each acting on the basis of its own perception of the world.
- Craig W. Reynolds (1987)

BRIEF OUTLINE FOR SECTION FOLLOWS:
	Self-organization and minimization of energy are so completely intertwined as to be almost equivalent in meaning.
	To maximize volume and minimize circumference, honeycombs will self-organize to an approximately hexagonal grid. In a retina, a hexagonal tiling pattern would be nice.
- ants
- lateral inhibition & the Mexican hat function & Kohonen nets and homunculus
- smooth gradients across a network & LGN models
	The fact that prey organisms tend to have eyes located on the sides of the hide, giving good side and rearwards vision, probably has a great deal to do with the tendency of these organisms to form flocks, schools, or herds.
	Collision avoidance keeps boids from hitting each other, or obstacles.
	Velocity matching makes boids attempt to fly at the same speed and in the same direction.
	Flock centering is the urge of the boid to stay at the center of the group of boids within its visual range.  Since this is a local function, the flock can split to go around obstacles. It also allows small flocks to merge with each other if they meet.
	These three rules are sufficient to generate flock-like behaviour. Boids released near each other will flock together, maneuvering for position. The flock quickly chooses a direction, and when the flock turns, all the boids do so in synchronization.
	Termite nest architecture becomes more and more complex as the size and complexity of the termite brain decreases.



.c25.7: A SEARCH STRATEGY AND OTHER SIMPLE ALGORITHMS

	Butterflies tend to return to the same place in their territory. (ref xxx Days of Insects)
	Animals tend to adopt a strategy of straight line movements and turns while searching for something, rather than moving in continuous curves. As a target is approached, the angle of the turns increases, and the turns occur more frequently. This allows a more detailed search.
	This diagram shows the path of a bird looking for food (Guthrie, 1980).


	This diagram shows a curve which describes the way a fly steers itself to stay on a straight course. The horizontal axis shows the angle the fly is flying, zero being straight ahead, and the vertical axis shows the correction the fly will make to bring itself back on course, as a function of heading.
DIAGRAM FLY'S TURNING CORRECTION

c25.7: A SEARCH STRATEGY AND OTHER SIMPLE ALGORITHMS

	Butterflies tend to return to the same place in their territory. (ref xxx Days of Insects)
	Animals tend to adopt a strategy of straight line movements and turns while searching for something, rather than moving in continuous curves. As a target is approached, the angle of the turns increases, and the turns oc

.cNEURON MODELS
6






Everything should be made as simple as possible, but no simpler.
- Albert Einstein


.c26.1: NEURAL MODELLING


	Research into network models proceeds on a variety of levels, ranging from the macro scales of sociological interaction, to the micro scale of molecular and chemical processes.*
	This table, adapted from (MacGregor, 1987) shows the possible levels of analysis that characterize models.

STRATIFICATION OF MODELS:

Group Behaviour
Behaviour, experience, intelligence
Constructs (superego, id, drives, cognitive maps, cell assemblies, statistical configurations, the various brain centers)
Discrete Signals and Events (field potentials, spike trains, generator potentials, hormonal modulations)
Membrane Activity (synaptic conductances, active dendrite conductances, action potential conductances)
Molecular and Chemical Processes (chemical synaptic transmission, gating processes)

	Models relating adjacent strata are the most useful because they show how events at one layer relate to events at a level below.  Events at a higher level can be used as constraints for modelling events on the lower level, and knowledge of the lower level processes can be used to predict events on the higher levels. Models which only relate variables of a single layer are weak in predictive power, and models which relate several layers are the most significant. Grossberg's Adaptive Resonance Theory provides a prime example of the latter category. Working from the Membrane Conductance Levels, ART works through the Discrete level, right up to the Constructs level. (Grossberg, 1987)
	The description of behaviour, intelligence, and experience in terms of both theoretical and actual constructs is what Cognitive Science, AI, and psychology all attempt. Membrane activity and discrete signals together are typically the domain of neurophysiology, neuroethology, and neural modeling.  Models relating the levels from behaviour through to membrane activity are typical of neural network theory.




.c26.2: HEBBIAN LEARNING

When an axon of cell A is near enough to excite a cell B, and repeatedly or persistently takes part in firing it, some growth process or metabolic change takes place in one or both cells, such that A's efficiency as one of the cells firing B, is increased.
- Donald O. Hebb


	In “The Organization of Behaviour”, published in 1949, Hebb formulated the first detailed synaptic learning rule, a presynaptic and post-synaptic correlation rule. Variations of his rule are in common use today. Models which use a pre- post- synaptic learning rule are generally refered to as Hebbian models.
	The problem is, Hebb's law doesn't work as stated. It only allows for the increase of synaptic efficiency - synaptic weights in a pure Hebbian system will increase without bound. Such a system will never be stable because as the neurons learn, their weights will keep climbing towards infinity, until finally they are unrepresentable, or meaningless.
	One possible solution which makes the rule work as true correlation learning is to state that neurons which fire together will have their synaptic efficiencies increased, and neurons that don't fire together will have their efficiencies decreased. An alternative is to introduce an inhibitory term so that cells that don't fire together tend to inhibit each other. Another solution in common use is to continually renormalize the weights of each cell, so that they always add up to a constant value, the theory here being that there can be only a certain amount of resource available to each cell. Learning rules making use of these modifications are also termed Hebbian, in honour of Hebb's ground breaking work.
	Over the years, many variations have been suggested to make the rule work. It is important to remember that all the modifications introduced into systems of Hebbian learning are introduced to cover for the tendency of the weights to climb uncontrollably to infinity, and that these constraints, in general, are entirely arbitrary heuristics telling us nothing about real neurons.




.c26.3: THE HODGKIN-HUXLEY MODEL


	The Hodgkin-Huxley model established that large, short variations in the conductances of Sodium and Potassium govern the neuron's action potential. It also established the ionic basis of transmembrane potentials. It showed that neural events could be accurately and precisely modeled. The system of equations does not describe the system in terms of more fundamental neural events, and therefore is merely a conceptual guide that doesn't represent the underlying process.

I = C
F(dV, dt) + g
S(  , Na) m
S(3,  )h
B(V - V
S( ,Na)) + g
S(  , K) n
S(4,  )
B(V - V
S( ,K)) + g
S(  , L) m
B(V - V
S( ,L))


F(dm, dt) =
F(
B(S
S(  ,m)(V) -m),T
S( ,m)(V))


F(dh, dt) =
F(
B(S
S(  ,h)(V) -h),T
S( ,h)(V))


F(dn, dt) =
F(
B(S
S(  ,n)(V) -n),T
S( ,n)(V))

where:
V : 	Potential, mV
m : 	Sodium active conductance within the cell. 0<m<1
h : 	Sodium active conductance outside the cell. 0<h<1
n : 	Potassium active conductance. 0<n<1
t : 	time interval, mS
I : 	Current, mA/cm
S(2, )
c = 1 mF/cm
S(2, )
g
S(  ,Na) = 120.0 mS/cm
S(2, )   g
S(  ,K) = 36.0 mS/cm
S(2, )  g
S(  ,L) = 0.3 mS/cm
S(2, )
V
S( ,Na) = 55.0 mV  V
S( ,K) = -72.0 mV  V
S( ,L) = -49.387 mV
The Hodgkin-Huxley model of single action potentials in squid giant axons

	Active conductances for Sodium and Potassium, GNa and GK are defined in terms of the hypothetical functions n, m and h in the differential equations above. a and b are the rate control parameters.

GRAPH OF WHAT GOES ON
	The Hodgkin-Huxley model established the significance of transmembrane potentials, and that large, brief variations in the conductances of Potassium and Sodium are responsible for action potentials.


.c26.4: A USEFUL MODEL

	The neuron model described in this section is developed into a large network controlling the locomotion of a simulated insect in chapter nine.
	This system and its description is based on the simple model described in MacGregor 1987.  The equations model the following standard neuron-equivalent electrical circuit.

DIAGRAM CIRCUIT

	Each battery - potentiometer pair represents the transmembrane conductance of particular ion channels, and the capacitor represents long, electrically polarized lipoproteins in the membrane. The motion of the charge at the end of these lipoproteins corresponds to electrical current, and when an applied electric field displaces such a molecule, the transfer of energy which moves the protein corresponds to a classic capacitative effect in electromagnetic theory. (MacGregor 1987, pp. 246 - 250) The transmembrane conductances are typically modulated by synaptic activity, and the conductances determine the potential within the neuron.


F(dE,dt) =
F(-E + I + G
S( ,K) (E
S( ,K) - E) , T
S( ,MEM))


F(dq,dt) =
F((-q-q
S( ,0)) + cE, T
S( ,q))

if E ≥ 0 (spiking),
F(dG
S( ,K), dt) =
F(-G
S( ,K) + B, T
S( ,G
S( ,K)))     P
S( ,S) = 50 mV

if E < 0 (not spiking),
F(dG
S( ,K), dt) =
F(-G
S( ,K), T
S( ,G
S( ,K)))     P
S( ,S) = E

where:
I	: injected current.
E	: transmembrane potential	q	: threshold
P
S( ,s)	: potential in soma	c	: threshold accomodation parameter
G
S( ,K) 	: Potassium conductance	q
S( ,0)	: resting threshold, 10 mV
T
S( ,MEM) : Membrane time constant	T
S( ,q)	: time constant of threshold rise, 25 mS
	5mS
T
S( ,G
S( ,K))	: time constant of Potassium conductance change, 5 mS.
B	: post-firing Potassium conductance, 20 mV
E
S( ,k)	: Potassium equilibrium potential, -10 mV

The injected current I is calculated using the following equation. The tonic excitation (inhibition) parameter is intended to cause a certain predisposition towards firing in the neuron.
I =
I
SU(i, ,w
S( ,i)P
S( ,E
S( ,i)) )+
I
SU(i, ,w
S( ,i)P
S( ,I
S( ,i)) + tonic)
Where:
w
S( ,i) are the synaptic weights
P
S( ,E
S( ,i)) are the excitatory signal inputs
P
S( ,I
S( ,i)) are the excitatory signal inputs
	The differential equations can be reformulated as first-order equations, using the following generic equation:


F(dE(t),dt) = -A(t)E(t) + B(t)

	If the functions A and B are constant over a time interval, then the solution to the equation is:

E
S( ,i+D) = E
S( ,i)e
S(-AD, ) +
F(B,A)
B
BC
((1 - e
S(-AD))

	The solution decays away from its initial value E
S( ,i) towards the target equilibrium value of B/A with an effective time constant of A
S(-1, ). (MacGregor, pp. 251 - 253)
	The original system of equations can now be recast in time slice form:


F(dE,dt) =
F(-E + I + G
S( ,K)
B
BC
((E
S( ,K) - E), T
S( ,MEM))
becomes:
E
S( ,i+D) = E
S( ,i) exp
B
BC
[(-
B
BC
((1+G
S ( ,k))D/T
S( ,MEM)) +
B
BC
((G
S( ,K)E
S( ,K) + I)
B
BC
[(1 -exp
B(-
B
BC
((1+G
S( ,k))D/T
S( ,MEM)))



F(dq,dt) =
F(
B(-q-q
S( ,0)) + cE, T
S( ,q))

becomes:
q
S( ,i+D) = q
S( ,i) exp
B
BC
((-D/T
S( ,q)) +
B(cE + q
S( ,0))
B
BC
[(1 - exp
B
BC
((-D/T
S( ,q)))


if E ≥ 0 (spiking),
F(dG
S( ,K), dt) =
F(-G
S( ,K) + B, T
S( ,G
S( ,K)))     P
S( ,S) = 50 mV
becomes:
G
S( ,K
S( ,i+D)) = G
S( ,K
S( ,i))exp
B(-D/T
S( ,G
S( ,K))) + B
B
BC
[(1 - exp
B(-D/T
S( ,G
S( ,K))))


if E < 0 (not spiking),
F(dG
S( ,K), dt) =
F(-G
S( ,K), T
S( ,G
S( ,K)))     P
S( ,S) = E
becomes:
G
S( ,K
S( ,i+D)) = G
S( ,K
S( ,i))exp
B(-D/T
S( ,G
S( ,K)))



.c26.4.1: TRANSIENT ON RESPONSE OF THE SIMULATED NEURON

	If a steady current I is supplied to the system, the transmembrane potential E rises exponentially, at a rate governed by the membrane time constant T
S( ,MEM). Simultaneously, the threshold, q, rises governed by parameter c, and threshold time constant T
S( ,q). A spike is generated when E exceeds q. The spike allows the potassium conductance G
S( ,k) to increase as specified by the constant B. The increased potassium conductance allows the transmembrane potential E to drop towards the potassium equilibrium potential E
S( ,k). The potassium conductance decays at a rate governed by T
S( ,G
S( ,K)), which allows the applied current to take over, sending the potential back up again, perhaps causing another spike, and another increase in G
S( ,K). As G
S( ,K) decreases, E goes back up, but the threshold has increased to such a level that no further firing occurs.



.c26.4.2: CONTROLLING THE BEHAVIOUR OF THE SIMULATED NEURON

	The parameter c controls the accomodation of the neuron to tonic input. No accomodation, c = 0, produces a neuron which will fire constantly at a rate governed by the applied current I. Taking the value of c to be somewhere between 0.5 and 1.0 produces a cell which produces transient on or off responses. Setting B and T
S( ,G
S( ,K)) at low levels produces a cell which recovers quickly from firing, because the lower potassium conductance doesn't allow the transmembrane potential E to bleed off that quickly. Increasing B and T
S( ,G
S( ,K)) increases the refractory period, making the neuron respond at a slower rate.




.c26.5: THE HISTORY OF THE PERCEPTRON:


	The Perceptron was the first neural network model to be introduced in a completely specified form.
	Of course, there had been many models introduced previously, but none had all the necessary elements: well defined operation of the neurons, rules for connectivity, a learning algorithm. Each problem had been addressed before, but never all in the same piece of work. Because the Perceptron was completely specified, had a training algorithm, and was rigourously analyzed, it had a major impact and a great many researchers jumped on the Perceptron bandwagon.
	The initial successes made the researchers incredibly optimistic, and the initial feeling was that the Perceptron could do anything. It took a decade before the limitations of the Perceptron came to light.
	Perceptrons recognized shapes, Perceptrons could classify things, Perceptrons could calculate many functions, in fact, Perceptrons could compute any linearly separable problem. Unfortunately, most problems are not linearly separable, and gradually, researchers became disillusioned with the whole concept of neural computing.
	That frustration, and the lack of major conceptual breakthroughs, killed Perceptron research, and by extension, research into neural computers. Perceptrons had, after all, been hyped and sensationalized as computer brains, artificial intelligence was but a step away. Even though the writing was already on the wall, generally tagged as the final blow was the publication of "Perceptrons" by Minsky and Papert in 1969.
	When the book arrived, it was lucid and clear in its proofs of what the Perceptron could and couldn't do. Rather than being a bad thing however, the book perhaps represents a coming of age for neural computing research: the shedding of unrealistic and extravagant expectations, and a return to a more rigorous approach.  Minsky and Papert warned us that holistic misconceptions must be dispelled.  Explanations like "The system is this way, well... Just, because," illuminate nothing. The book planted the seeds for a more rigourous and theoretically sound rebirth of neuromorphic computing research, which was signaled by the release of Rumelhart's and McClelland's "Parallel Distributed Processing" in 1986.
	The Perceptron finds its origins in the neuron model of McCulloch and Pitts (1943), a model which is now almost fifty years old. The Perceptron was a modification of the McCulloch and Pitts neuron, and the Perceptron is still very popular today in its latest formulation, the back-propagation network. The McCulloch-Pitts neuron has aged quite well, and is in fact in common use today in the form of digital logic gates.



.c26.5.1: THE MCCULLOCH-PITTS NEURON


	It's interesting to note that this neuron model evolved from a philosophical exercise, an attempt to develop a predicate calculus. Warren McCulloch was fascinated by multi-valued logic systems, and searched everywhere for one. The logic we regularly deal with is two-valued, binary, and for the predicate calculus described in their paper McCulloch and Pitts used binary logic. It's long been recognized that the output of a neuron is binary, all or none. McCulloch and Pitts used that as their initial assumption to insure that the activity of every neuron could be represented as a logical proposition.

“To each reaction of any neuron there is a corresponding assertation of a simple proposition.”

	This implied conjunction and disjunction of propositions represented by activity in the nervous system.
	They decided that a certain number of synapses, the neuron's threshold value, would have to be active in a given time slice or quantum before the neuron could fire. They stated that

“temporal summation may be replaced by spatial summation”

and this assumption is commonly used today. There would be two types of synapses, excitatory and inhibitory. The excitatory synapses would all have equivalent weight, and the action of the inhibitory synapse would be absolute, if an inhibitory synapse was active, the neuron would not fire. Other researchers would later discard those rules in favour of excitatory and inhibitory synapses that could take on different values or weights.
	Finally, with the assumption that network structure doesn't change over time, they showed that networks of their formal neurons were equivalent in computational ability to a Turing machine, although, unlike a Turing machine, the networks would not be general purpose.



	The McCulloch-Pitts neuron is sometimes called a threshold logic unit or TLU. The TLU has several inputs which impinge on a summation device. The output of the summer is then clipped by a step function with a variable threshold, and a 1 or 0 results.



.c26.5.2: THE PERCEPTRON


	The Perceptron was based on several fundamental ideas, many of which were later proved incorrect. Some of the assumptions were enough to make the concept unworkable in the long term. One of the main problems was caused by the assumption that the organization of a nervous system is random, subject to genetic constraints.  If this assumption is discarded, many useful networks can be made, specifically those which preserve topological relationships.
	The other assumptions were useful : The original system is plastic, meaning its structure is not fixed. Over time, through exposure to various stimuli, the system will self-organize. Positive and negative reinforcement control the formation of connections. The system performs 'similarity detection', in that similar stimuli activate the same sets of cells. For example, one cell would be an 'A' detector, another a 'B' detector, etc. This is a localized memory.
	Perceptrons were originally organized into several layers: a retina of sensory units communicating with association cells via an optional projection area. Response units followed the association units. All units were similar to the McCulloch-Pitts neuron, except that weights could take any value, positive-excitatory or negative-inhibitory. Between the retina and the association area, some kind of feedback reinforcement could take place, so that retina cells helped their particular association cells or vice versa. Connections between all the layers were to be random.





.c26.5.3: WHAT THE PERCEPTRON COULDN'T DO *


	A famous proof in the book “Perceptrons” is the “parity problem.” No combination of weights can induce a Perceptron to determine the parity of a bit pattern, unless at least one Perceptron is connected to every part of the input pattern.
	The “parity problem,” and the “exclusive-or problem” both point out the need for multilayer networks. Unfortunately, in 1969, no convergence procedure existed for multi-layer networks.†
	A theorem was proved by Kolmogrov which showed that a multi-layer network with N(2N+1) nodes could learn any continuous function of N variables. Unfortunately the theorem doesn't give any clues as to how to generate the weights. (Lippmann 1987)
	An interesting example from the book demonstrating the problems of linear separability is the “connectivity proof,”which involves diameter limited Perceptrons. A diameter limited Perceptron means that no single processing element can have access to the entire input space. The following set of figures is enough to show that no diameter limited Perceptron can determine whether a figure is connected or if it is not.



	Consider a grid superimposed over one of the patterns above, subdividing it into pixels, and further imagine that Perceptrons are connected in some fashion to the grid.
Because the Perceptron can only perform a weighted summation of its inputs, there is no way a diameter limited Perceptron can distinguish the patterns from one another, let alone determine which are connected.



	The problem is, information relating to the relationships of the elements is nonexistent. The geometric identity of an object represented this way is lost. The form of a representation is very important. Converting a pattern into a binary vector is seldom enough. Consider:



	Which figure is easier to recognize?
	Another problem with Perceptron solutions is scalability. Many demonstrations are toy problems, they show a solution, often elegantly, but they do not scale up - large problems may imply weights that are infinitely large, and therefore unrepresentable. For an example of this problem, have a look at the solution achieved by back propagation for the determination of symmetry, in section 4.2.



.c26.5.4: THE PERCEPTRON CONVERGENCE THEOREM


	The Perceptron Convergence Theorem is states that a Perceptron can learn any group of linearly separable patterns. Of course, since the Perceptron is usally implemented on a digital computer, it has a finite set of states. “Convergence” is then rather a vacuous idea, because a solution could be reached by stepping through and testing every possible state. (Minsky and Paper, 1969) Time of convergence is the important factor, and it is this which the convergence algorithm tries to give us.
	The classical Perceptron convergence algorithm works as follows:

INSERT ALGORITHM HERE


.c26.6: ADAPTIVE FILTERS


	Adaptive filters are the result of the work of Bernard Widrow and Marcian Hoff, dating back to about the same period as the introduction of the Perceptron. Their model, called the Adaline (ADAptive LINear Element) made an immediate impact because of the tack taken by their presentation: rather than being a purely theoretical model, their paper “Adaptive Switching Circuits” was mostly concerned with practical applications and implementations (Widrow and Hoff, 1960).
	The Adaline was put to immediate use, and has found its way into numerous applications. The original application was adaptive antennae, and today an adaptive filter trained by the Adaline's method of gradient descent is used extensively in communications: high speed modems, long distance telephone lines, satellite communications, and so on.
	The Adaline was an adaptive system, designed to minimize the number of errors occurring during the execution of a particular task. An operator had to give examples of input to the system, and examples of the desired response, and the system learned to match the examples. The performance of the system was directly related to the extent of the system's experience.



	The Adaline accepts binary inputs (of plus or minus one) and a bias value, all of which are weighted by the adjustable a's and summed. The quantizer converts the output of the summer to a binary value. Widrow and Hoff established a very important precedent by realizing the Adaline in hardware. The first Adalines had a meter that showed the output of the system, and numerous potentiometers for adjusting the weights by hand. A pattern would be entered using switches, and an error value would appear. All the weights would then have to be adjusted by the same absolute magnitude, and gradually, the error value would tend towards zero. A later automatic implementation used the plating of pencil leads - memistors, for memory resistor - to adjust the weights.
	The algorithm that trains the adaptive antennae, Adalines, adaptive filters, and many other systems besides, is called gradient descent. I f a problem is visualized in geometric space, it is easy to see the process - the algorithm searches for a local minimum in the problem space. The paradigm of gradient descent is used extensively by all types of neural nets. It is the basis of the Hopfield network, and also of Back Propagation.


	The ball represents the state of the system, and the curve represents the energy space of the system. The ball will try to roll down the gradient of the curve until it reaches the lowest point, the local minimum, where it will come to rest.
	It is important to remember that this diagram is only supposed to give an intuitive feel for the algorithm. In reality, the energy surface would have a much higher dimension, and as such, we can't even imagine what it would look or feel like.
	Anyway, referring to the simple diagram: If the system has more than one local minimum, there is no way to tell if the minimum that has been found is actually the global minimum. If there is more than one minimum, the system is nonlinear, and the main constraint on the gradient descent algorithm is revealed: it works only with linear systems. Some training rules attempt to overcome the problem of the local minimum by shaking the system, adding noise or energy, and then allowing the shaking to subside. If the system is stuck in a local minimum, it might bounce loose and thereby settle to the global minimum by the time the shaking stops. A metal might be heated so that all the molecules are shaking violently and randomly, and then slowly cooled down so that the molecules arrange themselves into a crystalline form, the most stable arrangement. This process is called annealing, and by analogy, the training rule for adaptive systems is called simulated annealing.*


.c26.6.1: ADALINES APPLIED

	The examples in this section are from "Neural Networks for Adaptive Filtering and Adaptive Pattern Recognition," by Bernard Widrow, and Rodney Winter, 1988.



	This diagram shows the basic adaptive filter. The input is filtered and compared to the desired response, and the difference between the two is used to tune the adaptive filter. The most difficult thing to understand is the desired response input. If we know the desired response, why do we need to filter the input? The desired response will be different for every application.
	It helps to consider an example:



	We can learn about the unknown system's dynamic response by feeding the input signal into both the adaptive filter and the unknown system. The adaptive filter will then learn the set of weights which lets it match the response of the unknown system.



.c26.7: STOCHASTIC NEURONS


	In a deterministic system, a regular periodic oscillator, say, the amount of information is very low: we know the amplitude of the oscillation, the period, the phase. On the other hand, in an indeterminate system, where no regular rule governs its operation, the information content is very high. Consider music for example: There is a long series of notes, each with its own description, or information. Each note is an event, and each event carries information with it. If an event is observed in an indeterminate system, that observation constitutes a specification of information.
	Qualitatively, the less likely an event, the more information is associated with that event. These simple observations led Shannon and Weaver (Shannon, 1949 XXX) to lay the groundwork for modern information theory, and to other useful concepts, such as the ‘bit’, which is the smallest possible unit of information.
	Stochastic models describe causal processes in determinate or indeterminate probabilistic terms by using probability density functions, correlation, or other quantizing methods.
	John von Neumann was searching for a language of the brain towards the end of his life. Theories about the brain typically employ the language and formalisms of physical law, and symbolic logic. In the final chapter of his book “The Computer and the Brain,” (1958), he suggests that the language of mathematics is not the language of the brain, but perhaps only a historical accident. “When we talk mathematics,” he said, “we may be discussing a secondary language based on the primary language used by the nervous system.”
	For a computer, high accuracy is a given. In a nervous system, however, physical constraints limit the accuracy. Neurons have a certain maximum pulse rate, a certain charge and discharge rate: physical limitations. Only a small accuracy is possible, orders of magnitude less that that of a digital computer. This leads to a very low precision system, but a reliable one... The system is statistical, rather than deterministic. In a probability governed system, it doesn't make all that much difference if a bit is lost here or there.
	An intriguing idea is to model network connectivity stochastically, or in terms of probability density functions. A well known model that used this approach to model a system with thousands of neurons was the bullfrog simulation, Rana Computrix, of Pellionisz (1977 XXX).



.c26.8: CHAOTIC NEURONS

Chaos exists as raw material from which to create order.
- Frank Herbert

	Chaos is coming up more and more often in the study of neural networks. Chaos is the order which hides within disorder which itself hides within order. It manifests itself as soon as a feedback path or a non-linear dynamic appears within a system. Strange attractors, bifurcations, basins of attraction, and so on - the terms will become more common. It is necessary to gain an understanding of the phenomenon.

DIAGRAM THE PARABOLA WITH A LINE ADAPTED FROM BRAITENBURG.

	Most dynamic systems exhibit chaotic behaviour.
	Walter Freeman's group has studied chaotic associative memories extensively. The networks are typically made up of oscillating neurons, and the mass action of the system is chaotic. When a pattern is presented, however, the system quickly bifurcates into a stable attractor, thus performing classification. Bill Baird has shown how attractors can be set up to store any analog vector desired.  ref IJCNN SUMMER 89
	Chaotic systems are unpredictable by nature. Small changes in initial conditions cause rapid divergence from an expected time series. Although chaos itself is unpredictable, the phase space diagram remains relatively unchanged.  The phase space diagram is sufficient to get Lyapunov coefficients, and study of the phase space diagram reveals the nature of the problem.



.c26.9: GATED DIPOLES




	A gated dipole with its inputs connected to its outputs will oscillate rhythmically.


*This section describes research. For a discussion of development, see Appendix A.

*Minsky and Papert's "Perceptrons" provides a readable and rigorous delineation of the Perceptron's capabilities.

†See section 7.3 on back propagation, for a convergence procedure that can handle multiple layer networks of Perceptrons.

*See section 7.4 for the Boltzmann machine, which makes use of simulated annealing to overcome the multiple minimum problem.
DESCRIPTION OF EXAMPLE HEBBIAN LEARNING SYSTEM (RECEPTIVE FIELDS)

	Unfortunately, Hebb'by itself is not enough to model a neural system. The problem is that the rule only crease of synaptic efficiency:le because as the neurons learn worse,	Over the yearscompensateity, and that these constraints in generaldon't don't t each other. Another solutionsum to a constant value. The justification for this rule is that is only a certain amount of resource (neurotransmitter)

DESCRIPTION MATHEMATICAL AND SIMULATION TREATMENT OF HEBBIAN LEARNING, CORRELATES TO LEARNING IN APLYSIAHodgkin-Huxley model established that it was possible to accurately model neuronal events. It demonstartediations in the conductances of sodium and pa neuron’ proposed by Hodgkin and Huxley describes the qualitative behaviour of neurons, but doesn'tor explain DESCRIPTION HOW MODEL WAS DERIVED. potentials in squid giant axons.6.3.1(,)
STANDARD EQUIVALENT ffect in electromagnetic theory.I	E		Following (MacGregor, 1987 pp. 251-253), the differential equations can be reformulated as frst-order equations, using the following generic equation:


F(dE(t),dt) = -A(t)E(t) + B(t)
ve time constant of A
S(-1, ).6.3DESCRIPTION OF TRANSIENT ON-RESPONSE AND RELATIONSHIP TO GROSSBERG'S GATED DIPOLE MODELS

DIAGRAM TRANSIENT ON RESPONSE DEMONSTRATION

6.3	The model can be controlled quite easily to generate a wide variety of behaviours. 6.4A BRIEFERCEPTRON a completely specified form.  efined operation of the neurons; rules for connectivity; More recently, both Back Propagation and Hopfield networks have enjoyed similar success for the same reasons. They were well defined, and methods of mathematically analyzing the systems were easily obtained.Initial successthe general feeling was Perceptrons recognized shapes;rceptrons could classify things;could calculate many functions;able problem.

INSERT BOX WITH PROOF THAT PERCEPTRONS AND SINGLE LAYER BACKPROP NETS CAN COMPUTE ANY LINEARLY SEPARABLE FUNCTION.

nearly separable, and graduallyle concept of neural computing.
	That frustration major conceptual breakthroughsral computers. Perceptrons had after alltelligence was but a step away! the publication of “Perceptrons” by Minsky and Papert in 1969 is final blow to research at that time.
	When the book arriveda particular strictly defined Perceptron could and couldn't do.

INSERT BOX ABOUT MINSKY AND PAPERT'S DEFINITION OF THE PERCEPTRON, EMPHASIZING NARROWNESS OF THE DEFINITION

	Recently it has become popular to knock Minsky and Papert for the publication of this book. I feel this is not goodas I feel it marked dispelled.  Explanations like “workshis way, well... Just, because,”led by the release of Rumelhart and McClelland's “arallel Distributed Processing” in 1986.
6.4it is still with us Chances are you have several hundred McCulloch-Pitts neurons on your wrist if you are wearing a digital watch.Td by multi-valued logic systemsspent years in the searchtrue or falsebynd Pitts used binary logic. It’ number of synapses, the neuron'used today in almost every neural network model (It is commonly expressed as the inner product of a synaptic weight vector w, and a signal vector x, arriving at those synapses:
I
SUi, ,w
S( ,i)x
S( ,i)).
	Tes were proposed: excitatory and inhibitory. . Ion that network structure doesn'y to a Turing machine, althoughis output6.4Some of the assumptions which led to the Perceptron also doomed it Some of the resulting problems are detailed in Section 6.4.3.randomness other assumptions proved moe useful:networknections. The system performs ‘similarity detection,’ example, one cell would be an ‘A’ detector, another a ‘B’ and so onform of ollowed the association units.

DIAGRAM PERCEPTRON NETWORK (OPTICAL ILLUSION VERSION)

	etina and the association areaociation cells or vice versa. As noted above, cthe layers were to be random.6.4



INSERT PROOF THAT NEURAL NETWORK CAN LEARN ANY L2 FUNCTION, AND REFERENCE
“Perceptrons"is defined as a network connected suchin some fashion to the grid. se topological  figure is easier to recognize?
demonstrations are toy problems in thatghts that are infinitely large refer to6.4d testing every possible state.nce algorithm tries to give us.

6.5In the diagram above, t

6.5do we need to filter the input?rn about the unknown system’
6.6, for exampleand, in an indeterminate systemthe of the system, the information content is potentially vas andistinctul concepts, such as the ‘bit,’ possible unit of information.  Information theory leads to swhich n, or other quantizing methods. MUST RESEARCH THIS CONTENTION.aw
 probabilistic system, it doesn'6.7being mentioned terms will become more and more familiar as time goes on. DESCRIBE WHAT LYAPUNOV COEFFICIENTS TELL US
6.8

 mulated insect in chapter nine.

 The Back Propagation algorithm championed by the PDP group is described in Section 7.2.

 Minsky and Papert's “Perceptrons” of 1969 provides a readable and rigorous delineation of the Perceptron's capabilities.

 Section 7.3 describes the back propagation algorithm which can train hidden layers.

Fukushima's Neocognitron (Section 7.7) shows one way of organizing pixel data so that identifying features can be abstracted and characters successfully recognized.



This assumption is brazenly defied by hyperacuity in sensory perception. As an example, the interaural time difference is used by the auditory system of the bat to determine the range and location of objects with an accuracy far greater than that implied by the slow neurons performing the computation. (See chapter 3 for details.)


I = S
S( ,i)w
S( ,i)P
S( ,E
S( ,i))+ S
S( ,i)w
S( ,i)P
S( ,I
S( ,i)) + tonic    S
S( ,i)

	DESCRIBE EXCLUSIVE OR FUNCTION

.c26.10: A POINT CHARGE CLASSIFER

DISCUSSION RELATION TO K MEANS CLASSIFIERS
	As far as references for this system go, any basic physics book will do. The classifier itself is of my own devising, although it does take a measure of inspiration from the central nervous system's topographic mappings, and on a practical level, from the Kohonen self organizing feature net.
	Imagine a series of vectors of unit length, all joined at a vertex, like strings tied onto a nail, and each possessing a charged point at the outside end. The charged points can all be different sizes, but they all have the same sign, so they repel each other. Since the vectors are free to swing in any direction, they will, until they reach equilibrium, where every point is balanced against every other - every point is basically as far away from every other as it can be, governed by its strength relative to every other's. Just like the laws governing the configurations of molecules. This process is inherently local, and could therefore be a useful neural or parallel processing metaphor.
	Because the vectors have unit length, they point somewhere on the surface of a hypersphere.
	Once these reference vectors have reached equilibrium, they are ready to act as classifiers. A point charge corresponding to an input arrives somewhere on the surface of the hypersphere, and then slides into one of the existing charges, which we will call attractors. Attractors and input charges have opposite signs. As a matter of convention, we will use plus for input, and minus for attractors.
	When the positive input charge arrives, it will attract the attractors, swinging them around a little. When the attractor and the input meet, they add in an absolute sense, and the attractor becomes heavier. Heavy attractors will not swing much at all, and therefore they act as classifiers.
	When attractors become quite heavy, they split into two smaller attractors, providing more resolution for classification.


	This process calls to mind the topographic mappings of the central nervous system. Consider the homunculus: Areas of its topology rich in input, such as the fingertips, will have many cells dedicated to sensory processing, whereas areas that receive less input, like the back of the hand, will have relatively small numbers of neurons monitoring them.
	At first, there might be only one attractor, but it would soon split as input arrived. The process could conceivably be limited by a certain maximum number of attractors, or by a certain desired amount of classification or granularity. One of the main functions of classification is to reduce the number of degrees of freedom of the input space, and if the dimensionality of the classifier approaches that figure, it can lose its usefulness.



.c26.10.1: IMPLEMENTATION DETAILS

	The problem of moving point charges about on the surface of a hypersphere is an n-square problem - pointing to combinatorial explosion - clearly not practical for simulation on a sequential machine. A different simulation paradigm is therefore necessary.
	Imagine a two dimensional hypersphere, a disc. Extending out at a normal - ninety degrees - from the disc is a balance vector. When equilibrium has been reached, this vector will be exactly normal, but as input arrives, it will tip. When an attractor grows after accreting the input, a certain redistribution of vector positions will be necessary to tip the balance vector back to vertical.




.c26.11: THE ADAPTIVE CRITICAL ELEMENT


	The Adaptive Search Element (ASE)/Adaptive Critical Element (ACE) system of Barto, Sutton and Anderson is investigated in terms of its applicability to maintaining a simulated autonomous underwater robot at a certain distance above the ocean floor.
	The ASE/ACE system is comprised of two neuron-like elements, trained by operant conditioning. The ASE controls two thrusters, one facing up, and one facing down, and the ACE criticizes the performance of the ASE. Together they work to avoid punishment - which comes if the submersible surfaces, or crashes into the bottom. The only data available to the system is a memory of its actions, the signal from a down facing depth sonar, and the punishment signal.
	The ASE/ACE is a true tabula rasa. The equations of motion acting on the submersible are unknown to the system In fact, at first the system doesn't even know what it is supposed to do. Through trial and error, the system explores its state space and the possibilities of control. Gradually the ASE learns to avoid those sequences of decisions which lead to punishment. The ACE learns to predict which states will lead to punishment, and so it sends a continuous reinforcement signal to the ASE to accelerate learning.
	The ASE alone is investigated, and then the standard ASE/ACE model. With slight modifications to the control algorithm to limit the range of synaptic weights, the system learns quickly. Finally, extending the equations of the ASE/ACE model from the real numbers of the original model to complex numbers allows more sophisticated control, and consequently more sophisticated behaviour to emerge.



Advances in our appreciation of the complexity of biological cells make it clear that the ... metaphors which place the neuron at the level of a computer logic gate are inadequate.
- Barto, Sutton, and Anderson



.c26.11.1: BACKROUND TO THE ASE/ACE SYSTEM

	In 1983, Andrew Barto, Richard Sutton, and Charles Anderson presented an unusual neural network for learning control problems. They chose a difficult problem to attack: the inverted pendulum - in other words, pole balancing. The system consisted of a cart which could be driven to the left or to the right at a fixed velocity, and a pole, attached to the cart by a hinge.
	Earlier modelling attempts required an example (like a skilled human) to copy, or continuous evaluative feedback of performance. This model had to learn how to control the system all by itself. The only feedback available from the outside world was a failure signal announcing that the pole had fallen over. The controlled system's dynamics - the equations of motion - were not programmed into the system. Evaluative feedback was of poor quality. These constraints are like those faced by biological organisms.
	Unlike most neural network models which involve a great many simple processing elements, the model developed by Barto, Sutton and Anderson was comprised of just two relatively complex neuron-like elements, the Adaptive Search Element (ASE), and the Adaptive Critical Element (ACE). The ASE sends a controlling signal to the physical system, and the ACE criticizes the performance of the ASE in an effort to make it learn faster. This type of system is known as "learning with a critic," as opposed to "learning with a teacher," which is the mode most neurally inspired systems operate in.




.c26.11.2: THE APPROACH


	Marvin Minsky calls one of the major problems in artificial intelligence research the "credit assignment problem." Some actions are beneficial; some are detrimental to system performance. A system needs some way of determining which actions were responsible for which results. Feedback is vital to learning.
	The starting point towards solving the problem was the hypothesis of A.H. Klopf (1982) that neurons could be conditioned in an operant or instrumental manner: classical conditioning. A neuron would learn to attain certain states while avoiding others.
	As to how this could be done, the muse came in the form of the "boxes" system of D. Michie and R.A. Chambers. (1968) State space was partitioned into "boxes," each with its own resident "demon" which would choose a direction for the cart to move. All the demons taken together are considered to be metaphors for synapses to a single neuron.

DIAGRAM PHASE SPACE

	In this diagram, a displacement, d, versus velocity, v , state space is shown partitioned into boxes (or synapses!). The shaded box shows the current system state: velocity and displacement are both large and positive. The demon within this box must choose an action that will be most likely to prevent a failure from occurring.
	Learning - adaptation - is based on an estimate of how long the system would continue operating dependent on particular actions. When the system fails, the individual estimates in each box must be updated to reflect that eventuality.
	The ACE/ASE is not a completely deterministic system. Rather, it relies on noise to explore the state space, and as a basis for subsequent learning. As Frank Herbert said, chaos, apparent disorder, provides the raw material for order.



.c26.11.3: DETAILS OF THE ASE


	Barto, Sutton, and Anderson chose the broom-balancing problem to attack, we chose one closer to our field of interest. We wish to control the depth of an underwater robot as it cruises along above irregular ocean-floor terrain. The only information available to the robot is its distance from the ocean floor, and a failure signal. The failure signal is supplied whenever the robot goes too close to the bottom, or if it gets too far from the bottom. The robot doesn't know this however, and must work to avoid the punishing failure signal.
	The system is comprised of three major parts: the robot, the ASE, and a state space decoder.


	 Displacement, d, refers to the distance the submersible is from a desired distance above the bottom. If the submersible is to track along four meters above the bottom, and the submarine is actually two meters above the bottom, then d = actual - desired = -2. Velocity, v, refers to the submersible's vertical velocity. Positive velocity will send the submarine down, negative velocity will send it up.
	The decoder divides the state vector up - displacement is a little high, a lot high, a little low, a lot low, velocity is zero, velocity is moderate up, and so on - and generates therefore a unique and finite set of combinations. For every possible combination, there is a single element in the decoder. If the state vector enters a particular element, that element gives an output of one, and every other element will be zero.

DIAGRAM 0's and 1's

	Upon failure, every element of the decoder will be set to zero, as the system is in no valid state. (This last is an important condition for proper operation of the equations.)
	The output of the decoder, x, is passed to the ASE, each element being connected to a particular synapse having a weight of w.

DIAGRAM SHADED BOXES

	This diagram shows what the synaptic weights might look like before much learning has taken place. Dark squares represent a negative weight - or a high likelihood that system will decide to thrust upwards, and light squares represent a positive weight - the probability of thrusting downwards.

y(t) = f
B
BC
[(
I
SU(i=1,n, w
S( ,i)(t)) x
S( ,i)(t) + noise(t))             f(x) =
B
LC
{(
A(+1 if x ≥0 , -1 if x < 0))


	Because of the addition of noise to the equation, the ASE's output is governed by chance. Noise has a Gaussian distribution.
	The output of the ASE, the bracketed term in equation 1, is passed through a thresholding function f, the quantizer, equation 2, which evaluates to either positive or negative one.

DIAGRAM QUANTIZER

	The quantizer is typical of the thresholders found in most neural network models. In this case, a squashing function such as a sigmoid curve is not used, because the weights usually stay within a reasonable range on their own, and besides, once a weight becomes very large, only sign is important, not value.
	The most recent choices made by the controller are the ones most likely to be responsible for the current success or failure of the system, and therefore the most eligible for having their weights changed. An eligibility trace e is stored for every synapse. The eligibility of a given synapse starts out high soon after the ASE makes a choice at that synapse, and decays as time progresses. The rate of decay is governed by d, which has a range of zero to one.

e
S( ,i)(t+1) = de
S( ,i)(t) + (1-d) y(t) x
S( ,i)(t)
	The value eligibility takes immediately after a decision is made works out to (1-d).
	The eligibility actually encodes more information than just how much time has elapsed since a decision occurred. The inclusion of the output of the ASE, term y in equation 3, means that eligibility will be positive decaying to zero if the output of the ASE was positive, and it will be negative decaying to zero if the output of the ASE was negative. Thus, the eligibility remembers the last choice made at a synapse, as well as how long ago that choice occurred.
	The next equation shows how the weights change over time as determined by a which is the rate of adaptation, e, which is the eligibility of a particular synaptic weight to change, and r, which is the reinforcement signal.

w
S( ,i)(t+1) = w
S( ,i)(t) + ar(t) e
S( ,i)(t)
	The system learns through operant conditioning. In equation 4, setting the reinforcement signal r to negative one is an aversive stimulus - punishment, in effect. A positive value for reinforcement would be reward, or positive reinforcement.
	As long as the system is functioning properly, the reinforcement signal is held at zero, and the weights do not change. On the other hand, if a failure occurs, the negative value of the reinforcement will penalize the most recent decisions (highest eligibility synapses) which led to the failure, making those decisions less likely to occur in the future.



.c26.11.4: DETAILS OF THE ACE


	When failure finally occurs, one decision would probably have been better than the other. The algorithm of the ASE is not sophisticated enough to take that fact into account, so, the role of the ACE is to provide a continuous reinforcement signal. The next diagram shows where the ACE fits onto the overall system. The reinforcement signal r is now fed in to the ACE instead of the ASE, and the ASE receives an internal reinforcement signal,r'.


	Using its learned weights, the ACE computes an improved reinforcement signal which it sends to the ASE so that learning can occurs continuously rather than only upon failure. The fact that reinforcement can arrive when good choices are made, as well as bad, means that learning will progress at a much quicker rate.
	The ACE receives the same signals from the decoder as the ASE, and has a synaptic memory trace for every box, just like the ASE does. Rather than storing a most likely decision in each synapse however, the ACE stores a prediction, p(t), or an expectation of the reinforcement that will be received from the environment for each individual state. Each synapse therefore contains a rating of the dangerousness of that particular state - dangerous state boxes will contain a strong prediction of failure.


	This diagram shows what the ACE eventually learns about the submersible control problem - if displacement and velocity are both large and of the same sign, failure will soon occur. The white squares show where no reinforcement arrives from the environment, the dark squares show that a failure signal is likely to occur very soon.
	The internal reinforcement signal, r', the ACE sends to the ASE is:

r'(t) = r(t) + gp(t) - p(t-1)

	The term g, the discount term, is provided so that in the absence of external reinforcement, the internal signals will gradually die away to nothing. When no failure has occurred, r(t) is zero. The internal reinforcement, is therefore the difference between the discounted predicted reinforcement gp(t), and the previous predicted reinforcement p(t-1).
	If the system moves from a low danger state to a high danger state, the internal reinforcement will be negative, punishing the system. If, on the other hand, the system moves from a high danger state to a lower danger state, reinforcement will be positive: reward. To quote Barto, Sutton, and Anderson, “the system thus learns which states are safe, and which are dangerous.”
	Let's examine equation 5 a little more closely. Upon failure, the output of the decoder, and consequently the ACE, p(t), will be zero, but the external reinforcement, r, will be -1. In this case, the internal reinforcement, r', will be the difference between the previous reinforcement signal, p(t-1) , and the failure signal. A fully predicted failure will therefore cause no reinforcement. Incorrect actions that came before the failure will be punished in accordance with how much the ACE's eligibility traces have decayed. The predictions of failure that came before the failure will be rewarded, because they were accurate predictions.
	The equations governing learning in the ACE are very similar to those which control the ASE.
v
S( ,i)(t+1) = v
S( ,i)(t) + b
B
BC
[(r(t) + gp(t) - p(t-1)) X
S( ,i)(t)
	The internal weights which yield the predictions are denoted v.
	Notice that the term appearing inside the square brackets is the same as the internal reinforcement signal, r', in equation 5. In form and substance, equation 6 is almost the same as the ASE's weight change formula, equation 4, except for the reinforcement term, and the form of the eligibility, in this case, X
S( ,i)(t).
X
S( ,i)(t+1) = lX
S( ,i)(t) + (1-l) x
S( ,i)(t)
	The ACE's eligibility trace equation is almost the same as the ASE's (equation 4).  Note that the initial value of a trace, the value it will acquire immediately after a decision is made is 1-.
	The last equation, equation 8, shows how the ACE makes its prediction.
p(t) =
I
SU(i=1, n, v
S( ,i)(t) x
S( ,i)(t))
	Recall that v represents the ACE's internal weights, and x represents the output of the decoder. If a failure has occurred, the prediction of the ACE is zero, because every element of the decoder will be zero.

.c26.11.5: THE EXPERIMENT


	We first developed an ASE system to control the robot, and then an ACE/ASE system to do the same thing. To reiterate the problem, the system was responsible for keeping the robot a certain distance above the ocean floor. The robot was equipped with a thruster to make it move forward, an upwards thruster, and a downwards thruster. The vertical facing thrusters operated at a constant force, F, in a mutually exclusive manner. Failure occurred when the robot went too high above the ocean floor, or if it went too low (crashed!).
	The initial model did not make use of the Adaptive Critical Element. Even still, it was able to learn the control task. The ACE is probably necessary for any more complex tasks, or if the dimensionality of the problem's state space increases. The solution arrived at by the combined ACE/ASE system was quite different in character, but more on that later.
	A simple set of equations described the simulated physical system. Velocity was constant in the forward direction. It was assumed that the robot's mass was 1, and that force could take on values of -1, 0, or +1. The 0, or off position, was not used in the initial simulations. In control theory, this is called a "bang-bang" system, because there is no gradual control, just the two opposing forces.

for F = -1  	d
S( ,i+1) = d
S( ,i) + v
S( ,i)Dt -
F((Dt)
S(2),2)   	v
S( ,i+1) = v
S( ,i) - Dt
for F = 0  	d
S( ,i+1) = d
S( ,i) + v
S( ,i)Dt  	v
S( ,i+1) = v
S( ,i)
for F = +1  	d
S( ,i+1) = d
S( ,i) + v
S( ,i)Dt +
F((Dt)
S(2),2)   	v
S( ,i+1) = v
S( ,i) + Dt
where:
	F	is force
	d 	is displacement from the desired distance above the bottom
	v	is the velocity of the submersible up or down

	The state space was quantized into sixty four partitions: eight velocities versus eight displacements. Velocities were partitioned as follows: ±0.25 m/s, ±0.5 m/s, ±1 m/s, and greater than ±2 m/s. Displacement was divided as follows: ±0.5 m, ±1 m, ±2 m, and greater than ±4 m. Note that this partitioning is exponential rather than linear.
	If the system state moved into one of the 4 m partitions, a failure signal was issued, and the current trial was terminated.
	Terrain data was generated using a fractal algorithm: dividing a line segment in half, randomly displacing the midpoint, and continuing until the length of the line segment was equal to the sample size. The roughness of the terrain was adjustable, and new terrain could be generated at any time during the simulation to test the system out over arbitrary landscapes.
	After the system was seen to work properly, several variations of the basic ASE/ACE configuration were tested that would allow the system to shut the thrusters off.


.c26.11.6: THE EFFECTS OF VARYING THE PARAMETERS

	The Gaussian noise input to the system was centered about zero, and its amplitude was adjustable during the run. Giving noise a large amplitude (on the same order as the learned weights) would cause the output of the ASE to thrash around a lot and eventually learn, but performance tended to be erratic. The ASE system worked fine with a low noise amplitude, and in fact, would operate best when no noise. In the ACE/ASE system, noise did not seem to disrupt operation at all. Noise was necessary during learning, however, to ensure full exploration of the state space, and by extension, more robust learning.
	The ASE adaptation parameter a, and the ACE adaptation parameter b were set as in the Barto et al. paper: a was 1000 so that the ASE would tend to make the same decision whenever a particular synapse was revisited during a particular trial, and b was set to 0.5.
	The ASE's eligibility decay rate was set to d = 0.9, and the ACE's trace decay rate was l= 0.8. Faster decays, for example d = 0.70, had the effect of allowing only the most recent choices to be updated, and general convergence did not seem likely to occur. A slower decay, such as d = 0.97 had the desirable effect of adapting synapses which had made choices a little earlier. In this case however, adaptation could go too far back in time, adapting synapses that had no effect on the failure.



.c26.11.7: ENHANCING THE ASE/ACE MODEL


	A system having only two modes of control, up or down, is not very useful in the real world. There is the problem of wear from continually switching the thrusters on and off, and also unreasonable fuel consumption. A simple modification was to implement a “dead zone” at the central four boxes of the state diagram where the thrusters would automatically be disabled. Learning proceeded normally, and the system did shut its thrusters off periodically.
	This solution departed from the original specification of the problem - which was to have the system learn control by itself - so alternative ASE/ACE architectures were explored.
	The basic model of the ASE/ACE system has only a single binary output. To add a third control option would require another bit of output.

	The first solution was to add another plane - a second ASE/ACE pair operating in parallel with the first. If both pairs output a -1, thrust was directed upwards, or if both pairs output a +1, thrust was downwards. If the pairs gave different values, the thruster was shut off.
	After training, the system would reach one of two possible solutions. The weights could end up identical between the two bit planes, thereby achieving the same solution as a single bit plane system (with no `off' states), or the system learned a solution where many boxes would choose the `thrusters off' option. The `off' boxes were scattered more or less randomly throughout state space.
	Analysis of the results revealed that the two bit plane solution was no better than that achieved by the single bit plane solution because there was no way one ASE/ACE pair could correlate its behaviour with the other's.

	The second solution involved a single ASE/ACE pair, with the difference that the equations were implemented using complex eligibilities and probabilities in the ASE. If the ASE's output was (1+1i), thrust was directed downwards, (-1-1i) directed thrust upwards, and (-1+1i) and (1-1i) turned the thrusters off. The external reinforcement signal to the ACE remained the same, -1 being punishment, and 0 being no reinforcement. The internal reinforcement from the ACE to the ASE was a complex number, with the real and imaginary parts being set equal to each other.
	After training, the solution achieved by the system was quite interesting, and certainly achieved the objective of minimizing fuel consumption. At large displacements, the system would apply brief thrusts to send the displacement back to zero, and the robot would coast until another large displacement was reached.



.c26.11.8: GENERAL CONCLUSIONS


	The criteria for failure is very important. In a broom balancing system, the failure state is very obvious: the broom has fallen over, or the cart has run up against the end stops.
	At first it was not apparent what a good failure criteria would be for a robot submarine following the ocean floor. Should it be some combination of depth and velocity? Heading towards the bottom at high speed is a bad thing to do. Maybe, though, heading towards the bottom at a slow speed is O.K. if speed is decreasing... Thinking about all the possibilities, and trying to derive a heuristic was not necessarily the best strategy for development. After all, the purpose of the system was to have it determine on its own which combinations were bad.
	In retrospect, the failure criteria are obvious: Failure occurs when the submarine surfaces or hits the bottom of the ocean. A refinement was to specify a narrow corridor for the robot to operate in, for example: more than ten meters above the bottom, less than fifteen.
	Uncommitted ASE synapses cause it to fire randomly. That is not a terrible defect of the algorithm, it simply means that for a given combination of state variables, neither possible choice is much better than the other, and therefore, the associated synapses don't contribute anything to the solution. A large number of uncommitted synapses in the simulation of the ASE alone system indicated that the partitioning of the system state space was too fine - finer than necessary to learn the control problem. The solution, of course, was to increase partitioning coarseness. With the ACE in control, almost every ASE synapse committed one way or the other.
	Experimentation with different partitioning sizes showed that a smaller system with coarse granularity learns fastest. If there is a fine granularity, there is a very large number of possibilities, each very similar to the next, each needing to be individually trained. Every time the system fails, it will be in a slightly different location, and the amount of time it takes to train the system seems to go up as the square of the size of the net.



.c26.11.8.1: THE ASE SYSTEM


	The ASE system would typically learn the basics of the control problem after relatively few (on the order of ten) trials if the terrain was not very rough, and in no more than a hundred trials if the terrain was very irregular.
	The terrain data had an important effect on whether or not the system would converge to a solution. With very steep slopes, the system would be unable to generalize: in some places, a steep slope meant that a high upwards velocity was necessary, and others, a high downwards velocity. The effect was to make the system continually generate errors. It could learn to negotiate one steep hill, but fail on another, and further, correcting for one hill would cause the learning from the other hill to disappear.
	Biasing the noise positive or negative changes the nature of the control problem. With a negative bias, for example, the system learns to counteract a constant upwards tendency. All the failures are on the upper bound of the control window. With a positive bias, the system learns to counteract a tendency to go crashing into the bottom. A submarine robot would probably do well to have a negative bias... Better to surface than to run aground!
	The adaptation, eligibility, and noise parameters controlled the ability of the system to converge to a solution. Within the range of parameters that let the system converge, variation of the parameters affected the speed of convergence.
	In practical use, noise with an amplitude of about thirty percent of a's value is appropriate to make the system explore its state space. After learning is complete, however, noise should be turned off, or at least brought down to the minimum possible so that the behaviour of the system is stable rather than erratic and "thrashy."



.c26.11.8.2: THE ASE/ACE SYSTEM


	The ACE/ASE system would learn a general solution very quickly, sometimes successfully navigating the terrain after only three or four trials, and refining its performance thereafter.
	The character of the solutions arrived at by the ASE alone and the ACE/ASE system are quite different. The ASE converges to a simple solution, a linear one, in fact. Adding the ACE changes the solution considerably.
	Rather than achieving a simple linear discrimination like the ASE alone does, the ACE/ASE system seems to arrive at a strategy. The robot seemed to learn to head upwards and downwards at steep slopes, apparently overcompensating sometimes, yet, this strategy allowed it to come to terms with very steep and irregular terrain.
	Introducing the robot to terrain that differed in character from the terrain it was trained on would sometimes cause a little confusion, sometimes leading to a failure, but the system would typically solve the problem on the next trial.
	The ACE/ASE system is able to handle much more difficult terrain than can the ASE alone.
	If the terrain is too difficult, the ACE/ASE fails. In one experiment, the system ran for around 20,000 time steps, then upon being presented with a very rough landscape, it forgot how to solve the simpler problems. The ACE's prediction values went haywire, and the ASE's weights disorganized themselves away from the solution that had been arrived at. The system had to be retrained on simpler terrain until its weights settled down again.
	Analysis of the failure revealed that it was due to ACE prediction values taking on nonsensical values. Values tended to be very large, so that adjustments upon failure made very little impact, and the system lost its ability to learn. The simple solution was to bound the values the predictions could take on. Forcing the values to stay within the range of the external reinforcement (-1 r) 0) cured the problem.
	This failure suggests that in a real system, a successful solution should perhaps be frozen beforehand and the ACE removed to avoid catastrophic failure in the field.



.c26.11.8.3: THE COMPLEX ASE


	This system learned as quickly as the regular ACE/ASE system. It offered the best solution in terms of fuel consumption.
	It is interesting that the equations generalized to complex numbers with no problems.  Unlike in the two bit plane solution, the two components of the output are intimately interrelated, and vary concurrently. Adaptation was therefore robust and useful.


.c26.11.9: IMPLEMENTATION DETAILS

	An algorithm which implements both the ASE and the ACE is presented below in pseudocode. The details are left out, but the structure is shown. This algorithm is fairly efficient, and runs in better than realtime on a workstation. A major improvement in speed results if in the for loop no multiplications are performed if an eligibility is close to zero.
	The weights and eligibilities are stored in arrays. The number of dimensions of the array is the same as the dimensionality of the input space. In the robot submersible example, the array was two dimensional: one dimension for displacement, and another dimension for velocity. The broom balancer would need a four dimensional array if implemented in this way (pole angle and angular velocity, cart displacement and velocity).
	The synaptic index i which appears in the listing is the output of the decoder. It would be an index into the weight arrays.
	Note that in the function AdaptACE it is necessary to clip the eligibility traces at zero and minus one to keep them from flying out of bounds. (Because the environment only supplies 0 or -1, the ACE's predictions should stay within that range.)




function AdaptASE (reinforcement)
	ASEoutput = ASEsynapseWeighti + noise;
	if (ASEoutput > 0) then ASEoutput = +1;
	else ASEoutput = -1;

	ASEsynapseEligibilityi += ASEoutput * (1-d);

	for every synapse
		ASEsynapseEligibility = d * ASEsynapseEligiblity;
		ASEsynapseWeight += a * reinforcement * ASEsynapseEligibility;



function AdaptACE (reinforcement)
	if (reinforcement = -1) then
		internalReinforcement = reinforcement - previousASEoutput;
	else
		internalReinforcement =
			reinforcement + g ACEsynapsei - previousASEoutput;
		ACEsynapseEligibilityi += 1- l;
	previousACEoutput = ACEsynapsei ;

	for every synapse
		ACEsynapseEligibility = l * ASEsynapseEligibility;
		ACEsynapseWeight += b * internalReinforcement * ACEsynapseEligibility;
		if (ACEsynapseWeight < -1) then ACEsynapseWeight = -1;
		if (ACEsynapseWeight > 0) then ACEsynapseWeight = 0;

	AdaptASE (internalReinforcement);



main program;
	clear all weights and eligibilities;
	initialize simulated physical system

	repeat
		update physical system;
		decoder selects the synapse index i;

		if (no failure) then AdaptACE(0);
		else
			AdaptACE (-1);  { punishment }
			reset all eligibility traces;














xÄ
6.106.10.76.106.106.106.106.10
 weights and eligibilities;
	initialize simulated physical system

	repeat
		update physical system;
		decoder selects the synapse index i;

		if (no failure) then AdaptACE(0);
		else
			AdaptACE (-1);  { punishment }
			reset all eligibility traces;




*This section describes research. For a discussion of development, see Appendix A

.cNETWORK MODELS
7






Seeking over generalized solutions is fruitless.  Be skeptical; recognize that different types of processing apply to different domains.
- paraphrasing Marvin Minsky and Seymour Papert in Perceptrons




.c27.1: THE HEURISTICS OF MODELLING NEURAL NETWORKS

No matter how accurate an hourglass is, it will never emulate a windup clock, because the hourglass will never have cogs and wheels.
- Chappel Brown & R.Colin Johnson

When a computer simulates a storm, we don't get wet.
- John Searle of UCLA Berkeley

(both quotes from Electronic Engineering Times, June 22, 1987, p42)


	This section is intended for those researchers whose forté is not computer science, but would nonetheless like to build simulations that work and take a reasonable amount of time to execute.
	Slowness is the inherent nature of a neural network model implemented on a serial computer with a limited number of central processing units. Large arrays, high connectivity, solutions to many systems of differential equations, and many other aspects of neural computation all imply a problem whose time requirements increase at least with the square of the number of neurons. For this reason, the equations are seldom implemented exactly as they are presented in research papers, but instead these systems of equations are used as guidelines to developing practical implementations. Coherencies in a problem must be exploited and simplifications used, insofar as they don't drastically change the nature of the computations.



.c27.1.1: REDUCING EQUATIONS


	The Kohonen self organizing feature net can be taken as an example of a system that can be dramatically reduced from its original formulation.
 The network requires a laterally interconnected feedback system to implement a winner-take-all circuit. We know, however, that after the system has had a chance to settle, only one neuron will show any activity at all.  That neuron will be the one which most closely matched the input pattern. For this reason, it is not necessary to simulate the whole dynamical process: the final outcome can be assumed. It is only necessary to find the winner and set its output appropriately, thus eliminating a large amount of simulation overhead.
	The Adaptive Critical Element/Adaptive Search Element (ACE/ASE) system of Barto, Sutton and Anderson (1984) succumbs readily to reduction.  Like the winner-take-all circuit of the Kohonen net, the ACE/ASE makes use of an element with a singleton output. Consider the equation that calculates the output of the ASE, y(t):

y(t)= f
B(
I
SU(i=1, n, w
S( ,i)(t)) x
S( ,i)(t) + noise(t))

	The function f is a step transfer function, w represents the weight of a synapse, x is the output of the decoder, and noise is added to make the ASE explore its state space.  The decoder's output, x, is all zeroes except for a single one corresponding to the current state of the system. We can make use of this fact to reduce the equation to a simple lookup operation:

y(t) = f
B(w
S( ,i)(t) + noise(t))

	The subscript i is the index to the active element of the decoder. All the other equations in the ACE/ASE system reduce in a like manner. These simplifications, and the solution of the equations using timestep simulation rather than solution of the differential equations allow the ACE/ASE system to operate in realtime, even on a very simple processor.

	As an admittedly extreme final example, the insect locomotion controller detailed in Chapter 9 can be reduced from a complex system of Hodgkin-Huxley type simulated neurons to a single heuristic rule.


.c27.1.2: DOING THE MATH

	A real neuron has a noisy output: apparently more probabilistic than strictly frequency coded. They can fire spontaneously, or they can miss a spike somewhere along the line. Due to the sheer number of neurons however, these variations are not important - in other words, the accuracy of a neuron is not important.
	A neuron might fire at a rate from less than a single spike a second, to a rate of a couple of hundred spikes a second.  A neuron is noisy, possibly inaccurate, and it has a small dynamic range. To counter these deficits, there are many in a network and they are arranged in redundant circuits.
 In consideration of these facts, it seems that neural network models should not need to rely on highly accurate floating point math - floating point math is slow, after all. Sixteen bit integer arithmetic should provide sufficient accuracy, and an order of magnitude improvement in the time it takes to evaluate an equation. Models which require the accuracy of floating point math should be reassessed for biological plausibility. These models may be interesting, but they are computationally expensive and most likely implausible as models of biological functioning.
	The following circuit (an analog computer), can be interfaced to the parallel port of a computer for low accuracy computation of the output of a neuron.
DIAGRAM NEURON ON PARALLEL PORT.
	Digital Signal Processors can very efficiently model neural nets, as one of the standard convolutions built into their hardware is the sum of weighted inputs computation used in almost every neural network model. DESCRIPTION MORE ON THE IMPORTANCE OF DIGITAL SIGNAL PROCESSORS>




.c27.1.3: INSTANCING


	In computer graphics, instancing means duplicating an object and placing it somewhere else in a picture.  One wheel is defined and duplicated four times to put on a car.
	In a neural network simulation, don't hardcode a network.  It's tempting at first: after all, the program being designed is probably only intended as a proof of concept. Foresight can enhance productivity later.  For example, if a system is designed for a single bit output, everything will go fine until the day it becomes apparent that two bits would do the job far more efficiently.  Then what? Uproot all the code and duplicate it? Better to have a universal definition and local variables. Then you can extend the model to two or a hundred bits with no corresponding increase in the complexity of the code.
	Object oriented languages, and languages with good local/global isolation make implementing neural networks easy.



.c27.1.4: NEURON SCHEDULING


	Asynchronous update helps prevent oscillations that occur when every neuron in a network is updated simultaneously. This fact also points up the significance of noise and randomness in a network: regularity leads to the stability of a local minimum, or oscillation.
	Asynchronicity as implemented by most simulations of neural computers is not true asynchronicity, rather, it is randomly ordered sequential updating. True asynchronicity means that neurons can update in parallel at any time. True asynchronicity could possibly yield more robust systems, however, more research is needed in this area.



.c27.1.5: LANGUAGE ISSUES


	C is the language of choice these days owing to its portability, modularity, and flexibility. DISCUSSION: What about the network description languages?  What are their tradeoffs? How about the modelling systems?
DISCUSSION: FUNCTIONAL PROGRAMMING AND LOGIC LANGUAGES - PROLOG AND SIMULATION

DESCRIPTION AN EFFICIENT ALGORITHM USING POINTERS FOR GRAPH IMPLEMENTATION


.c27.1.6: DEBUGGING A NETWORK


	The sure cure for debugging headaches is good design, and a well thought out program. Programs developed iteratively, a small piece at a time, extensively tested at every step, usually work well and don't require a lot of time to debug later.
	Once the software is debugged - variables are being initialized as intended, the equations have been implemented correctly, the external environment is successfully simulated - a more difficult task begins.  How can a network of processing elements, governed not by an algorithm, but usually a set of differential equations, be debugged?
	It isn't the equations by themselves that do the processing, it is instead the interactions between numerous processing elements all acting independently but hopefully together.  How to do something with such a collection - something beyond just crossing fingers?
	Hinton diagrams are invaluable for monitoring the action in a network.  They can help to reveal weights that go sailing out to ridiculous values, activity that clusters in one area and never anywhere else, lack of meaningful organization.
DIAGRAM HINTON DIAGRAM
DIAGRAM CIRCLE WITH VECTORS
	In a system with normalized weight vectors a circular or spherical display might be appropriate.
	Going beyond three dimensions, it becomes necessary to display only a few aspects of net activity at a time, perhaps not all layers, or not all memory traces, or some normalized approximation.
	Sometimes it is helpful to be able to see connectivity, although this becomes quite impractical when networks are scaled up beyond a few dozen neurons.  A clever display invented by XXX combines connectivity and weight information, and shows very graphically the evolution of weights. The weights associated with each input line determine how long the vectors between each layer of neurons are.
DIAGRAM DYNAMIC LINES FROM NIPS 89

	Oscilloscope-like displays of activity for multiple units is often useful when trying to determine the activity of a network over time.
	In winner-take-all circuits, it is very helpful to highlight the active processing unit on the screen with a brighter colour.
	Once some method of monitoring the action is in place, analysis begins.
	Here are a few common problems to watch out for, possible causes, and suggestions on what to check.

NOTE: CROSS CHECK WITH OTHER RESEARCHERS FOR MORE TIPS

Activity favours a single, or few, neurons
Every cell takes a similar value
Meaningful learning doesn't take place.
input normalization procedure
Environment simulator
Main update loop
Adaptation parameter is inappropriate (Too large - weights swing wildly, too small - weights stationary.
Some cells continually suppressed
Network can't discriminate between inputs
Input is not going everywhere it should, or not arriving
The problem is ill-defined.
Weights grow without bound
There is an error in the equation as implemented




.c27.2: THE HOPFIELD NETWORK


Hopfield makes the portentous statement ‘this case is isomorphic with an Ising model,’ thereby allowing a deluge of physical theory and theorists to enter network modelling. The flood of new participants has transformed the field of neural networks.
- James A. Anderson (1988)


	Like Rosenblatt's earlier work on the Perceptron, and Widrow and Hoff's Adaline, the initial presentation by David Hopfield of his network was quite well defined, and significantly, it showed how the network could be realized in hardware (Hopfield, 1982). Many silicon implementations have been developed or are in the works.  It is amusing to note that it has since become fashionable to end a paper with the suggestion that a system can be implemented in hardware.  Few systems, however, have had the durability or applicability of Hopfield's paradigm.
	Hopfield's original network model used a collection of McCulloch-Pitts binary neurons, completely and symmetrically connected to each other. A point in space represents the state of the system, and memories are stable points, or attractors, in state space.  As the system evolves through time the state of the system slides into one of the attractors.
	Memories can be created in the system so that the presentation of part of a stored pattern evokes the whole pattern - the state of the system slides into attractors. The system thus functions as a Content Addressable Memory, or CAM.
	Binary McCulloch-Pitts neurons are very simple: they do a weighted summation of their inputs and compare that sum to a certain threshold.  If the threshold is exceeded the neuron fires, otherwise, it is quiet.

V
S( ,i) =
B
LC
{(
A(1, 0) if
I
SU(i≠j, , T
S( ,ij)) V
S( ,j)
A(> U
S( ,i),<U
S( ,i)) )

	V
S( ,i) represents the current state of neuron i. U
S( ,i) is the threshold of neuron i, typically taken to be zero.
 	Each neuron updates randomly and asynchronously in time, a stochastic process which takes place at some particular rate for each neuron.
represents the current state of neuron i
	T is the connection matrix describing the synaptic weighting, or “synaptic efficiency” that exists between units i and j.
	Note that if a connection existed for i=j, along the main diagonal of the matrix, a neuron would have a connection going to itself: feedback, in other words.
	Symmetrical connections were used because they allow for an easy analysis of network behaviour: specifically, generating the Lyapunov energy measure, as detailed below.
	As V, the current output of a particular neuron, can take on only the values of zero or one, it represents a strong nonlinearity.  As such, it allows the model to make choices.  As Hopfield said, the very “essence of computation is nonlinear logical operations.”
	The most important contribution of the Hopfield model was the introduction of an energy, or Lyapunov function.  For a symmetric matrix with no feedback, the Lyapunov is:
E = -
F(1,2)S
I
SU(i≠j, , T
S( ,ij)) V
S( ,j)


	Changing the state of of neuron i changes the total energy of the system as follows:
DE = - DV
S( ,i)
I
SU(i≠j, , T
S( ,ij)) V
S( ,j)
	Hopfield says “this case is isomorphic with an Ising model.” DESCRIPTION OF ISING MODEL
	The energy function shows how the network converges to stable states.  DV
S( ,i) is always positive, and since the energy, E, is bounded, iteration of the algorithm will lead to energy minimums: stable states. Similar memories often fuse into the same stable state.
	To use a Hopfield network set up as an associative memory, the connection strengths between neurons must be initialized:
T
S( ,ij) =
I
SU(i=0, M-1, x
S(s,i)) x
S(s,j)
	x
S(s,i) is element i of exemplar of class S, and can take on values of plus or minus one.  To prevent feedback, i should not be equal to j, and there should be zeroes on the main diagonal.
	The system works best if the exemplars are orthogonal to each other.
	It turns out that a binary Hopfield network as outlined above is just a special case of a more general graded output network. (Hopfield, 1984) Real neurons exhibit time delays, and so do real circuits.  A Hopfield network will work if it is constructed using op-amps as neurons and resistors for interneuron conductances.



DEVELOP EQUATIONS FOR GRADED SYSTEM HERE

	The system moves in state space in the same manner as the stochastic model, and therefore, the stochastic model can be used to model and debug a system on a digital computer before it is implemented in silicon. (Hopfield 1984)  The graded network is more powerful than the bianry one, however, this assertation is true if going from stochastic to graded model, but not the other way. As an example, the Queens Problem outlined in section 7.2.1 doesn't translate well to binary neurons.
	A Hopfield network can hold about 15% as many stable states as there are neurons.  Similar memories tend to fuse into a single attractor.  If more states are stored, too much crosstalk occurs between the states, and spurious attractors appear.  Spurious attractors are errors, of course.
	Without a symmetry restriction, stable states still occur, but the error rate increases, and simple limit cycles and chaotic attractors appear.  According to Baird, the bifurcations and attractors can be controlled, yielding a network capable of storing n memories.
	Because the Hopfield network is a distributed memory, graceful degradation of performance occurs as neurons fail.




.c27.2.1: SOME USES FOR THE HOPFIELD NETWORK

DIAGRAM 4-BIT A/D CONVERTER

	This is a four bit analog to digital converter designed by Hopfield in 1982. (XXX)

DIAGRAM REWORKED A/D CONVERTER

	This is also a four bit analog to digital converter, redesigned by Alan Gleeman of Gleeman Instruments Inc.  (Circuit redrawn from Electronic Engineering Times, May 4, 1987 pXXX)  The total number of connections has been reduced from twenty to fourteen.  In both of these circuits, minima exist where the converter doesn't return accurate results. XXX has developed a method of choosing the weights so that minima are eliminated. SUMMARIZE WORK ON ELIMINATING MINIMAS.

DIAGRAM ANOTHER A/D CONVERTER WHICH WORKS BETTER

	The Hopfield network is useful for optimization problems, if the problem can be specified well. An easy to understand example of an optimization problem is the Queens problem, where n queens must be placed on an nxn chessboard such that no queen threatens any other. To accomplish that, every row, column, and diagonal must contain only one queen. There a large number of solutions, 8! = 92, in fact.
	Neurons can represent all kinds of information, for example - distances, probabilities, the presence or absence of a feature, and so on. In this case, a neuron is placed in each chessboard position, and an active neuron represents the existence of a queen in that position. For the network to solve the problem, we must give it a set of constraints to satisfy - specifically, one queen per row, column, and diagonal. These constraints are programmed by having each neuron inhibit every other neuron in its row, column, and diagonal. All the neurons are connected in a similar fashion.
	Each neuron receives inputs from a bunch of other neurons, and as well, it must receive a constant reference input. This reference voltage (as a rule of thumb) should be about one half of the connection strength. For this example, if the algorithm outlined below is used, inhibitory connection strengths of -4.3, and a reference input of 2.15 work quite well.
	The network is first initialized to some random state and then allowed to converge. A pattern emerges fairly quickly, although it usually takes a little trading around of two or three queens to achieve a final solution. The network almost always finds a solution, but it does have a tendency to caught in local minima - solutions which balance out, but are qualitatively incorrect. In these situations, a few conflicting queens will be partially turned on, but not firmly committed. The constraints are therefore satisfied, but the solution doesn't make sense - three quarters of a queen here, and a quarter isn't a good solution!

The algorithm listed below iterates a graded analog Hopfield network to convergence.


calculateNeuron(i)

	sum = reference value
 	for j = 1 to number_of_neurons
		sum += connection[i][j] * output_of_neuron (j)

	if (sum > 10) new_output_of_neuron = 1
		else if (sum < -10) new_output_of_neuron = 0
	 	else new_output_of_neuron = 1 / (1 + exp(0 - sum))

	if (new_output_of_neuron not= output_of_neuron(i)
		output_of_neuron(i) = new_output_of_neuron
		return true
	else
		return false

updateNetwork

	flag = false
	for i = 1 to number_of_neurons
		flag = flag or calculateNeuron(i)
	return flag

simulateSystem

	repeat
		displayNetworkStatus
	until updateNetwork = false

	The routine simulateSystem will iterate the network until updateNetwork returns a value of false. This happens when none of the neurons in the network change their state.




The Kohonen self organizing feature net can be found in section 7.5. The ACE/ASE system appears in section 6.10.

Another possibility, hyperacuity in neural systems, is described in Chapter 5.


7.3: SOME APPLICATIONS FOR BACK PROPAGATION NETWORKS


	DISCUSSION OF APPLICATIONS ALSO REFERENCE TO L2 REPRESENTATION PROOF



.c27.3.1: INTRODUCTION TO BACK PROPAGATION


	Back Propagation trains multiple layer networks of Perceptron-like thresholding devices. The thresholding devices are typically nothing more than a weighted summer, a thresholder, and an output transfer function. The sigmoid curve is often chosen as the output transfer function for two reasons: it turns up frequently in neurobiological analyses, and Grossberg has analyzed the mathematics quite rigorously, proving the sigmoid's usefulness.
	There is no advantage to computation using a multilayer linear system, because any sequence of linear transformations can be accomplished by an equivalent transformation in a single step. Even in a linear system, learning in a multiple layer network is more effective, because it allows progressive computation and transformation of the signal. The network can always be ‘folded’ into a single layer later.
	Another weakness of a linear system is that there is no curb to the values which can exist in such a system. This leads to both values that are unrepresentable, and to the ultimate meaningless of the weights: as the weights in some of the units grow without bound, the information contained in one weight as compared to another which has not been growing becomes less and less. The only valuable information left is order of magnitude, rather than the stored quantity.
	Introducing the non-linearity takes care of the magnitude problem. Below a certain point, activity is forced towards zero, and above a certain point, activity heads towards saturation. The output function is almost always nonlinear, monotonically increasing, and differentiable at all points. The most common transfer functions are a step function, a clipped ramp, or a sigmoid. In the middle the sigmoid curve allows a near-linear response. A very steep sigmoid provides simple thresholding, like in the McCulloch-Pitts neuron. Shallower curves allow the responsiveness of the neuron to be fine tuned.
	The original form of the back propagation network consisted of an input layer where signals could be presented, a hidden layer whose function was to devise an “internal representation of the world,” and an output layer which would generate a response pattern.

DIAGRAM A TYPICAL BACKPROP NET

	Adjacent layers were completely connected with each other: each neuron in one layer had a connection to a neuron in the layer above. There were no lateral connections within a layer, and there were no feedback connections. The signal always travelled from the input through the hidden layer to the output.
	A back propagation network implements a distributed memory - as in Lashley's engrams, every cell contributes to the memory. Input is presented as a distributed pattern, and output is a distributed pattern.
	When a network is being trained, input is presented along with a training pattern. The input is transformed as it goes through the hidden layer, and transformed again by the output layer. At this point, the output pattern is compared to the training pattern, a difference, or error, is computed, and the error is propagated back to the input recursively whilst each processing element adjusts itself in accordance with the error signal.
	Because every unit gets the same error signal, the network must initially have all its weights set randomly. If all the weights started the same, learning would never occur, because all the weights would stay the same.
	This requirement of propagating errors back through the net is one of the arguments against back propagation being a neurally plausible system, because the error signal must be global , and neural circuitry is local within networks.
	Another argument against neural plausibility is the fact that a partial derivative must be calculated at every synaptic weight...
	Nevertheless, back propagation remains a useful and well explored system for training networks, and many of the popular examples of neural networks which perform speech generation or recognition, remove noise, or predict the stock market, all use back propagation.
BE MORE EXPLICIT, EXPLAIN WHY NETTALK IS A STANDARD



.c27.3.2: DERIVATION OF BACK PROPAGATION


	The input to a given unit comes from either outside the network or from a previous layer. The individual elements of the input are weighted by the matrix w and summed. The resulting sum is passed through a sigmoid transfer function, yielding a unit's activation. The output y of unit j is given by:
y
S( ,j) = -s
B(
I
SU(i, , y
S( ,i)) w
S( ,ji))

	The output transfer function s is the familiar sigmoid curve:

s(x) =
F(1, 1 + e
S(-x, ))
	The sigmoid forces the final output of the unit, y, into the range between zero and one (inclusive).
	The error function which must be minimized for every possible state of the system is based on the difference between the output y, and the training pattern d:
E =
F(1,2) S
S( ,c)S
S( ,j)
B(y
S( ,jc) - d
S( ,jc))
S(2, )
	In order to minimize E, the gradient descent procedure is generalized for multiple layers.
 In the equation, c is an index for individual cases of input-output pairs. j is the processing element index. y is the actual state of the unit, and d is the desired state.
	A pattern is presented at the input of the network and propagated towards the output. The difference between the actual output and the desired output, dE/dy, is calculated for each output. (The bracketed term in equation 3.)
	Using the chain rule to get dE/dx:

F(dE,dx
S( ,j)) =
F(dE,dy
S( ,j)) x
F(dy
S( ,j),dx
S( ,j))

	Differentiating the sigmoid to get dy/dx, and then substituting into equation 4 gives:


F(dE,dx
S( ,j)) =
F(dE,dy
S( ,j)) x y
S( ,j)(1 - y
S( ,j))

	We know, therefore, how a change in the input, dx, will affect the total error. We can now calculate how a change in weights affects those resulting errors.

F(dE,dw
S( ,ji)) =
F(dE,dx
S( ,j)) x
F(dx
S( ,j),dw
S( ,ji)) =
F(dE,dx
S( ,j)) x y
S( ,i)
	The expression y
S( ,i) comes from the derivative of the first equation:
x
S( ,j) = S
S( ,i) y
S( ,i)w
S( , ji)
dx
S( ,j) = y
S( ,j)w
S( ,ji)
y
S( ,i) =
F(dx
S( ,j),w
S( ,ji))

	The ith unit's contribution to dE/dy is given by:

F(dE,dx
S( ,j)) x
F(dx
S( ,j),dy
S( ,i)) =
F(dE,dx
S( ,j)) x w
S( ,ji)
	Adding all the inputs gives:

F(dE,dy
S( ,i)) = S
S( ,j )
F(dE,dx
S( ,j)) x w
S( ,ji)
	dE/dy can now be computed for any unit in any layer, given dE/dy for all the units in a previous layer. This procedure can then be repeated for each earlier layer, calculating dE/dw for the weights. This value can then be used to modify the weights after each I/O pass:

Dw = -e
F(dE,dw)

	Where the factor governing rate of convergence is e.

Dw(t) = e
F(dE,dw(t)) + aDw(t-1)

	This equation is in time-step notation. It introduces a which is an exponential decay term between zero and one that determines the contribution of previous changes to the current weight change. This decay term is sometimes called the ‘momentum term.’ In practice, it is typically about 0.9.




.c27.3.3: FEEDBACK IN BACK PROPAGATION NETWORKS


	A common solution to achieve feedback in a back propagation network is to “unwrap” the network - copies are made of the original network for each extra step. The weights of each network copy are shared.




.c27.4: THE BOLTZMANN MACHINE AND SIMULATED ANNEALING


	The Boltzmann machine takes advantage of the laws of thermodynamics. When a metal is heated, it becomes very disordered, and the molecules all bounce around with a high energy. As the metal is slowly cooled, the molecules lose energy, and arrange themselves into a crystal: a configuration with very low potential energy. The forces of repulsion and attraction between molecules are minimized in a crystal, there's nowhere else for the molecules to go. This is the process of annealing, and the Boltzmann machine uses simulated annealing. John von Neumann suggested that computers would one day have to use the principles of thermodynamics (von Neumann, 1958).
	A simple analogy: marbles in a tray will organize themselves into a hexagonal pattern when shaken gently and allowed to settle. A more accurate analogy than marbles might be made by a glass jar filled with sand (ref XXX Calgary 1986). The jar is filled with a homogenous mix of sand of varying grades, with a little space left on top. The jar is then vigoursly shook, but the amount of shaking is slowly decreased to nothing. The sand will organize itself into layers with coarse sand on the top and fine sand at the bottom. Of course, the sand also conforms itself to the shape of the bottle. Once shaking has stopped, the sand will have found a minimum-energy solution - there is no more potential for the sand to go somewhere else, or organize further.
	As in Hopfield's network, a global energy function is defined for a Boltzmann machine. If the energy of the function is imagined to be a surface with peaks and dips, the simulated annealing process can be thought of minimizing the energy function, or finding the deepest valley in the energy surface by bouncing the state of the machine around until the lowest valley is found. The Lyapunov energy function for a Boltzmann machine is:
E = -
I
SU(i < j, ,W
S( ,ij)S
S( ,i)S
S( ,j))

	W is the weighted symmetric connection matrix, and the S's are the outputs of individual binary thresholding units.
	The Boltzmann machine makes use of the Metropolis (1953) algorithm. If the energy gap between the on and off states of unit K is DE
S( ,k), then regardless of the previous state, the new state S
S( ,k) will be set to one with a probability of:
p
S( ,k) =
F(1,1 + exp(-DE
S( ,k)/T))
	T is the temperature, and has an effect like noise. This equation is known as the Boltzmann distribution. Through the injection of noise, the system can escape local minima.
	At high temperatures/noise, the system will be more likely to jump around, and it can escape local minimums, shaken loose of a valley, as it were. This process of shaking loose of a valley in order to move into a deeper one effects the process of a global search of the energy space. At a high temperature, the system will never settle, but as the temperature is lowered, one of the lower energy minima will be chosen.

MORE DETAIL NEEDED AND REFERENCE TO METROPOLIS PAPER




.c27.5: THE KOHONEN SELF ORGANIZING FEATURE NET


The nature of neural systems is to comply with the statistical nature of the environment and its events.
- Teuvo Kohonen


	The Kohonen net is based on the principle of the topographic mapping. (XXX NEED MORE NEED MORE)
	This derivation follows that in Teuvo Kohonen's book, “Self Organization and Associative Memory” (Kohonen, 1988)
DESCRIBE DERIVATION OF FOLLOWING EQUATION

h
S( ,i)(t) = s
B
BC
[(y
S( ,i)(t) +
I
SU(k=-n,n, g
S( ,k)h
S( ,i+k)(t-1)))
h is the output of a particular neuron.
g is the lateral inhibition function
y is the input signal
s is the transfer function, typically sigmoid.

	Activity tends to cluster in a lateral inhibitory net, forming “bubbles” of activation. The size of the bubbles is dependent on the width of the lateral inhibitory function. (As an aside, lateral inhibition could implement an attention mechanism, perhaps in the reticular formation surrounding the thalamus.)

	A network of neurons is arranged in a grid - a linear array, a square matrix, an hexagonal matrix. The evidence of the orientation sensitive cells in the visual cortex is that in the vertical dimension, each cortical column responds to approximately the same stimuli.
	Using actual brain structures as inspiration, we may suppose it is unnecessary to extend the model to more than two dimensions. Metaphorically, a neuron in a Kohonen network could correspond to a single cortical column.
	Each neuron in the network receives the same signals. Unit i has the response:
h
S( ,i) =
I
SU(j=1,n,m
S( ,ij)x
S( ,j))
	h is the activity of neuron i, c is the input signal having j elements, and m is the weight from unit i to input element j.
	Instead of finding the place of maximum resonance through lateral inhibition and feedback as in equation 1, the unit which best matches the input can be chosen, its output set to one, and all other outputs set to zero.
	This equation illustrates the process of finding the best match between the signal and the stored memory traces. The min function returns the index i to the best matching unit.
min
S( ,i) || x - m
S( ,i) ||
	Adaptation of the memory traces is carried out as follows:

F(dm
S( ,ij),dt) = a(t)
B
BC
{(h
S( ,i)(t)x
S( ,j)(t) - gh
S( ,i)(t) m
S( ,ij)(t))
	INSERT DISCUSSION OF THE EQUATION HERE. a is the adaptation parameter intended to govern the rate of convergence. Interpretation of the other variables is the same as for the first two equations.
	Unfortunately, this equation falls easy prey to what Stephen Grossberg calls the stability-plasticity dilemma. Should learning stop at some point, or should learning be continuous? How do we keep new input from destroying old memories? How do we make sure the memories don't become out of date so that they no longer reflect the data coming from the environment? There is no easy answer, and in this equation the adaptation parameter a decays to zero as time progresses.
	The memories will freeze eventually, when a finally decays to zero, and therefore, the map may no longer correspond to the environment after a long time. This is a deficiency in the algorithm, one which should be addressed.
	The force which causes self organization is the process of finding the best matching unit, and increasing matching at this unit and its topological neighbours. Since we must increase matching of the neighbours, we define a topological neighbourhood function which surrounds the maximally firing unit. All units within the neighbourhood of that unit can take the output value h = 1, and units outside can take h = 0. The size of the neighbourhood starts out large to cause gross organization of the net, and then it can be made smaller over time so that finer details of the organization can emerge.
DIAGRAM HEXAGON NEIGHBOURHOODS
	Figure 1. This diagram shows a portion of a self organizing feature net. It shows the decreasing size of the neighbourhood function for a particular neuron as time progresses.



.c27.5.2: DETAILS OF IMPLEMENTATION


	During initialization all the weights, m, are set to unit length (from the origin to somewhere on the surface of a hypersphere).
DIAGRAM CIRCLE DIAGRAM

	It is necessary to consider the distribution of the vectors when designing a normalization function. The usual normalization procedure might be to take the Euclidean metric - the square root of the sum of the squares - and scale all the vectors based on that. This may not extract the most useful information, however. For example, in a situation where a submarine needs information about its current depth versus where it wants to be, the Euclidean metric will tell how far the submarine is from its desired depth, but it won't tell if the submarine is above or below that spot! A possible solution here is to use the Euclidean metric, but impose a sign convention on it, minus for above, and plus for below.
	The learning process can be simplified down to two essential steps: similarity matching, and adaptation.
	Similarity matching is performed by the following function:
min
S( ,i) ||x - m
S( ,i)||
	Next, adaptation is performed:
m
S( ,new) = m
S( ,old) + N(radius)a(x - m
S( ,old))
	m is an individual cell's weight, which can be considered the cell's internal representation of what it knows how to detect. x is the input signal, and a is the adaptation parameter which starts small, and gets smaller as time goes on, until finally the network ceases to be plastic. N is the lateral inhibitory neighbourhood function, having the same form as the Mexican hat curve.
	This diagram shows a typical quantized Mexican Hat lateral inhibition function as stored in an array for quick computation. Each step occurs at increasing radius from the best matched neuron. Radius is in cell body widths.

DIAGRAM MEXICAN HAT QUANTIZED

y =
F(sin(r),r)  where r is the radius from the center of the function.

	Figure 2. Compare this with the neighbourhood diagram, figure 1...
	Convergence of the model could be speeded by the use of a different process to seed the net with an approximate statistical distribution of the input space. A very simple method to initialize one hundred neurons would be to seed each neuron with the first one hundred input vectors that arrive from the environment.
	Simulated annealing could provide a little bit of order to the weights; order which would normally require a great many iterations to achieve, if only the SOFN algorithm was relied upon. For specific applications where the significant features of the distribution are known beforehand, it would be prudent to seed the net by hand, as a matter of practicality.



.c27.5.3: OBSERVATION OF AN EXPERIMENT


	It can happen that the inputs that are received by the network all occur within a certain limited range of values. If this happens there will be an initial tendency for one neuron to keep firing time after time, thus preventing other neurons from learning. The one active neuron's weight will change dramatically to follow the input, and other neurons will change little. The problem becomes less as the neighbourhood function becomes smaller. A possible solution is to make a certain refractory period during which a recently selected neuron can't fire. This would be analogous to the restoral of electrical levels in a real neuron. Another thing that can happen is that all weights will collapse to the same template. This too seems to be a problem of a too-wide initial neighbourhood.



.c27.5.4: DISTRIBUTION OF THE LEARNED VECTORS


	A Kohonen net approximates a Voronoi tessellation. DESCRIPTION AND DIAGRAMS



.c27.6: ADAPTIVE RESONANCE THEORY


You can't abstract the self-adjusting search mechanism from the attentional mechanism that stabilizes the system.
- Stephen Grossberg


	Adaptive Resonance is based on the premise that expectancy governs perception. In a simple system where input is presented and a response appears, feedback is necessary for meaningful learning. Individual neural events, such as action potentials or habituation or whatever, require a larger framework to bind them together and give them relevance. Feedback resonance - resonance between expectancy and actual input - provides such a framework.
	The Adaptive Resonance Theory (ART) also addresses what Grossberg calls the “capacity catastrophe.” Information keeps arriving from the environment, and a learning system can be overwhelmed. Knowledge gained earlier can be erased, or made unusable by crosstalk in a distributed system. Usually, learning is frozen at some point to prevent this from happening. Frozen weights require a stationary environment. Unfortunately, the real world is not static. Adaptive Resonance therefore continuously evolves new categories for information and refines old categories to reflect the environment.
	The first step to understanding adaptive resonance is to imagine a possible error situation. Given a system where input is presented, and a response is elicited, what should happen if two markedly different inputs evoke the same response? It would be appropriate then to learn a new response.

DIAGRAM LEARNING A NEW CATEGORY

	In adaptive resonance theory, the elicited response of a given processing element is fed back to its input. If there is a mismatch, the input is suppressed, and the activity of the unit dies away. On the other hand, if the patterns match, they reinforce each other, or resonate.
	Matching is accomplished by adding the input and the expectancy. If the two are very different, their sum will average to noise, and therefore the unit generating the expectancy will be suppressed. If the patterns match, the similarities will allow the two to reinforce each other and resonate. Learning occurs in the resonant condition.
	It isn't quite so simple a matter as just adding the two signals together - a little processing is necessary after that. In a neuronal context, a cell with an on-center, off-surround receptive field, like one class of cells found in the visual cortex, can be used. If the two signals result in noise, essentially a uniform response across the receptive field, the inhibitory action of the off-surround will suppress activity. On the other hand, a match will result in the resonant condition.

	The most difficult problem is determining how much uniformity, that is, how much noise, the system will tolerate before it decides it has a new pattern. A dynamic inhibitory mechanism to adjust vigilance to suit the environment is the answer.
	If a mismatch, subject to whatever criteria, has occurred, the input layer must send some feedback to the expectancy layer. The input layer has limited information - it has no knowledge of the patterns known by the expectancy layer, so it can only send a very general signal back. This signal is termed nonspecific arousal. Nonspecific arousal is a reaction to unexpected or novel input. Grossberg makes an analogy demonstrating the arousing effects of unexpectedness by suggesting that we suddenly thump a table, and watch people jump.
	The arousal signal serves to reset the entire system, thus preventing the storage of short term patterns in long term memory. Grossberg suggests that there are perhaps physical correlates of the arousal system in the brain, for example, the P300 wave which is a pronounced peak recorded in ECG readings three hundred milliseconds after a stimulus. It is further possible that every nervous subsystem has its own arousal-reset wave. (Grossberg 1980)
	Once a resonance condition exists, the network will tolerate small differences between sensory inputs and the expectancy pattern because the resonance will continuously try to deform the sensory input to match the expectancy. If the difference becomes too great, however, an arousal, or reset wave will be triggered.
	The arousal signal must shut off expectancy layer cells that generate mismatched templates. However, inactive cells shouldn't be inhibited, because they should have a chance to subsequently offer up their own expectancy templates. Therefore, after a cell has generated a mismatch, it should stay inhibited long enough to allow another cell to offer an expectancy.
	The process of arousal and inhibition continues until a resonant condition exists: a matching template has been found, or failing that, a group of uncommitted of cells which can then learn the new pattern. ART architectures therefore self organize stable codes in response to their environment.
	When an ambiguous pattern, such as a Necker cube, is presented to an ART network, the mechanisms will allow for spontaneous switching between percepts.

DIAGRAM THE NECKER CUBE AND HEX CUBES

	Which face forms the front of the Necker cube? Is the middle cube of the lower figure convex or concave? The percept switches back and forth as attention shifts, or as the eye moves, or possibly even as neurotransmitters charge and recharge.
	To realize the adaptive resonance network, a lateral inhibitory circuit was designed. Grossberg called it a “recurrent shunting on-center off-surround network.”

DIAGRAM OF SAID NETWORK

	Like on-center off-surround cells, this network will perform noise suppression and edge detection.
	The individual cells in the network use a sigmoid transfer function to keep the activation from building to infinity. At low activation values, the cell's output is kept small, and through feedback, it will slide to zero (or fully off). At high activation values, the cell will tend towards saturation (or fully on) through feedback. In the middle range, the response is almost linear, and feedback will send the output either one way or the other, depending on the sum total input from the other cells.
	Below a certain level input is squelched, and above it, the input is contrast enhanced. An enhanced and resonating short term memory pattern can subsequently be stored in long term memory to generate new expectancy templates.
MORE DIAGRAMS NECESSARY



.c27.7: THE NEOCOGNITRON


	A consistently difficult task is to recognize patterns subject to distortion and translation. The NeoCognitron is a multistage feature extractor and pattern recognizer that can solve this problem to an impressive extent.
	The Cognitron, essentially a layered Perceptron, came before the NeoCognitron. The major improvement introduced by the NeoCognitron was a more complicated architecture which allowed the network to recognize shifted and distorted patterns.
	The NeoCognitron couldn't recognize more than one pattern at a time, so feedback connections were added to the model. Selective attention was thus implemented.
	At the input level, very small details are recognized - vertices, line segments, dots. Many cells recognize the same details, but at different positions. The next layer recognizes that certain features are active at a certain spot, and as the signal flows through each subsequent layer, more and more complex patterns are extracted and fewer and fewer cells are active. Finally, at the last layer, a character is recognized, and only a single cell is active (Johnson, 1987).
	Once a single cell is activated, the backward connections come into play. During training, the backward connections are reinforced to the same magnitude of the forward connections. Because of the architecture of the network, signals retrace the same path backward as they followed forward.
	Forward cells receive facilitation from the backward signal flow. At this point, noise in the pattern is suppressed. If the network is recognizing the letter ‘A’ for example, the final ‘A’ cell will not send reinforcement signals back along pathways that were not learned during training. The activity of the superfluous active cells will therefore decay to nothing .

DIAGRAM FUKUSHIMA'S NEOCOGNITRON

(diagram redrawn from Fukushima, 1987)



This derivation follows that in “Learning Representations by Back-Propagating Errors” by Rumelhart et al., 1986.


Section 6.6 has a discussion of gradient descent and the problems of local minima.

Section 4.1 describes topographic mappings in some detail. Section 2.2 is about the orientation selective cells of the visual cortex.  Section 4.1 describes a possible attentional mechanism which is entirely regulated by lateral inhibition. Section 3.3 describes the application of a Kohonen net to speech recognition.


Section 2.2 discusses on-center off-surround cells in greater detail.

.cBODIES & ROBOTS
8







The fundamental principle guiding the design of biological mechanisms is purely and simply: minimization of energy.




.c28.1: MANIPULATORS:


DIAGRAM THE BONES OF THE HAND AND SOME ANTECEDENT HANDS

Interphalangeal joints

Metacarpalphalangeal joints

carpometacarpal joint

	The human hand makes a good model for a general-purpose robotic manipulator. The opposable thumb is necessary to allow delicate manipulation and fine control. When a power grip is necessary, the fingers are used in opposition to the palm, allowing maximum contact area between the hand and the object. For power grips, force is applied by the forearm muscles, rather than by the finger muscles. Two fingers and one thumb are enough to allow stable grips, and three fingers and one thumb are enough to allow the transferral of a grip. (Grupen et al., 1989)
	Covering a manipulator with a compliant material like foam rubber has the effect of distributing applied forces over the surface of a gripped object, and of protecting delicate mechanisms of the manipulator - touch and heat sensors for example.
	The human hand's interphalangeal joints are simple hinges that allow a sweep of movement (flexion - extension) through ninety degrees.
	The metacarpal phalangeal joints allow the fingers and thumb to swing in towards the palm. The fingers' joints swing through about ninety degrees, and the thumb's swings through about sixty. The fingers' metacarpal phalangeal joints also swing back and forth, adduction and abduction, through about thirty degrees. The thumb's joint doesn't move very much at all.
	The thumb's carpometacarpal joint can move through two degrees of freedom: a rotation almost in the plane of the palm towards the palm and away from the hand (adduction - abduction) through about ninety degrees, and flexion - extension through almost ninety degrees.




.c28.2 MAINTAINING ORIENTATION AND BALANCE:


	Organisms as simple as the jellyfish contain systems for detecting and maintaining balance. Jellyfish and many other simple organisms rely on otoliths - small solid objects suspended in a jelly - to get information about orientation and rotational acceleration. The otoliths are subject to acceleration and gravity, and the jelly surrounding them often provides a damper, returning the otoliths to a neutral position when acceleration stops. The otoliths impinge on a sensory transducer, typically hair cells, and information is thus made available to the central nervous system.

DIAGRAM JELLYFISH OTOLITHS

	The diagram shows how the otoliths function in a jellyfish. If the jellyfish is level, a certain tonic level of output is maintained. The spiking rate increases if the jellyfish is tipped. The jellyfish has many of these 'tip' sensors arranged around the edge of the umbrellar portion of its body.
	The vertebrate's vestibular mechanism is far more complex than the simple tip sensing of the jellyfish, and thus the vestibular mechansim returns far more detailed information. The vestibular mechanism consists of three rings - the semicircular canals - containing thousands of hair cells. The rings are oriented at almost perfect right angles to each other, and therefore return three dimensional data.

DIAGRAM THE VESTIBULAR MECHANISM

	The actual sensing is done by the macula. The macula has numerous hair cells, each with a preferred orientation subtlely different from the preferred orientation of its neighbours. The otoliths impinging on the haircells are imbedded in a jelly.  As the orientations of the hair cells are not all simply in the same direction, acceleration does not generate an all or none response for a given direction of acceleration. The output of the macula is much more sophisticated than that...  A small number of axons, twenty thousand on either side of the head, send afferents from the hair cells to the central nervous system. The afferents feed via the vestibular complex to the vestibulo-ocular system, the vestibulo-cerebellar system, and to trunk, neck, and limb motoneurons via the vestibulo-spinal system. The muscles can thus feel the changes in the macula, and they can adjust themselves to maintain balance. (Shepherd 1988)

DIAGRAM WIRING OF VESTIBULO-X SYSTEMS




8.2.1: AN ARTIFICIAL VESTIBULAR MECHANISM:


	It is very easy to give a mechanism a sense of orientation using a system modelled on the semicircular canal system of the inner ear. This model duplicates the spirit, if not the structure of the vestibular mechanism. Instead of having three connected semicircular canals, this model consists of three loops which can be placed anywhere on a circuit board, as long as the loops are all oriented at right angles to each other.
	Photodetectors replace the hair cells as sensory transducers, an air bubble replaces the otoliths, oil replaces the jelly. An artificial neural network replaces the processing that would be done by a central nervous system. The network receives the data, conditions it, and extracts significant features such as orientation in three space and instantaneous angular acceleration.
	The secret to the system is the gaskets. The order of the gaskets, from the light source to the photodetectors is a thin transparent gasket, a thicker gasket with a ring cut in it, and a final layer holding photodetectors arranged to line up with the ring in the middle layer. The ring is almost filled with dark tinted oil, but it has a little bit of air in it to make a bubble.
	The air bubble will always be on the top, and the light will therefore be able to shine through and activate a photodetector. Knowing which photodetector is active tells the rotation of the device. Adding more photodetectors around the ring increases angular resolution.
	Fixing three of these devices together each ninety degrees from the other gives complete three dimensional rotational position information.

DIAGRAM THE ARTIFICIAL VESTIBULAR SYSTEM

	The time it takes the bubble to go from one photodetector to the next supplies rotational speed information.
	This sort of mechanism would be very cheap to produce, and useful wherever it is necessary to keep something level, whether it be an aircraft, a submarine, a car, or a robot.
	If a robot must simply stay upright, it wouldn't be necessary to give it a circular sensor, a simple arc would suffice. The curvature of the arc would control tipping sensitivity. A very gentle arc would give strong sensitivity to tipping, whereas a very steep arc would make the robot sensitive to only the most extreme tipping.
	Rather than using a system of gaskets, it would be cheaper to construct the arc constructed using a short piece of glass tubing, just like the level a carpenter uses.

	Using principles of local computation and self organization, the Neural Network in the proposed Artificial Network extracts attitude information and rotational acceleration. Attitude is readily available from the first order neurons, and rate of change of attitude is available from second order neurons. Practicality suggests that three-space information be returned rather than individual sensor and neuronal signals, so the output of the network is converted to a six dimensional vector:

x = (qx , qy , qz, dqx, dqy, dqz)

	The neural network in the experiment was implemented on a single chip microcomputer. The output was made available at a standard digital data port having the following form:

	command port:	16 bit instruction
	data port:	16 bit data output
	interrupt signal:	2 bit data output

	The commands available include query x, set interrupt parameters and query neuroni. The maskable interrupt signals to the host CPU occur whenever a change in attitude or in angular acceleration has exceeded some predetermined threshold. Learning occured only during research and development of the artificial vestibular mechansim. In subsequent applications, the learned weights for fixed in ROM as there is no need to change them.


.c28.3 BIOLOGICAL MATERIALS AS SENSORS:


.cINVERTEBRATE NERVOUS ORGANIZATION
9








.c29.1 INTRODUCTION TO INVERTEBRATE NERVOUS SYSTEMS


	The simplicity of the invertebrate nervous system raises the possibility of delineating, understanding, and simulating the entire nervous system. The whole invertebrate nervous system probably contains on the order of a hundred thousand neurons. Of those half are probably concerned with the reduction of sensory information. Furthermore, there are less than a thousand motor neurons and the number of interneurons controlling and modulating the motor neurons is likewise quite small.
	Invertebrate nervous systems appear to have many neurons which perform unique functions. A conceptual parallel can be drawn between these specialized neurons and the various ganglia and nuclei of vertebrate systems which act as processing substations. Command neurons were proposed to be neurons which could be shown to be necessary and sufficient to switch on or off individual behaviours. Neurons are often found which seem to subserve particular behaviours, but further investigation usually reveals complications. In some cases different frequencies or intensities of stimulation will evoke different behaviours, and most behaviours can usually be elicited at many disparate locations. This highlights the inherently distributed nature of the nervous system. However, at this early stage of understanding theorizing with specialized neurons still yields useful results.

DISCUSSION OF WJDAVIS ideas.

W.J.DAVIS diagram:
hierarchy of functionality vs emergent behaviour
localization of functionality vs distribution of behaviour
single command neurons vs consensus circuits
These new concepts imply:
	redundancy and robustness
	- reverberation whereby a motopattern outlives the stimulus that produced it.
	- command locus should be close to the site of the information
	- command neurons occupy priveledged positions with respect to incoming data.
	- specialization in an identically connected network can be maintained by the cell's relation to outside data.
	- learning is distributed throughout the entire system.

Hierarchy vs reciprocity
	elemental origin of network properties
	implicit functional polarization vs emergent network properties
	startle response has to be hierarchical.
	individual properties such as hot cold blue red are represented in individual nodes vs properties are implicit in the network, but don't explicitly exist anywhere.

Implicit Functional overlap versus Distributed function
	compartmentalized functions versus implicit functional segregation

Unicellular command vs consensus
	Functional organization and differentiation within a network is possibly a result of the location of the neurons with respect to sensory input - the incoming information organizes the network, so the outer most layers are the most specialized.

	There is a trend evident in invertebrate nervous system development. The various ganglia are quite large in older, more primitive forms. In the more modern species, the ventral and posterial ganglia tend to be smaller, and their functions are taken over by the head ganglia. Predatory species have more developed capabilities than do less active species. Hunting spiders, as an example, have more developed sensory processing capabilities than do webspinners. (A similar phenomenon in the case of vertebrates is the fact that grazing or scavenging organisms will have less developed brains than the predators.)
	Invertebrate nervous systems generally have a ladder-like organization: the “rungs” are formed by segmental ganglia and the cerebral and caudal ganglia form either end. Examining more and more complex phyla shows that the ganglia become clustered closer and closer to the cerebral ganglion, being ultimately subsumed into it. Typically however, each segment of an invertebrate's body contains a variety of ganglia where local processing takes place.
	The ladder architecture is exemplified by the leech's nervous system (as illustrated below), but the circuit is fundamentally important to all invertebrates. Examples of the ladder architecture are the control of swimming in the leech, crawling in Nereis, chewing in the lobster's stomach, and walking in insects. A swimming motion is often accomplished by contraction of muscles on one side, and relaxation on the other. Symmetrical spikes could fire both sides, with contralateral inhibition of motoneurons providing the desired action. Inhibitory pathways could prevent repetitive ipselateral firing.

DIAGRAM OF THE LEECH

		Through the inhibitory connections between the ganglia, the ladder circuit forms a pattern generator. Even though pattern generators produce rhythmic outputs, pacemaker cells are seldom found in the circuits (Laurent and Hustert, 1988). Rather, the patterns are a consequence of the pattern of inhibitory connections between naturally charging and discharging cells. The patterns provide a low energy operational modality - the neurons settle into a pattern whereby they can all fire maximally in time. As an example, two identical neurons connected such that each inhibits the other will settle into a pattern whereby they fire alternately with the spikes maximally separated in time. This circuit is called the “half-center” model by (Pearson, 1976). The diagram below shows the results of a simulation demonstrating two Hodgkin-Huxley type neurons interconnected as the half-center model.

DIAGRAM A SIMPLE PATTERN GENERATOR

	Pattern generators often produce several characteristic patterns, each modulated by varying levels of excitatory or inhibitory activity on the individual neurons. In a a walking controller, for example, several gaits can exist as emergent properties of the system - walk, pace, canter, trot , or run. All the patterns are produced by the same circuit, but are a consequence of different levels of tonic excitation, or possibly of differential activation of interneurons in the circuit. A separate circuit sometimes exists to ‘kickstart’ a pattern generator by providing an initial muscular wave, although it is possible that noise in a system could be a sufficient mechanism for self starting. It is important to remember that behaviour is distributed in all nervous systems, vertebrate and invertebrate. In general, the circuits controlling various behaviours can not generally be considered completely in isolation. In moths, for example, attempts to fly are accompanied by rhythmic discharges in the auditory neurons (Guthrie, 1980).

	Behaviour is a function of an organism's perception of the environment, modulated by the senses, and controlled by the brain. The corpora penduculata or “mushroom body” is the brain of the insect. Its prime function is the integration of sensory information. The calyx performs visual processing; and the stalk and ventral lobes handle smell and other senses. The corpora penduculata is named for its shape, as shown in the diagram below.

DIAGRAM THE CORPORA MUSHROOM

	The corpora penduculata serves as a source of commands - controlling the various behaviours by selective inhibition. A release from inhibition allows a behaviour to occur. Crawling behaviour in insects, for example, occurs spontaneously unless inhibited. Proof that the cerebral ganglion controls behaviour through inhibition is provided by experiment and observation. Severing the cerebral ganglion from the nerve cord causes the leech to swim continuously. The female preying mantis decapitates the male to elicit copulatory behaviour. In a normal Nereis, tapping the head of a creeping specimen will cause it to stop and withdraw reflexively. A decapitated Nereis spontaneously creeps, and the withdrawal reflex is suppressed (Guthrie, 1980).


.c29.2: FAST RESPONSE PATHWAYS - THE STARTLE RESPONSE

	One exception to the distributive - emergent paradigm discussed above is the startle response system. Startle responses mediate such functions as escape from predators or other aversive stimuli, so a quick response is necessary. A simple hierarchical structure is implied as it would allow the initial stimulus to cascade easily through the system without much interference.
	Adaptation of the neurons involved is not a factor - complex discrimination is absent. An example of a startle response is the gill withdrawal reflex of Aplysia evoked by a tap on the gill mantle. Another example is the cephalopod escape mechanism. The diagram below illustrates the giant fibre system of the squid which comprises the fast response pathways.

DIAGRAM SQUID GIANT AXONS

(Diagram adapted from Guthrie 1980)
	Invertebrate nervous systems have a very low bandwidth - there are few cells, and these are dedicated to particular behaviours. Compared to higher animals, there isn't that much facility for complex information communication through the organism. Low bandwidth - high reliability startle response pathways enable the organism to bypass slow acting and possibly behaviourally limited central control and therefore react to a stimulus in a period much shorter than the organism's normal response time.
	Startle responses are reflex actions. Trigger neurons generally cause startle responses via the fast pathways. In a simple nervous system, only one of many spikes signalling a dangerous situation might be sufficient to activate a fast response pathway - the probability of a transmission failure is therefore very low. Thus the low bandwidth constraint is not a problem. The types of stimuli that cause the startle response have a very low information content because reflexes should by definition be immediate without the necessity for time consuming intermediate processing. Long fibres, thick axons, myelin sheaths - all these subserve rapid transmission of signals.
	The startle response system is not isolated from the rest of the nervous system. In insects, the large fibre system tends to prime neurons for specific reactions, rather than directly effecting control. Activation of a fast response pathway could suppress the neurons which give the organism its usual control, thereby ensuring the reliability of the startle reaction.
		In terms of probability and magnitude of reaction, the speed and complexity of the startle reaction is inversely proportional to the complexity of the nervous system. An organism with a complex nervous system will have a much wider range of behaviours available to it, and therefore the reflex systems will be less and less likely to control the behaviour of the organism.




.c29.3: THE NEURAL CONTROL OF LOCOMOTION

The similarity of the walking systems in the cat and the cockroach suggests that the number of ways of optimally constructing a walking system is quite limited.

- Keir Pearson (1976)


	It is still a matter of debate as to whether gait patterns are produced primarily through central pattern control or as an emergent property of the sensory signals available to the local ganglia. There is some evidence for the first argument, and also for the second. The cockroach tends to operate in a ‘ballistic’ mode, moving in straight lines at top velocities using the simplest, fastest gait. In this case a sophisticated sensory driven pattern generation mechanism would be superfluous. On the other hand, an insect moving carefully on a treacherous surface will have to rely quite heavily on the information available from its feet (personal communication, Randall Beer, 1989).
	The control of locomotion is similar in all organisms - it is mediated by the brain, but controlled locally by the ganglia. The hypothesis that local ganglia control the walking reflex correlates quite well with the principles of information theory - for example, the principle that control should be located near the source of incoming data (Davis 1976). Cats and cockroaches whose brains have been severed from the central nerve cord will still walk if pushed or placed on a treadmill, demonstrating that walking is a local reflex action (Pearson 1976). Clearly the stepping motion is initiated as a function of sensory feedback.  However, the resulting gait patterns are not as regular as those produced by an intact animal. As will be demonstrated in the next section, a circuit with no central pattern control generates rather arbitrary gaits, thus demonstrating the need for some kind of coordination.


.c29.3.1: THE ROLE OF SENSORY FEEDBACK

	Theory suggests that loading sensors inhibit the central pattern generators during the stance phase thus preventing the swing phase from being initiated when a leg is carrying a significant portion of the animal's weight (Pearson, 1976).  When another leg is placed down, it begins to carry some weight, relieving the weight on an already placed leg, thereby allowing that leg to step. This mechanism also plays the largest part in allowing the animal to adapt to differing terrains (REFERENCE).
	Beer, Chiel, and Sterling used backward and forward angle sensors to detect the extreme leg positions, and thus provided the first step towards a sensory driven locomotor controller (Beer, Chiel, and Sterling, 1989). The backwards angle sensor excites the central pattern generator, predisposing it to fire and therefore swing the leg forward. The forward angle sensor inhibits the pattern generator so that the extreme forward position of the leg will prevent the leg from swinging any farther forward. The forward angle sensor also excites the extensor motor neuron to begin the backwards cycle. In the model of Beer et al, illustrated in the diagram below, these sensors were binary, firing at the extreme position, but providing no detailed positional information.

DIAGRAM OF MODEL

	It is difficult to get robust behaviour with binary sensors - imagine that it was necessary to rely on hot/not hot sensors for touch: If the hot sensors reported “hot,” how would you know whether an object was pleasantly warm, or painful to touch? Different behaviours are appropriate in each case. In general, a range of return values is more informative.
	The insect's leg has a variety of mechanoreceptors, some of which -correspond to forward and backward angle sensors: the spurs on the back of the foot signal backward extension, strain sensors in the insect's exoskeleton serve as forward angle sensors. In addition, the pads on the bottom of the insect's foot, the pulvilli, are load sensors (see Figure 14).
	Natural sensory afferents have nonlinear responses and the simulations described in this chapter use reponses summarized below. The more extreme the angle of the leg, the greater the firing frequency of the sensory neurons - so that for very extreme angular displacements, the signals can't be ignored, and are therefore analogous to pain. This observation points the way to learning in the circuit, perhaps via instrumental conditioning.


FIGURE 11 - ACTIVITY FROM SENSORY AFFERENTS

	Although the circuit thus far described controls flexion and extension, it does not address the problems of levation and depression. Most of the process of walking is carried out by four groups of muscles within the insect's body which use the whole leg as a lever to propel the body forward. In crustacea, the leg is like a gimbal mounted strut with two degrees of freedom (see Figure 6), whereas the insect's leg is like a freely rotating ball in a socket.

DIAGRAM COXA AND LEG

	In both insects and the crustacea, the muscles controlling the leg are the flexors, extensors, levators, depressors, and retractors. Flexors bring the leg forward, extensors push it back. Levators lift the leg, and depressors push it down. Retractors retract the claw at the end of the tarsus.

DIAGRAM THE INSECTS FOOT

Diagram modified from Laurent and Hustert (1988).

	A detailed, yet conceptually simple sequence of sensory events drives the stepping reflex. The diagram below shows some of the main connections from sensory afferents to motoneurons, summarizing the results in (Laurent and Hustert, 1988). In the discussion that follows, stance refers to the phase of the stepping cycle when the foot is in contact with the ground, and swing refers to the phase when the leg is swinging forward in preparation for another stance phase.

DIAGRAM WIRING OF FOOT

	Triangles represent excitatory connections, circles are inhibitory connections. The dotted connections show a reflex reaction - touching the dorsal surface of the foot causes a strong levation reaction. This is a stumble reflex: if the top of the tarsus hits some obstacle, the leg is lifted to avoid the obstacle.

DIAGRAM STEP CYCLE

1)	At the beginning of the stance phase the pulvilli contact the ground, exciting the depressor and retractor motoneurons and inhibiting the leavtor motoneurons.
2)	The excited depressor pushes the foot more strongly against the ground and the extensor moves the body forward.
3)	The excited retractor pulls the unguis in until the claw touches the ground. The claws further excite the retractor insuring a firm and reliable contact with the ground.
4) 	By the end of the stance phase, the claw is fully retracted and the leg is extended towards the rear of the animal. The leg is almost ready to begin the swing phase.
5)	The distal anterior spurs touch the ground, exciting the depressor motoneurons and inhibiting the levator and retractor motoneurons. This provides the final thrust and preparation before the swing phase begins.
6)	As other legs take the load of the animal's weight, the claw relaxes, and pressure on the pulvilli is descreased.
7)	Inhibition to the levator is almost gone, allowing the tarsus and then the leg to be levated.
8)	The leg is then swung forward by the flexor in preparation for another stance phase.

	The following diagram shows the complete locomotion controller. The spur afferents excite the central pattern generator to end the stance phase by exciting the levator (and indirectly the flexor) motoneurons. The forward angle sensor ends the swing cycle by inhibiting the pattern generator when the leg has reached the extreme forward position and exciting the depressor (and indirectly the extensor) motoneurons.
	The excitatory afferents from the pulvilli and the mutual inhibition of the levator and depressor motoneurons complete the stance phase. The swing phase is completed because of the lack of any inhibitory activity on the the levator while the foot is not touching the ground.
	Excitation occurs first at the levator, which in turn excites the flexor because the leg should be lifted before it is pulled forward. At the end of the swing phase, the depressor must be excited before the extensor since the foot should touch the ground before thrust is applied. Therefore, both the depressor and the pulvilli afferents must excite the extensor before it becomes active.
	The flexor is gated by the forward angle sensor and loading on the pulvilli. This is because the leg shouldn't be pulled forward if the foot is touching the ground or if the leg has already been fully flexed. The extensor is gated by the spur afferents because the leg must stop moving when it has reached full extension.
	The speed the animal travels is governed by the length of the stance phase, as the swing phase almost always takes the same length of time (Pearson, 1976).
 A speed input is therefore provided to the extensor motor neurons. This speed input is gated by the spur afferent, as the leg shouldn't be drawn back after it has reached full extension.

DIAGRAM REFLEXES

	The retractor circuit is synergistic to the rest of the system - it helps generate the full motion of the foot during the walking cycle as detailed above. The leg withdrawal reflex provides a “stumble” which can allow the animal to deal with highly irregular terrain or obstacles. An example of how the reflex works is easily observed if the front of a cat's foot is tapped during the swing phase. The leg will suddenly halt its swing, quickly withdraw and lift, and the extend over the obstacle that blocked the leg's swing.
	In the simulation, the circuitry of the stepping reflex was simulated using the Hodgkin-Huxley type neurons described in Section 6.3. The circuitry was duplicated six times, once for each leg (although the retractor and stumble reflexes were not simulated). If the central pattern generators are not interconnected, the circuit walks driven by sensory feedback. The gait patterns generated by this circuit are highly irregular however, due to the lack of any sort of inter-leg coordination beyond that provided by load information. Note that the only regular pattern observed is the tripod gait which results if the stance phase is driven at maximum speed.
	The stepping reflex is quite robust and removing connections or randomly perturbing synaptic weights causes the gradual degradation of performance we have come to expect from neural networks. A leg will keep stepping even if all connections are corrupted to some small degree, thus demonstrating the inherent robustness of this circuit design.



9.3.2: THE ROLE OF CENTRAL PATTERN GENERATION

	Observation tells us that contralateral or adjacent pairs of legs never swing at the same time (Pearson, 1976). This set of constraints is sufficient to generate the full range of gaits observed in nature. The first connections conventionally hypothesized, therefore, connect the pattern generator cells (one for each leg) in an inhibitory ladder to produce coordination of all the legs. There is no central motor store, no programmed walking pattern. Rather walking is an emergent behaviour of this distributed system.
 The central pattern generators impose their oscillatory pattern upon the stepping reflex circuit of the previous section. Section 9.3.3 details a number of modes of operation of this circuit.


DIAGRAM THE LADDER ARCHITECTURE

DIAGRAM THE TRIPOD GAIT
	Making the rear legs of the insect longer will give them a lower stepping frequency. The inhibitory connections therefore entrain the whole system to the frequency of the rear legs, producing a metachronal wave, where a ripple effect can be seen : the legs step from rear to front, a sequence commonly observed in nature. In almost all species, the metachronal wave starts posteriorly and moves anteriorly.
	The diagram below shows a timeslice of activity in a network of pacemakers connected as in the ladder architecture shown above. The rate of charging of the rear two pacemakers was slowed by lowering the tonic current input, and by the end of the Figure, all the pacemakers have been entrained to the slower frequency.

	DIAGRAM ENTRAINMENT.

	Following Pearson (1976) we can connect the pattern generators to flexor burst generators which swing the legs, and extensor generators which produce the stance phase. Refer to the following diagram.

	DIAGRAM PEARSON's BASIC CIRCUIT

	The level of tonic excitation controls the speed of the stance phase by controlling the power and speed of the thrust applied to the leg. The time taken for the stance controls the speed at which the animal travels and consequently the gait. The speed the animal can run is continuously variable. Observation of cockroaches tells us that it can run at any speed from 1 to 80 cm/s (corresponding to leg frequencies of 1 to 23 Hz), and the various stepping patterns smoothly blend from one to the next.
	Pearson's basic circuit is repeated six times to generate a preliminary circuit for an insect's locomotion controller. A command neuron can be added to the circuit, which inhibits the central pattern generators and motoneurons. Refer to the following diagram. If the command neuron becomes quiet, then the circuit should spontaneously begin walking, although it may be necessary to give the last pair of generators a burst of excitation to start the walking sequence. In a reciprocally connected system, excitation of an individual neuron should be able to activate the entire system (Davis 1976). The simulation of Beer and Chiel demonstrated this phenomenon. When the simulated cockroach was “pushec” it walked spontaneously (Beer and Chiel, 1989).

DIAGRAM PRELIMINARY CONTROLLER

	Experimentation (Beer, Chiel, and Sterling, 1989) reveals that this circuit will indeed generate valid gaits, but it is not robust, as is demonstrated by “lesion” studies. If a ganglion is “damaged” the gait produced by the circuit quickly breaks down as all coordination is lost.

DIAGRAM A LESION STUDY.

	This diagram shows a compressed representation of what happens to a gait if the central pattern generator controlling the middle right leg is lesioned.
 At first, the middle left ganglion fires sporadically, and then at about the same time, the middle left ganglion and the two rear ganglions stop working, leaving the front two going by themselves. The reason for the failure is that the pattern is the result of the mutual inhibition of the central pattern generators, with no sensory feedback involved. It seems a plausible remedy would be for damage to reconfigure the interactions of the central pattern generators with more of an emphasis on sensory feedback.
	Real invertebrates respond robustly to damage. If an invertebrate loses a limb it doesn't even slow down, only the stepping pattern changes. Shedding a limb is often a survival reflex. The gait adjusts so as to remain stable, and the invertebrate continues on its way.

	The natural modes of oscillation of the ladder architecture are the gait patterns generated by the model. It is easy to understand the patterns of oscillation as can be seen in the following sequence of diagrams. For each gait, the pattern of inhibition for each phase of the gait is shown, as is the standard gait diagram over a number of time steps. These gaits are representative, since a continuous range of gaits exist, each blending smoothly into the next.
	It is the duration of the stance phase relative to the duration of the swing phase that determines the gait, as well as the effect of entrainment of the slower stepping rear legs. Changing the length of the swing phase makes the gait slower, but the gait patterns remain unchanged.

DISCUSSION MODES OF OSCILLATION AND RESULTS



.c29.3.4: A ROBOTIC CONTROLLER



	This diagram shows an artist's conception of the robot insect as it will appear when all systems are finally integrated.

DISCUSSION THE ROBOTIC CONTROL ALGORITHM RESULTS AND CONCLUSIONS



This type of learning system is explored further in Section 6.9, where the Adaptive Critical Element is described.

The relationship of the timing of the stance and swing phases to gait pattern generation is detailed in section 9.3.3.

Rodney Brooks has built upon the principal of emergent behaviours to generate his distributed subsumption architecture (Brooks, 1989). A major difference between that wrk and the work reported here is that in Brooks’ work, the gait pattern was precomputed and stored in the controlling computer's memory, whereas here the gaits are emergent behaviours of cooperating units.

This hypothetical architecture doesn't tell the whole story. Insects placed on water, for example, can propel themselves with synchronous contralateral kicks. Some arthropods can walk backwards or even sideways. These are radically different behaviours, elicited by different sensory input, and are not behaviours supported by this architecture. It is possible that each different behaviour is controlled by a collection of disjoint pattern generating circuits, selected amongst by the cerebral ganglion (Hoyle, 1976).

The “lesion” was performed by “switching off” the central pattern generator corresponding to the mddle right leg in the ladder architecture circuit.


Clarkson, Mark A., The Quest for the Molecular Computer, Byte, May 1989, pp. 269-273

Drexler, K. Eric, Engines of Creation, 1985

Hecht, Jeff, Physical Limits of Computing, Computers in Physics, Jul/Aug. 1989, pp. 34-40

Lang, Gordon R., M. Dharssi, F.M. Longstaff, P.S. Longstaff, P.A.S. Metford, M.T. Rimmer, An Optimum Parallel Architecture for High-Speed Real-Time Digital Signal Processing, IEEE Computer Magazine, vol. 21, no.2, February 1988, pp. 47-57

Shannon & Weaver, Towards a Theory of Information, 1949

Wiener, Norbert, Cybernetics, 1965, MIT Press, Cambridge MA (xuberhths)



General References and Collections of Papers - Neural Networks


Advances in Neural Information Processing Systems, 1987, Morgan Kaufmann Publishers

Advances in Neural Information Processing Systems, Volume 1, 1988, Morgan Kaufmann Publishers

Advances in Neural Information Processing Systems, Volume 2, 1989, Morgan Kaufmann Publishers

Aihara, Kazuyuki, Neural Computers: The Study of Brain and Neuron (in Japanese), Tokyo Electrical Engineering Institute, Tokyo, 1988

Anderson, James A., editor, Foundations of Neuro-computing, MIT Press, Cambridge MA, 1988

The Brain, a Scientific American Book, 1979, W.H. Freeman and co., New York

Caianello, E.R., editor, Neural Networks: Proceedings of the School on Neural Networks, June 1967 in Ravello, 1968, Springer-Verlag Berlin

Churchland, Patricia Smith, Neurophilosophy: Toward a Unified Science of the Mind-Brain, MIT Press, Cambridge MA, 1986

The DARPA Study on Neural Networks

Durbin, Richard, Christopher Miall, Graeme Mitchison (editors), The Computing Neuron, Addison Wesley, 1989

Eckmiller, Rolf, Cristoph von der Marlsburg Eds., NATO ASI Series: #41. Neural Computers, Springer Verlag, Heidelberg, 1988

First IEEE International Conference on Neural Networks, San Diego, 1987

Gaines, Brian R., Sixth Generation Computing: a Conspectus of the Japanese Proposals, SIGART Newsletter, Jan. 1986, no. 95, pp. 39-

Grossberg, Stephen, editor, Neural Networks and Natural Intelligence, MIT Press, Cambridge MA, 1988

International Joint Conference on Neural Networks, 1988

International Joint Conference on Neural Networks, 1989

International Joint Conference on Neural Networks, Washington D.C. 1990

International Joint Conference on Neural Networks, San Diego, 1990

Irwin, Louis N., (ed.), Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, 1988, Birkhauser, Boston

Johnson, R. Colin, Neural Networks in Japan, Electronic Engineering Times, April 6 1987, p. 49

Kohonen, Teuvo, Self Organization and Associative Memory, second edition, Springer Verlag, Heidelberg, 1988

Lippmann, Richard P., An Introduction to Computing with Neural Networks, IEEE ASSP Magazine, vol. 3, no. 4, April 1987, pp. 4-22

McClelland, James L., David E. Rumelhart, Parallel Distributed Processing, vol. 1, MIT Press, Cambridge MA, 1986

McClelland, James L., David E. Rumelhart, Explorations in Parallel Distributed Processing: A Handbook of Models, Programs and Exercises, MIT Press, Cambridge MA, 1989

McCulloch, Warren S., Embodiments of Mind, MIT Press, Cambridge MA, 1965, reissued 1988

MacGregor, Ronald, Neural and Brain Modeling, Academic Press Inc., San Diego, 1987

Minsky, Marvin, The Society of Mind, Picador, London, 1987

Rietmann, Ed, Experiments in Artificial Neural Networks, Tab Books, 1988

Rumelhart, David E., James L. McClelland, Parallel Distributed Processing, vol. 1, MIT Press, Cambridge MA, 1986

von Neumann, John, The Computer and the Brain, MIT Press, 1958



Adaptive Control


Anderson, Charles W., Learning to Control an Inverted Pendulum Using Neural Networks, IEEE Control Systems Magazine, April 1989, pp. 31-36

Barto, Andrew G., Connectionist Learning for Control: An Overview, COINS Technical Report 89-89, September 1989, Department of Computer Science, University of Massachusetts at Amherst

Barto, Andrew G., Richard S. Sutton, & Charles W. Anderson, Neuronlike adaptive elements that can solve difficult learning control problems, IEEE Transactions on Systems, Man, and Cybernetics, 1983, SMC-13, pp. 834-846

Barto, Andrew G., Richard S. Sutton, Chris J.C.H. Watkins, Learning and Sequential Decision Making, COINS Technical Report 89-95, September 1989, Department of Computer Science, University of Massachusetts at Amherst

Fujii, Teruo, Tamaki Ura, Development of Motion Control System for AUV Using Neural Nets, Proceedings of the IEEE Symposium on Autonomous Underwater Vehicle Technology, June 5 and 6, 1990, Washington D.C., pp. 81-86

Josin, Garry, Development of a Neural Network Autopilot Model for a High Performance Aircraft, 1990 International Joint Conference on Neural Networks, pp. II: 547-550

Michie D., & R.A. Chambers, BOXES: An experiment in adaptive control, in Machine Intelligence 2, E. Dale and D. Mitchie (eds.), Oliver and Boyd, Edinburgh, pp. 137-152 (1968)

Nguyen, Widrow, Bernard, The Truck Backer Upper, 1989 International Joint Conference on Neural Networks, pp. II: 357-363

Porcino, Nick, and James S. Collins, An Application of Neural Networks to the Control of a Free Swimming Submersible, Proceedings of the 1990 International Joint Conference on Neural Networks, Washington D.C., pp. II:417-420

Sutton, Richard S., Integrated Architectures for Learning, Planning, and Reacting Based on Approximating Dynamic Programming, in Proceedings of the Seventh International Conference on Machine Learning, June 1990

Watkins, Chris J.C.H., Learning from Delayed Rewards, PhD Thesis, May 1989, Kings College




Adaptive Resonance Theory

See also Vision - General for more related papers by Stephen Grossberg. Note that many of the papers cited here have been collected in the volume "Neural Networks and Natural Intelligence," edited by S. Grossberg and published by MIT Press in 1988.

Carpenter, Gail, Stephen Grossberg, The ART of Adaptive Pattern Recognition by a Self Organizing Neural Network, IEEE Computer Magazine, March 1988, vol. 21, no. 3, pp. 77-88

Cohen, Michael A., Stephen Grossberg, Masking Fields: A Massively Parallel Neural Architecture for Learning, Recognizing, and Predicting Multiple Groupings of Patterned Data, Applied Optics, 1987, vol. 26, no. 10, pp. 1866-1891

Grossberg, Stephen, How does the brain build a cognitive code? Psychological Review, 1980, vol. 87, pp. 1-51

Grossberg, Stephen, Competitive Learning: From Interactive Activation to Adaptive Resonance, Cognitive Science, 1987, vol. 11, pp. 23-67

Grossberg, Stephen, Gail Carpenter, A Massively Parallel Architecture for a Self Organizing Neural Pattern Recognition Machine, Computer Vision, Graphics, and Image Processing, 1987, vol. 37, pp. 54-115

Grossberg, Stephen, Daniel S. Levine, Neural Dynamics of Attentionally Modulated Pavlovian Conditioning: Blocking, Inter-stimulus Interval, and Secondary Reinforcement, Applied Optics,1987, vol. 26, pp. 5015-5030



Back Propagation and Gradient Descent

Allred, Lloyd G., Gary E. Kelly, Supervised Learning Techniques for Backpropagation Networks, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I:721-728

Fahlman, Scott E., Christian Lebiere, The Cascade-Correlation Learning Architecture, Feb. 14, 1990, CMU-CS-90-100, School of Computer Science, Carnegie Mellon University, Pittsburg, PA 15213

Fang, Yan, Terrence J. Sejnowski, Faster Learning for Dynamic Recurrent Backpropagation, in Neural Computation, vol. 2, no. 3, pp. 270-273

Fukuda, T., T. Shibata, M. Tokita, T. Mitsuoka, Neural Network Application for Robotic Motion Control, Adaptation and Learning, in Proceedings of the International Joint Conference on Neural Networks, San Diego,1990, pp. III:447-451

Hagiwara, Masafumi, Novel Back Propagation Algorithm for Reduction of Hidden Units and Acceleration of Convergence using Artificial Selection, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I:625-630

Irie, Bunpei, Sei Miyake, Capabilities of Three-Layered Perceptrons, in Proceedings of the 1988 International Joint Conference on Neural Networks, pp. I: 641-648

Jones, R.D., Y.C. Lee, C.W. Barnes, G.W. Flake, K. Lee, P.S. Lewis, S. Qian, Function Approximation and Time Series Prediction with Neural Networks, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I:649-665

McClelland, James L., David E. Rumelhart, Parallel Distributed Processing, vol. 1, MIT Press, Cambridge MA, 1986

McClelland, James L., David E. Rumelhart, Explorations in Parallel Distributed Processing: A Handbook of Models, Programs and Exercises, MIT Press, Cambridge MA, 1989

Nguyen, Derrick, Bernard Widrow, Improving the Learning Speed of 2-Layer Neural Networks by Choosing Initial Values of the Adaptive Weights, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III:21-26

Parker, David B., A Comparison of Algorithms for Neuron-Like Cells, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird UT, 1986, John S. Denker ed., pp. 327-332

Rumelhart, David E., Geoffrey E. Hinton, Ronald J. Williams, Learning Representations by Back-Propagating Errors, Nature, 1986, vol. 323, pp. 533-536

Rumelhart, David E., James L. McClelland, Parallel Distributed Processing, vol. 1, MIT Press, Cambridge MA, 1986

Stinchcombe, Maxwell, Halbert White, Approximating and Learning Unknown Mappings using Multilayer Feedforward Networks with Bounded Weights, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III:7-16

Tollenaere, Tom, SuperSAB: Fast Adaptive Back Propagation with Good Scaling Properties, in Neural Networks, vol. 3, no. 5, pp. 561-574

White, Halbert, Connectionist Nonparametric Regression: Multilayer Feedforward Networks Can Learn Arbitrary Mappings, Neural Networks, vol. 3, no. 5, pp. 535-550, 1990

Widrow, Bernard & Marcian Hoff, Adaptive Switching Circuits, IRE WESCON Convention Record, 1960, NY, IRE, pp96-104

Widrow, Bernard, Introduction (Historical Anecdotes): Proceedings of the First IEEE Conference on Neural Nets, 1987

Widrow, Bernard, Rodney G. Winter, Robert A. Baxter, Learning Phenomena in Layered Neural Networks, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II:411-429

Widrow, Bernard, Rodney G. Winter, Neural Networks for Adaptive Filtering and Adaptive Pattern Recognition, IEEE Computer Magazine, March 1988, vol. 21, no. 3, pp. 25-39

Widrow, Bernard, Lehr, Wan, MRIII A Robust Algorithm for Training Analog Neural Networks, 1990 International Joint Conference on Neural Networks, Washington D.C., pp. I: 533-540



Boltzmann Machines

Ackley, David H., Geoffrey E. Hinton, & Terrence J. Sejnowski, A Learning Algorithm for Boltzmann machines, Cognitive Science, 1986, vol 9, pp.147-169

Metropolis N., A.W. Rosenbluth, M.N. Rosenbluth, A.H. Teller, E. Teller, Equation of State Calculations for Fast Computing Machines, Journal of Chemical Physics, June 1953, vol. 21, no. 6, p. 1087-1092

Press, W.H., B.P. Flannery, S.A. Teukolsky, W.T. Vetterling, The Travelling Salesman Problem (incl. Boltzmann machine program listing), in Numerical Recipes in C: The Art of Scientific Computing, Cambridge University Press, 1988, pp. 345-352


Chaos in Neural Networks

Baird, Bill, Bifurcation Analysis of a Network Model of Rabbit Olfactory Bulb with Periodic Attractors Stored by a Sequencee Learning Algorithm, in Proceedings of the First IEEE International Joint Conference on Neural Networks, San Diego, 1987, pp. II:147-152

Baird, Bill, ... and their Bifurcations in Dynamic Neural Networks, 1988 International Joint Conference on Neural Networks, pp. I: 9-16

Freeman, Walter J., Why Neural Networks Don't Yet Fly: Inquiry Into the Neurodynamics of Biological Intelligence, in Proceedings of the 1988 International Joint Conference on Neural Networks, pp. II:1 -7

Gelperin, Alan, David W. Tank, Odour-modulated Collective Network Oscillations of Olfactory Interneurons in a Terrestrial Mollusc, Nature, May 31. 1990, vol. 345, pp. 437-440

Yao, Freeman, Walter J., Pattern Recognition in Olfactory Systems, 1989 International Joint Conference on Neural Networks, pp. I: 699-704


Emergence

Highly recommended references are asterisked.
  Discussions of the original concept of emergence: Bergson, Morgan, Nagel, Denbigh, Pepper, Klee
  Computational emergence: Langton, Hillis, Forrest
  Functional emergence (emergence of modelling relations): Rosen, Pattee, Cariani (see also Nagel & Klee)
  Critiques of emergence in computer simulations: Rosen (1973, 1985), Pattee (1989), Cariani (1987-90), Carello et al (1984)

I'd appreciate any additional references which are primarily focussed on fundamental issues raised by the problem of emergence. Thanks.
  -- Peter Cariani (peterc@chaos.cs.brandeis.edu)

Some references on the problem of emergence
========================================================================
Bergson, Henri (1911) Creative Evolution. (New York: Random House), 1946. [one of the original expositors of the concept of Emergent Evolution]

Cariani, Peter (1988) Why Artificial Life Needs Evolutionary Robotics. unpublished manuscript, available upon request.

Cariani, Peter (1989) On the Design of Devices with Emergent Semantic Functions. Ph.D. dissertation, Dept. of Systems Science, State University of New York at Binghamton. [the problem of emergence as it relates to AI and evolutionary robotics; limitations of purely simulational approaches; relation between types of adaptivity and emergence]

Cariani, P. (1989) "Adaptivity, emergence and machine-environment dependencies." Proc, 33rd Annual Meeting, Int. Soc. for Systems Sciences (formerly ISGSR), III:31-37.

Cariani, P. (1990) " Implications from structural evolution:semantic adaptation." Proceedings of the International Joint Conference on Neural Networks, Washington, D.C., January, 1990, I: 47-50.

Cariani, P. (1990) "Emergence and Artificial Life." manuscript submitted to Proceedings, Second Workshop on Artificial Life, available upon request.

Cariani, P. (1990) "Adaptation and Emergence in Organisms and Devices." in press, Journal of General Evolution.

Carello, C., M.T. Turvey, P. N. Kugler, and R. E. Shaw (1984), "Inadequacies of the computer metaphor." Handbook of Cognitive Neuroscience. Ed., M. Gazzaniga (New York: Plenum Press). [functional limitations of
  computing devices: good general discussion]

Denbigh, KG (1975) An Inventive Universe. (New York: George Braziller). [thermodynamics, determinism and emergence, good general discussion]

Forrest, S. (1989) "Emergent Computation: Self-organizing, Collective, and Cooperative Phenomena in Natural and Artificial Computing Networks," Proceedings of the Ninth Annual Center for Nonlinear Studies and Computing Division Conference, April, 1989. [a serious attempt to formulate a definition of emergent computation]

Hillis, Daniel (1988), "Intelligence as an emergent behavior; or the songs of Eden" Daedelus AI issue, Winter, 1988 (reprinted by MIT Press).Eden," Daedalus, Winter, 1988,175-189.

Klee, R. L. (1984), "Micro-determinism and concepts of emergence, "Philosophy of Science 51: 44-63. [excellent paper discussing clashes differing conceptions of hierarchies and emergence]

Langton, C. (1986), "Studying artificial life with cellular automata," Physica D 22:120-149.

Langton, C. (1989), "Artificial life," Artificial Life, SFI Studies in the Sciences of Complexity. Ed. C. Langton (Reading, MA: Addison-Wesley).

Morgan, C.L. (1927), Emergent Evolution. (London: Northgate and Williams). [one of the original expositors of the concept of emergent evolution]

Nagel, E. (1961), The Structure of Science. (New York: Harcourt, Brace & World) (see pp.367-380 and Chapter 12; an excellent discussion of the problem)

Pattee, H. H. (1972), "The nature of hierarchical controls in living matter," Foundations of Mathematical Biology, Vol. I, R. Rosen, ed. (New York: Academic Press).

Pattee, H. H. (1973), "Physical problems in the origin of natural controls," Biogenesis, Evolution, Homeostasis. Ed., A. Locker (New York: Pergamon). [emergence and the formation of hierarchical constraints]

Pattee, H. H. (1973), "The physical basis of the origin of hierarchical control." Hierarchy Theory: The Challenge of Complex Systems. Ed., H. Pattee (New York: George Braziller).

Pattee, H. H. (1989), "Simulations, Realizations, and Theories of Life," Artificial Life, SFI Studies in the Sciences of Complexity (Reading, MA: Addison-Wesley).

Pepper, Stephen (1926), "Emergence," Journal of Philosophy 23-241-245.

Rosen, R. (1973), "On the generation of metabolic novelties in evolution," Biogenesis, Evolution, Homeostasis. Ed., Alfred Locker (New York: Pergamon). [must reading for Alife simulators; a discussion of the concept of organism and emergent functional properties in simulations]

Rosen, R. (1978) Fundamentals of Measurement and Representation of Natural Systems. (New York: North Holland).

Rosen, R. (1985), Anticipatory Systems. Pergamon Press, New York. [A very dense, but very important book; lays out an entire theory of modelling relations in organisms and devices]

Rosen, R. (1987) On the scope of syntactics in Mathematics and Science: The Machine Metaphor. In: J Casti, ed. Real Brains, Artificial Minds. North-Holland, New York.


Fuzzy Systems

Fuzzy systems were invented by L.A. Zadeh in 1965 and are just now coming into vogue. Influential authors are Lotfi A. Zadeh, Abraham Kandel, Ronald R. Yager, Brian R. Gaines (U of Calgary) and Bart Kosko.

Diamond, J., R. McLeod, W. Pedrycz, A Fuzzy Cognitive System: Examination of a Referential Neural Architecture, in Proceedings of the International Joint Conference on Neural Networks, San Diego,1990, pp. II:617-622

Fujii, Teruo, Tamaki Ura, Development of Motion Control System for AUV Using Neural Nets, Proceedings of the IEEE Symposium on Autonomous Underwater Vehicle Technology, June 5 and 6, 1990, Washington D.C., pp. 81-86

Fukuda, T., T. Shibata, M. Tokita, T. Mitsuoka, Neural Network Application for Robotic Motion Control, Adaptation and Learning, (Fuzzy Turbo for Back Propagation) in Proceedings of the International Joint Conference on Neural Networks, San Diego,1990, pp. III:447-451

Hisdal, Ellen, Developments in the Wake of the Theory of Possibility, in Fuzzy Sets: Theory and Applications to Policy Analysis and Information Systems, Paul P. Wang and S.K. Chang (eds.), Plenum Press, New York, 1980, pp. 87-91

Iwata, Toshiaki, Kazuo Machida, Yoshitsugu Toda, Fuzzy Control Using Neural Network Techniques, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III: 365-370

Kandel, Abraham, Fuzzy Statistics and Policy Analysis, in Fuzzy Sets: Theory and Applications to Policy Analysis and Information Systems, Paul P. Wang and S.K. Chang (eds.), Plenum Press, New York, 1980, pp. 133-145

Kong, Seong-Gon, Bart Kosko, Comparison of Fuzzy and Neural Truck Backer-Upper Control Systems, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III:349-358

Kosko, Bart, Neural Systems and Fuzzy Systems, Prentice-Hall, 1990

Kosko, Bart, Adaptive Inference in Fuzzy Knowledge Networks, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II: 261-268

Patrikar, Ajay, John Provence, A Self-Organizing Controller for Dynamic Processes using Neural Networks, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III:359-364

Scott, Leland L., Necessary and Sufficient Conditions for the Values of a Function of Fuzzy Variables to Lie in a Specified Subinterval of [0,1], in Fuzzy Sets: Theory and Applications to Policy Analysis and Information Systems, Paul P. Wang and S.K. Chang (eds.), Plenum Press, New York, 1980, pp. 35-47

Takemori, Toshikazu, Nobuji Miyasaka, Shozo Hirose, Thermal Comfort Sensor based on Probabilistic Energy Neural Network, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:471-476

Wang, Paul P., C.Y. Wang, Experiment on Character Recognition Using Fuzzy Filters, in Fuzzy Sets: Theory and Applications to Policy Analysis and Information Systems, Paul P. Wang and S.K. Chang (eds.), Plenum Press, New York, 1980, pp. 195-221

Zadeh, Lotfi A., Fuzzy Sets, Information and Control, vol. 8, 1965, New York, Academic Press, pp. 338-353



Hopfield and Optimization Networks

Hopfield, John J., Neural Networks and physical systems with emergent computational abilities, Proceedings of the National Academy of Sciences, 1982, vol 79. pp. 2554-2558

Hopfield, John J., Neurons with graded response have collective computational properties like those of two state neurons, Proceedings of the National Academy of Sciences, 1984, vol. 81, pp. 3088-3092

Shackleford, Barry J., Neural Data Structures: Programming with Neurons, Hewlett-Packard Journal, vol. 40, no.3, June 1989, pp. 69-78

Tank, David, John J. Hopfield, Concentrating Information in Time: Analog Neural Networks with Application to Speech Recognition Problems, 1987 International Joint Conference on Neural Networks, pp. IV: 455-468


Learning

Methods of training neural networks are legion. This list is a guide to some of the more well known and significant research related to learning in neural networks.

See also Self Organizing Feature Nets and Vector Quantization, Back Propagation, Spatio-Temporal Neural Networks, and Time Delay Neural Networks

Albus, James S., Brains, Robotics, and Behavior, BYTE Books (McGraw Hill), 1981

Alkon, Daniel L., Memory Traces in the Brain, Cambridge University Press, 1987

Anderson, James A., A Simple Network generating an Interactive Memory, Mathematical Biosciences, 1972, vol. 14, pp. 197-220

Barto, Andrew G., From Chemotaxis to Cooperativity: Abstract Exercises in Neuronal Learning Strategies, in The Computing Neuron, R. Durbin, C. Miall, G. Mitchison (Eds.), Addison Wesley, 1989, pp. 73-98

Barto, Andrew G., Michael I. Jordan, Gradient Following Without Back Propagation in Layered Networks, in Proceedings of the First IEEE Conference on Neural Networks, San Diego, 1987, pp. II:629-636

Cybenko, Function Approximation by Superposition of Nonlinear Functions, Information and Control, 1990

Dimopoulos, Nikitas J., Don Radvan, W.A. Keddy, Learning in Asymptotically Behaving Neural Networks, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III:233-238

Gluck, Mark A. & Richard F. Thompson, Modelling the Neural Substrates of Associative Learning and Memory: A Computational Approach, Psychological Review, 1987, vol 94, no. 2, pp. 176-191

Hebb, Donald O., The Organization of Behaviour, Wiley & Sons, New York, 1949

Hecht-Nielsen, Robert, Counter-Propagation Networks, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II:19-32

Hecht-Nielsen, Robert, Kolmogorov's Mapping Neural Network Existence Theorem, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. III:11-14

Kanerva, Pentti, Parallel Structures in Human and Computer Memory, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird UT, 1986, John S. Denker ed., pp. 247-258

Klopf, A. Harry, The Hedonistic Neuron: A Theory of Memory, Learning, and Intelligence, Hemisphere Press, Washington DC, 1982

Klopf, A. Harry, A Drive-Reinforcement Model of Single Neuron Function: An Alternative to the Hebbian Neuronal Model, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird UT, 1986, John S. Denker ed., pp. 265-269

Klopf, A. Harry, Drive-Reinforcement Learning: A Real-Time Learning Mechanism for Unsupervised Learning, in Proceedings of the First IEEE International Joint Conference on Neural Networks, San Diego, 1987, pp. II:441-445

Klopf, A. Harry, A neuronal model of classical conditioning, Psychobiology, 1988, vol. 16, no. 2, pp. 85-125

Kosko, Bart, Differential Hebbian Learning, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird UT, 1986, John S. Denker ed., pp. 277-282

Kosko, Bart, Stochastic Competitive Learning, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:215-226

Lashley. Karl S., In Search of the Engram, Society of Experimental Biology Symposium, no. 4, Psychological Mechanisms in Animal Behaviour, Cambridge University Press, 1950, pp. 454-480

Minsky, Marvin & Seymour Papert, Perceptrons, expanded edition, MIT Press, Cambridge MA, 1969 re-released 1988

Psaltsis, Demetri, David Brady, Xiang-Guang Gu, Steven Lin, Holography in Artificial Neural Networks, Nature, vol. 343, 25 Jan. 1990, pp. 325-330

Rosenblatt, Frank, The Perceptron: A probabilistic model for information storage and retrieval in the brain, Psychological Review, 1958, vol. 65, pp. 386-408

Yau, Hung- Chun, Michael T. Manry, Iterative Improvement of a Gaussian Classifier, Neural Networks, vol. 3, no. 4, 1990, pp. 437-443


Locomotion - General

Gewecke, Michael, Swimming Behaviour of the Water Beetle Dytiscus Marginalis L. (Coleoptera, Dytiscidae), in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 111-120

Hirose, Shigeo, Akio Morishima, Design and Control of a Mobile Robot with an Articulated Body, in The International Journal of Robotics Research, vol. 9, no. 2, April 1990, pp. 99-114

Horsmann, Ulrich, Gernot Wendler, The Role of a Fast Wing Reflex in Locust Flight, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 157-165

Robertson, Meldrum, Central Neuronal Interactions in the Flight System of the Locust, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 183-194

Rowell, Hugh F., Heinrich Reichert, Compensatory Steering in Locusts: the Integration of Non-Phase Locked Input with a Rhythmic Motor Output, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 175-182

Ruppell, Georg, Kinematic and Behavioural Aspects of Flight of the Male Banded Agrion, Calopteryx (Agrion) Splendens L., in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 195-204

Siddiqui, Shahid S., Neural Circuitry Mediating Locomotion in C. Elegans: Molecular Correlates of Inhibitory Motor Neurons, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I:155-160

Stent, Gunther S., William B. Kristan, W. Otto Friesen, Carol A. Ort, Margaret Poon, Ronald L. Calabrese, Neuronal Generation
of the Leech Swimming Movement, Science, vol. 200, no. 23, June 1978, pp. 1348-1356

Wendler, Gernot, Harry Teuber, Jorg Peter Jander, Walking, Swimming, and Intermediate Locomotion in Nepa Rubra, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 103-110


Locomotion - Walking Organisms

The study of the neural control of walking teaches us much about the distributed nature of intelligent control. Neural locomotion control architectures are elegant and robust and increasingly well understood.

Alexander, R. McN., Three Uses for Springs in Legged Locomotion, in The International Journal of Robotics Research, vol. 9, no. 2, April 1990, pp. 53-61

Barrington, E.J.W., Invertebrate Structure and Function, Thomas Nelson and Sons, Don Mills, Ont., 1969, (Locomotion in Terrestrial Arthropods, pp. 134-141)

Bassler, Ulrich, Proprioceptive Control of Stick Insect Walking, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 43-48

Beer, Randall D., Hillel J. Chiel, Leon S. Sterling, Heterogeneous Neural Networks for Adaptive Behaviour in Dynamic Environments, in Advances in Neural Information Processing Systems, Volume 1, Morgan Kaufman Publishers, 1989

Chiel, Hillel J., & Randall D. Beer, A Lesion Study of a Heterogeneous Artificial Neural Network for Hexapod Locomotion, in Proceedings of International Joint Conference on Neural Networks 1989, pp. I: 407-414

Cruse, Holk, The Influence of Load, Position, and Velocity on the Control of Leg Movement of a Walking Stick Insect, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 19-26

Dean, Jeffrey, A Simulation of Proprioceptive Input from the Coxal Hair Rows of the Stick Insect: Possible Effect of Step Velocity on the Representation of Joint Angle, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 49-57

Delcomyn, Fred, Sense Organs and the Pattern of Motor Activity During Walking in the American Cockroach, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 87-96

Franklin, Robert F., The Locomotion of Hexapods on Rough Ground, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 69-78

Graham, D., Pattern and Control of Walking in Insects, in Berridge, M.J., J.E. Treherne, V.B. Wigglesworth, (Eds.) Advances in Insect Physiology, volume 18, 1985, Academic Press, New York, pp. 31-140

Gray, James, Animal Locomotion, Weidenfeld and Nicolson, London, 1968

Hoyle, Graham, Arthropod Walking, in Neural Control of Locomotion, R.M.Herman, S.Grillner, P.S.G. Stein, & D.G. Stuart (Eds), Plenum Press, New York, 1976, pp. 137-179

Hustert, Reinhold, The Contribution of Proprioceptors to the Control of Motor Patterns of Legs in Orthopterous Insects - The Locust Example, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 59-67

Jander, Jorg Peter, Mechanical Stability in Stick Insects When Walking Straight and Around Curves, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 33-42

Laurent, Gilles & Reinhold Hustert, Motor Neuronal Receptive Fields Delimit Patterns of Motor Activity During Locomotion of the Locust, Journal of Neuroscience, vol. 8, no. 11, Nov. 1988, pp. 4349-4366

Pearson, Keir G., The Control of Walking, Scientific American, vol 276, Dec. 1976

Pearson, Keir G., Robert F. Franklin, Characteristics of Leg Movements and Patterns of Coordination in Locusts Walking on Rough Terrain, International Journal of Robotics Research, vol. 3, no. 2, Summer 1984, pp. 101-112

Porcino, Nick, A Neural Network Controller for Hexapod Locomotion, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I-189-194

Siegler, Melody V.S., Nonspiking Interneurons and Motor Control in Insects, in Berridge, M.J., J.E. Treherne, V.B. Wigglesworth, (Eds.) Advances in Insect Physiology, volume 18, 1985, Academic Press, New York, pp. 249-304


Locomotion - Walking Robots

Brooks, Rodney A., A Robot That Walks: Emergent Behaviors from a Carefully Evolved Network, Proceedings of the 1989 IEEE International Conference on Robotics and Automation, Volume 2, pp. 692-696

Furusho, J., A. Sano, Sensor-Based Control of a Nine-Link Robot, in The International Journal of Robotics Research, vol. 9, no. 2, April 1990, pp. 83-98

Gorinevsky, D.M., A. Yu. Shneider, Force Control in Locomotion of Legged Vehicles over Rigid and Soft Surfaces, in The International Journal of Robotics Research, vol. 9, no. 2, April 1990, pp. 4-23

Hirose, Shigeo, A Study of a Design and Control of a Quadruped Walking Vehicle, International Journal of Robotics Research, vol. 3, no. 2, Summer 1984, pp. 113-133

Kaneko, Makoto, Kazuo Tanie, and Mohamad Nor Bin Mohamad Than, A Control Algorithm for Hexapod Walking Machine Over Soft Ground, IEEE Journal of Robotics and Automation, vol. 4, no. 3, June 1988, pp. 294-302

Miura, Hirofumi, Isao Shimoyama, Dynamic Walk of a Biped, International Journal of Robotics Research, vol. 3, no. 2, Summer 1984, pp. 60-74


Miscellaneous

Berke, Peter, That Does Not Compute, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. IV: 819-826

Feldman, Jerome A., Neural Representations of Conceptual Knowledge, in Neural Connections, Mental Computations, L.Nadel, L.A.Cooper, P.Culicover, & R.M.Harnish (eds.), MIT Press, Cambridge MA, 1989

Gaines, Brian R., Positive Feedback Processes Underlying Functional Differentiation, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II:387-394

McCulloch, Warren S. & Walter Pitts, A Logical Calculus of Ideas Imminent in Nervous Activity, Bulletin of Mathematical Biophysics, 1943, vol. 5, pp. 115-133

Steels, Luc, Self-Organization through Selection, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II:55-62

Treffner, Paul J., Ecological Connectionism and Animal-Environment Mutuality, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II:813-820


Miscellaneous Applications

Belew, Richard K., Designing Appropriate Learning Rules for Connectionist Systems (text retrieval), in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II: 479-486

Dahl, Edward Denning, Neural Network for an NP-Complete Problem: Map and Graph Colouring, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. III: 113-120

Kimoto, Takashi, Kazuo Asakawa, Morio Yoda, Masakazu Takeoka, Stock Market Prediction System with Modular Neural Networks, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I:1-6

Konger, Christopher, Jose C. Principe, Murat Taner, Neural Network Classification of Event Related Potentials for the Design of a New Computer Interface, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 367-372

Takefuji, Yoshiyasu, Paul Hollis, Yoon Pin Foo, Yong B. Cho, Error Correcting System Based on Neural Circuits, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. III: 293-300

Tesauro, Gerald, Neurogammon: A Neural Network Backgammon Program, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III: 33-39

Wang, Lixin, J.M. Mendel, Structured Trainable Networks for Matrix Algebra, Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:125-132


Navigation

Arkin, Ronald C., Motor Schema-Based Mobile Robot Navigation, International Journal of Robotics Research, April 1987, pp. 264-271

DeMuth, Gordon, Steve Springsteen, Obstacle Avoidance Using Neural Networks, Proceedings of the IEEE Symposium on Autonomous Underwater Vehicle Technology, June 5 and 6, 1990, Washington D.C., pp. 213-215

Fernandez, On Tropistic Processing and its Applications, Neural Information Processing Systems, pp. 262-269

Hassoun, Mohamad H., Ashvin J. Sanghvi, Fast Computation of Optimal Paths in Two- and Higher-Dimension Maps, in Neural Networks, vol. 3, no. 3, 1990, pp. 355-363

Hassoun, Mohamad H., Ashvin Sanghvi, Locally Interconnected Layered Neural Network for Path Optimization, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III:811-817

Jorgensen, C.C., Neural Network Representation of Sensor Graphs in Autonomous Robot Path Planning, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. IV: 507-515

Moravec, Hans, Sensor Fusion in Uncertainty Grids for Mobile Robots, in Annual Research Review of the Robotics Institute, Carnegie Mellon University, 1987, pp. 33-48

Park, Lee, Neural Computation for Collision Free Path Planning, 1990 International Joint Conference on Neural Networks, pp. II: 229-232


NeoCognitron

Barnard, Etienne, David Casasent, Shift Invariance and the NeoCognitron, Neural Networks, vol. 3, no. 4, 1990, pp. 403-410

Fukushima, Kunihiko, A Neural Network Model for Selective Attention, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II:11-18

Fukushima, Kunihiko, A Neural Network for Visual Pattern Recognition, IEEE Computer Magazine, March 1988, vol. 21, no. 3, pp. 65-75

Fukushima, Kunihiko, Analysis of Visual Pattern Recognition by NeoCognitron, Neural Networks, vol. 2, no. 6, 1989, pp. 413-420

Fukushima, Kunihiko, Spatio Temporal vs. Spatial Pattern Recognition by the NeoCognitron, in Proceedings of the International Joint Conference on Neural Networks, Washington D.C., 1990, pp. II:279-282

Ito, Kunihiko Fukushima, Recognition of Spatio Temporal Patterns with a Hierarchical Neural Network, in Proceedings of the International Joint Conference on Neural Networks, Washington D.C., 1990, pp. I:273-276

Miyake, Sei, Kunihiko Fukushima, A Neural Network Model for the Mechanism of Pattern Information Processing, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird UT, 1986, John S. Denker ed., pp. 305-308

Rajapakse, Jagath, Raj Acharya, Medical Image Segmentation with MARA, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:965-972


Neuroethology - Invertebrate

Abbott, Larry, Scott Hooper, Tom Kepler, Eve Marder, Oscillating Networks: Modeling the Pyloric Circuit of the Stomatogastric Ganglion, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 175-180

Alkon, Daniel L., Membrane Channels, Conditioning Induced Changes, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 72-75

Barrington, E.J.W., Invertebrate Structure and Function, Thomas Nelson and Sons, Don Mills, Ont., 1969, (Nervous System and Learning in Cephalopods, pp. 330-336)

Beer, Randall D., Hillel J. Chiel, Neural Implementation of Motivated Behaviour: Feeding in an Artificial Insect, in D.S. Touretzky (ed.), Advances in Neural Information Processing Systems 2, 1990, Morgan Kaufmann Publishers

Davis, William J., Organizational Concepts in the Central Motor Networks of Invertebrates, in Neural Control of Locomotion, R.M. Herman, S. Grillner, P.S.G. Stein, & D.G. Stuart (Eds), Plenum Press, New York, 1976, pp. 265-292

Eckert, Roger, Paramecium, the Ionic Basis of Sensorimotor Behaviour, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 97-99

Erber, Joachim, Honeybee Learning, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, p. 47

Kandel, Eric R., Small Systems of Neurons, in The Brain, a Scientific American Book, 1979, W.H. Freeman and co., New York, pp. 28-38

Kupfermann, I., K.R. Weiss, The Command Neuron Concept, Behavioural Brain Science, 1978, pp. 1:3-39

Lent, Charles M., Michael H. Dickinson, The Neurobiology of Feeding in Leeches, Scientific American, June 1988, vol. 258, no. 6, pp. 98-103

Lockery, Shawn R., G. Wittenburg, W.B. Kristan Jr., N. Qian, and Terrence Sejnowski, Neural Network Analysis of Distributed Representations of Sensory Information in the Leech, Neural Information Processing Systems 2, David Touretzky ed., Morgan Kaufmann Publishers, 1990

Lockery, Shawn R., Yan Fang, Terrence Sejnowski, A Dynamic Neural Network Model of Sensorimotor Transformations in the Leech, in Neural Computation, vol. 2, no. 3, pp. 274-282

Ruppell, Georg, Kinematic and Behavioural Aspects of Flight of the Male Banded Agrion, Calopteryx (Agrion) Splendens L., in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 195-204

Stabel, Jasmine, Gernot Wendler, Hans Scharstein, The Escape Reaction of Acheta Domesticus Under Open Loop Conditions, in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 79-85








Truman, James W., Metamorphosis (Caterpillars, Moths), in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 76-78


Neuroethology - Miscellaneous

Neuroethology is the study of the neural control of behaviour. The neuro-architectures employed by biological nervous systems can lead to elegant and robust neural networks for the intelligent control of distributed systems.

Camhi, Jeffrey M., Neuroethology: Nerve Cells and the Natural Behaviour of Animals, Sinauer Associates Inc. Publishers, Sunderland, Massachusetts, 1984

Cliff, D.T., Computational Neuroethology: A Provisional Manifesto, Cognitive Science Research Paper, Serial No. CSRP 11111162, May 1990, The University of Sussex, School of Cognitive and Computing Science, Falmer, Brighton BN1 9QN, England, UK

Coss, Richard G., Albert Globus, Spine Stems on Tectal Interneurons in Jewel Fish are Shortened by Social Stimulation, Science,   vol. 200. 19 May 1978, pp. 787-789

Crick, Francis, Function of the thalamic reticular complex: the searchlight hypothesis, Proceedings of the National Academy of Sciences, 1984, 81: 4586-4590

Crick, Francis, The Brain, Scientific American, 1977










Creutzfeldt O.D. & P. Huggelund, Science, 1975, vol. 188, pp. 1025-1027

Delcomyn, Fred, Neural Basis of Rhythmic Behavior in Animals, Science, vol. 210, 31 Oct. 1980, pp. 492-498

Drawbaugh, Donald W., Toward a Model of the Hippocampus, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:717-721

Dumont, James P.C., R. Meldrum Robertson, Neuronal Circuits: An Evolutionary Perspective, Science, vol. 233, 22 Aug. 1986, pp. 849-852

Fair, Charles M., Memory and Central Nervous Organization, Paragon House Publishers, New York, 1988

Guthrie D.M., Neuroethology: An Introduction, Blackwell Scientific Publications, Oxford, 1980

Heron W., et al, In Sensory Deprivation, P. Solomon et al., eds., pp 66666666-33, Harvard University Press, 1961

Hyde, Vickie, Momentum: The Rhythms of Life, Japan Times, Oct. 18, 1988, p. 10

Masino, Tom, Eric I. Knudsen, Horizontal and Vertical components of Head Movement are Controlled by Distinct Neural Circuits in the






Barn Owl, Nature, May 31, 1990, vol. 345, pp. 434-437

Nottebohm, Fernando, Birdsong, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 9-12

Olmsted, David, The Reticular Formation as a Multi-Valued Logic Neural Network, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 619-624

Pellionisz, Andreas J., R. Llinas, D.H. Perkel, A computer model of the cerebellar cortex of the frog, Neuroscience, 1977, vol. 2, pp. 19-36

Reichert, H., C.H.F. Rowell, C. Griss, Course Correction Circuitry Translates Feature Detection into Behavioural Action in Locusts, Nature, vol. 351, 9 May 1985, pp. 142-144

Shadmehr, Reza, Gary D. Lindquist, A Neural Network for Pattern Generation in the Scratch Reflex, in Proceedings of the 1988 International Joint Conference on Neural Networks, pp. II:25-32

Stein, Barry E., H.P. Clamann, S.J. Goldberg, Superior Collicus: Control of Eye Movements in Neonatal Kittens, Science, vol. 210, 3 Oct. 1980, pp. 78-80

Stein, Paul S.G., Intrinsic Capabilities of Neural Networks in the Turtle Spinal Cord: Selection and Generation of Motor Patterns, in Proceedings of the International   Joint Conference on Neural Networks, San Diego, 1990, pp. II:669-674

Treffner, Ecological Connectionism and Animal-Environment Mutuality, 1987 International Joint Conference on Neural Networks, pp. II: 813-820


Neurophysiology

Aoki, Chiye, Philip Siekevitz, Plasticity in Brain Development, Scientific American, Dec. 1988, vol. 258, no. 12, pp. 34-42

Braitenberg, Valentino, Brains, Structural Similarities of, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 18-19

Bras, Helene, Paul Gogan, Suzanne Tyc-Dumont, The Mammalian Central Neurone is a Complex Computing Device, in Proceedings of the IEEE First International Conference on Neural Networks, San Diego, 1987, pp. IV: 123-126

Crick, Francis, Brain Physiology, in Parallel Distributed Processing, vol 2, Rumelhart & McClelland, Eds., MIT Press, Cambridge MA, 1987

Dawes, R.L., Biomasscomp: A Procedure for Mapping the Architecture of a Living Neural Network into a Machine, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. III: 215-225

Durbin, Richard, Nematode C. elegans, Nervous System, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 82-83

Gardner, Daniel, Synaptic Diversity Characterizes Biological Neural Nets, IEEE First International Conference on Neural Networks, San Diego, 1987, pp. IV: 17-22

Gottlieb, David I., GABAergic Neurons, Scientific American, vol. 258, no. 2, Feb. 1988

Jerison, Harry J., Brain Size, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 15-17

Kimelberg, Harold K., & Michael D. Norenberg, Astrocytes, Scientific American, April 1989, vol. 260, no. 4, pp. 66-76

Koopowitz, Harold, Brain, Primitive, Flatworms, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 13-14

Nauta, Walle J.H., Michael Feirtag, The Organization of the Brain, in The Brain, a Scientific American Book, 1979, W.H. Freeman and co., New York, pp. 40-53

Ridgway, Sam H., The Cetacean Central Nervous System, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 20-25

Stevens, John K., Reverse Engineering the Brain, BYTE, April 1985, pp 287-299

Stevens, Charles F., The Neuron, in The Brain, a Scientific American Book, 1979, W.H. Freeman and co., New York, pp. 14-25

Young, J.Z., Octopus Brain, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 97-99


Robotic Control - General

See also Vehicles

This is an area of research which is slowly emerging as an important field of study in neural networks. Most of the problems associated with robotic task planning and execution have been individually attacked using neural networks, but a central unifying vision is still lacking
(cf. Brooks, Minsky, Ozguner for attempts at decentralized distributed control).

Arbib, M.A., G.F. Franklin, N. Nilsson, Some Ideas on Information Processing in the Cerebellum, in Neural Networks: Proceedings of the School on Neural Networks, June 1967 in Ravello, E.R. Caianello, editor,    1968, Springer-Verlag Berlin, pp. 43-58

Blackburn M.R., and H.G. Nguyen, An Artificial Neural Network for Autonomous Undersea Vehicles, Naval Ocean Systems Center, San Diego CA, July 1988, Technical document 1318

Donnett, Jim, Tim Smithers, Neuronal Group Selection Theory, A Grounding in Robotics, Neural Information Processing Systems 2, David Touretzky ed., Morgan Kaufmann Publishers, 1990, pp. 308-315

Durrant-Whyte, Hugh. F., Integration, Coordination and Control of Multi-Sensor Robot Systems, Kluwer Academic Publishers, Boston, 1988

Fu, K. S., R.C. Gonzalez, C.S.G. Lee, Robotics: Control, Sensing, Vision, and Intelligence, McGraw Hill, 1987

Goldberg, Barak Pearlmutter, Using Back Propagation with Temporal Windows to Learn the Dynamics of the CMU Direct Drive Arm II, Neural Information Processing Systems 1, pp. 356-363

Graf, Lalonde, A Neural Controller for Collision Free Movement of General Robotic Manipulators, 1988 International Joint Conference on Neural Networks, pp. I: 7777777-84

Kung, Sun-Yuan, Jenq-Neng Hwang, Neural Network Architectures for Robotic Applications, IEEE Transactions on Robotics and Automation, vol. 5, no. 5, Oct. 1989, pp. 641-657

Kuperstein, Michael, Jorge Rubinstein, Implementation of an Adaptive Neural Controller for Sensory-Motor Coordination, IEEE Control Systems Magazine, April 1989, pp. 25-30

Lee, Sukhan, Rhee M. Kil, Robot Kinematic Control Based on Bidirectional Mapping Neural Network, in Proceedings of the International Joint Conference on Neural Networks, 1990, pp. III: 327-335

Niznic, Carol A., Wayne Hoss, Charles Watts, Modelling and Mathematical Formalism for Robotic Cerebellar Neural Network Pathway Information Measures, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. IV: 583-591

Ritter, Schulten, Using Kohonen's Net for Motor Control and Perception, 1988 International Joint Conference on Neural Networks, pp. I: 109-116


Robotic Control - Layered Control

Bellingham, James G., Thomas R. Consi, Robert M. Beaton, William Hall, Keeping Layered Control Simple, Proceedings of the IEEE Symposium on Autonomous Underwater Vehicle Technology, June 5 and 6, 1990, Washington D.C., pp. 3-8

Brooks, Rodney A.,      A Robust Layered Control System for a Mobile Robot, IEEE Journal of Robotics and Automation, vol. RA-2, no. 1, March 1986, pp. 14-23

McCulloch, Walter S., Logic and Closed Loops for a Computer Junket to Mars, in Neural Networks: Proceedings of the School on Neural Networks, June 1967 in Ravello, E.R. Caianello, editor,1968, Springer-Verlag Berlin, pp. 65-91

Nagata, Shigemi, Minoru Sekiguchi, Kazuo Asakawa, Mobile Robot Control by a Structured Hierarchical Neural Network, IEEE Control Systems Magazine, April 1990, pp. 69-76

Ozguner, U., Decentralized and Distributed Control Approaches and Algorithms, Proceedings of the 28th Conference on Decision and Control, Tampa Florida, Dec, 1989, pp. 1289-1294


Robotic Control - Manipulators

Gardner, Esther P., What the Robot's Hand Should Tell the Robot's Brain, in Proceedings of the 1988 International Joint Conference on Neural Networks, pp. II: 557-565

Grupen, Roderic A., Thomas C. Henderson & Ian D. McCammon, A Survey of General-Purpose Manipulation, International Journal of Robotics Research, Feb. 1989, vol. 8, no. 1, pp. 38-62

Iberall, Thea, A Ballpark Approach to Modelling Human Prehension, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. IV: 535-543

Jacobsen, C., E. Wood, F. Knutti, B. Biggers, The UTAH/MIT Dextrous Hand: Work in Progress, International Journal of Robotics Research, Winter 1984, vol. 3, no. 4, pp. 21-50

Tsutsumi, Kazuyoshi, Haruya Matsumoto, Neural Computation and Learning Strategy for Manipulator Position Control, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. IV: 525-534


Robotics - Vehicles

See also Robotic Control and Proprioceptive Sensing

The motivated behaviours of the systems inspired by Braitenberg's classic Vehicles are among the most sophisticated and robust ever achieved by artificial intelligence systems (cf. Brooks, 1986). For the most part still overlooked by the mainstream, this notion for intelligent control will probably be the most fruitful of all AI methodologies in the future.

Beer, Randall B., Hillel S. Chiel, and Leon S. Sterling, A Biological Perspective on Autonomous Agent Design, in P. Maes (Ed.) New Architectures for Autonomous Agents, MIT Press and Elsevier North Holland, 1990

Braitenberg, Valentino, Vehicles: Experiments in Synthetic Psychology, MIT Press, Cambridge, 1984

Brooks, Rodney A., A Robust Layered Control System for a Mobile Robot,    IEEE Journal of Robotics and Automation, vol. RA-2, no. 1, March 1986, pp. 14-23

Connell, Jonathon, The Omni Photovore, Omni Magazine, November 1988, pp. 201-212

Nagata, Shigemi, Minoru Sekiguchi, Kazuo Asakawa, Mobile Robot Control by a Structured Hierarchical Neural Network, IEEE Control Systems Magazine, April 1990, pp. 69-76

Reynolds, CraigDistributed Control for Intelligent Systems, in review for Neural Information Processing Systems vol. 3, Morgan Kaufmann, 1991

Reynolds, Craig W., Flocks, Herds, and Schools: A Distributed Behavioural Model, ACM Computer Graphics, vol. 21, no. 4, July 1987, pp. 25-34

Wilhelms, Jane, and Robert Skinner, A "Notion" for Interactive Behavioral Animation Control, IEEE Computer Graphics and Applications, May 1990, pp. 14-22


Self Organizing Feature Nets and Vector Quantization

Ahalt, Stanley C., Ashok K. Krishnamurthy, Prakoon Chen, Douglas E. Melton, Competitive Learning Algorithms for Vector Quantization, Neural Networks, vol. 3, no. 3, 1990, pp. 277-290

Baras, John S., Anthony La Vigna, Convergence of Kohonen's Learning Vector Quantization, in Proceedings of the International Joint Conference on Neural Networks, 1990, pp. III: 17-20

DeSieno, Duane, Adding a Conscience to Competitive Learning, 1988 International Joint Conference on Neural Networks, pp. I: 117-124

Kangas, Teuvo Kohonen, Laaksonen, Simula, Venta, Variants of Self Organizing Maps Using Minimal Spanning Trees, 1989 International Joint Conference on Neural Networks, pp. II: 517-522

Kohonen, Teuvo, K. Makisara, Representation of Sensory Information in Self-Organizing Feature Maps, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird UT, 1986, John S. Denker ed., pp. 271-276

Kohonen, Teuvo, A Neural Phonetic Typewriter, IEEE Computer Magazine, March 1988, vol. 21, no. 3, pp. 11-22

Kohonen, Teuvo, Improved Versions of Learning Vector Quantization, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I:545-550

Koikkalainen, Pasi, Erkki Oja, Self Organizing Hierarchical Feature Maps, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:279-284

Stojanovski, Jordan, Artificial Neural Network for Mapping, in Proceedings of the International Joint Conference on Neural Networks, Washington D.C., 1989

Tanaka, Takehisa, Motohiko Naka, Kunio Yoshida, Improved Back-Propagation Combined with LVQ, in Proceedings of the International Joint Conference on Neural Networks, Washington D.C., 1990, pp. I: 731-734

Xu, Lei, Erkki Oja, Adding Top-Down Expectation into the Learning Procedure of Self-Organizing Maps, in Proceedings of the International Joint Conference on Neural Networks, Washington D......C., 1990, pp. I: 735-738


Sensor Fusion

Eggers, Mitch, Tim Khuon, Neural Network Data Fusion Concepts and Application, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:7-16

Moravec, Hans, Sensor Fusion in Uncertainty Grids for Mobile Robots, in Annual Research Review of the Robotics Institute, Carnegie Mellon University, 1987, pp. 33-48

Rajapakse, Jagath, Raj Acharya, Multi Sensor Data Fusion within Hierarchical Neural Networks, International Joint Conference on Neural Networks, San Diego, 1990, pp. II:17-22


Signal Processing - Biological

de Boer, Egbert, Pattern Recognition of Spectral Information in Hearing, in Organization of Neural Networks: Structures and Models, W.      von Seelen ed., VCH Verlagsgesellschaft mbH, Weinheim, 1988, pp. 17-30, pp. 31-49

Elsner, Popov, Neuroethology of Acoustic Communication, in Advances in Insect Physiology, vol. 13, 1978, Academic Press, NY, pp. 299-355

Evans, E.F., Upper and Lower    Levels of the Auditory System: A Contrast of Structure and Function, in Neural Networks: Proceedings of the School on Neural Networks, June 1967 in Ravello, E.R. Ciaanello, editor, 1968, Springer-Verlag Berlin

Mead, Carver, The Artificial Cochlea, Proceedings of the International Joint Conference on Neural Networks

Schreiner, Christoph E., Merzenich, Michael M., Elements of Signal Coding in the Auditory Nervous System, in Organization of Neural Networks: Structures and Models, W. von Seelen ed., VCH Verlagsgesellschaft mbH, Weinheim, 1988, pp. 17-30

Shamma, Shihab A., Neural Networks for Speech Processing and Recognition, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. IV: 397-405

Travis, Bryan, A Layered Neural Network Applied to the Auditory System, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird, UT 1986, John S. Denker, ed., pp. 432-438

Travis, Bryan, Computational Model of Auditory Cortex, Proceedings   of the IEEE First International Conference on Neural Networks, San Diego, 1987, pp. IV:67-71


Signal Processing - Multi-Signal Separation

See also Sonar and Radar Signal Processing, and Sound Source Localization and Biological Signal Processing

The separation and processing of multiple signals is uncharted territory. Spatio-temporal signal processing with neural networks remains largely an unsolved problem, and therefore little progress
in the related subordinate fields has been made.








Eggers, Mitch, Tim Khuon, Neural Network Data Fusion Concepts and Application, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:7-16

Hassoun, Song, Shen, Spitzer, Self Organizing Auto-Associative Dynamic Multiple Layer Neural Network for the Decomposition of Repetitive Superimposed Signals, in Proceedings of the International Joint Conference on Neural Networks, Washington D.C., 1990, pp. I: 621-626

Jelonek, Thomas M., James P. Reilly, Maximum Likelihood Estimation for Direction of Arrival using a Nonlinear Optimizing Neural Network, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 253-258

Kassebaum, John, Manoel Fernando Tenorio, Christoph Scaefers, The Cocktail Party Problem, Neural Information Processing Systems 2, David Touretzky ed., Morgan Kaufmann Publishers, 1990, pp. 542-549

Kohonen, Teuvo, Kimmo Raivio, Olli Simula, Olli Venta, Jukka Henriksson, Combining Linear Equalization and Self-Organizing Adaptation in Dynamic Discrete-Signal Detection, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 223-228

Murano, Kazuo, Shigeyuki Unagami, Fumio Amano, Echo Cancellation and Applications, IEEE Communications Magazine, January 1990, pp. 49-55

Sung, Sinmo, Fredric M. Ham, Wesley Shelton, A New Robust Neural Network Method for Coherent Interference Rejection in Adaptive Array Systems, in Proceedings of the International Joint   Conference on Neural Networks, San Diego, 1990, pp. II:119-124

Wan, Kovacs, Rosen, Widrow, Development of Neural Net Interfaces for Direct Control of Neuroprosthesis, 1990 International Joint Conference on Neural Networks, pp. II: 3-21


Signal      Processing - Sonar and Radar

Most of these applications involve analysis of the spectral content of returned sonar or radar signals to characterize or identify targets. Almost all use back propagation or a variant thereof to learn certain exemplar patterns; almost all report good results but long training times. Note that few of these applications involve spatio-temporal signal processing. In most cases, sonar or radar returns are represented as static patterns which are presented to static neural  networks.

Ahalt, Garber, Jouny, Krishnamurtha, Performance of Synthetic Neural Net Classification of Noisy Radar Signals, Neural Information Processing Systems 1, pp. 281-288

Decatur, Application of Neural Networks to Radar Terrain Classification, 1989 International Joint Conference on Neural Networks, pp. I: 283-288

Farhat, Bai, Echo Inversion and Target Shape Estimation by Neuromorphic Processing, Neural Networks, pp. 117-126

Khotanzad, Lu, Srinath, Target Detection Using a Neural Network Based Passive Sonar System, 1989 International Joint Conference on Neural Networks, pp. I: 335-340

Kuczewski, Neural Network Approaches to Multi-Target Tracking, 1987 International Joint Conference on Neural Networks, pp. IV: 619-633

Orlando, Mann, Haykin, Radar Classification of Sea Ice Using Traditional and Neural Classifiers, 1990 International Joint Conference on Neural Networks, pp. II: 263-266

Ramani, Patrick, Hanson, Anderson, Fish Detection and Classification Using a Neural Network   Based Active Sonar System, 1990 International Joint Conference on Neural Networks, pp. II: 527-530

Roitblat, Moore, Nachtigall, Penner, Au, Dolphin Echolocation-Identification of Returning Echoes Using a Counter Propagation Network, 1989 International Joint Conference on Neural Networks, pp. I: 295-300

Roth, Neural Networks for Extraction of Weak Targets in High Clutter Environments, 1989 International Joint Conference on Neural Networks, pp. I: 275-282

Schiling Mastebroek, Zaegman, An Adaptive Heterodyne Filtering Procedure for the Imaging of Moving Objects, Neural Information Processing Systems, pp. 662-673

Vrckovnik, Chung, Carter, An Application of Neural Networks to Impulse Radar Waveforms for Asphalt Covered Bridge Decks, International Joint Conference on Neural Networks, San Diego, 1990, pp. II: 453-456

Wang, Wu, Ziemer, Application of Neural Networks to Pulse Doppler Radar Systems for Moving Target Indication, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II: 271-274

Winters, Jack H., Super-resolution for Ultrasonic Imaging in Air Using Neural Networks, 1988 International Joint Conference on Neural Networks, pp. I: 609-616


Signal Processing - Sound Source Localization

Much progress has been made in understanding the biological mechanisms for sound source localization. Rigorous studies by Konishi and Suga of the owl and the bat have formed the basis of almost all the data available. With the exception of Mead's silicon cochlea and auditory localization mechanisms, this detailed neurophysiological knowledge stands waiting for application, and is thus an important untapped resource.

Carr, Masakazu Konishi, Proceedings of the National Academy of Sciences, vol. 85, pp. 8311-8315

Knudsen, Eric I., Masakazu Konishi, A Neural Map of Auditory Space in the Owl, Science, vol. 200, May 19, 1978, pp. 795-797

Kuwada, Shigeyuki, Tom C.T. Yin, Robert E. Wickesberg, Response of Cat Inferior Collicus Neurons to Binaural Beat Stimuli: Possible Mechanisms for Sound Localization, Science, vol 206, Nov. 2, 1979, pp. 586-588

Lazzaro, John, Carver Mead, A Silicon Model of Auditory Localization, Neural Computation, David Touretzky ed., Morgan Kaufmann Publishers, 1989, vol. 1, no. 1, pp. 47-57

Manley, Geoffrey A., Christine Koeppl, Masakazu. Konishi, A Map of Interaural Intensity Differences in the Brainstem of the Barn Owl, Journal of Neuroscience, Aug. 1988, vol. 8, no. 8, pp. 2665-2676

Simmons, J.A........, Acoustic Imaging Computations by Bats: Unification of Diversely Represented Stimulus Features into Whole Images, Neural Information Processing Systems 2, D. Touretzky, ed, Morgan Kaufmann Publishers, 1990, pp. 2-9

Simmons, James A., Lynda Chen, The Acoustic Basis for Target Discrimination by FM Echolocating Bats, Journal of the Acoustic Society of America, vol. 86, no. 4, Oct. 1989, pp. 1333-1350

Simmons, James A., Donna Howell, Nobuo Suga, Information Content of Bat Sonar Echoes, American Scientist, vol. 63, no. 2, Mar.-Apr. 1975, pp. 204-215

Simmons, J.A., E.G. Freedman, S.B. Stevenson, L. Chen, T.J. Wohlgenant, Clutter Interference and the Integration Time of Echoes in the Echolocating Bat, Eptesicus Fuscus, Journal of the Acoustic Society of America, vol. 86, no. 4, Oct. 1989, pp. 1318-1332

Spence, C.D., J.C. Pearson, Computation of Sound Source Elevation in the Barn Owl, Neural Information Processing Systems 2, D. Touretzky, ed, Morgan Kaufmann Publishers, 1990, pp. 10-17












Spence, C.D., J.C. Pearson, Gelfland, Peterson, Neuronal Maps for Sensory Motor Control in the Barn Owl, Neural Information Processing Systems 1, David Touretzky ed., Morgan Kaufmann Publishers, 1989, pp. 366-374

Suga, Nobuo, Cortical Computational Maps for Auditory Imaging, Neural Networks, 1990, vol. 3, no. 1, pp. 3-21

Suga, Nobuo, Biosonar and Neural Computation in Bats, Scientific American, June 1990, vol. 262, no. 6, pp. 60-68

Sugie, Noboru, Jie Huang, Noboru Ohnishi, Localizing Sound    Source by Incorporating a Biological Auditory Mechanism, 1988 International Joint Conference on Neural Networks, pp. II: 243-250

Sussman, Harvey M., Neural Coding of Relational Invariance in Speech - Human Language Analogues to the Barn Owl, Psychological Review, 1989, vol. 96, no. 4, pp. 631-642

Wagner, Takahashi, Konishi, Journal of Neuroscience, 1987, vol. 7, p. 3114


Signal Processing - SpatioTemporal

Despite the large number of references listed for this section, spatio-temporal signal processing by neural networks remains one of the most important unsolved problems. The major players in this arena are the proponents of recurrent back propagation methods (cf. Pearlmutter, 1989), Fukushima's latest versions of the NeoCognitron, Kohonen's Self Organizing Feature Nets, and Waibel's Time Delay Neural Networks (TDNN).

Of these methods, the NeoCognitroarpenter and Grossberg's Adaptive Resonance Theory has yet to prove itself for this application.


Of these methods, the NeoCognitron and TDNN show the most promise for robust performance. Sharing many similarities, the principle feature of these networks is progressive hierarchical feature extraction.

Beroule, Dominique, Guided Propagation Inside a Topographic Memory, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. IV: 469-476

Dayhoff, Judith E., Regularity Properties in Pulse Transmission Networks, in Proceedings of the International Joint Conference on Neural Networks,   San Diego, 1990, pp. III: 621-626

Gluck, Parker, Reifsnider, Learning with Temporal Derivatives in Pulse Coded Neural Systems, Neural Information Processing Systems 1, pp. 195-203

Lippmann, Richard P., Beckman, Adaptive Neural Net Preprocessing for Signal Detection in Non-Gaussian Noise, Neural Information Processing Systems 1, pp. 124-132

Luria, A model of speech generation and perception, 1977

Neumann, Wheeler, Burnside, Bernstein, Hall, A Technique for the Classification and Analysis of    Insect Courtship Song, 1990 International Joint Conference on Neural Networks, pp. II: 257-262

Ogmen, Haluk, Simon Gagne, Early Spatio-Temporal Integration by Gated Competitive Networks, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. II:805-811

Paris, Orsark, Varanasai, Aazhang, Neural Net Receivers in Multiple Access Communications, Neural Information Processing Systems 1, pp. 272-280

Pearlmutter, Barak, Learning State Space Trajectories in Recurrent Neural Networks, 1989 International Joint Conference on Neural Networks, pp. II: 365-372

Szu, Scheff, Simulated Annealing Feature Extraction from Occluded and Cluttered Objects, 1990 International Joint Conference on Neural Networks, pp. II: 76-79

Szu, Foo, Space Scanning Curves for Spatio Temporal Representations Useful for Large Scale Neural Network Computing, 1990 International Joint Conference on Neural Networks, pp. II: 703-705

Uchiyama, Shimohara, Tokunaga, A Modified Leaky Integrator Network for Temporal Pattern Processing, 1989 International Joint Conference on Neural Networks, pp. I: 469-475

van den Bout, Miller, TinnMann (incl. code), in Proceedings of the 1989 International Joint Conference on Neural Networks,   pp. II: 205-211

Wan, Eric A., Temporal Backpropagation for FIR Neural Networks, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 575-580

Watson, Mark, A Neural Network Model for Phoneme Recognition







Using the Generalized Delta Rule for Connection Strength Modification (incl. code), in Proceedings of the IEEE First International Conference on Neural Networks, San Diego, 1987, pp. IV: 389-396


Tensor Network Theory

Georgopoulos, Apostolos P., Ronald E. Kettner, Andrew B. Schwartz, Primate Motor Cortex and Free Arm Movements to Visual Targets in Three-Dimensional Space. II. Coding of the Direction of Movement by a Neuronal Population, Journal of Neuroscience, vol. 8, no. 8, Aug. 1988, pp.  2929-2937

Georgopoulos, Apostolos P., Joseph T. Lurito, Michael Petrides, Andrew B. Schwartz, Joe T. Massey, Mental Rotation of the Neuronal Population Vector, Science, vol. 243, Jan. 13, 1989, pp. 234-236

Kettner, Ronald E., Andrew B. Schwartz, Apostolos P. Georgopoulos, Primate Motor Cortex and Free Arm Movements to Visual Targets in Three-Dimensional Space. III. Positional Gradients and Population Coding of Movement Direction from Various Movement Origins, Journal of Neuroscience, vol. 8, no. 8, Aug. 1988, pp. 2938-2947

Pellionisz, Andras J., Tensor Network Theory and its Application to Computer Modeling of the Meta-organization of Sensorimotor Hierarchies of Gaze, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird UT, 1986, John S. Denker ed., pp. 339-345

Pellionisz, Andras J., Sensorimotor Operations: a Ground for the Co-Evolution of Brain Theory with Neurobotics and Neurocomputers, in Proceedings of the First IEEE International Conference on Neural Networks, San Diego, 1987, pp. IV: 593-600

Pellionisz, Andras J., Intelligent Decisions and Dynamic Coordination Properties of Geometrical Representation by Generalized Frames Intrinsic to Neural and Robotic Systems, in Proceedings of the 1988 International Joint Conference on Neural Networks, pp. II: 603-610

Pellionisz, Andras J., Tensorial Aspects of the Multidimensional Massively Parallel Sensorimotor Function of Neuronal Networks, Progress in Brain Research, vol. 76, O. Pompeiano and J.H.J. Allum ((((((eds.), 1988, Elsevier Science Publishers B.V. (Biomedical Division), pp. 341-354

Pellionisz, Andras J., Neural Geometry: Towards a Fractal Model of Neurons, in Models of Brain Function, R.M. Cotterill (ed.), 1989, Cambridge University Press















Pellionisz, Andras J., Neural Geometry: The Need of Researching Association of Covariant and Contravariant Coordinates that Organizes a Cognitive Space by Relating Multisensory-Multimotor Representation, in Proceedings of the International Joint Conference on Neural Networks, Washington D.C., 1989

Pellionisz, Andras J., Tensor Network Model of the Cerebellum and Olivary System Quantitatively Elaborated for the Optokinetic Reflex, in Experimental Brain Research Series 17, 1989, Springer-Verlag Berlin Heidelberg, pp.400-424

Schwartz, Andrew B., Ronald E. Kettner, Apostolos P. Georgopoulos, Primate Motor Cortex and Free Arm Movements to Visual Targets in Three-Dimensional Space. I. Relationships Between Single Cell Discharge and Direction of Movement, Journal of Neuroscience, vol. 8, no. 8, Aug. 1988, pp. 2913-2927


Time Delay Neural Networks

Hampshire, John B., Alex Waibel, Connectionist Architecture for Multi-Speaker Phoneme Recognition, Neural Information Processing Systems 2, David Touretzky ed., Morgan Kaufmann Publishers, 1990, pp. 203-210

Hirai, Akihiro, Alexander Waibel, Phoneme-based Word Recognition by Neural Network: A Step Toward Large Vocabulary Recognition, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. III: 671-676

Lang, Kevin J., Alex Waibel, Geoffrey Hinton, A Time Delay Neural Network for Isolated Word Recognition, Neural Networks, vol. 3, no. 1, pp. 23-44

Sawai, Hidefumi, Alex Waibel, Haffner, Miyatake, Kiyohiro Shikano, Parallelism, Hierarchy, and Scaling in Time Delay Neural Nets for Spotting Japanese Phonemes/CV Syllables, 1989 International Joint Conference on Neural Networks, pp. II: 81-88

Waibel, Alexander, Toshiyuki Hanazawa, Geoffrey Hinton,, Kiyohiro Shikano, Kevin J. Lang, Phoneme Recognition Using Time-Delay Neural Networks, IEEE Transactions on Acoustics, Speech, and Signal Processing, vol.37, no. 3, March 1989, pp. 328-339


Vision - General

Of all the components of the nervous system, the visual system is perhaps most well studied. Starting with the seminal work of Hubel and Wiesel on orientation sensitive cells in the visual cortex, understanding of the visual system has progressed rapidly. Though not yet widespread,
the most successful computer vision systems to date are those which make use of the data collected by neurophysiologists.

Asogawa, Minoru, Adaptive Input Field Neural Network that can Recognize Rotated and/or Shifted Characters, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 407-421

Dhawan, Atam P., Thomas Dufresne, Low-Level Image Processing and Edge Enhancement Using A Self Organizing Neural Network, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 503-510

Hirai, Yuzo, Yasuyuki Tsukui, Position Independent Neuro Pattern Matching and its Application to Handwritten Numerical Character Recognition, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 407-421

Hutchinson, James A., Christof Koch, Simple Analog and Hybrid Networks for Surface Interpolation, in AIP Conference Proceedings 151: Neural Networks for Computing, Snowbird UT, 1986, John S.   Denker ed., pp. 235-240

Kanizsa, Gaetano, Subjective Contours, in The Mind's Eye: Readings from Scientific American, J.M. Wolfe (ed.), New York, W.H. Freeman & Co., 1986, pp. 82-86

Lehar, Steve M., Andrew J. Worth, David N. Kennedy, Application of the Boundary Contour System/Feature Contour System to Magnetic Resonance Brain Scan Imagery, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I:435-440

MacKay, David J.C., Analysis of Linsker's Application of Hebbian Rules to Linear Networks, submitted to Network; an abbreviated version appears in Neural Information Processing Systems 2, Morgan Kaufmann Publishers

Mallot, Hanspeter A., Werner von Seelen, Fotios Giannakopoulos, Neural Mapping and Space-Variant Image Processing, Neural Networks, vol. 3, no. 3, 1990, pp. 245-263

Menon, Murali M., William Wells III, Massively Parallel Image Restoration, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I:::::: 511-516

Meuller, P., P. Spiro, D. Blackman, R.E. Furman, Neural Computation of Visual Images, in Proceedings of the IEEE First International Conference on Neural Networks, San Diego, 1987, pp. IV: 75-88

Silverman, Ronald H., Andrew S. Noetzel, Image Processing and Pattern Recognition in Ultrasonograms by Backpropagation, in Neural Networks, vol. 3, no. 5, 1990, pp. 593-604

Usui, Shiro, Shigeki Nakauchi, Masae Nakano, Reconstruction of Munsell Color-Space by a Five Layered Neural Network, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. II:515-520

Wolfe, Jeremy M. (editor), The Mind's Eye, Readings from Scientific American, New York, W.H. Freeman & Co., 1986

York, Bryant W., Mary K. Atkins,    Some Performance Results for a Connection Machine Implementation of the Boundary Contour System, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 351-358


Vision - Image Compression

Work is progressing quietly on the image compression front. Compression ratios on the order of 60-75% are regularly achieved, although quality varies. As in spatio-temporal signal processing, the biggest progress seems to come from those networks which implement progressive hierarchical
feature extraction.

Daugman, John G., Relaxation Neural Network for Non-Orthogonal Image Transforms, Proceedings of the 1988 International Joint Conference on Neural Networks, pp. I: 547-560

Kanerva, Pentti Contour Map Encoding of Shape for Early Vision, Neural Information Processing Systems 2, David Touretzky, ed., Morgan Kaufmann Publishers, 1990, pp. 282-289

Manikopoulos, C., G. Antoniou, S. Metzelopoulou, LVQ of Image Sequence Source and ANS Classification of      Finite State Machine for High Compression Coding, in Proceedings of the International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 481-486

Naillon, Theeten, Neural Approach to TV Image Compression using a Hopfield Type Network, Neural Information Processing Systems 1, pp. 264-271

Okamoto, Toshiaki, Mitsuo Kawato, Toshio Inui, Sei Miyake, Model Based Image Compression, Neural Information Processing Systems 2, David Touretzky ed., Morgan Kaufmann Publishers, 1990, pp. 298-305












Vision - Invertebrate
---------------------

Arnett, D.W., Receptive Field Organization of Units in the First Optic Ganglion of Diptera, Science, vol. 173, pp. 929-931

Barrington, E.J.W., Invertebrate Structure and Function, Thomas Nelson and Sons, Don Mills, Ont., 1966666669, (Photoreception, pp. 280-290)

Bouzerdoum, Abdesselam, Robert B. Pinter, A Shunting Inhibitory Motion Detector that Can Account for the Functional Characteristics of Fly Motion Sensitive Interneurons, in International Joint Conference on Neural Networks, San Diego, 1990, pp. I: 149-153

Braitenberg, Valentino, On Chiasms, in Neural Networks: Proceedings of the School on Neural Networks, June 1967 in Ravello, E.R. Ciaanello, editor, 1968, Springer-Verlag Berlin, pp. 34-42

Brodie, Scott E., Bruce W. Knight, & Floyd Ratliff, The response of the Limulus retina to moving stimuli: a prediction by Fourier analysis, Journal of General Physiology, 1978, vol. 72, pp. 129-166

Collet, T., A.J. King, Vision During Flight, in G.A. Horridge (ed.), The   Compound Eye and Vision of Insects, 1975, Claredon Press, Oxford, pp. 437-466

Horridge, G. Adrian, The Compound Eye of Insects, in The Mind's Eye: Readings from Scientific American, J.M. Wolfe (ed.), New York, W.H. Freeman & Co., 1986, pp. 24-35

Horridge, G. Adrian, I.A. Meinertzhagen, The Accuracy of the Patterns of Connexions of the First- and Second-Order Neurons of the Visual System of Calliphora, Proceedings of the Royal Society of London, Biological Sciences, vol. 175, 1970, pp. 69-82

Horridge, G. Adrian, B. Walcott, A.C. Ioannides, The Tiered Retina of Dytiscus: a New Type of Compound Eye, Proceedings of the Royal Society of London, Biological Sciences, vol. 175, 1970, pp. 83-94

Kien, J., Motion Detection in Locusts and Grasshoppers, in G.A. Horridge (ed.), The Compound Eye and Vision of Insects, 1975, Claredon Press, Oxford, pp. 410-422

Kirschfeld, Kuno, Fly, Visual System, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, pp. 42-43

Kruppel, Thomas, Michael Gewecke, Visually Induced Flight Manoeuvres in the Tethered Locust (Schistocerca Gregaria), in Insect Locomotion, Michael Gewecke and Gernot Wendler (eds.), Verlag Paul Parey, 1985, pp. 167-174

Macagno, Eduardo R., Ian A. Meinertzhagen, Visual System Development, Invertebrates, in Comparative Neuroscience and Neurobiology: Readings from the Encyclopedia of Neuroscience, Louis N. Irwin (ed.), 1988, Birkhauser, Boston, p. 129-132

Mazokhin-Porshnyakov, Georgii A., Insect Vision, 1969, Plenum Press, New York

Mimura, K., Units of the Optic Lobe, Especially Movement Perceptions Units of Diptera, in G.A. Horridge (ed.), The Compound Eye and Vision of Insects, 19999999999999975, Claredon Press, Oxford, pp. 423-436

Northrop, R.B., Information Processing in the Insect Compound Eye, in G.A. Horridge (ed.), The Compound Eye and Vision of Insects, 1975, Claredon Press, Oxford, pp. 378-409

Ogmen, H., S. Gagne, Neural Network Architectures for Motion Perception and Elementary Motion Detection in the Fly Visual System, in Neural Networks, vol. 3, no. 5, pp. 487-505, 1990

Poggio, Tomaso, Werner Reichardt, Visual Control of Orientation Behaviour in the Fly, Part II: Towards the Underlying Neural Interactions, Quarterly Review of Biophysics, vol. 9, no. 3, 1976, pp. 377-438

Reichardt, Werner, Tomaso Poggio, Visual Control of Orientation Behaviour in the Fly, Part I: A Quantitative Analysis, Quarterly Review of Biophysics, vol. 9, no. 3, 1976, pp. 311-375


Vision - Motion Perception



Courellis, S.H., V.Z. Marmarelis, An Artificial Neural Network
for Motion Detection and Speed Estimation, in Proceedings of the International
Joint Conference on Neural Networks, San Diego, 1990, pp. I: 407-421



Hutchinson, James A., Christof Koch, Jin Luo, Carver Mead, Computing
Motion Using Analog and Binary Resistive Networks, IEEE Computer Magazine,
vol. 21, no. 3, pp. 52-63



Tang, D.S., Neurocomputation of Image Motion, in Proceedings
of the International Joint Conference on Neural Networks, San Diego,
1990, pp. I: 401-406



Zhou, Y.T., R. Chellappa, A Network for Motion Perception, in
Proceedings of the International Joint Conference on Neural Networks,
San Diego, 1990, pp. II:875-884







Vision - Toads and Frogs



Betts, Bill, The Toad Optic Tectum as a Recurrent On-Center Off-Surround
Neural Net with Quenching Threshold, in Proceedings of the 1988 International
Joint Conference on Neural Networks, pp. II: 47-54



Gaze, R.M., M.J. Keating, G. Szekely, Lynda Beazley, Binocular
Interaction in the Formation of Specific Intertectal Neuronal Connexions,
Proceedings of the Royal Society of London, Biological Sciences, vol.
175, 1970, pp. 104-147



Katz, Lawrence C., Martha Constantine-Paton, Relationships Between
Segregated Afferents and Postsynaptic Neurons in the Optic Tectum
of Three-Eyed Frogs, Journal of Neuroscience, vol. 8, no. 9, September
1988, pp. 3160-3180



Lettvin, J.Y., H.R. Maturana, W.S. McCulloch, & W.H. Pitts, What
the Frog's Eye Tells the Frog's Brain, Proceedings of the IRE, vol
47, no. 11, November 1959, pp. 1940-1959



Wang, Deliang, Michael A. Arbib, Mechanisms of Pattern Discrimination
in the Toad's Visual System, in Proceedings of the International Joint
Conference on Neural Networks, San Diego, 1990, pp. II:477-482






Vision - Vertebrate



Ahumada, Albert J. Jr, Simulated Annealing in Networks for Computing
Possible Arrangements for Red and Green Cones, in Proceedings ceedings of the
IEEE First International Conference on Neural Networks, San Diego,
1987, pp. IV: 107-114



Bienenstock, Elie L., Leon N. Cooper, & Paul W. Munro, Theory
for the development of neuron selectivity: orientation specificity
and binocular interaction in the visual cortex, Journal of Neuroscience,
1982, vol. 2, pp. 32-48



Bruce, Vicki, Patrick R. Green, Visual Perception: Physiology,
Psychology, and Ecology, Lawrence Erlbaum Associates, Hillsdale NJ,
1985



Grossberg, Stephen, Cortical Dynamics of Three-Dimensional Form,
Color, and Brightness Perception, I: Monocular Theory, Perception
and Psychophysics, 1987, vol. 41, no. 2, pp. 87-116



Grossberg, Stephen, Cortical Dynamics of Three-Dimensional Form,
Color, and Brightness Perception, II: Binocular Theory, Perception
and Psychophysics, 1987, vol. 41, no. 2, pp. 117-158



Grossberg, Stephen, Ennio Mingolla, Computer Simulation of Neural
Networks for Perceptual Psychology, Behavior Research Methods, Instruments,
and Computers, 1986, vol. 18, no. 6, pp. 601-607



Grossberg, Stephen, Dejan Todorovic, Neural Dynamics of 1-D and
2-D Brightness Perception: A Unified Model of Classical and Recent
Phenomena, in Neural Networks and Natural Intelligence, Stephen Grossberg,
editor, MIT Press, Cambridge MA, 1988, pp. 127-194



Hubel David H., Torsten N. Wiesel, Receptive fields, binocular
interaction and functional architecture in the cat's visual cortex,
Journal of Physiology (London), 1962, vol 160, pp. 106-154



Hubel David H., Torsten N. Wiesel, Brain Mechanisms of Vision,
in The Brain, a Scientific American Book, 1979, W.H. Freeman and co.,
New York, pp. 84-96



Loebner, Egon E., Concurrency Assurance in Vertebrate Retinas,
in Proceedings of the First IEEE International Conference on Neural
Networks, San Diego, 1987, pp. IV: 147-159



Poggio, Gian F., Francisco Gonzalez, Friedemann Krause, Stereoscopic
Mechanisms in Monkey Visual Cortex: Binocular Correlation and Disparity
Selectivity, Journal of Neuroscience, Dec. 1988, vol. 8, no. 12, pp.
4531-4550



Schiller, Peter H., Sean D. True, Janet L. Conway, Effects of
Frontal Eye Field and Superior Collicus Ablations on Eye Movements,
Science, vol 206, Nov. 2 1979, pp. 590-592



Schrodinger, E., On the Trichromatic and Opponent-Process Theories,
translated by Keith K. Niall, Spatial Vision, vol. 3, no. 2, 1988,
pp. 79-95



Seelen, W. v., H.A. Mallot, F. Giannakopoulos, E. Schulze, Properties
of Cortical Systems - A Basis for Computer Vision, in Proceedings
of the IEEE First International Conference on Neural Networks, San
Diego, 1987, pp. IV: 89-96



von der Marlsburg, Christoph, Self Organization of Orientation
Sensitive Cells in the Striate Cortex, Kybernetik, vol 14, pp. 85-100



Wiesel Torsten N., & David H. Hubel, Spatial and Chromatic interactions
in the lateral geniculate body of the rhesus monkey, Journal of Neurophysiology
, 1966, vol. 29, pp. 1115-1156




Neural VLSI

Card, H.C., W.R. Moore, Silicon Models of Associative Learning in Aplysia, Neural Networks, vo, vol. 3, no. 3, 1990, pp. 333-346

Culhane, Andrew D., Martin C. Peckerar, A Neural Net Approach to Discrete Hartley and Fourier Transforms, IEEE Transactions on Circuits and Systems, vol. 36, no. 5, May 1989, pp. 695-703

Koch, Christoph, Wyeth Bair, John G. Harris, Timothy Horiuchi, Andrew Hsu, Jin Luo, Real Time Computer Vision and Robotics Using Analog VLSI Circuits, Neural Information Processing Systems 2, David Touretzky ed., Morgan Kaufmann Publishers, 1990, pp. 750-757

Lazzaro, John, Carver Mead, A Silicon Model of Auditory Localization, Neural Computation, David Touretzky ed., Morgan Kaufmann Publishers, 1989, vol. 1, no. 1, pp. 47-57

Maher, Mary Ann C., Stephen P. Deweerth, Mish A. Mahowald, Carver A. Mead, Implementing Neural Architectures Using Analog VLSI Circuits, IEEE Transactions on Circuits and Systems, vol. 36, no. 5, May 1989, pp. 643-652

Mead, Carver, The Artificial Cochlea, Proceedings of the International Joint Conference on Neural Networks...

Mead, Carver A., Silicon Models of Neural Computation, in Proceedings of the IEEE First International Conference on Neural Networks 1987, vol 1

Mead, Carver A., Analog VLSI and Neural Systems, Addison Wesley, 1989

van den Bout, David E., Thomas K. Miller III, A Digital Architecture Employing Stochasticism for the Simulation of Hopfield Neural Nets, IEEE Transactions on Circuits and Systems, vol. 36, no. 5, May 1989, pp. 732-738




When somebody's giving out data, take as much as you can.
	- Bernard Widrow in Plenary Talk at IJCNN 87<F46>




Japan Neural Network Society contact:

Hideki Kawahara,
NTT Basic Research Laboratories
3-9-11 Midori-cho, Musashino, Tokyo 180, Japan
tel: 81 422 59 2276, fax: 81 422 3393
kawahara@nttlab.nt.ntb.ntb.ntb.ntb.ntb.ntb.ntt.jp   (kawahara@av-convex.ntt.jp)


s and Natural Intelligence, Stephen Grossberg,
editor, MIT Press, Cambridge MA, 1988


Reference List - Neural Networks

Compiled by Nick Porcino, 1990


General References - Computers

Bernstein, Philip A., Sequoia: A Fault-Tolerant Tightly Coupled Multiprocessor for Transaction Processing, IEEE Computer Magazine, vol. 21, no. vol. 21,


APPENDIX A





Beware jargon: it can hide ignorance, and carries little knowledge.
- Frank Herbert



a priori - the mind, prior to, and independent of, sensory experience.

ACE - see Adaptive Critical Element

 action potential - The all or nothing electrical impulse generated by a neuron when the soma's internal potential exceeds a certain threshold. see axon, soma

PICTURE FRAME

 Adaline - ADAptive LINear Element. 6.6. A processing element, often implemented in hardware, which learns using the gradient descent algorithm. Its descendants find common application today in the communications industry (Widrow and Winters, 1988). see gradient descent, memistor

 adaptation - 1. the decline in responsiveness of sensory cells. 2. learning. see habituation

 Adaptive Critical Element (ACE) - 6.9. A complex neuron-like element which oversees the operation of an Adaptive Search Element (ASE), and gives the ASE reinforcement feedback based on a prediction of performance (Barto, Sutton, & Anderson, 1983). Based on the principles of stochastic dynamic programming and optimal linear predictors. see Adaptive Search Element

 Adaptive Resonance Theory - 7.6. Adaptive resonance describes a situation in which an expected pattern and a perceived pattern reinforce each other through a feedback process. The system adjusts its expectancy and the sensory data to bring them more in line with each other (Grossberg 1980). Adaptive Resonance Theory (ART) has been extensively developed by Stephen Grossberg and Gail Carpenter. see gated dipole

PICTURE FRAME

 Adaptive Search Element (ASE) - 6.9. A complex neuron-like element which makes decisions based on the memories it has stored. It learns through the process of operant conditioning (Barto, Sutton, & Anderson, 1983). see Adaptive Critical Element, operant conditioning

PICTURE FRAME

 afferent pathways - lead to the cortex from the senses.  see efferent

 amacrine cells - 1.1. neurons possessing no axon. They have a graded response - analog rather than digital like most neurons. Amacrine cells are very common in the retina.

PICTURE FRAME

 aminergic neuron - 1.1. A neuron using amine as a neurotransmitter. see astrocyte, cholinergic neuron, GABAergic neuron

 amygdala - 1.1. A component of the limbic system. When stimulated it can provoke anger and aggressive responses. see limbic system

 apical dendrite - 1.1. Dendrites extending upwards from the upper aspect of the neuron towards the outer surface of the brain. see basal dendrite

 Aplysia - the Sea Slug. 9.2. A sea creature about the size of a fist. Its nervous system has been extensively studied and characterized because of its simplicity and accessibility. see Limulus

PICTURE FRAME

 ASE - see Adaptive Search Element

 associative memory - see CAM

 astrocyte - 1.1. Star shaped glial cells which form scaffolding for brain growth during ontogenesis, and later are involved in neurotransmitter uptake and metabolism. see glial cells

PICTURE FRAME

 axon - 1.1. Attached to the soma of the neuron, the axon is the electrically active nerve process which generally acts as the final output of the neuron. The axon fires an all-or-nothing (or digital) pulse after the electrical potential within the soma reaches a certain threshold. The pulse is called an action potential. see action potential, Amacrine cells, dendrite, synapse

 back propagation or back error propagation - 7.3. A method of training multilayer Perceptrons using recursive gradient descent. The process involves calculating the difference between expected output and actual output, and using that value as an error which is propagated back to all the processing units in the network. The individual units adjust their weights based on this error value to reduce the total error (cf. Rumelhart and McClelland, 1986). see gradient descent, Lyapunov function, weight

 basal dendrite - 1.1. Dendrites extending from the lower aspect of the neuron parallel to the brain surface, and downwards towards the white matter. see apical dendrite

 Boltzmann machine - 7.4. a neural network that learns using the technique of simulated annealing. (Ackley, Hinton, & Sejnowski, 1985) see simulated annealing

 Broca's Area - an area of the brain concerned with the XXX of speech. see Wernicke's Area

PICTURE FRAME

 CAM - 7.2. Content Addressable Memory is a memory system which will respond with a complete pattern when stimulated by a pattern or part of a pattern.

 caudal - in the tail.

 cerebellum - 1.2. A part of the central nervous system associated with motor control, apparently finessing the commands coming down from the motor cortex. It has a very regular structure, with only five major types of neurons: Purkinje, basket, Golgi. see climbing fibres, mossy fibres

PICTURE FRAME

 chaos - 6.5. Complexity hides in simplicity and simplicity hides in complexity. A small system of nonlinear equations can lead to chaotic, random behaviour, yet the behaviour is ordered, governed by attractors in state space.

 cholinergic neuron - 1.1. A neuron using acetylcholine as a neurotransmitter. see aminergic neuron, astrocyte, GABAergic neuron

 cingulate gyrus - part of the limbic system. see limbic system

 classical conditioning - see operant conditioning

 climbing fibres - are an excitatory input carrying somatosensory information to the cerebellum. They originate mainly in the inferior olive. Mossy fibres are the other source of input to the cerebellum. see cerebellum, mossy fibres

CMAC - Cerebellar Model of Arithmetic Memory

 cochlea - 3.1. A coiled resonant structure within the ear. Sensory hair cells on the basilar membrane of the cochlea detect sounds of different frequencies, and thus perform the first step of hearing. Associated with the cochlea is the vestibular mechanism. See vestibular mechanism

PICTURE FRAME

command fibre or neuron - 9.1. A neuron or axon which can be shown to be necessary and sufficient to elicit a given motor response.  Definition due to Kupfermann & Weiss (1978).

 competitive learning - Unsupervised learning where the various processing elements in a network compete to respond most strongly to a particular stimulus, and subsequently learn to respond to particular stimuli.

 connectionism - A computer science term describing systems where the pattern of connectivity of the individual processing units is the most important aspect of a network's computation.

 connectivity - Describes the manner in which processing elements are connected to one another, be it complete connectivity where every cell is connected to every other, or local connectivity where cells communicate only with their neighbours.

 corpus callosum - 1.2. The bundle of nerve fibres connecting the right and left hemispheres of the brain. It connects the two more or less symmetrically: each area on one side of the brain is connected to the corresponding area on the other.

PICTURE FRAME

 dendrites - 1.1. Electrically passive nerve processes which receive signals from other neurons via the synapses. see axon, neuron synapse

 deterministic process - A process where the action to take in any state is defined unambiguously. see stochastic process

 distributed representation - every cell is involved in representing a given concept; a concept is represented as a pattern of activity across all the cells. Lashley called distributed representations engrams. Because the information is spread across many cells, little information is lost if a few cells becomes inoperative. For this reason, the performance of a distributed network degrades gradually as individual processing elements fail. There is a possibility of confusion, since every pattern interacts with every other, possibly causing crosstalk or distortion. see local representation

 dorsal - means upper

 efferent pathways - go from the cortex to the muscles and other parts of the body. see afferent

 emergent properties - Arise as a function of network design, resulting from aggregate behaviour, and are therefore not inherent to any individual processing unit. see intrinsic properties

 engram - see distributed representation

 evoked potential - a change in electrical potential within the soma of a neuron caused, or evoked, by a stimulus. see action potential

 excitatory synapse - an input which predisposes a neuron to fire, in other words, exciting the neuron. see inhibitory synapse, weight

 forebrain - see midbrain, hindbrain

PICTURE FRAME

 fovea - The central area of the vertebrate retina, where detail vision takes place. see saccade

 fractal - an object which displays the property of self-similarity is said to be fractal. The closer you look, the more a fractal stays the same. Fractal is short for fractional dimension. The fractal (or Hausdorff) dimension of the brain is approximately 2.5.

 GABAergic neuron - a neuron principally using gamma-aminobutyric acid (GABA) as an inhibitory neurotransmitter. see aminergic neuron, astrocyte, cholinergic neuron

 gated dipole - see Adaptive Resonance Theory

PICTURE FRAME

 glial cell - see astrocyte, interneuron

 Golgi cell -

 gradient descent - A method of solving a problem by causing the system space to evolve down into the bottoms of the valleys of an energy surface. see Adaline, back propagation, Boltzmann
machine, simulated annealing, weight

 grandmother cell - a cell that embodies a single concept: if this cell is active, the concept is extant in the system, if the cell is inactive, the concept isn't extant. see local representation

 grey matter - The portion of the nervous system principally composed of cell bodies. Processing takes place here. Communications between various areas of grey matter are taken care of by the white matter.  Half the thickness of cortex is grey matter. see white matter

PICTURE FRAME

 habituation - learned conditioning to a stimulus. If a reflex habituates to repeated stimuli, the reaction to that particular stimuli becomes less and less. It is interesting to note that habituation and fatigue are a type of memory. see adaptation 1

 Hebbian learning - Learning methods which owe their basis to Donald Hebb's famous postulate:
 “When an axon of cell A is near enough to excite a cell B, and repeatedly or persistently takes part in firing it, some growth process or metabolic change takes place in one or both cells, such that A's efficiency as one of the cells firing B, is increased.”

This rule is not enough to teach a network, but it is a good start.  The problem with the rule is that there is no way for synaptic weights to decrease. Systems which use Hebb's postulate as a basis for a learning rule are said to be Hebbian.

 hindbrain - see forebrain, midbrain

PICTURE FRAME

 homunculus - 1. The topographic mapping (in motor cortex) of the body's somatosensory afferents. 2. In philosophy, the observer inside the head which gives us self consciousness. The homunculus compels paradox, however: Who watches the watcher? see topographic mappings

PICTURE FRAME

 Hopfield network - A fully connected hetero-associative network. This network minimizes an energy function (called a Lyapunov function). If an energy function can be defined for a system, a Hopfield network can solve it. (Hopfield 1982) The introduction of the Lyapunov function was a crucial turning point, because it opened the way to many different forms of analysis. For example, the Hopfield network was shown to be isomorphic to an Ising spin system, thereby giving physicists a back door into neural net research.

PICTURE FRAME

 hypothalamus - a body located near the pituitary gland. It seems to control production of hormones.

PICTURE FRAME

inferior collicus - an auditory processing station between the cochlea and the auditory cortex. see mesencephalicus lateralis dorsalis

PICTURE FRAME

 inhibitory synapse - an input which discourages a neuron from firing, in other words, inhibiting it. see excitatory synapse, lateral inhibition, synapse

 interneuron - see astrocyte, glial cell

intrinsic properties - see emergent properties

Kohonen network - see self organizing feature map

PICTURE FRAME

 lateral geniculate nucleus (LGN) - one of the processing stations between the retina and the visual cortex. It has many retinotopic mappings which perform such functions as edge detection and enhancement, motion analysis, noise suppression, and so on.

PICTURE FRAME

 lateral inhibition - A very important organizing principle in common usage throughout the brain: neighbouring neurons inhibit each other. The amount of inhibition is often modulated by a bell-shaped function of radius, so that nearby neurons are actually reinforced, but more distant ones are suppressed. Lateral inhibition has been observed in the retina of the horseshoe crab Limulus, and is the principle concept behind self organizing feature maps.  see nhibitory synapse, Limulus, self organizing feature maps, tonotopic mappings

PICTURE FRAME

 limbic system - In general, the limbic system seems to be concerned with behavioural strategy. It is comprised of the hippocampus (which appears to be involved with conditioning), the cingulate gyrus, the septum, and the amygdala. see amygdala, cingulate gyrus, septum, cingulate gyrus

PICTURE FRAME

 Limulus - the Horseshoe Crab. A sea creature whose nervous system has been extensively studied and characterized due to its simplicity and accessibility. Limulus has a simple compound eye which makes use of lateral inhibition to perform image processing such as edge detection and enhancement. see Aplysia, lateral inhibition

PICTURE FRAME

 local representation - A single cell represents a single concept. If that cell is active, the concept is active. There is no crosstalk between patterns with this representation. see distributed representation, grandmother cell

 Lyapunov function - an energy function describing a system.

 memistor - from Memory Resistor. An adaptive circuit element which implements synaptic weights for the Adaline. see Adaline

 mesencephalicus lateralis dorsalis (MLD) - the avian homologue of the inferior collicus. In the owl, the MLD contains a topological mapping of auditory space. (Knudsen & Kohishi 1978). see inferior collicus

 midbrain - see forebrain, hindbrain

PICTURE FRAME

 mossy fibres - excitatory input to the cerebellum. The climbing fibres are the other source of input to the cerebellum. see cerebellum, climbing fibres

 negative reinforcement - Reinforcement due to the cessation of an aversive stimulus. see operant conditioning

 neurocomputing - the study of computers that use brain-inspired processing architectures.

 neuroecology - the study of environments and systems and populations in terms of neuroethology. " The highest function of Ecology is the understanding of consequences." - Frank Herbert. see neuroethology

 neuroethology - the study of how behaviour is governed by the interactions of neurons and nervous systems and environment.  The study of ethology arguably began with Charles Darwin's book of 1872 "The Expression of Emotions in Man and Animals."  see neuroecology

 neuroglia - see astrocytes, glial cell

 neuromimetic - a word used to describe systems which function in a matter presumed to be similar to the functioning of a neuron.

 neuromorphic - see neuromimetic

 neuron - The cells comprising the central nervous system. Differing ion concentrations across the cell membrane define the electrical activity of the neuron, and the interaction of the activities of all the neurons with each other, and with the environment, defines the behaviour of the nervous system, and consequently, of the organism. The principal output of the neuron is through an electrical spike, called the action potential, propagated along the axon, and the principal input arrives from other neurons, through the dendrites via the synapses. see action potential, axon, dendrite, soma, synapse

PICTURE FRAME

 neurotransmitter -

 ommotidium pl. ommotodia - a single unit of an invertebrate's compound eye, comprised of a lense, and light sensing apparatus. see Limilus

PICTURE FRAME

 ontogenesis - the development of an organism, from a single cell to mature adult.

PICTURE FRAME

 operant conditioning - see classical conditioning

 optic tectum - In lower vertebrates, the optic tectum is the functional homologue of the superior collicus. see superior collicus

 Parallel Distributed Processing (PDP) -

 PDP - see Parallel Distributed Processing

 Perceptron -

 percept - a single perception.

 pituitary - a gland involved in the control and production of hormones. The pituitary of salamanders can detect light, and thus acts almost as a third eye.

 plasticity - the ability of a neuron to adapt or change.  If a neuron is not plastic, it can't learn.

 plasticity-stability dilemma - A sometimes paradox confronting designers of neural computers. Should learning stop at some point? If it doesn't stop, how do you deal with the continuous influx of new information from the environment, yet not lose old learning?

 prioreceptive - sensory feedback from the muscles.

 Purkinje cell -

 pyramidal tract - routes axons out from the motor cortex to the spinal cord.

 Rana Computrix -

 red nucleus - involved with motor control.

PICTURE FRAME

retinotopic mapping - see topographic mapping

 saccade - A reflex action performed by the saccadic system. A saccade directs the gaze of a vertebrate to a particular spot, bringing detail vision to bear on the object of interest. see fovea, vestibular ocular reflex

 self organizing feature map - a technique pioneered by Finnish researcher Teuvo Kohonen whereby a network of neurons interacting through lateral inhibition form a topology preserving mapping of an input space. Self organizing feature maps are often used to reduce the dimensionality of an input space. see lateral inhibition, weight

PICTURE FRAME

 septum - see limbic system

 sigmoid curve -

PICTURE FRAME

 simulated annealing - a computational technique whereby energy is added to a system, and that energy is slowly reduced, allowing the system to settle into a global minimum. By analogy to the physical process of cooling a metal and allowing it to crystallize, this process is called simulated annealing. Simulated annealing introduces the concepts of thermodynamics to computing machines. (Metropolis, Teller, & Teller, 1953) see Boltzmann machine, gradient descent, weight

 soma - Latin, means body. Plural is somata. By itself, it often refers to a cell body. The soma of a cell contains the metabolic machinery which keep it alive, also assembling the structural components making up the axon, dendrites, etc. see neuron, somatosensory

 somatosensory - referring to the senses of the body - touch, heat, pressure, etc.

 stellate cell -

 stochastic process - see deterministic process

 striate cortex - Area 17 of the brain, the visual cortex.

PICTURE FRAME

 superior collicus - also called the optic tectum. see optic tectum

PICTURE FRAME

 synapse - the place where neurons communicate with each other. Axons communicate with dendrites through the release of neurotransmitters across the synaptic cleft. The neurotransmitters released serve to excite or inhibit the receiving neuron. see excitatory synapses, inhibitory synapses, weight

PICTURE FRAME

 syncytium - a group of neurons fused into one functional entity during ontogenesis, or early in nervous system development. see ontogenesis

PICTURE FRAME

 tabula rasa - The idea of John Locke (1632-1704) that the mind before birth or a particular experience is like a blank tablet, or a fresh sheet of paper, ready to receive information.

 tonotopic mapping - this is a mapping that organizes sound from the cochlea such that similar frequencies are grouped together. In the cochlea, for example, the low frequency sensors are located near the apex of the basilar membrane, and the high frequency sensors are near the base. see topographic mapping

PICTURE FRAME

 topographic mappings - one of the most important computational modalities used by the central nervous system. Topographic mappings preserve shape: for example, the skin is mapped to very specific parts of the brain, in such a way that the spatial relationships between the signals from the touch receptors are preserved. see retinotopic mapping, tonotopic mapping

PICTURE FRAME

 transfer function - an equation which describes a transformation of the signals.

vestibular mechanism - 8.2.

 vestibulo-ocular reflex - the reflex action which keeps an image centered on the retina despite movements of the head. see fovea, saccade, vestibular mechanism, visuomotor system

 visuomotor system - implements the vestibulo-ocular reflex. see vestibulo-ocular reflex

 Voronoi tessellation - see self organizing feature net

PICTURE FRAME

 weight - Since not every signal arriving at a neuron is equally important, weighting a signal assigns importance. In a neuron model, weights are typically assigned to individual synapses, and learning is the modification of these weights. see plasticity, synapse

 Wernicke's Area - see Broca's Area

PICTURE FRAME

 white matter - The portions of the nervous system which are comprised mainly of axons: nerve processes. Computation does not occur here, rather, the white matter serves as cabling, connecting the grey matter. Half the thickness of cortex is white matter.  see grey matter

PICTURE FRAME


.cBIBLIOGRAPHY

APPENDIX D




When somebody's giving out data, take as much as you can.
- Bernard Widrow (1986)



Ackley, David H., Geoffrey E. Hinton, & Terrence J. Sejnowski. A Learning Algorithm for Boltzmann machines.  Cognitive Science, vol 9, pp.147-169. (1985)
The process of simulated annealing, built upon the shoulders of the Metropolis algorithm. (Metropolis, Teller, & Teller, 1953)

Aihara, Kazuyuki. Neural Computers: The Study of Brain and Nerve. Tokyo Electrical Engineering Institute, Tokyo, 1988. (in Japanese)

Anderson, James A. A Simple Network generating an Interactive Memory.  Mathematical Biosciences, vol. 14, pp. 197-220 (1972)

Anderson, James A. Foundations of Neuro-computing.  MIT Press, Cambridge MA, 1988.
This volume is a valuable collection of many classic and seminal works on neural networks. Many of the papers would be difficult to find anywhere else.

Barto, Andrew G. Richard S. Sutton, & Charles W. Anderson. Neuronlike adaptive elements that can solve difficult learning control problems.  IEEE Transactions on Systems, Man, and Cybernetics. SMC-13, pp. 834-846. (1983)
This paper introduced the Adaptive Critical Element/Adaptive Search Element (ACE/ASE) model which implemented "learning with a critic" to solve the broom balancing problem.

Beer, Randall D., Hillel J. Chiel, L.S. Sterling. Heterogeneous Neural Networks for Adaptive Behaviour in Dynamic Environments, in Advances in Neural Information Processing Systems, Volume 1. Morgan Kaufmann Publishers. (1989)
This paper demonstrates a locomotion controller based on the work of Pearson (1976). See also Chiel et al 1989.

Bienenstock, Elie L., Leon N. Cooper, & Paul W. Munro. Theory for the development of neuron selectivity: orientation specificity and binocular interaction in the visual cortex.  Journal of Neuroscience, vol 2: pp. 32-48. (1982)

Braitenburg, Valentino. Vehicles: Experiments in Synthetic Psychology. MIT Press, Cambridge. (1984)

Brodie, Scott E., Bruce W. Knight, & Floyd Ratliff. The response of the Limulus retina to moving stimuli: a prediction by Fourier analysis.  Journal of General Physiology, vol 72. pp. 129-166. (1978)
This paper is collected in Anderson 1988.

Brooks, Rodney A. A Robot That Walks: Emergent Behaviors from a Carefully Evolved Network. In Proceedings of the 1989 IEEE International Conference on Robotics and Automation, Volume 2. pp. 692-696.

Camhi, Jeffrey M. Neuroethology: Nerve Cells and the Natural Behaviour of Animals.  Sinauer Associates Inc. Publishers, Sunderland, Massachusetts, 1984.

Carpenter, Gail, Stephen Grossberg. The ART of Adaptive Pattern Recognition by a Self Organizing Neural Network.  IEEE Computer, March 1988. pp. 77-88

Chiel, Hillel J., & Randall D. Beer. A Lesion Study of a Heterogeneous Artificial Neural Network for Hexapod Locomotion, in Proceedings of the International Joint Conference on Neural Networks, 1989. vol. 1, pp. 407 - 414. (1989)
This paper demonstrates a locomotion controller based on the work of Pearson (1976). See also Beer et al 1989, Brooks 1989.

Connell, Jonathon. The Omni Photovore.  Omni Magazine, November 1988. pp. 201-212
Contains circuit schematics and construction diagrams for a simple do-it-yourself light seeking robot, like those described in Vehicles. (Braitenburg)

Coss, Richard G., Albert Globus. Spine Stems on Tectal Interneurons in Jewel Fish are Shortened by Social Stimulation.  Science, vol 200. 19 May 1978. pp 787-789

Crick, Francis. The Brain. Scientific American 1977 (ref XXX)

Crick, Francis. Function of the thalamic reticular complex: the searchlight hypothesis.  Proceedings of the National Academy of Sciences, 81: 4586-4590 (1984)

Crick, Francis. Brain Physiology, in Parallel Distributed Processing, vol 2, Rumelhart & McClelland, Eds. MIT Press, Cambridge MA., 1987 (ref XXX)

Creutzfeldt O.D. & P. Huggelund. Science vol. 188. pp. 1025-1027 (1975) (XXX find this and read it)

Davis, W.J. Cerebral Organization in Invertebrates, in Neural Control of Locomotion, R.M. Herman, S. Grillner, P.S.G. Stein, & D.G. Stuart (Eds.) Plenum Press, New York. pp. 265-292. (1976)
The beginnings of a paradigm shift in theory from hierarchical networks to distributed networks.

Eckmiller, Rolf, Cristoph von der Marlsburg (Eds.) NATO ASI Series: #41. Neural Computers.  Springer Verlag, Heidelberg, 1988

This collection of papers contains many interesting reports.

Fair, Charles M. Memory and Central Nervous Organization.  Paragon House Publishers, New York, 1988.

Fukushima, Kunihiko. A Neural Network for Visual Pattern Recognition. IEEE Computer Magazine, March 1988. pp 65-75
The inventor describes the details of his NeoCognitron is some detail.

Gluck, Mark A. & Richard F. Thompson. Modelling the Neural Substrates of Associative Learning and Memory: A Computational Approach.  Psychological Review, vol 94, No. 2, pp. 176-191. (1987)

Gottlieb, David I. GABAergic Neurons.  Scientific American, Feb. 1988.

Grossberg, Stephen. How does the brain build a cognitive code?  Psychological Review, vol 87. pp. 1-51. (1980)
This article presents the theories which eventually lead up to Adaptive Resonance Theory (ART) in a logical and progressive fashion. This paper is collected in Anderson 1988.

Grupen, Roderic A., Thomas C. Henderson & Ian D. McCammon. A Survey of General-Purpose Manipulation.  The International Journal of Robotics Research, Vol. 8, No. 1. (Feb. 1989)

Guthrie D.M. Neuroethology: An Introduction.  Blackwell Scientific Publications, Oxford, 1980.

Hebb, Donald O. The Organization of Behaviour, Wiley & Sons, New York, 1949.

Heron W., et al. In Sensory Deprivation, P. Solomon et al., eds., pp 6-33, Harvard University Press, 1961

Hopfield J.J. Neural Networks and physical systems with emergent computational abilities.  Proceedings of the National Academy of Sciences, vol 79. pp. 2554-2558 (1982)

Hopfield J.J. Neurons with graded response have collective computational properties like those of two state neurons.  Proceedings of the National Academy of Sciences. vol 81. pp. 3088-3092 (1984)

Hoyle, Graham. Arthropod Walking, in Neural Control of Locomotion, R.M. Herman, S. Grillner, P.S.G. Stein, & D.G. Stuart (Eds.) Plenum Press, New York. pp. 137 - 179. (1976)

Hubel D.H. & T.N. Wiesel. Receptive fields, binocular interaction and functional architecture in the cat's visual cortex. Journal of Physiology (London). vol 160. pp. 106-154. (1962)

Hyde, Vickie. Momentum: The Rhythms of Life.  Japan Times, Oct. 18, 1988, p10

Johnson, R. Colin. Neural Networks in Japan.  Electronic Engineering Times, April 6, 1987. p 49

Kimelberg, Harold K., & Michael D. Norenberg. Astrocytes.  Scientific American, April 1989. 66-76

Klopf A.Harry. The Hedonistic Neuron: A Theory of Memory, Learning, and Intelligence.  Hemisphere Press, Washington DC, 1982.
This work provided the central metaphor for the ACE/ASE system of Barto, Sutton, & Anderson 1983.

Knudsen, Eric I. & Masakazu Konishi. A Neural Map of Auditory Space in the Owl.  Science, vol. 200, May 19, 1978. pp 795-797
This paper showed that sound direction is topologically mapped in the mesencephalicus lateralis dorsalis (MLD) area of the brain. The MLD is the avian homologue of the inferior collicus.

Kohonen, Teuvo. The `Neural' Phonetic Typewriter.  IEEE Computer, March. 1988a. pp. 11-22

Kohonen, Teuvo. Self Organization and Associative Memory, second edition.  Springer Verlag, Heidelberg, 1988b
Contains much material on associative memory, and many proofs related to the self organizing feature net.

Kupfermann I., & K.R. Weiss.  The Command Neuron Concept. Behav. Brain Science. 1:3-39. 1978

Kuwada, Shigeyuki, Tom C.T. Yin, & Robert E. Wickesberg. Response of Cat Inferior Collicus Neurons to Binaural Beat Stimuli: Possible Mechanisms for Sound Localization.  Science, vol 206, Nov. 2, 1979. pp. 586-588

Lashley. Karl S. In Search of the Engram.  Society of Experimental Biology Symposium, No. 4. Psychological Mechanisms in Animal Behaviour. Cambridge University Press, 1950. pp 454-480 (1950)

Laurent, Gilles & Reinhold Hustert. Motor Neuronal Receptive Fields Delimit Patterns of Motor Activity During Locomotion of the Locust. Journal of Neuroscience, vol. 8, no. 11, Nov. 1988. pp. 4349-4366

Lettvin, J.Y., H.R. Maturana, W.S. McCulloch, & W.H. Pitts. What the Frog's Eye Tells the Frog's Brain.  Proceedings of the IRE, vol 47, No. 11 (Nov. 1959), pp 1940-1959

Lipmann, Richard P. An Introduction to Computing with Neural Networks.  IEEE ASSP Magazine, vol. 3, no. 4. (April 1987). pp. 4-22

Luria, A model of speech generation and perception, 1977

McClelland & Rumelhart. Parallel Distributed Processing, vols 1 and 2, 1986

McCulloch, Warren S. Embodiments of Mind. MIT Press, Cambridge MA, 1965, reissued 1988.
This collection contains many intriguing essays, including the two very famous ones written with Walter Pitts, noted below.

McCulloch, Warren S. & Walter Pitts. A Logical Calculus of Ideas Imminent in Nervous Activity.  Bulletin of Mathematical Biophysics. vol 5, pp. 115-133. (1943)

MacGregor, Ronald J. Neural and Brain Modeling,  Academic Press Inc., San Diego. 1988.

Mead, Carver. Silicon Models of Neural Computation.  Proceedings. IEEE First International Conference on Neural Networks 1987, vol 1.

Metropolis N., A. Rosenbluth, A Teller, & E. Teller. Equation of State Calculations for Fast Computing Machines.  Journal of Chemical Physics, vol 6, p. 1087 (1953)
Introduced the concepts of thermodynamics to computers in the form of simulated annealing. This became the basis of the Boltzmann machine reported in Ackley et al, 1985.

Michie D., & R.A. Chambers. BOXES: An experiment in adaptive control, in Machine Intelligence 2, E. Dale and D. Mitchie, Eds. Oliver and Boyd, Edinburgh. pp. 137-152 (1968)
This system was the inspiration for the ACE/ASE system of Barto, Sutton, & Anderson 1983.

Minsky, Marvin. The Society of Mind.  Picador, London, 1987.

Minsky, Marvin & Seymour Papert. Perceptrons, expanded edition.  MIT Press, Cambridge MA, 1969 rereleased 1988.
Although this book is often blamed for the first death of neural network research, it is a useful reference work, with good examples, and lucid prose. It gives a good feeling for what a Perceptron can't do, and equally importantly, what it can.

Pearson, Keir. The Control of Walking. Scientific American, vol 276. December 1976.

Pellionisz, Andreas. Rana Computrix ( ref XXX), 1977

Reynold, Craig W. Flocks, Herds, and Schools: A Distributed Behavioural Model.  IEEE Computer Graphics, July 1987, vol 21, No. 4. pp. 25-34

Rietmann, Ed. Experiments in Artificial Neural Networks. Tab Books, 1988. (ref XXX city?)

Rosenblatt, Frank. The Perceptron: A probabilistic model for information storage and retrieval in the brain.  Psychological Review, vol. 65. pp. 386-408 (1958)

Rumelhart, David E., Geoffrey E. Hinton, & Ronald J. Williams. Learning Representations by Back-Propagating Errors.  Nature, vol. 323. pp. 533-536 (1986)

Schiller, Peter H., Sean D. True, & Janet L. Conway. Effects of Frontal Eye Field and Superior Collicus Ablations on Eye Movements.  Science, vol 206. Nov. 2 1979. pp. 590-592

Shannon & Weaver. Towards a Theory of Information, 1949

Sharra, Shihab. Neural Nets for Speech Processing and Recognition.  Proceedings IEEE First International Conference on Neural Nets, vol IV, p. 397 (1987)
Presents a model of cochlear audio processing incorporating realistic stages and parameters, and shows how speech recognition could work.

Shepherd, Gordon M. Neurobiology, second edition. Oxford University Press, New York, 1988

Stein, Barry E., H.P. Clamann, & S.J. Goldberg. Superior Collicus: Control of Eye Movements in Neonatal Kittens.  Science, vol. 210, 3 Oct. 1980. pp. 78-80

Stent, Gunther S., William B. Kristan, W. Otto Friesen, Carol A. Ort, Margaret Poon, Ronald L. Calabrese. Neuronal Generation of the Leech Swimming Movement.  Science Vol 200, 23 June 1978. pp. 1348-1356

Stevens, John K. Reverse Engineering the Brain. BYTE, April 1985, pp 287-299

Travis, Bryan. Computational Model of Auditory Cortex.  Proceedings IEEE First International Conference on Neural Nets, vol IV, p. 67 (1987)
Details four tonotopic maps from the Medial Geniculate Nucleus to the Auditory Cortex.

von der Marlsburg, Christoph. Self Organization of Orientation Sensitive Cells in the Striate Cortex. Kybernetik, vol 14, pp. 85-100 (19xxx)
This was one of the first attempts to relate a computational model to known physiology, and to compare the results to physiological data. This paper is collected in Anderson, 1988.

Welker W.I., & S. Seidenstein. Somatic Sensory Representation in the Cerebral Cortex of the Raccoon (Procyon Loter) J. Comp. Neurol, vol. 111, pp. 469-501 (1959)

Wiesel T.N., & D.H. Hubel. Spatial and Chromatic interactions in the lateral geniculate body of the rhesus monkey.  J. Neurophysiology, vol. 29, pp. 1115-1156 (1966)

Widrow, Bernard & Marcian Hoff. Adaptive Switching Circuits.  IRE WESCON Convention Record, NY, IRE, pp. 96-104 (1960)
This paper introduced the gradient descent (also called Least Mean Squares or LMS) method of training adaptive circuits.

Widrow, Bernard. Introduction to Proceedings of the First IEEE Conference on Neural Nets. (1987)
Contains amusing anecdotes relating to the first hardware implementations of the Adaline (ADAptive LINear Element) and the Madaline (Many ADALINEs).

Widrow, Bernard, & Rodney Winter. Neural Networks for Adaptive Filtering and Adaptive Pattern Recognition.  IEEE Computer, March 1988. pp. 25-39

von Neumann, John. The Computer and the Brain. (ref XXX publisher?), 1958.
