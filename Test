# Basic Structure & Feedforward Networks

**Terms addressed:** Feedforward Networks, One-way flow, Multilayer perceptron, Typical uses, Layers, Connections, Parameters.

The generated visualizer provides an excellent visual of a basic network. While it only shows a single neuron being calculated in detail, it hints at the overall architecture.

A Feedforward Network, often called a Multilayer Perceptron (MLP), is the foundational design where information strictly moves in a one-way flow from inputs to outputs (as the visualizer arrows show). They are typically used for simple prediction and classification tasks on structured data, such as forecasting a numerical value or sorting data into categories[cite: 2].

> **Output-Y:** 0.618  
> **Bias (b):** +0.10  
> **Error E:** 0.0731  
> **Math representation:** $z = (x_{1} \times w_{1}) + (x_{2} \times w_{2}) + b$ (yielding $z = 0.48$), passing through the Sigmoid activation to produce an output $y = 0.618$ and an error $E = 0.0731$[cite: 2].

---

### 1. Layers
A full network stacks these units. The visualizer shows:
* **An Input Layer:** On the far left, featuring inputs $X_{1}$ (1.00) and $X_{2}$ (0.40)[cite: 2].
* **A Hidden Layer / Processing Unit:** The blue rectangles in the middle, labeled "Weighted Sum ($\sigma Z$)" and "Activation Sigmoid". This is where the core calculation happens[cite: 2].
* **An Output / Evaluation Unit:** The circle on the far right labeled "Total Error (E)" alongside the final output value of 0.618. *Note: The visualizer illustrates just one single neuron within a layer.*[cite: 2]

### 2. Connections & Parameters
* **Connections:** The arrows connecting inputs to calculations represent the connections[cite: 2].
* **Parameters:** Each connection is assigned specific parameters that the network learns during training[cite: 2]. The visualizer labels these clearly:
  * **Weights ($w_{1}, w_{2}$):** These determine the input's importance. In the example, $w_{1}$ ($0.50$) is weighted positively, and $w_{2}$ ($-0.30$) is weighted negatively[cite: 2].
  * **Bias ($b$):** The extra offset (labeled "Bias (b)" pointing into the Weighted Sum with a value of $+0.10$), which shifts the neuron's response[cite: 2].

**References:**
* 3Blue1Brown. (2017). *But what is a neural network? | Chapter 1, Deep learning* [Video]. YouTube. https://www.youtube.com/watch?v=19v8efdO6vs
* Nielsen, M. A. (2015). *Neural Networks and Deep Learning* (Chapter 1: Using neural nets to recognize handwritten digits). Determination Press. http://neuralnetworksanddeeplearning.com/
* freeCodeCamp. (2020). *Neural Networks Explained Simply in Python*. freeCodeCamp.org. https://www.freecodecamp.org/news/neural-networks-explained-simply-in-python/

---

## Advanced Concept Definitions

While the visualizer is great for the math of a single neuron, we need standard definitions for the other foundational terms listed[cite: 2, 3]:

### Depth vs. Width
This describes the "shape" of the network, beyond the single unit shown[cite: 3].
* **Depth:** The number of hidden layers stacked between input and output. Deep Learning is characterized by high depth (many layers), allowing it to solve complex, layered problems[cite: 3].
* **Width:** The number of neurons within a single layer[cite: 3].

**References:**
* Nielsen, M. A. (2015). *Neural Networks and Deep Learning* (Chapter 5: Why are deep neural networks hard to train?). Determination Press. http://neuralnetworksanddeeplearning.com/
* Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning* (Chapter 6: Deep Feedforward Networks). MIT Press.

---

## RNNs (Recurrent Neural Networks)

**Terms addressed:** Sequences, Hidden-State Memory, Text and Time Series[cite: 3].

Unlike the one-way flow of the visualizer, RNNs are specialized for Sequences[cite: 3]. They "recalculate" outputs multiple times for a sequence of data, feeding information from one step into the next[cite: 3]. This creates a built-in Hidden-State Memory[cite: 3]. This recursive calculation makes RNNs excellent at processing ordered data like Text (interpreting sentences) and Time Series (forecasting stock trends based on history)[cite: 3].

**References:**
* Olah, C. (2015). *Understanding LSTM Networks*. Colah's Blog. https://colah.github.io/posts/2015-08-Understanding-LSTMs/
* DeepLearning.AI & Coursera. (n.d.). *Sequence Models* (Course 5 of Deep Learning Specialization by Andrew Ng). Coursera. https://www.coursera.org/specializations/deep-learning

---

## CNNs (Convolutional Neural Networks)

**Terms addressed:** Filters, Images, Pooling[cite: 3].

CNNs are structurally distinct, specialized for Images and spatial data[cite: 3]. Instead of connections from every input to every neuron (as implied by the visualizer), they use specialized mathematical structures called Filters[cite: 3]. These filters scan small windows of an image to detect specific features, like edges or corners[cite: 3]. This process is usually paired with a step called Pooling, which simplifies the input data to focus on key features and reduce computational load[cite: 3].

**References:**
* Starmer, J. (2022). *Convolutional Neural Networks (CNNs) Explained* [Video]. YouTube. https://www.youtube.com/@statquest
* DeepLearning.AI & Coursera. (n.d.). *Convolutional Neural Networks* (Course 4 of Deep Learning Specialization by Andrew Ng). Coursera. https://www.coursera.org/specializations/deep-learning

---

## Transformers

**Terms addressed:** Attention, Language Models, Parallel Processing[cite: 3].

This is the state-of-the-art architecture for many complex AI tasks today, especially the large Language Models that power modern chatbots[cite: 3]. Transformers replace the recurrent memory of RNNs with a concept called the Attention mechanism[cite: 3]. This technique lets the network "pay attention" to multiple parts of an entire sentence or sequence simultaneously, understanding full context all at once[cite: 3]. Crucially, this allows for Parallel Processing, which makes Transformers vastly faster to train than RNNs and CNNs when handling large amounts of data[cite: 3].

**References:**
* Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., & Polosukhin, I. (2017). Attention Is All You Need. *Advances in Neural Information Processing Systems (NeurIPS)*. https://arxiv.org/abs/1706.03762
* Alammar, J. (2018). *The Illustrated Transformer*. Jay Alammar's Blog. https://jalammar.github.io/illustrated-transformer/
