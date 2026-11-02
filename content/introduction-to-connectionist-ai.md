# 1.2 Key Characteristics

Connectionist AI has several important characteristics that explain how it learns and processes information. These characteristics are inspired by the way the human brain works.

**Requires a Lot of Data**

Connectionist AI often requires a large amount of data to learn effectively. Instead of relying entirely on instructions written by humans, it studies examples to recognize patterns.

For example, if we want to teach an AI to recognize cats, we need to provide it with many pictures of cats. These pictures should include different breeds, colors, sizes, and positions. By studying these examples, the AI can learn to recognize cats in new pictures.

**Many Simple Units Working in Parallel**

Connectionist AI uses many small processing units called artificial neurons. Each neuron performs a relatively simple calculation, but thousands or millions of neurons can work together to complete complex tasks.

For example, when recognizing a face, different groups of neurons may learn to recognize eyes, noses, mouths, and other facial features. Together, these patterns help the AI identify the face.

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

Connectionist AI can sometimes recognize patterns even when the input is not perfect.

For example, an AI trained to recognize handwritten numbers may still identify the number 8 even if the handwriting is messy, tilted, or slightly distorted. This is possible because it has learned patterns from many handwriting examples.

**Example:**

| Input | Result |
|---|---|
| Clearly written `8` | Recognized as 8 |
| Tilted `8` | Recognized as 8 |
| Messy handwritten `8` | May still be recognized as 8 |

**Learns from Examples**

Connectionist AI learns by studying examples instead of requiring humans to manually program every possible rule.

For example, to teach an AI to recognize spam emails, we provide it with many emails labeled as either "Spam" or "Not Spam". The AI studies the patterns in these emails and uses what it learns to classify new messages.

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

---

# 1.3 Knowledge Stored in Connections

In Connectionist AI, knowledge is represented through the connections between artificial neurons. These connections have numerical values called **weights**, which determine how strongly one neuron influences another.

**Weights as Memory**

Weights act like a form of memory in a neural network. They represent the importance of different connections and patterns learned during training.

For example, when learning to recognize cats, a neural network may develop stronger responses to patterns such as pointed ears, whiskers, and certain facial features. These learned patterns are reflected in the network's weights.

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

A higher weight means that a connection has a stronger influence on the receiving neuron. A lower weight means that its influence is weaker.

**Learning Through Adjusting Weights**

Learning in a neural network happens when its weights are adjusted to improve predictions. During training, the network makes predictions, compares them with the correct answers, and adjusts its weights to reduce mistakes.

For example, if an AI incorrectly identifies an apple as an orange, its training process adjusts the weights so that it can become better at distinguishing between the two objects.

One common method used to adjust weights is called **backpropagation**.

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

The process repeats during training so that the network can gradually improve its predictions.

**Distributed Representations**

Distributed representation means that knowledge is spread across multiple artificial neurons instead of being stored in just one neuron.

For example, when recognizing a car, different neurons may respond to its color, shape, wheels, and other features. Together, these neurons create a representation of the object.

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

This allows the network to recognize different objects using combinations of learned patterns.

**Simple Analogy:**

Think of a group project. One student knows about colors, another understands shapes, and another recognizes objects. Together, they can identify different things. No single student holds all the knowledge.

---

# 1.4 Traditional Machine Learning

Traditional machine learning and Connectionist AI are both approaches to machine learning. However, they can differ in how they process data, use computing resources, and identify important features.

**Data and Computing Requirements**

Traditional machine learning models can often work with smaller datasets and require less computing power, depending on the task.

In comparison, connectionist models, especially deep neural networks, often benefit from larger datasets and more computing power because they learn complex patterns through multiple layers of artificial neurons.

For example, a traditional machine learning model predicting house prices might use information such as house size, location, and number of bedrooms. A neural network can also use these features while learning more complicated relationships between them.

**Comparison:**

| Traditional Machine Learning | Connectionist AI |
|---|---|
| Can often work with smaller datasets. | Often benefits from larger datasets. |
| Usually requires less computing power. | Can require more computing power. |
| Often uses manually selected features. | Can automatically learn features. |

**Hand-Made Features vs. Learned Features**

A feature is a piece of information that helps an AI make a prediction.

In traditional machine learning, humans often select and prepare the features that the model will use. This process is called **feature engineering**.

For example, when creating a system to recognize cats, humans might manually select features such as fur color, ear shape, and eye shape. The model then learns how to use these features.

In Connectionist AI, especially deep learning, neural networks can automatically learn useful features from the training data.

For example:
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
| Humans often select important features. | The network can learn features automatically. |
| Can often work with smaller datasets. | Often benefits from larger datasets. |
| Usually requires less computing power. | Can require more computing power. |
| Often easier to interpret. | Can be harder to interpret. |

---

# 1.5 Biological vs Artificial Neuron; Connectionist vs Symbolic AI

Connectionist AI was inspired by the way the human brain processes information. However, artificial neurons are simplified mathematical models rather than exact copies of biological neurons.

**Biological Neurons**

A biological neuron is a specialized nerve cell that receives, processes, and sends information throughout the nervous system.

Its main parts include:

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

1. Dendrites receive signals from other neurons.
2. The cell body combines these signals.
3. If the neuron reaches the necessary activation threshold, it produces an electrical impulse.
4. The axon carries the impulse to other cells.

**Artificial Neurons**

An artificial neuron is a simplified mathematical model inspired by a biological neuron. Instead of using real electrical and chemical signals, it processes numerical information.

Its main components include:

| Component | Function |
|---|---|
| Inputs | Receive numerical information. |
| Weights | Determine the importance of each input. |
| Summation | Combines the weighted inputs. |
| Activation Function | Determines the neuron's output. |
| Output | Passes processed information to other neurons. |

**Visual Representation:**

    INPUTS              PROCESSING             OUTPUT

    x₁ ---- w₁ ---\
                   \
    x₂ ---- w₂ ----+---> Weighted Sum
                   /          |
    x₃ ---- w₃ ---/           v
                         Activation
                           Function
                              |
                              v
                            OUTPUT

Each input has a weight that determines how much it contributes to the final result.

For example, imagine an artificial neuron deciding whether an email is spam. It receives information about suspicious words, unknown links, and the sender. It combines these inputs and produces an output that contributes to the spam prediction.

**Biological vs Artificial Neurons**

| Biological Neuron | Artificial Neuron |
|---|---|
| Dendrites receive signals. | Inputs receive numerical information. |
| Synapses influence signal strength. | Weights control connection strength. |
| Cell body combines incoming signals. | Summation combines weighted inputs. |
| Neuron activation produces an electrical impulse. | Activation function calculates an output. |
| Axon transmits signals. | Output passes information onward. |

Although both neurons receive and process information, biological neurons use complex electrical and chemical processes, while artificial neurons perform mathematical calculations.

**Connectionist AI vs Symbolic AI**

Connectionist AI and Symbolic AI are two different approaches to creating artificial intelligence. They mainly differ in how they represent knowledge and solve problems.

Connectionist AI learns patterns from examples through interconnected artificial neurons. Its knowledge is represented through connection weights that are adjusted during training.

Symbolic AI uses predefined rules, symbols, and logical reasoning. Instead of learning everything from examples, it follows instructions created by humans.

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
| Main Approach | Learns patterns from data. | Uses predefined rules and logic. |
| Knowledge | Stored in connection weights. | Stored as symbols and rules. |
| Learning | Adjusts weights during training. | Rules are often manually created. |
| Data Requirements | Often needs many training examples. | Can work with relatively little training data. |
| Best Suited For | Pattern recognition and complex data. | Explicit rules and logical reasoning. |
| Example | Image recognition neural networks. | Rule-based expert systems. |

**Explainability**

Explainability refers to how easily humans can understand why an AI system produces a particular result.

Symbolic AI is generally easier to explain because its decisions follow explicit rules that can be examined.

Connectionist AI can be harder to explain because its decisions may depend on thousands or millions of interconnected weights. This makes it difficult to identify exactly how each connection contributes to a prediction.

For this reason, neural networks are sometimes described as **black-box models**.

**Example: Loan Application**

Imagine an AI system deciding whether to approve a loan application.

- **Symbolic AI:** Might reject the application because the applicant does not meet a specific written requirement.
- **Connectionist AI:** Might reject the application based on many learned patterns, without providing a simple explanation of how each factor contributed.
