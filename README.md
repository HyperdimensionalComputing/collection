<meta name='keywords' content='regex, regular expressions, regexp'>

# Collection of Hyperdimensional Computing Projects
Here, we aim to provide a comprehensive collection of projects using hyperdimensional computing. Please let us know if you have any related project.


## Introduction to Hyperdimensional Computing
The way the brain works suggests that rather than working with numbers that we are used to, computing with hyperdimensional (HD) vectors, e.g., 10,000 bits is more efficient. Computing with HD vectors, referred to as “*hypervectors*,” offers a general and scalable model of computing as well as well-defined set of arithmetic operations that can enable fast and one-shot learning (no need of back-propagation like in neural networks). Furthermore it is memory-centric with embarrassingly parallel operations and is extremely robust against most failure mechanisms and noise. 
Hypervectors are high-dimensional (e.g., 10,000 dimensions), they are (pseudo)random with independent identically distributed components and holographically distributed (i.e., not microcoded). Hypervectors can use various coding: dense or sparse, bipolar, binary, real and can be combined using arithmetic operations such as multiplication, addition, and permutation. The vectors can be compared for similarity using distance metrics.
### Useful Reading
* [Hyperdimensional Computing: An Introduction to Computing in Distributed Representation with High-Dimensional Random Vectors](http://redwood.berkeley.edu/vs265/kanerva09-hyperdimensional.pdf) 
* [High-dimensional Computing as a Nanoscalable Paradigm](https://iis-people.ee.ethz.ch/~arahimi/papers/TCAS17.pdf)
* [Vector Symbolic Architectures Answer Jackendoff's Challenges for Cognitive Neuroscience](https://arxiv.org/abs/cs/0412059)
* [Pentti Kanerva. 1988. Sparse Distributed Memory. MIT Press, Cambridge, MA, USA](https://mitpress.mit.edu/books/sparse-distributed-memory)
* [Chris Eliasmith. 2013. How to Build a Brain: A Neural Architecture for Biological Cognition. Oxford University Press, Oxford, UK](http://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199794546.001.0001/acprof-9780199794546)
* [Tony A. Plate. 2003. Holographic Reduced Representation: Distributed Representation for Cognitive Structures. CSLI Publications, Stanford, CA, USA](https://dl.acm.org/citation.cfm?id=862031)


## One-shot Learning for Intracranial EEG (iEEG) Seizure Detection
* **Task:** An efficient algorithm with end-to-end binary operations for both learning and classification of human epileptic seizures from intracranial electroencephalography (iEEG)
  * Input: 36 to 100 implanted iEEG electrodes
  * Output: Binary classification (interictal vs. ictal states)
* **Implementation:** Matlab and Python
* **Remarks:** One-/few-shot learning from seizures with higher accuracy than SVM and MLP; linearly scalable to large number of electrodes; lower memory footprint
* [**Link to code**](http://ieeg-swez.ethz.ch)


##  Energy-Efficient Seizure Detection for Long-term Human Intracranial EEG (iEEG) 
* **Task:** The main idea of this algorithm is to combine local binary patterns (LBP) with hyperdimensional (HD) computing followed by a patient-specific postprocessing to learn and detect seizures from intracranial electroencephalography (iEEG)
  * Input: 24 to 128 implanted iEEG electrodes
  * Output: Binary classification (interictal vs. ictal states)
* **Implementation:** Python, OpenMP, Verilog
* **Remarks:** No false alarms over 1357 hours of testing; Lower number of undetected seizures, false alarms (to zero), execution time, and energy consumption for classification on a TX2 embedded device compared to support vector machine (SVM), convolutional neural network (CNN), and long short-term memory recurrent neural network (LSTM); Fast learning from one or two seizure examples.
* [**Link to code**](http://ieeg-swez.ethz.ch)


## Hand Gesture Recognition from Electromyography (EMG) Signals
* **Task:** A smart prosthetic application, namely hand gesture recognition from a stream of EMG sensors
  * Input: EMG signals from 4 channels
  * Output: 5 classes as different hand gestures
* **Implementation:** Matlab
* **Remarks:** ~3x less training data; higher accuracy than SVM
* [**Link to code**](https://github.com/abbas-rahimi/HDC-EMG)


## Hand Gesture Recognition from Flexible EMG Sensors 
* **Task:** An end-to-end system using a large-area, high-density EMG sensor array for robust hand gesture recognition
  * Input: 64 EMG electrodes
  * Ouput: 5 classes as different hand gestures
* **Implementation:** Matlab
* **Remarks:** One-shot learning; higher accuracy than SVM
* [**Link to code**](https://github.com/a-moin/flexemg)
* [**System Demo**](https://bwrc.eecs.berkeley.edu/sites/default/files/files/u2630/flexemg_v2_lq.mp4#t=2)


## An Accelerator of HD Computing on a Parallel Ultra-Low Power Platform
* **Task:** HD computing's acceleration on a silicon prototype of the PULPv3 4-core chip (1.5 mm2, 2 mW) with optimization of memory accesses and operations
* **Implementation:** C (for ARM Cortex M4 processors) and OpenMP (for multi-core processors)
* **Remarks:** Simultaneous 3.7× end-to-end speed-up and 2× energy saving compared to its single-core execution
* [**Link to code**](https://github.com/fabio-montagna/PULP-HD)


## FPGA Optimizations of Dense Binary HD Computing
* **Task:** Hardware techniques for optimizations of HD computing, in a synthesizable VHDL library, to enable co-located implementation of both learning and classification tasks on only a small portion of an FPGA
* **Implementation:** VHDL (RTL)
* **Remarks:** Design space exploration with library modules shows simultaneous 2.39× area and 986× throughput improvements
* [**Link to code**](https://github.com/eardbi/hd-vhdl-library)


## Brain–Computer Interfaces from Electroencephalography (EEG) Signals 
* **Task:** Binary classification of EEG error-related potentials for noninvasive brain–computer interfaces
  * Input: 64 EEG electrodes
  * Output: Binary classification (correct class vs. error class)
* **Implementation:** Matlab
* **Remarks:** ~3x less training data and preprocessing; no *domain expert knowledge* for electrode selection 
* [**Link to code**](https://github.com/abbas-rahimi/HDC-EEG-ERP)


## Motor-Imagery based Brain–Computer Interfaces
* **Task:** Multiclass learning and inference using motor-imagery based brain–computer interface (MI-BCI) from electroencephalography (EEG) signals
  * Input: 16 EEG electrodes, and 22 EEG electrodes
  * Output: Multicalss classification (3 classes, and 4 classes)
* **Implementation:** Python
* **Remarks:** ~26x faster training time, and ~22x lower energy 
* [**Link to code**](https://github.com/MHersche/HDembedding-BCI)
 

## Tradeoffs in Choice of Density and Mapping Characteristics
* **Task:** Discussing tradeoffs of selecting parameters of binary HD representations when applied to pattern recognition tasks. Particular design choices include density of representations and strategies for mapping data from the original representation.
* **Implementation:** Matlab
* **Remarks:** For the considered pattern recognition tasks both sparse and dense approaches behave nearly identical. At the same time implementation peculiarities may favor one approach over another
* [**Link to code**](https://github.com/denkle/Binary-Hyperdimensional-Computing-Trade-offs-in-Choice-of-Density-and-Mapping)


## European Language Recognition
* **Task:** European language recognition from letter *n*-grams
  * Input: Streams of characters
  * Output: 21 classes as the European languages 
* **Implementation:** Matlab and SystemVerilog (RTL)
* **Remarks:** ~50% energy saving; 8.8x higher robustness in memory failures
* [**Link to code**](https://github.com/abbas-rahimi/HDC-Language-Recognition)


## Learning Behavior Hierarchies via High-Dimensional Sensor Projection
* **Task:** A knowledge-representation architecture allowing a robot to learn arbitrarily complex, hierarchical/symbolic relationships between sensors and actuators
* **Implementation:** C++
* **Remarks:** Despite their extreme computational simplicity, these architectures can be easily “programmed” to perform subsumption hierarchies and other rule-like behaviors in the service of interesting tasks, in the absence of explicit if/then statements or other traditional symbolic constructs
* [**Link to code**](https://github.com/simondlevy/vsarobot)
