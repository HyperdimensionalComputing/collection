# Collection of Hyperdimensional Computing Projects
Here, we aim to provide a comprehensive collection of projects using hyperdimensional computing. Please [let us know](mailto:abbas@iis.ee.ethz.ch) if you have any related project.


## Introduction to Hyperdimensional Computing
The way the brain works suggests that rather than working with numbers that we are used to, computing with hyperdimensional (HD) vectors, referred to as “*hypervectors*,” is more efficient. Computing with hypervectors, offers a general and scalable model of computing as well as well-defined set of arithmetic operations that can enable fast and one-shot learning (no need of backpropagation). Furthermore it is memory-centric with embarrassingly parallel operations and is extremely robust against most failure mechanisms and noise. 
Hypervectors are high-dimensional (e.g., 10,000 bits), (pseudo)random with independent identically distributed components leading to holographic representation (i.e., not microcoded). Hypervectors can use various coding: dense or sparse, bipolar, binary, real, complex. They can be combined using arithmetic operations such as multiplication, addition, and permutation, and be compared for similarity using distance metrics.

### Useful Reading
* [Hyperdimensional Computing: An Introduction to Computing in Distributed Representation with High-Dimensional Random Vectors](https://link.springer.com/article/10.1007/s12559-009-9009-8) 
* [High-dimensional Computing as a Nanoscalable Paradigm](https://iis-people.ee.ethz.ch/~arahimi/papers/TCAS17.pdf)
* [Vector Symbolic Architectures Answer Jackendoff's Challenges for Cognitive Neuroscience](https://arxiv.org/abs/cs/0412059)
* [Pentti Kanerva. 1988. Sparse Distributed Memory. MIT Press, Cambridge, MA, USA](https://mitpress.mit.edu/books/sparse-distributed-memory)
* [Chris Eliasmith. 2013. How to Build a Brain: A Neural Architecture for Biological Cognition. Oxford University Press, Oxford, UK](http://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199794546.001.0001/acprof-9780199794546)
* [Tony A. Plate. 2003. Holographic Reduced Representation: Distributed Representation for Cognitive Structures. CSLI Publications, Stanford, CA, USA](https://dl.acm.org/citation.cfm?id=862031) 
  * [Tony A. Plate's Ph.D. Thesis](https://www.researchgate.net/publication/2459882_Distributed_Representations_and_Nested_Compositional_Structure)



## Integrating Event-based Dynamic Vision Sensors with Sparse Hyperdimensional Computing for Online Learning 
* **Project specification:** Developing an embedding to compresses events generated across 346×260 differential pixels to a sparse 8160-bit vector that not only simplifies inference, but also enables online learning with the same memory footprint to solve regression tasks.
  * Input: Features extracted from event-based 346×260 differential pixels
  * Output: Regression for estimating velocities (in x- and y-direction)
* **Implementation:** Python and OpenMP (on an 8-core accelerator)
* **Remarks:** 9.84× more energy-efficient and 6.25× faster than an optimized 9-layer perceptron with comparable accuracy; Online learning capability by using estimates and confidences of an initial model trained with only 25% of data, our method continuously updates the model for the remaining 75% of data, resulting in a close match with accuracy obtained with an oracle model on ground truth labels.
* [**Link to code**](https://github.com/iis-eth-zurich/hd_dvs)
* [link to paper](https://www.research-collection.ethz.ch/handle/20.500.11850/425534)


## One-shot Learning for Intracranial EEG (iEEG) Seizure Detection
* **Project specification:** Desining an efficient algorithm with end-to-end binary operations for both learning and classification of human epileptic seizures from intracranial electroencephalography (iEEG)
  * Input: 36 to 100 implanted iEEG electrodes
  * Output: Binary classification (interictal vs. ictal states)
* **Implementation:** Matlab and Python
* **Remarks:** One-/few-shot learning from seizures with higher accuracy than SVM and MLP; linearly scalable to large number of electrodes; lower memory footprint
* [**Link to code and FREE dataset**](http://ieeg-swez.ethz.ch)
* [link to paper](https://www.research-collection.ethz.ch/handle/20.500.11850/305686)


##  Energy-Efficient Seizure Detection for Long-term Human Intracranial EEG (iEEG) 
* **Project specification:** Designing an energy-efficient algorithm for long-term iEEG monitoring. The main idea of this algorithm is to combine local binary patterns (LBP) with hyperdimensional (HD) computing followed by a patient-specific postprocessing to learn and detect seizures from intracranial electroencephalography (iEEG)
  * Input: 24 to 128 implanted iEEG electrodes
  * Output: Binary classification (interictal vs. ictal states)
* **Implementation:** Python, OpenMP, Verilog
* **Remarks:** No false alarms over 1357 hours of testing; Lower number of undetected seizures, false alarms (to zero), execution time, and energy consumption for classification on a TX2 embedded device compared to support vector machine (SVM), convolutional neural network (CNN), and long short-term memory recurrent neural network (LSTM); Fast learning from one or two seizure examples.
* [**Link to code and largest iEEG datset**](http://ieeg-swez.ethz.ch)
* [link to paper](https://www.research-collection.ethz.ch/handle/20.500.11850/307983)


##  Multimodality Emotion Recognition with Physiological Signals
* **Project specification:** Designing a fast learning algorithm to fuse physiological signals across different modalities such as GSR, ECG, and EEG for emotion recognition. The algorithm maps real-valued features to binary hypervectors using a random nonlinear function, and further encodes them over time, and fuses across three different modalities. 
  * Input: 32 GSR features, 77 ECG features, and 105 EEG features
  * Output: 2 parallel binary classifiers (high vs. low arousal, and positive vs. negative valence)
* **Implementation:** Matlab
* **Remarks:** Compared to GaussianNB, SVM, and XGB, our algorithm achieves higher classification accuracy for both valence (83.2% vs. 80.1%) and arousal (70.1% vs. 68.4%) using only 1/4 training data. It also achieves at least 5% higher averaged accuracy compared to all the other methods in any point along the learning curve.
* [**Link to code**](https://github.com/enjui/HDC-MER)
* [link to paper](https://www.research-collection.ethz.ch/handle/20.500.11850/315807)


##  An EMG Gesture Recognition System with Flexible High-Density Sensors 
* **Project specification:** Design and development of an embedded system using a large-area, high-density EMG sensor array for robust hand gesture recognition
  * Input: 64 EMG electrodes
  * Ouput: 5 classes as different hand gestures
* **Implementation:** Matlab and C
* **Remarks:** One-shot learning; higher accuracy than SVM
* [**Link to code and dataset**](https://github.com/a-moin/flexemg)
* [**System Demo**](https://bwrc.eecs.berkeley.edu/sites/default/files/files/u2630/flexemg_v2_lq.mp4#t=2)
* [link to paper](https://iis-people.ee.ethz.ch/~arahimi/papers/ISCAS18.pdf)


## Hand Gesture Recognition using Electromyography (EMG) Signals
* **Project specification:** Designing an algorithm for hand gesture recognition from a stream of EMG sensors for a smart prosthetic application
  * Input: EMG signals from 4 channels
  * Output: 5 classes as different hand gestures
* **Implementation:** Matlab
* **Remarks:** ~3x less training data; higher accuracy than SVM
* [**Link to code and dataset**](https://github.com/abbas-rahimi/HDC-EMG)
* [link to paper](https://iis-people.ee.ethz.ch/~arahimi/papers/ICRC16.pdf)


## An Accelerator for HD Computing on a Parallel Ultra-Low Power Platform
* **Project specification:** HD computing's acceleration on a silicon prototype of the PULPv3 4-core chip (1.5 mm2, 2 mW) with optimization of memory accesses and operations
* **Implementation:** C (for ARM Cortex M4 processors) and OpenMP (for multi-core processors)
* **Remarks:** Simultaneous 3.7× end-to-end speed-up and 2× energy saving compared to its single-core execution
* [**Link to code**](https://github.com/fabio-montagna/PULP-HD)
* [**Demo**](https://www.youtube.com/watch?v=rjaw0LTqZZg)
* [link to paper](https://iis-people.ee.ethz.ch/~arahimi/papers/DAC18.pdf)

## CPU/GPU Hyperdimensional Computing Library
* **Project specification:** A general library including all the operations of HD computing for efficent execution on CPU and GPU
* **Implementation:** CPU/GPU
* **Remarks:** Efficent execution on CPU (bit packing, cicular buffers, hamming distance LUT), and exploring various memory accesses (global, shared, thread-local) in GPUs with further optimizations
* [**Link to code**] https://github.com/skurella/hdlib

## FPGA Optimizations of Dense Binary HD Computing
* **Project specification:** Hardware techniques for optimizations of HD computing, in a synthesizable VHDL library, to enable co-located implementation of both learning and classification tasks on only a small portion of an FPGA
* **Implementation:** VHDL (RTL)
* **Remarks:** Design space exploration with library modules shows simultaneous 2.39× area and 986× throughput improvements
* [**Link to code**](https://github.com/eardbi/hd-vhdl-library)
* [link to paper](https://arxiv.org/abs/1807.08583)


## Motor-Imagery based Brain–Computer Interfaces
* **Project specification:** Multiclass learning and inference using motor-imagery based brain–computer interface (MI-BCI) from electroencephalography (EEG) signals
  * Input: 16 EEG electrodes, and 22 EEG electrodes
  * Output: Multicalss classification (3 classes, and 4 classes)
* **Implementation:** Python
* **Remarks:** ~26x faster training time, and ~22x lower energy 
* [**Link to code and dataset**](https://github.com/MHersche/HDembedding-BCI)
* [link to paper](https://arxiv.org/abs/1812.05705)


## Brain–Computer Interfaces using Electroencephalography (EEG) Signals 
* **Project specification:** Binary classification of EEG error-related potentials for noninvasive brain–computer interfaces
  * Input: 64 EEG electrodes
  * Output: Binary classification (correct class vs. error class)
* **Implementation:** Matlab
* **Remarks:** ~3x less training data and preprocessing; no *domain expert knowledge* for electrode selection 
* [**Link to code**](https://github.com/abbas-rahimi/HDC-EEG-ERP)
* [link to paper](https://iis-people.ee.ethz.ch/~arahimi/papers/MONET17.pdf)


## Tradeoffs in Choice of Density and Mapping Characteristics of Binary HD Computing
* **Project specification:** Exploring tradeoffs of selecting parameters of binary HD representations when applied to pattern recognition tasks. Particular design choices include density of representations and strategies for mapping data from the original representation.
* **Implementation:** Matlab
* **Remarks:** For the considered pattern recognition tasks both sparse and dense approaches behave nearly identical. At the same time implementation peculiarities may favor one approach over another
* [**Link to code**](https://github.com/denkle/Binary-Hyperdimensional-Computing-Trade-offs-in-Choice-of-Density-and-Mapping)
* [link to paper](https://iis-people.ee.ethz.ch/~arahimi/papers/TNNLS18.pdf)


## European Language Recognition
* **Project specification:** Designing an algorithm and memory-centric architecture for European language recognition from letter *n*-grams
  * Input: Streams of characters
  * Output: 21 classes as the European languages 
* **Implementation:** Matlab and SystemVerilog (RTL)
* **Remarks:** ~50% energy saving; 8.8x higher robustness in memory failures
* [**Link to code**](https://github.com/abbas-rahimi/HDC-Language-Recognition)
* [link to paper](https://iis-people.ee.ethz.ch/~arahimi/papers/ISLPED16.pdf)


## Learning Behavior Hierarchies via High-Dimensional Sensor Projection
* **Project specification:** A knowledge-representation architecture allowing a robot to learn arbitrarily complex, hierarchical/symbolic relationships between sensors and actuators
* **Implementation:** C++
* **Remarks:** Despite their extreme computational simplicity, these architectures can be easily “programmed” to perform subsumption hierarchies and other rule-like behaviors in the service of interesting tasks, in the absence of explicit if/then statements or other traditional symbolic constructs
* [**Link to code**](https://github.com/simondlevy/vsarobot)
* [link to paper](https://www.aaai.org/ocs/index.php/WS/AAAIW13/paper/download/7075/6578)

## A non-linear notation for hyperdimensional computing
* **Project specification:** A non-linear 2-dimension encoding for representing an N-dimensional data structure well suited for the representation of hyperdimensional programs
* **Implementations:** ANTLR, Clojure, C++, Haskell, Javascript, Python, TypeScript
* **Remarks:** A novel non-linear way to encode data structures that relies entirely on a token's position in 2-D space for parsing.
* [**Link to code**](https://github.com/treenotation)
* [**Demo**](https://jtree.treenotation.org/designer/)
* [link to paper](https://arxiv.org/abs/1703.01192)
