## Chapter 4: Introduction to Connectionist AI


### 4.1 Context and History

Connectionist AI developed from the idea that computers could imitate certain aspects of how the human brain processes information. Instead of relying only on programmed rules, researchers explored networks of artificial neurons that could learn patterns from data [6].

Its development involved several important stages, including early neuron models, the perceptron, periods of setbacks, the revival of backpropagation, and the deep learning boom [6][9].

**Early Neuron Models**

The idea of artificial neurons began in the 1940s, when researchers Warren McCulloch and Walter Pitts introduced a mathematical model of a biological neuron in 1943 [1].

Their model showed how simplified artificial neurons could receive inputs and produce outputs based on logical operations. This became one of the earliest foundations of neural networks [1][6].

Unlike real biological neurons, these artificial neurons used mathematical calculations to represent how information could be processed [1][9].

**Main Idea:**
- Artificial neurons receive inputs.
- They process information using mathematical rules.
- They produce an output depending on the inputs.

**Visual Representation:**

    INPUTS
      |
      v
    +----------------+
    | Artificial     |
    | Neuron         |
    +----------------+
      |
      v
    OUTPUT

This early research introduced the possibility of building computer systems inspired by the human brain.

**The Perceptron**

In 1958, psychologist Frank Rosenblatt introduced the **Perceptron**, an early type of artificial neural network [2].

The perceptron was designed to learn how to classify information into different categories. It could adjust its weights based on training examples, allowing it to improve its predictions [2].

For example, a perceptron could be trained to distinguish between two categories by learning from examples of each category.

**How It Works:**

1. Receives input values.
2. Assigns weights to each input.
3. Calculates a weighted sum.
4. Uses an activation function to produce an output.
5. Adjusts its weights when its prediction is incorrect.

**Visual Representation:**

    INPUTS
      |
      v
    +------------------+
    | Assign Weights   |
    +------------------+
      |
      v
    +------------------+
    | Calculate Sum    |
    +------------------+
      |
      v
    +------------------+
    | Activation       |
    | Function         |
    +------------------+
      |
      v
    +------------------+
    | Classification   |
    +------------------+

The perceptron was an important development because it demonstrated that machines could learn from examples instead of relying entirely on manually written instructions [2][6].

However, early perceptrons had limitations. A single-layer perceptron could only solve problems that were linearly separable, meaning the categories could be separated using a straight line or a similar linear boundary [3].

**Setbacks in Connectionist AI**

Despite the early excitement surrounding perceptrons, researchers soon discovered important limitations.

In 1969, Marvin Minsky and Seymour Papert published a book called *Perceptrons*, which discussed the limitations of single-layer perceptrons [3].

One famous example was the **XOR problem** [3].

A single-layer perceptron could not correctly solve XOR because its outputs could not be separated using a single straight line [3].

**XOR Example:**

| Input A | Input B | Output |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

This problem demonstrated that simple perceptrons could not solve every type of classification task [3].

**Other Challenges:**
- Limited computing power made larger neural networks difficult to develop [4][6].
- Training more complex networks was challenging [4][6].
- Researchers lacked effective methods for adjusting weights across multiple layers [4][5].

As a result, interest and funding for neural network research decreased during periods often associated with the **AI Winter** [4][6].

**Visual Timeline:**

    Early Neural Networks
             |
             v
        Perceptron
             |
             v
      Technical Limitations
             |
             v
       Reduced Interest
             |
             v
          AI Winter

Although progress slowed, researchers continued exploring ways to improve neural networks.

**Revival of Backpropagation**

Interest in neural networks increased again during the 1980s, partly due to the development and wider recognition of **backpropagation** [5][6].

Backpropagation is a training algorithm that allows neural networks with multiple layers to adjust their weights more effectively [5].

Unlike a single-layer perceptron, a multi-layer neural network can learn more complicated patterns by processing information through hidden layers [5][8].

Backpropagation works by calculating the error between a network's prediction and the correct answer, then sending information about that error backward through the network to determine how its weights should change [5][8].

**How Backpropagation Works:**

1. The network receives input data.
2. It produces a prediction.
3. The prediction is compared with the correct answer.
4. The network calculates the error.
5. The error is propagated backward through the network.
6. The weights are adjusted to reduce the error.

**Visual Representation:**

          INPUT DATA
               |
               v
        +--------------+
        | Input Layer  |
        +--------------+
               |
               v
        +--------------+
        | Hidden Layer |
        +--------------+
               |
               v
        +--------------+
        | Output Layer |
        +--------------+
               |
               v
           PREDICTION
               |
               v
         Calculate Error
               |
               v
       BACKPROPAGATION
               |
               v
         Adjust Weights
               |
               +-------> Repeat Training

Backpropagation made it more practical to train multi-layer neural networks and helped researchers overcome some of the limitations of earlier models [5].

In 1986, David Rumelhart, Geoffrey Hinton, and Ronald Williams published influential research demonstrating how backpropagation could help neural networks learn internal representations [5].

This contributed significantly to the renewed interest in connectionist AI [5][6][9].

**The Deep Learning Boom**

During the 2000s and especially the 2010s, connectionist AI experienced major improvements due to advances in computing power, larger datasets, and better training techniques [6][8].

This period became known as the **Deep Learning Boom** [6].

Deep learning uses neural networks with multiple layers to learn increasingly complex patterns from data [8].

Several developments contributed to its growth:

- **More Data:** The growth of the internet created enormous amounts of digital data for training AI systems [6][7].
- **Greater Computing Power:** GPUs made it possible to train larger neural networks more efficiently [6][7].
- **Improved Algorithms:** New techniques helped neural networks train more effectively [6][8].
- **Better Results:** Deep learning achieved major improvements in tasks such as image recognition, speech recognition, and natural language processing [7][8].

**Important Milestone: AlexNet (2012)**

One major breakthrough occurred in 2012 when a deep neural network called **AlexNet** achieved outstanding results in the ImageNet image recognition competition [7].

AlexNet used multiple layers of artificial neurons and GPUs to recognize objects in images [7].

Its success demonstrated the potential of deep learning and encouraged further research and investment in neural networks [7][8].

**Visual Representation:**

    MORE DIGITAL DATA
            |
            v
    GREATER COMPUTING POWER
            |
            v
      IMPROVED ALGORITHMS
            |
            v
    +----------------------+
    |   DEEP NEURAL        |
    |   NETWORKS           |
    +----------------------+
            |
            v
      BETTER AI RESULTS
            |
     +------+------+------+
     |      |      |      |
     v      v      v      v
   Images Speech  Text  Other
          Recognition Processing Tasks

Today, deep learning is used in many areas, including [8]:
- Image and facial recognition.
- Speech recognition and voice assistants.
- Language translation.
- Recommendation systems.
- Generative AI tools.

**Historical Timeline**

| Year / Period | Development | Importance |
|---|---|---|
| 1943 | McCulloch and Pitts' artificial neuron model [1]. | Introduced an early mathematical model of artificial neurons. |
| 1958 | Rosenblatt's Perceptron [2]. | Demonstrated that machines could learn from examples. |
| 1969 | *Perceptrons* by Minsky and Papert [3]. | Highlighted limitations of single-layer perceptrons. |
| 1970s | AI Winter [4]. | Interest in neural network research decreased. |
| 1980s | Revival of backpropagation [5][6]. | Made training multi-layer neural networks more practical. |
| 1986 | Research by Rumelhart, Hinton, and Williams [5]. | Helped popularize backpropagation. |
| 2012 | AlexNet wins the ImageNet competition [7]. | Demonstrated the potential of deep learning. |
| 2010s–Present | Deep Learning Boom [6][8]. | Neural networks became widely used in modern AI applications. |

**References**

1. McCulloch, W. S. and Pitts, W. (1943). *A Logical Calculus of the Ideas Immanent in Nervous Activity.* Bulletin of Mathematical Biophysics, 5, 115–133. https://doi.org/10.1007/BF02478259
2. Rosenblatt, F. (1958). *The Perceptron: A Probabilistic Model for Information Storage and Organization in the Brain.* Psychological Review, 65(6), 386–408. https://doi.org/10.1037/h0042519
3. Minsky, M. and Papert, S. (1969). *Perceptrons: An Introduction to Computational Geometry.* MIT Press.
4. Russell, S. and Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. Chapter 1 (history of AI).
5. Rumelhart, D. E., Hinton, G. E., and Williams, R. J. (1986). *Learning Representations by Back-Propagating Errors.* Nature, 323, 533–536. https://doi.org/10.1038/323533a0
6. Goodfellow, I., Bengio, Y., and Courville, A. (2016). *Deep Learning.* MIT Press, Chapter 1 (Section 1.2, Historical Trends in Deep Learning). https://www.deeplearningbook.org/
7. Krizhevsky, A., Sutskever, I., and Hinton, G. E. (2012). *ImageNet Classification with Deep Convolutional Neural Networks.* Advances in Neural Information Processing Systems 25. https://proceedings.neurips.cc/paper_files/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf
8. LeCun, Y., Bengio, Y., and Hinton, G. (2015). *Deep Learning.* Nature, 521, 436–444. https://doi.org/10.1038/nature14539
9. Shao, F. and Shen, Z. (2023). *How Can Artificial Neural Networks Approximate the Brain?* Frontiers in Psychology, 13, 970214. https://doi.org/10.3389/fpsyg.2022.970214

---

### 4.2 Key Characteristics

Connectionist AI has several important characteristics that explain how it learns and processes information. These characteristics are inspired by the way the human brain works [2][3].

**Requires a Lot of Data**

Connectionist AI often requires a large amount of data to learn effectively [2][4]. Instead of relying entirely on instructions written by humans, it studies examples to recognize patterns [1].

For example, if we want to teach an AI to recognize cats, we need to provide it with many pictures of cats. These pictures should include different breeds, colors, sizes, and positions. By studying these examples, the AI can learn to recognize cats in new pictures [1].

**Many Simple Units Working in Parallel**

Connectionist AI uses many small processing units called artificial neurons. Each neuron performs a relatively simple calculation, but thousands or millions of neurons can work together to complete complex tasks [2][3].

For example, when recognizing a face, different groups of neurons may learn to recognize eyes, noses, mouths, and other facial features. Together, these patterns help the AI identify the face [1].

**Visual Representation:**

    INPUT: FACE IMAGE
           |
    +------+------+------+
    |      |      |      |
    v      v      v
    +----+ +----+ +----+
    | G1 | | G2 | | G3 |
    +----+ +----+ +----+
      |      |      |
      v      v      v
     Eyes   Nose   Mouth
      |      |      |
      +------+------+ 
             |
             v
      COMBINE PATTERNS
             |
             v
       FACE RECOGNIZED

**Tolerates Noisy Input**

Noisy input refers to information that is unclear, incomplete, distorted, or contains unwanted details.

Connectionist AI can sometimes recognize patterns even when the input is not perfect [5].

For example, an AI trained to recognize handwritten numbers may still identify the number 8 even if the handwriting is messy, tilted, or slightly distorted. This is possible because it has learned patterns from many handwriting examples [5].

**Example:**

| Input | Result |
|---|---|
| Clearly written `8` | Recognized as 8 |
| Tilted `8` | Recognized as 8 |
| Messy handwritten `8` | May still be recognized as 8 |

**Learns from Examples**

Connectionist AI learns by studying examples instead of requiring humans to manually program every possible rule [1][2].

For example, to teach an AI to recognize spam emails, we provide it with many emails labeled as either "Spam" or "Not Spam". The AI studies the patterns in these emails and uses what it learns to classify new messages [1].

**Learning Process:**

    TRAINING EXAMPLES
           |
           v
    +----------------+
    | Neural Network |
    +----------------+
           |
           v
     Studies Patterns
           |
           v
     Adjusts Connections
           |
           v
       Learns Patterns
           |
           v
     Classifies New Emails

**References**

1. LeCun, Y., Bengio, Y., and Hinton, G. (2015). *Deep Learning.* Nature, 521, 436–444 (see "Supervised learning" and the discussion of layers of learned features). https://doi.org/10.1038/nature14539
2. Goodfellow, I., Bengio, Y., and Courville, A. (2016). *Deep Learning.* MIT Press, Chapter 1 (Section 1.2, Historical Trends in Deep Learning). https://www.deeplearningbook.org/
3. Rumelhart, D. E., McClelland, J. L., and the PDP Research Group (1986). *Parallel Distributed Processing: Explorations in the Microstructure of Cognition, Volume 1: Foundations.* MIT Press.
4. Krizhevsky, A., Sutskever, I., and Hinton, G. E. (2012). *ImageNet Classification with Deep Convolutional Neural Networks.* Advances in Neural Information Processing Systems 25. https://proceedings.neurips.cc/paper_files/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf
5. LeCun, Y., Bottou, L., Bengio, Y., and Haffner, P. (1998). *Gradient-Based Learning Applied to Document Recognition.* Proceedings of the IEEE, 86(11), 2278–2324. https://doi.org/10.1109/5.726791

---

### 4.3 Knowledge Stored in Connections

In Connectionist AI, knowledge is represented through the connections between artificial neurons [1][4]. These connections have numerical values called **weights**, which determine how strongly one neuron influences another [1][4].

**Weights as Memory**

Weights act like a form of memory in a neural network. They represent the importance of different connections and patterns learned during training [1].

For example, when learning to recognize cats, a neural network may develop stronger responses to patterns such as pointed ears, whiskers, and certain facial features. These learned patterns are reflected in the network's weights [5].

**Visual Representation:**

    NEURON A                    NEURON C
    +---------+                 +---------+
    |         |                 |         |
    |    A    |---------------->|    C    |
    |         |   Weight: 0.8   |         |
    +---------+                 +---------+
                                     ^
                                     |
    NEURON B                         |
    +---------+                      |
    |         |----------------------+
    |    B    |    Weight: 0.3
    |         |
    +---------+

A higher weight means that a connection has a stronger influence on the receiving neuron. A lower weight means that its influence is weaker [4].

**Learning Through Adjusting Weights**

Learning in a neural network happens when its weights are adjusted to improve predictions. During training, the network makes predictions, compares them with the correct answers, and adjusts its weights to reduce mistakes [2][5].

For example, if an AI incorrectly identifies an apple as an orange, its training process adjusts the weights so that it can become better at distinguishing between the two objects.

One common method used to adjust weights is called **backpropagation** [2][5].

**Learning Process:**

    INPUT DATA
        |
        v
    +----------------+
    | Neural Network |
    +----------------+
        |
        v
     Prediction
        |
        v
    Compare with Correct Answer
        |
        v
     Calculate Error
        |
        v
     Adjust Weights
        |
        +-----------> Repeat Training

The process repeats during training so that the network can gradually improve its predictions [2].

**Distributed Representations**

Distributed representation means that knowledge is spread across multiple artificial neurons instead of being stored in just one neuron [3][4].

For example, when recognizing a car, different neurons may respond to its color, shape, wheels, and other features. Together, these neurons create a representation of the object [3][5].

**Visual Representation:**

          OBJECT: RED CAR
                |
       +--------+--------+
       |        |        |
       v        v        v
    +------+ +------+ +------+
    | Red  | | Shape| |Wheels|
    |Color | |      | |      |
    +------+ +------+ +------+
       |        |        |
       +--------+--------+
                |
                v
      COMBINED REPRESENTATION
                |
                v
          RECOGNIZES
            RED CAR

This allows the network to recognize different objects using combinations of learned patterns [3].

**Simple Analogy:**

Think of a group project. One student knows about colors, another understands shapes, and another recognizes objects. Together, they can identify different things. No single student holds all the knowledge.

**References**

1. Rumelhart, D. E., McClelland, J. L., and the PDP Research Group (1986). *Parallel Distributed Processing: Explorations in the Microstructure of Cognition, Volume 1: Foundations.* MIT Press.
2. Rumelhart, D. E., Hinton, G. E., and Williams, R. J. (1986). *Learning Representations by Back-Propagating Errors.* Nature, 323, 533–536. https://doi.org/10.1038/323533a0
3. Hinton, G. E., McClelland, J. L., and Rumelhart, D. E. (1986). *Distributed Representations.* In *Parallel Distributed Processing, Volume 1* (pp. 77–109). MIT Press.
4. Goodfellow, I., Bengio, Y., and Courville, A. (2016). *Deep Learning.* MIT Press, Chapter 6 (Deep Feedforward Networks) and Chapter 15 (Representation Learning). https://www.deeplearningbook.org/
5. LeCun, Y., Bengio, Y., and Hinton, G. (2015). *Deep Learning.* Nature, 521, 436–444. https://doi.org/10.1038/nature14539

---

### 4.4 Traditional Machine Learning

Traditional machine learning and Connectionist AI are both approaches to machine learning. However, they can differ in how they process data, use computing resources, and identify important features [1][2].

**Data and Computing Requirements**

Traditional machine learning models can often work with smaller datasets and require less computing power, depending on the task [1].

In comparison, connectionist models, especially deep neural networks, often benefit from larger datasets and more computing power because they learn complex patterns through multiple layers of artificial neurons [1][2].

For example, a traditional machine learning model predicting house prices might use information such as house size, location, and number of bedrooms. A neural network can also use these features while learning more complicated relationships between them.

**Comparison:**

| Traditional Machine Learning | Connectionist AI |
|---|---|
| Can often work with smaller datasets [1]. | Often benefits from larger datasets [1][2]. |
| Usually requires less computing power [1]. | Can require more computing power [1][2]. |
| Often uses manually selected features [2][3]. | Can automatically learn features [2][3]. |

**Hand-Made Features vs. Learned Features**

A feature is a piece of information that helps an AI make a prediction.

In traditional machine learning, humans often select and prepare the features that the model will use. This process is called **feature engineering** [2][3].

For example, when creating a system to recognize cats, humans might manually select features such as fur color, ear shape, and eye shape. The model then learns how to use these features.

In Connectionist AI, especially deep learning, neural networks can automatically learn useful features from the training data [2][3].

For example [2]:
- Early layers may recognize edges and simple shapes.
- Middle layers may recognize parts of objects.
- Later layers may recognize complex patterns, such as a cat's face.

**Visual Comparison:**

    TRADITIONAL MACHINE LEARNING

             CAT IMAGE
                 |
                 v
        HUMAN SELECTS FEATURES
                 |
         +-------+-------+
         |       |       |
         v       v       v
        Fur     Ears    Eyes
         |       |       |
         +-------+-------+
                 |
                 v
         MACHINE LEARNING
                 |
                 v
             PREDICTION


          CONNECTIONIST AI

             CAT IMAGE
                 |
                 v
         +---------------+
         | Neural Network|
         +---------------+
                 |
                 v
         Learns Simple Features
                 |
                 v
         Learns Complex Features
                 |
                 v
             PREDICTION

**Comparison Table**

| Traditional Machine Learning | Connectionist AI |
|---|---|
| Humans often select important features [2][3]. | The network can learn features automatically [2][3]. |
| Can often work with smaller datasets [1]. | Often benefits from larger datasets [1][2]. |
| Usually requires less computing power [1]. | Can require more computing power [1][2]. |
| Often easier to interpret [4]. | Can be harder to interpret [4]. |

**References**

1. Goodfellow, I., Bengio, Y., and Courville, A. (2016). *Deep Learning.* MIT Press, Chapter 1 (Introduction) and Chapter 5 (Machine Learning Basics). https://www.deeplearningbook.org/
2. LeCun, Y., Bengio, Y., and Hinton, G. (2015). *Deep Learning.* Nature, 521, 436–444. https://doi.org/10.1038/nature14539
3. Bengio, Y., Courville, A., and Vincent, P. (2013). *Representation Learning: A Review and New Perspectives.* IEEE Transactions on Pattern Analysis and Machine Intelligence, 35(8), 1798–1828. https://doi.org/10.1109/TPAMI.2013.50
4. Rudin, C. (2019). *Stop Explaining Black Box Machine Learning Models for High Stakes Decisions and Use Interpretable Models Instead.* Nature Machine Intelligence, 1, 206–215. https://doi.org/10.1038/s42256-019-0048-x

---

### 4.5 Biological vs Artificial Neuron, Connectionist vs Symbolic AI

Connectionist AI was inspired by the way the human brain processes information. However, artificial neurons are simplified mathematical models rather than exact copies of biological neurons [3][5].

**Biological Neurons**

A biological neuron is a specialized nerve cell that receives, processes, and sends information throughout the nervous system [1].

Its main parts include [1]:

| Part | Function |
|---|---|
| Dendrites | Receive signals from other neurons. |
| Cell Body (Soma) | Combines and processes incoming signals. |
| Axon | Carries signals away from the cell body. |
| Synapses | Connection points where neurons communicate. |

**Visual Representation:**

          DENDRITES
         \    |    /
          \   |   /
           \  |  /
         +---------+
         |  CELL   |
         |  BODY   |
         |  (SOMA) |
         +---------+
              |
              |
              v
       ====================>
               AXON
                           |
                           v
                     AXON TERMINALS
                           |
                           v
                        SYNAPSES
                           |
                           v
                      NEXT NEURON

**How Does It Work?**

1. Dendrites receive signals from other neurons [1].
2. The cell body combines these signals [1][2].
3. If the neuron reaches the necessary activation threshold, it produces an electrical impulse [2].
4. The axon carries the impulse to other cells [1][2].

**Artificial Neurons**

An artificial neuron is a simplified mathematical model inspired by a biological neuron [3][4]. Instead of using real electrical and chemical signals, it processes numerical information [4].

Its main components include [4]:

| Component | Function |
|---|---|
| Inputs | Receive numerical information. |
| Weights | Determine the importance of each input. |
| Bias | A learnable number added to the weighted sum. It shifts how easily the neuron activates. |
| Summation | Combines the weighted inputs and the bias. |
| Activation Function | Determines the neuron's output. |
| Output | Passes processed information to other neurons. |

**Visual Representation:**

    INPUTS              PROCESSING             OUTPUT

    x₁ ---- w₁ ---\
                   \
    x₂ ---- w₂ ----+---> Weighted Sum + Bias (b)
                   /          |
    x₃ ---- w₃ ---/           v
                         Activation
                           Function
                              |
                              v
                            OUTPUT

Each input has a weight that determines how much it contributes to the final result [4]. The bias is one extra number for the whole neuron, not for each input. Weights and biases together are the network's **parameters**: the numbers that are adjusted during training [4].

For example, imagine an artificial neuron deciding whether an email is spam. It receives information about suspicious words, unknown links, and the sender. It combines these inputs and produces an output that contributes to the spam prediction.

**Biological vs Artificial Neurons**

| Biological Neuron | Artificial Neuron |
|---|---|
| Dendrites receive signals [1]. | Inputs receive numerical information [4]. |
| Synapses influence signal strength [1][2]. | Weights control connection strength [4]. |
| The neuron needs to reach an activation threshold [2]. | The bias shifts how easily the neuron activates [4]. |
| Cell body combines incoming signals [1]. | Summation combines weighted inputs [4]. |
| Neuron activation produces an electrical impulse [2]. | Activation function calculates an output [4]. |
| Axon transmits signals [1]. | Output passes information onward [4]. |

Although both neurons receive and process information, biological neurons use complex electrical and chemical processes, while artificial neurons perform mathematical calculations [1][5].

**Connectionist AI vs Symbolic AI**

Connectionist AI and Symbolic AI are two different approaches to creating artificial intelligence. They mainly differ in how they represent knowledge and solve problems [5][6][7].

Connectionist AI learns patterns from examples through interconnected artificial neurons. Its knowledge is represented through connection weights that are adjusted during training [4][5].

Symbolic AI uses predefined rules, symbols, and logical reasoning. Instead of learning everything from examples, it follows instructions created by humans [6][7].

For example, imagine creating an AI system to determine whether someone qualifies for a student discount.

- **Symbolic AI:** Uses a predefined rule such as "IF the person is a student, THEN they qualify for a student discount."
- **Connectionist AI:** Learns patterns from examples of people who qualify and do not qualify for the discount.

**Visual Comparison:**

    ARTIFICIAL INTELLIGENCE
              |
       +------+------+
       |             |
       v             v
  CONNECTIONIST AI  SYMBOLIC AI
       |             |
       v             v
  Training Examples Written Rules
       |             |
       v             v
  Neural Network   Logical Reasoning
       |             |
       v             v
  Learned Patterns  Decision
       |             |
       v             v
   Prediction       Output

**Comparison Table**

| Comparison | Connectionist AI | Symbolic AI |
|---|---|---|
| Main Approach | Learns patterns from data [5]. | Uses predefined rules and logic [6][7]. |
| Knowledge | Stored in connection weights [4]. | Stored as symbols and rules [6]. |
| Learning | Adjusts weights during training [4]. | Rules are often manually created [7]. |
| Data Requirements | Often needs many training examples [4]. | Can work with relatively little training data [7]. |
| Best Suited For | Pattern recognition and complex data [4]. | Explicit rules and logical reasoning [6][7]. |
| Example | Image recognition neural networks [4]. | Rule-based expert systems [7]. |

**Explainability**

Explainability refers to how easily humans can understand why an AI system produces a particular result [8][9].

Symbolic AI is generally easier to explain because its decisions follow explicit rules that can be examined [7][8].

Connectionist AI can be harder to explain because its decisions may depend on thousands or millions of interconnected weights. This makes it difficult to identify exactly how each connection contributes to a prediction [8][9].

For this reason, neural networks are sometimes described as **black-box models** [8].

**Example: Loan Application**

Imagine an AI system deciding whether to approve a loan application.

- **Symbolic AI:** Might reject the application because the applicant does not meet a specific written requirement.
- **Connectionist AI:** Might reject the application based on many learned patterns, without providing a simple explanation of how each factor contributed.

**References**

1. National Institute of Neurological Disorders and Stroke (NINDS). *Life and Death of a Neuron (Brain Basics).* https://www.ninds.nih.gov/publications/life-and-death-neuron-brain-basics
2. Kandel, E. R., Koester, J. D., Mack, S. H., and Siegelbaum, S. A. (2021). *Principles of Neural Science* (6th ed.). McGraw-Hill.
3. McCulloch, W. S. and Pitts, W. (1943). *A Logical Calculus of the Ideas Immanent in Nervous Activity.* Bulletin of Mathematical Biophysics, 5, 115–133. https://doi.org/10.1007/BF02478259
4. Goodfellow, I., Bengio, Y., and Courville, A. (2016). *Deep Learning.* MIT Press, Chapter 6 (Deep Feedforward Networks). https://www.deeplearningbook.org/
5. Shao, F. and Shen, Z. (2023). *How Can Artificial Neural Networks Approximate the Brain?* Frontiers in Psychology, 13, 970214. https://doi.org/10.3389/fpsyg.2022.970214
6. Newell, A. and Simon, H. A. (1976). *Computer Science as Empirical Inquiry: Symbols and Search.* Communications of the ACM, 19(3), 113–126. https://doi.org/10.1145/360018.360022
7. Russell, S. and Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. Chapter 1.
8. Rudin, C. (2019). *Stop Explaining Black Box Machine Learning Models for High Stakes Decisions and Use Interpretable Models Instead.* Nature Machine Intelligence, 1, 206–215. https://doi.org/10.1038/s42256-019-0048-x
9. Phillips, P. J. et al. (2021). *Four Principles of Explainable Artificial Intelligence.* NISTIR 8312, National Institute of Standards and Technology. https://doi.org/10.6028/NIST.IR.8312
