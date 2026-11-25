## Chapter 7: Why Big Data Fuels Neural Networks

Explanations
Neural networks became powerful when three things arrived together: lots of data, networks with many parameters, and fast hardware (GPUs) to train them.
flowchart LR
    D["📦 Big data<br/>many examples"] --> B["🚀 Deep learning<br/>breakthroughs"]
    P["🧠 Many parameters<br/>big networks"] --> B
    G["⚡ GPUs<br/>fast parallel math"] --> B
    B -->|"success attracts<br/>more data and investment"| D
    
1. More data gives better learning
A network learns patterns from examples. More (and more varied) examples help it find the real pattern instead of memorizing quirks, which means less overfitting and better generalization (see Chapter 5, Section 5.3). Research on language models found that test loss falls predictably as dataset size, model size and training compute increase, a result called scaling laws.
⚠️ Caution: more data only helps if it is good data. Wrong or irrelevant examples (a Veracity problem) teach wrong patterns, and extra data cannot rescue a poor model design.
2. Many parameters need many examples
Every weight and bias is a parameter the network must tune. More parameters give a network more freedom, including the freedom to memorize the training set. To pin all those parameters down to real patterns, the network needs many examples. Research also shows that the amount of overfitting follows simple equations of model size and dataset size.
Ways to reduce overfitting when data is limited include data augmentation (flipping or cropping images to make new variations), dropout (randomly switching neurons off during training) and early stopping.
3. Deep learning breakthroughs
Year
Event
2009
ImageNet, a huge labeled image collection, is introduced
2010
The ILSVRC contest begins: classify images into 1,000 categories
2012
AlexNet wins by a large margin and starts the deep learning era
After 2012
Deeper networks push the error lower and lower

AlexNet in numbers: trained on 1.2 million images in 1,000 classes, with about 60 million parameters, on two GPUs for 5 to 6 days. It reached a top-5 error of 15.3% versus 26.2% for the runner-up. (Top-5 error means the correct label was not among the network's five best guesses.)
Its win combined the three ingredients: big labeled data (ImageNet), big compute (GPUs), and good ideas (a deep convolutional network, ReLU, dropout).
4. The role of GPUs
Training a network is mostly matrix multiplication: a layer's weighted sums for many inputs, done as a huge table of multiply-and-add steps. These steps are independent of each other, so they can be done at the same time ("parallel").


CPU
GPU
Cores
A few powerful cores (many desktop CPUs have roughly 8 to 16)
Thousands of simple cores (e.g., 5,760 on a GTX TITAN Z)
Strength
Complex tasks, one after another
The same simple calculation on lots of numbers at once
Fit for neural networks
Fine for small networks
Ideal: training is "embarrassingly parallel"

CPU and GPU usually work together: the CPU directs the program, and the GPU does the heavy parallel math.

Terminology
Term
Meaning
Parameter
A weight or bias the network learns
Labeled data
Examples that come with the correct answer (a photo tagged "cat")
Scaling laws
Predictable improvement in performance as data, model size and compute grow
ImageNet / ILSVRC
A large labeled image dataset and the yearly contest built on it
Top-5 error
Percentage of images where the right label is not in the network's top five guesses
Data augmentation
Creating extra training examples by altering existing ones (flip, crop)
Dropout
Randomly switching off neurons during training to reduce overfitting
CPU / GPU
General-purpose processor / processor with thousands of cores for parallel work
Parallel processing
Doing many calculations at the same time


Worked example: a small image network
A network takes a 28 × 28 image (784 pixel values), has a hidden layer of 128 neurons, and an output layer of 10 neurons (10 classes).
Step
Calculation
Result
1. Count parameters, hidden layer
784 × 128 weights + 128 biases
100,352 + 128 = 100,480
2. Count parameters, output layer
128 × 10 weights + 10 biases
1,280 + 10 = 1,290
3. Total parameters
100,480 + 1,290
101,770
4. Compare with data
100 examples vs 60,000 examples
100 ÷ 101,770 ≈ 0.001 vs 60,000 ÷ 101,770 ≈ 0.59 examples per parameter
5. Work for one batch
784 × 128 × 1,000 images (first layer only)
100,352,000 multiplications

What to notice:
With only 100 examples, the network has about 1,000 parameters for every example, so it can simply memorise them. With 60,000 examples the data is far better matched to the network's size.
Step 5 shows why GPUs matter: the 100 million multiplications for one batch's first layer are independent, so thousands of cores can share them.

Learner activity
Task 1. Count the parameters in a network with layers 100 → 50 → 5 (weights plus biases).
Task 2. Network A (from Task 1) and Network B (101,770 parameters) are both trained on only 500 examples. Which is at greater risk of overfitting, and what could you do to reduce the risk?
Task 3. In one or two sentences, explain why matrix multiplication suits a GPU better than a CPU.

Answers and expected outcomes
<details> <summary><b>Click to reveal</b></summary>
Task 1
Hidden layer: 100 × 50 = 5,000 weights + 50 biases = 5,050
Output layer: 50 × 5 = 250 weights + 5 biases = 255
Total = 5,305 parameters
Task 2
Network B is at greater risk. It has about 0.005 examples per parameter (500 ÷ 101,770), compared with about 0.09 for Network A (500 ÷ 5,305), so it has far more freedom to memorize.
Ways to reduce the risk: collect more (good) data, use data augmentation, apply dropout, use early stopping, or use a smaller network.
Task 3
Matrix multiplication is a huge number of independent multiply-add steps. A GPU's thousands of simple cores can do many of them at the same time, while a CPU's few cores must work through far more of them one after another.
Expected outcome: the learner can count a network's parameters, explain why many parameters need many examples, and name the three ingredients (data, parameters/model size, GPUs) behind the deep learning breakthroughs.
Teacher check: ask, "What three things came together for AlexNet's 2012 win?" A good answer: big labeled data (ImageNet's 1.2 million images), big compute (two GPUs), and strong ideas (a deep convolutional network with ReLU and dropout).
</details>

### References

1. Krizhevsky, A., Sutskever, I., & Hinton, G. E. (2012). ImageNet Classification with Deep Convolutional Neural Networks. *Advances in Neural Information Processing Systems 25*. https://proceedings.neurips.cc/paper_files/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf
2. Kaplan, J., et al. (2020). Scaling Laws for Neural Language Models. arXiv:2001.08361. https://arxiv.org/abs/2001.08361v1
3. Red Gate Simple Talk. "Deep Learning with GPU Acceleration." https://www.red-gate.com/simple-talk/business-intelligence/data-science/deep-learning-with-gpu-acceleration
4. apxml.com. "Comparing CPU and GPU Architectures." https://apxml.com/courses/planning-optimizing-ai-infrastructure/chapter-1-foundations-ai-compute-infrastructure/comparing-cpu-gpu-architectures
