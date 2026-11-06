# Section 3: Where Big Data Meets Connectionist AI
## Chapter 1. Why Big Data Fuels Neural Networks

Explanations
Neural networks became powerful when three things arrived together: lots of data, networks with many parameters, and fast hardware (GPUs) to train them.
flowchart LR
    D["📦 Big data<br/>many examples"] --> B["🚀 Deep learning<br/>breakthroughs"]
    P["🧠 Many parameters<br/>big networks"] --> B
    G["⚡ GPUs<br/>fast parallel math"] --> B
    B -->|"success attracts<br/>more data and investment"| D
    
1. More data gives better learning
A network learns patterns from examples. More (and more varied) examples help it find the real pattern instead of memorizing quirks, which means less overfitting and better generalization (see Overfitting and Generalization). Research on language models found that test loss falls predictably as dataset size, model size and training compute increase, a result called scaling laws.
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


## Chapter 2. Preparing Data for a Network

When Big Data meets Connectionist AI, large amounts of data are used to train artificial neural networks (ANNs). However, before a neural network can learn, the data must be prepared properly.

**Preparing data for a network** means organizing, cleaning, and arranging information so that an AI model can understand patterns and make predictions.

For example, imagine you want to train an AI to recognize pictures of cats and dogs. Before training, you need to prepare the pictures, give them labels, organize them, and divide them into different groups.

There are six important steps:

### 1. Features and Labels

**Features** are the pieces of information a model learns from. A picture is made of tiny dots called **pixels**. Each pixel is stored as a number for its color and brightness. These numbers are the features the network receives.

**Labels** are the correct answers that the AI is supposed to predict.

For example, if an AI learns to recognize cats and dogs from pictures:

- Features: the **pixel values** of each picture (numbers for the color and brightness of each tiny dot). A neural network learns patterns such as ears, whiskers, and fur by itself (see Connectionist AI 1.4).
- Labels: Cat or Dog.

In traditional machine learning, people often choose the features by hand. A neural network learns them from the pixels.

| Patterns a person can see in the picture | Label (Correct answer) |
|---|---|
| Pointed ears, whiskers, small body | Cat |
| Long ears, larger body, different fur | Dog |
| Round face, whiskers, fluffy fur | Cat |

#### How it works
1. The AI receives information (features).
2. It examines the characteristics.
3. It learns how those characteristics relate to the correct answers (labels).
4. It uses what it learned to make predictions about new data.

**Simple example:** A student learns to identify fruits by looking at their colors, shapes, and sizes. The fruit's name is the correct answer.

### 2. Cleaning and Scaling

Before training, data needs to be cleaned and sometimes scaled.

**Data Cleaning** means fixing or removing incorrect, incomplete, or duplicated information.

Examples:
- Removing duplicate pictures.
- Fixing spelling mistakes.
- Filling in missing information.
- Removing incorrect entries.

**Data Scaling** means adjusting numbers so that they are within a suitable range, making it easier for a neural network to learn. One common method is **min-max scaling**:

```text
scaled value = (value - smallest value) / (largest value - smallest value)
```

| Information | Original value | Smallest in the data | Largest in the data | Scaled value |
|---|---:|---:|---:|---:|
| Age | 12 | 10 | 20 | 0.20 |
| Height (cm) | 170 | 140 | 190 | 0.60 |
| Weight (kg) | 60 | 40 | 90 | 0.40 |

**Worked line:** an age of 12, in data where the youngest is 10 and the oldest is 20, gives (12 - 10) / (20 - 10) = 2 / 10 = **0.20**.

> **Important:** work out the smallest and largest values from the **training data only**, then use the same numbers on the validation and testing data. Think of a student who sees the exam questions before the exam. Their score would look great but would not show what they really learned. If the scaling uses the testing data, the test is spoiled in the same way. This is called **data leakage** (see Connectionist AI 2.3). Remove duplicate pictures before splitting, so the same picture is not in both the training and testing groups.

*These scaled values are illustrative, not calculated using one shared scaling formula.*

#### Why is it important?
- Cleaning prevents incorrect information from confusing the AI.
- Scaling helps prevent numbers with very different ranges from dominating the learning process.

**Simple example:** Before doing a school project, you organize your notes, remove repeated information, and arrange your numbers into a consistent format.

### 3. Splitting Data

**Data Splitting** means dividing a dataset into separate groups for different purposes.

There are three common groups:

| Dataset | Purpose |
|---|---|
| Training data | Used to teach the AI. |
| Validation data | Used to check and improve the model during development. |
| Testing data | Used to evaluate the final model using data it has not trained on. |

For example, imagine 700 pictures are set aside for training (see Splitting Data).

Instead of processing all 700 pictures at once, you divide them into batches of 100.

| Batch | Number of pictures |
|---|---:|
| Batch 1 | 100 |
| Batch 2 | 100 |
| Batch 3 | 100 |
| Batch 4 | 100 |
| Batch 5 | 100 |
| Batch 6 | 100 |
| Batch 7 | 100 |

#### How it works
1. The AI learns from the training data.
2. Developers use validation data to adjust the model.
3. Testing data checks how well the model performs on unfamiliar pictures.

**Why is it important?**

It helps determine whether the AI has actually learned patterns or simply memorized its training examples.

### 4. Class Imbalance

**Class Imbalance** happens when a dataset contains significantly more examples of one category than another.

For example, imagine an AI trained to recognize cats and dogs:

| Category | Number of pictures |
|---|---:|
| Cats | 900 |
| Dogs | 100 |

The dataset has many more cat pictures than dog pictures.

#### Why is this a problem?

The AI may become better at recognizing cats because it sees them much more frequently. It might struggle to recognize dogs.

#### How can we solve it?
> **Important:** apply oversampling, undersampling, and class weighting to the **training data only**, after the split. Otherwise, copies of the same picture can end up in both the training and testing groups.
- **Oversampling:** Adding or repeating examples from the smaller category.
- **Undersampling:** Reducing examples from the larger category.
- **Class weighting:** Giving more importance to mistakes involving the less common category.

**Simple example:** Imagine a class where 90 students study English and only 10 study Mandarin. If a teacher only focuses on the majority, the Mandarin students may receive less attention.

### 5. Batching

**Batching** means dividing a large dataset into smaller groups called *batches* so that a neural network can process the data more efficiently.

For example, imagine you have 1,000 pictures to train an AI.

Instead of processing all 1,000 pictures at once, you divide them into batches of 100.

| Batch | Number of pictures |
|---|---:|
| Batch 1 | 100 |
| Batch 2 | 100 |
| Batch 3 | 100 |
| Batch 4 | 100 |
| Batch 5 | 100 |
| Batch 6 | 100 |
| Batch 7 | 100 |
| Batch 8 | 100 |
| Batch 9 | 100 |
| Batch 10 | 100 |

#### How it works
1. The AI processes the first batch.
2. It learns from the information.
3. It updates its internal parameters (the values it adjusts while learning).
4. It moves to the next batch.
5. This continues until all batches have been processed.

#### Why is it important?
- Makes large datasets easier to process.
- Helps manage computer memory.
- Allows the AI to update its learning gradually.

**Simple example:** Instead of studying 1,000 pages in one sitting, you study 100 pages at a time.

### 6. Putting Everything Together

Here is how all six steps connect when preparing Big Data for a neural network.

The overall process:

1. **Features and Labels:** Identify the information the AI needs and the correct answers.
2. **Cleaning and Scaling:** Fix incorrect data and adjust numerical values (work out the scaling numbers from the training data only).
3. **Splitting:** Divide the dataset into training, validation, and testing groups.
4. **Class Imbalance:** Make sure the AI does **not** favor categories with more examples.
5. **Batching:** Divide the training data into smaller groups for processing.
6. **Training:** Feed the prepared batches into the neural network so it can learn patterns.

### Summary Table

| Topic | Simple meaning | Main purpose |
|---|---|---|
| Features and Labels | Inputs and correct answers | Help AI learn relationships |
| Cleaning and Scaling | Fixing and adjusting data | Improve data quality |
| Splitting | Dividing data into groups | Evaluate AI performance |
| Class Imbalance | Unequal category examples | Stop the AI from favoring the larger category |
| Batching | Processing smaller groups | Manage training efficiently |

### Understanding the Connection to Big Data and Connectionist AI

- **Big Data** provides large amounts of information for AI to learn from.
- **Data preparation** organizes that information into a usable format.
- **Connectionist AI** uses artificial neural networks to identify patterns and relationships in the data.
- **Training** allows the network to adjust its internal parameters based on what it learns.

One important thing to remember: data preparation directly affects how well a neural network learns. Poor-quality data can lead to inaccurate predictions, even if the AI model itself is advanced.

**In simple terms:** Big Data gives AI the information, data preparation gets that information ready, and Connectionist AI uses it to learn.

### References for Further Reading

1. [Google Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course) – Machine learning fundamentals and data preparation.
2. [Scikit-learn: Preprocessing Data](https://scikit-learn.org/stable/modules/preprocessing.html) – Data cleaning, scaling, and preprocessing.
3. [TensorFlow: tf.data Guide](https://www.tensorflow.org/guide/data) – Preparing datasets and batching for neural networks.
4. [Imbalanced-learn Documentation](https://imbalanced-learn.org/stable/) – Understanding and handling class imbalance.


## Chapter 3. Applications and Case Studies

Big Data gives neural networks (Connectionist AI) the many examples they need to learn. This section shows five real uses and then follows one use from start to finish. Each use follows the same pattern: **lots of data in, a neural network learns patterns, and it gives a useful answer.**

### 1. Image Recognition

**What it does:** The computer looks at a picture and says what is in it (a cat, a car, a flower).

**How Big Data and neural networks help:**
- **Big Data:** ImageNet is a collection of over 15 million labeled pictures in about 22,000 categories. A popular contest version uses about 1.2 million training pictures in 1,000 categories [1].
- **Neural network:** A convolutional neural network (CNN) learns shapes and patterns from the pictures.

**Milestone:** In the 2012 ImageNet contest, a CNN called AlexNet won with a top-5 error rate of 15.3%. The second-best entry had 26.2%. "Top-5" means the correct label was not among the model's five best guesses [1]. This result is widely seen as the start of the deep-learning boom in computer vision.

**Limits:** The AI only knows what its pictures taught it, so it can fail on unusual pictures (see *Dependence on Data*). Face-recognition tests have shown different error rates for different groups of people (see *Bias and Fairness*) [2].

**Key idea:** *More labeled pictures plus a powerful network made computers much better at "seeing".*

### 2. Language

**What it does:** The computer reads, translates or writes text.

**How Big Data and neural networks help:**
- **Big Data:** Large collections of text, for example sentences translated by people.
- **Neural network:** The **Transformer**, introduced in 2017, uses a method called **attention**. Attention helps the network decide which words in a sentence matter most for understanding another word [3].

**Milestone:** On a standard English-to-German translation test (WMT 2014), the Transformer scored 28.4 BLEU, more than 2 points better than the best earlier results. BLEU is a score for comparing machine translations. It also trained faster than older approaches [3]. Transformers are the base of many modern language tools.

**Limits:** A translation can sound fluent but still be wrong, so important texts need a human check. Language AI also needs lots of data and energy (see *Energy and Compute Cost*).

**Key idea:** *Attention lets AI focus on the words that matter.*

### 3. Fraud Detection

**What it does:** Banks use AI to spot card payments that might be stolen or fake, so they can stop or check them.

**How Big Data and neural networks help:**
- **Big Data:** Huge numbers of card transactions happen every day, far too many for people to check [4].
- **Neural network and other machine learning:** The model learns what normal spending looks like and flags payments that look different.

**Why it is hard** (reviews of research name these problems) [4][5][6]:
- **Very few frauds:** Most transactions are honest, so the AI sees few fraud examples (*class imbalance*).
- **Speed:** The check must happen in real time, and many research systems still work offline [4].
- **Criminals change their tricks:** Patterns change over time (*concept drift*) [6].

**Example (illustrative):** A card used in your town at lunchtime and in another country ten minutes later looks suspicious, so the bank asks you to confirm it.

**Key idea:** *Fraud AI looks for the rare "odd one out" in a huge pile of normal data.*

### 4. Healthcare Imaging

**What it does:** AI studies medical pictures, such as photos of the back of the eye, to help find disease early.

**How Big Data and neural networks help:**
- **Big Data:** In a 2016 study, researchers trained a CNN on 128,175 retinal photos. Each photo had been graded by eye doctors [7].
- **Neural network:** It learned to spot signs of **diabetic retinopathy**, an eye disease linked to diabetes.

**Results:** In tests on two separate sets of photos, the algorithm reached about 97.5% sensitivity and 93.4% specificity on one set and 96.1% and 93.9% on the other [7]. *Sensitivity* means how many sick patients it finds. *Specificity* means how many healthy patients it correctly clears.

**Limits:**
- The authors said more research was needed before using it in real clinics [7].
- Another team tried to repeat the study with public data and got lower scores. The AI's results depend strongly on the images it learns from [8].

**Key idea:** *AI can help doctors look at more images, but doctors and careful testing are still needed.*

### 5. Recommendations

**What it does:** AI suggests videos, music, shopping items or games you might like.

**How Big Data and neural networks help:**
- **Big Data:** The system uses what each person watched and searched, plus the context [9].
- **Neural network:** YouTube described a system with two neural networks. The first, *candidate generation*, narrows a huge video collection down to hundreds of possible videos. The second, *ranking*, orders them so the best ones are shown to you [9].

**Limits:** Recommendations depend on collecting data about people, which links to *Privacy* and *Dependence on Data*. Because the AI learns from past behavior, it may keep showing you more of the same.

**Key idea:** *Recommenders turn millions of choices into a short list that fits you.*

### 6. End-to-End Case: AI Screening for Diabetic Eye Disease

This case follows one AI from idea to real use. It is based on the first AI device cleared by the US Food and Drug Administration (FDA) to give a screening result without a doctor reading the image [10].

**In short:** a health worker takes a photo of the back of the eye, the software looks at it, and it gives one of two answers: "see an eye specialist" or "screen again in 12 months."

| Step | What happens |
|---|---|
| **1. Problem** | Diabetes can damage blood vessels in the eye (diabetic retinopathy). Early detection matters, but many patients are not adequately screened [10]. |
| **2. Data** | Many retinal photos, each graded by expert eye doctors. In the research study, 128,175 photos were used [7]. |
| **3. Model** | A CNN learns to tell photos that show signs of the disease from photos that do not [7]. |
| **4. Testing** | The FDA reviewed a study of 900 patients with diabetes at 10 primary-care sites. The AI correctly found disease that was moderate or worse in 87.4% of cases (its *sensitivity*) and correctly cleared 89.5% of patients without it (its *specificity*) [10][11]. |
| **5. Use in the real world** | A health worker takes photos with a retinal camera, the photos are uploaded, and the software gives one of two results: refer the patient to an eye specialist, or screen again in 12 months [10][11]. |
| **6. Limits** | It is designed only for diabetic retinopathy, only for adults with diabetes, and it should not be used for pregnant patients or for other eye conditions [10]. |

**Two terms, with the study's numbers:**

- **Sensitivity** asks: of the patients who really have the disease, how many does the AI find? At 87.4%, about 87 of every 100 patients with the disease are found. About 13 are missed.
- **Specificity** asks: of the patients who do not have the disease, how many does the AI correctly clear? At 89.5%, about 90 of every 100 healthy patients are cleared. About 10 are sent to a specialist when they did not need to be.

No test is perfect, which is why doctors and careful testing are still needed.

**Connections to the Ethics section:**
- **Privacy:** Medical photos are sensitive and must be protected.
- **Bias and Fairness:** The AI should be tested on many kinds of patients.
- **Dependence on Data:** Good, correctly graded photos are essential [8].
- **Explainability:** Doctors and patients want to know why a result was given.
- **Energy and Compute Cost:** Training and running the model needs computing power.

**Key idea:** *A useful AI needs good data, careful testing, clear limits and people who stay responsible.*

### Summary Table

| Application | Data | What the AI does | Main limit |
|---|---|---|---|
| Image recognition | Millions of labeled pictures | Names what is in a picture | Unusual pictures, uneven accuracy across groups |
| Language | Large text collections | Translates and understands text | Fluent but wrong answers; high compute |
| Fraud detection | Huge numbers of transactions | Flags unusual payments | Few frauds, criminals change tactics |
| Healthcare imaging | Expert-graded medical photos | Helps find disease | Needs careful clinical testing |
| Recommendations | What people watch and search | Suggests items to people | Privacy and "more of the same" |
| End-to-end case | Retinal photos | Screens for diabetic eye disease | Only works for its intended use |


### References

1. Krizhevsky, A., Sutskever, I., Hinton, G. E. (2012). *ImageNet Classification with Deep Convolutional Neural Networks.* NeurIPS 25 / Communications of the ACM. https://doi.org/10.1145/3065386
2. Grother, P., Ngan, M., Hanaoka, K. (2019). *Face Recognition Vendor Test (FRVT) Part 3: Demographic Effects*, NISTIR 8280. https://doi.org/10.6028/NIST.IR.8280
3. Vaswani, A. et al. (2017). *Attention Is All You Need.* https://arxiv.org/abs/1706.03762
4. Yazici, Y. (2020). *Approaches to Fraud Detection on Credit Card Transactions Using Artificial Intelligence Methods.* https://arxiv.org/abs/2007.14622
5. Kalid, S. N. et al. (2024). *Detecting Frauds and Payment Defaults on Credit Card Data Inherited With Imbalanced Class Distribution and Overlapping Class Problems: A Systematic Review.* IEEE Access, 12. https://doi.org/10.1109/ACCESS.2024.3362831
6. Gulshan, V. et al. (2016). *Development and Validation of a Deep Learning Algorithm for Detection of Diabetic Retinopathy in Retinal Fundus Photographs.* JAMA, 316(22), 2402–2410. https://doi.org/10.1001/jama.2016.17216
7. Voets, M., Møllersen, K., Bongo, L. A. (2019). *Reproduction study using public data of: Development and validation of a deep learning algorithm for detection of diabetic retinopathy in retinal fundus photographs.* https://pmc.ncbi.nlm.nih.gov/articles/PMC6553744
8. Covington, P., Adams, J., Sargin, E. (2016). *Deep Neural Networks for YouTube Recommendations.* RecSys '16. https://doi.org/10.1145/2959100.2959190
9. US Food and Drug Administration (11 April 2018). *FDA permits marketing of artificial intelligence-based device to detect certain diabetes-related eye problems.* https://www.fda.gov/NewsEvents/Newsroom/PressAnnouncements/ucm604357.htm
10. Healio (11 April 2018). *FDA allows marketing of IDx-DR artificial intelligence device for diabetic retinopathy detection.* (Secondary news report of [10].)


## Chapter 4. Ethics, Privacy, and Limits

Big Data and neural networks (Connectionist AI) can do amazing things, but they come with responsibilities and limits. A good AI builder asks: *"Can we build it?"* and also *"Should we, and how do we do it safely?"*

### 1. Privacy

**What it means:** Privacy is your right to control who knows things about you. Big Data systems collect huge amounts of information, such as names, photos, locations and what you watch or search.

**Why it matters:**
- Data that looks harmless alone can reveal personal things when combined (where you live, your daily routine).
- Leaked or stolen data can be misused.

**Example (illustrative):** A fitness app records your running route every morning. If a stranger saw it, they could guess where you live and when you leave home.

**How to protect privacy:**
- **Collect only what is needed.** The EU's GDPR says personal data must be limited to what is necessary for the purpose ("data minimization") [1].
- **Use data only for clear, stated purposes, and keep it only as long as necessary** [1].
- **Keep data secure** against unauthorized access, loss or damage [1].
- **Follow the law.** China's Personal Information Protection Law (PIPL) took effect on 1 November 2021 [2]. It requires lawful, legitimate and necessary handling of personal information, in good faith [3].

**Key idea:** *Just because data can be collected does not mean it should be.*

### 2. Bias and Fairness

**What it means:** Bias is when an AI treats some people or groups unfairly. Fairness means treating people equally and giving everyone a fair chance.

**Where bias comes from:** The US standards institute NIST groups AI bias into three kinds: **systemic** (unfairness built into society and institutions), **statistical and computational** (e.g. unbalanced or unrepresentative data), and **human** (the choices and assumptions of the people involved) [4].

**Real example:** NIST tested 189 face-recognition algorithms from 99 developers and found that most of the algorithms studied made different amounts of errors for different demographic groups (sex, age, race or country of birth). It also found that different algorithms performed very differently [5].

**How to reduce bias:**
- Use **diverse, balanced data**.
- **Test the AI on different groups** and compare the results.
- **Keep checking** after release, because bias happens in the wider context where the system is used, not only in the code [4].

**Limit to remember:** NIST treats bias as something to identify and manage, not a problem that one technique can fix completely [4].

**Key idea:** *AI learns from us, so unfair data can lead to unfair AI.*

### 3. Dependence on Data

**What it means:** Neural networks learn from examples, so they are only as good as the data they are given. People often say **"Garbage In, Garbage Out"** [8].

**Why it matters:**
- **Too little data:** the network cannot learn patterns well [8].
- **Wrong or messy data** (typos, mislabeled examples, missing values): it learns wrong things [8].
- **Old data:** the world changes, so a model can become out of date [8].
- **Unusual situations:** an AI may fail on cases that look different from its training examples [8].

**Example (illustrative):** An AI trained to recognize cats only from daytime photos may fail on a photo taken at night.

**How to handle it:** clean the data, check its quality (accuracy, completeness, variety), update and retrain when needed, and let humans double-check important results.

**Key idea:** *Data quality matters as much as data quantity.*

### 4. Explainability

**What it means:** Explainability is being able to understand *why* an AI made a decision. Deep neural networks are often called **"black boxes"** because their millions of connections make their reasoning hard to follow [9].

**Four principles from NIST for explainable AI** [6]:
1. **Explanation:** the system gives evidence or reasons for its output.
2. **Meaningful:** the explanation is understandable to the person receiving it.
3. **Explanation accuracy:** the explanation correctly reflects how the system actually produced the output.
4. **Knowledge limits:** the system only operates in conditions it was designed for, or when it is confident enough in its output.

**Why it matters:** trust, finding and fixing mistakes, spotting hidden bias, and decisions in serious areas such as health or loans, where people deserve a reason.

**Example (illustrative):** If an AI rejects a loan application, the person should learn why (for example, "income too low") rather than only "rejected".

**Key idea:** *A good AI should give answers and be able to show reasons.*

### 5. Energy and Compute Cost

**What it means:** Training and running big AI models and storing Big Data needs powerful computers in data centers, which use a lot of electricity.

**Facts (International Energy Agency, 2025)** [7]:
- Data centers used about **1.5% of the world's electricity in 2024 (about 415 TWh)**.
- Global data-center electricity demand is projected to **more than double to about 945 TWh by 2030**, slightly more than Japan's total electricity use today.
- AI is the biggest driver of this increase.

**Why it matters:** more electricity demand can raise emissions if power comes from fossil fuels, and the cost of big models limits who can build them.

**How to reduce the cost:**
- Build **smaller, more efficient models** where they do the job.
- **Reuse** existing trained models instead of starting from zero [10].
- Use **efficient hardware** and **cleaner electricity**.
- Ask first: *Do we really need a giant AI for this task?*

**Key idea:** *Smarter AI should also mean greener AI.*

### References

1. European Union. *General Data Protection Regulation (GDPR), Article 5: Principles relating to processing of personal data.* https://gdpr-info.eu/art-5-gdpr/
2. CMS Law. *PRC Promulgated Personal Information Protection Law* (adopted 20 Aug 2021, effective 1 Nov 2021). https://cms.law/en/chn/legal-updates/PRC-Promulgated-Personal-Information-Protection-Law
3. Noerr. *PIPL: Data protection made in China* (28 Oct 2021). https://www.noerr.com/en/insights/pipl-data-protection-made-in-china
4. Schwartz, R. et al. (2022). *Towards a Standard for Identifying and Managing Bias in Artificial Intelligence*, NIST SP 1270. https://doi.org/10.6028/NIST.SP.1270
5. Grother, P., Ngan, M., Hanaoka, K. (2019). *Face Recognition Vendor Test (FRVT) Part 3: Demographic Effects*, NISTIR 8280. https://doi.org/10.6028/NIST.IR.8280
6. Phillips, P. J. et al. (2021). *Four Principles of Explainable Artificial Intelligence*, NISTIR 8312. https://doi.org/10.6028/NIST.IR.8312
7. International Energy Agency (2025). *Energy and AI.* https://www.iea.org/reports/energy-and-ai
8. Google for Developers. *Machine Learning Crash Course.* https://developers.google.com/machine-learning/crash-course
9. Rudin, C. (2019). *Stop Explaining Black Box Machine Learning Models for High Stakes Decisions and Use Interpretable Models Instead.* Nature Machine Intelligence, 1, 206–215. https://doi.org/10.1038/s42256-019-0048-x
10. Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*, Chapter 15: Representation Learning. MIT Press. https://www.deeplearningbook.org/


## Chapter 5. Synergy and Future

Big Data and Connectionist AI are closely connected technologies. Big Data provides large amounts of information, while Connectionist AI uses artificial neural networks to learn patterns from that information.

When combined, they allow systems to process large datasets, discover hidden patterns, make predictions, and support better decision-making.[1]

**How Big Data and Connectionist AI Work Together**

Big Data provides the information needed to train and improve neural networks. In return, Connectionist AI helps analyze large amounts of data more efficiently by identifying patterns that may be difficult for humans to recognize.

For example, an online shopping platform collects millions of customer transactions. A neural network can analyze this information to understand customer behavior and recommend products that customers may be interested in.

**Visual Representation:**

    +----------------------+
    |       BIG DATA       |
    |                      |
    | Large Amounts of Data|
    +----------------------+
               |
               v
    +----------------------+
    |   CONNECTIONIST AI   |
    |                      |
    | Neural Networks Learn |
    | Patterns from Data   |
    +----------------------+
               |
               v
    +----------------------+
    |    AI ANALYTICS      |
    |                      |
    | Predictions, Insights|
    | and Detection        |
    +----------------------+
               |
               v
       BETTER DECISIONS

This combination allows organizations to turn large amounts of raw data into useful information.

**AI Improving Analytics**

Connectionist AI can improve Big Data analytics by identifying complex patterns, detecting unusual activities, and automatically discovering useful information.

Two important applications are **Anomaly Detection** and **Automated Insights**.

**Anomaly Detection**

Anomaly detection is the process of identifying data that is significantly different from normal patterns.[2]

Connectionist AI can learn what normal behavior looks like by studying historical data. It can then identify unusual activities that may require further investigation.

For example, a bank may use a neural network to analyze customer transactions. If a transaction is very different from a customer's usual spending behavior, the system may flag it for review.

**How It Works:**

1. Collect historical data.
2. Train the neural network to recognize normal patterns.
3. Analyze new data.
4. Identify unusual activities.
5. Flag potential anomalies for further investigation.

**Visual Representation:**

    +------------------+
    |  HISTORICAL DATA |
    +------------------+
             |
             v
    +------------------+
    |  NEURAL NETWORK  |
    | Learns Normal    |
    | Patterns         |
    +------------------+
             |
             v
    +------------------+
    |    NEW DATA      |
    +------------------+
             |
             v
    +------------------+
    | Compare Patterns |
    +------------------+
             |
        +----+----+
        |         |
        v         v
      NORMAL   UNUSUAL
        |         |
        v         v
      Accept    Flag for
               Investigation

**Examples of Anomaly Detection:**

- **Banking:** Identifying unusual transactions that may indicate fraud.
- **Healthcare:** Detecting unusual patterns in patient monitoring data.
- **Manufacturing:** Identifying unusual machine behavior that may indicate equipment problems.
- **Cybersecurity:** Detecting unusual network activities that may indicate security threats.

Anomaly detection helps organizations identify potential problems earlier, although unusual activity does not always mean something is wrong.

**Automated Insights**

Automated insights refer to information or patterns that an AI system discovers from data without requiring humans to manually examine every record.[3][4]

Connectionist AI can analyze large datasets and identify trends, relationships, and changes that may be useful for decision-making.

For example, an online shopping platform may analyze customer purchases and discover that certain products are frequently bought together.

The system can then provide useful insights, such as recommending related products or adjusting marketing strategies.

**How It Works:**

1. Collect large amounts of data.
2. Analyze the information using AI.
3. Identify patterns and relationships.
4. Generate useful insights.
5. Present the results to users.

**Visual Representation:**

    +------------------+
    |     BIG DATA     |
    +------------------+
             |
             v
    +------------------+
    |   NEURAL NETWORK |
    +------------------+
             |
             v
    +------------------+
    | Identify Patterns|
    +------------------+
             |
             v
    +------------------+
    | Generate Insights|
    +------------------+
             |
             v
    +------------------+
    |  PRESENT RESULTS |
    +------------------+
             |
             v
       BETTER DECISIONS

**Examples of Automated Insights:**

- **Retail:** Discovering which products customers frequently purchase together.
- **Marketing:** Identifying customer groups with similar purchasing behavior.
- **Education:** Identifying learning patterns and areas where students may need additional support.
- **Transportation:** Discovering traffic patterns to help improve route planning.

Automated insights reduce the amount of manual work needed to examine large datasets and help people discover useful information more quickly.

**Anomaly Detection vs Automated Insights**

| Comparison | Anomaly Detection | Automated Insights |
|---|---|---|
| Main Purpose | Identifies unusual patterns. | Discovers useful patterns and information. |
| Focus | Detecting unexpected changes. | Understanding trends and relationships. |
| Example | Detecting unusual bank transactions. | Discovering popular product combinations. |
| Result | Flags potential problems. | Provides information for decision-making. |

---

**Future Direction**

As Big Data and Connectionist AI continue to develop, their combination is expected to create more advanced and efficient systems.

Several important directions include:

**1. More Real-Time AI**

Future AI systems may process and analyze information as soon as it is generated.

For example, traffic systems could analyze live information from sensors and cameras to identify congestion and update traffic recommendations.

This could help organizations respond to changing situations more quickly.

**2. More Advanced Automation**

AI systems may become better at handling tasks that currently require significant human effort.

For example, businesses could use AI to automatically organize data, identify patterns, generate reports, and suggest possible actions.

However, human supervision will still be important to check the accuracy and reliability of the results.

**3. Explainable AI**

As AI becomes more involved in important decisions, understanding how it reaches its conclusions becomes increasingly important.

Explainable AI focuses on making AI decisions easier for humans to understand.[5][6]

For example, instead of simply rejecting a loan application, an AI system could provide information about the main factors that influenced its decision.

**4. Edge AI**

Edge AI combines artificial intelligence with edge computing.[7]

Instead of sending all information to a central server, AI models can process data directly on devices such as smartphones, cameras, and sensors.

For example, a smart camera could recognize objects locally without constantly sending video to the cloud.

This can reduce delays and the amount of data transferred.

**5. Responsible AI and Data Privacy**

As AI systems collect and analyze more information, protecting personal data and ensuring responsible use become increasingly important.[5][6]

Future development will need to focus on:
- Protecting sensitive information.
- Reducing unfair bias in AI systems.
- Improving transparency.
- Ensuring that AI decisions are reliable.
- Following data protection regulations.

**Future Trends Comparison:**

| Future Direction | Main Idea | Example |
|---|---|---|
| Real-Time AI | Processes information as it is generated. | Live traffic analysis. |
| Advanced Automation | Automates more data-related tasks. | Automatically generating business reports. |
| Explainable AI | Makes AI decisions easier to understand. | Explaining factors behind a loan decision. |
| Edge AI | Runs AI directly on devices. | Smart cameras recognizing objects locally. |
| Responsible AI | Focuses on fairness, privacy, and reliability. | Protecting personal information used for AI training. |

**Overall Summary:**

    BIG DATA
    Provides Large Amounts of Information
                |
                v
    CONNECTIONIST AI
    Learns Patterns from Data
                |
                v
    IMPROVED ANALYTICS
    Detects Anomalies and Generates Insights
                |
                v
    FUTURE DEVELOPMENT
    Real-Time AI, Automation, Edge AI,
    Explainability and Responsible AI
                |
                v
    MORE INFORMED DECISIONS

Big Data and Connectionist AI complement each other. Big Data provides the information, while Connectionist AI helps transform that information into useful insights. Together, they create opportunities for more advanced analytics and intelligent systems in the future.

### References

1. *Big Data Analytics Deep Learning Techniques and Applications: A Survey.* Information Systems. https://doi.org/10.1016/j.is.2023.102318

2. Microsoft Learn. *Anomaly Detection Tutorial for Power BI.* https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-anomaly-detection

3. Microsoft Learn. *Get Power BI Insights.* https://learn.microsoft.com/en-us/power-bi/explore-reports/end-user-insight-types

4. Microsoft Learn. *Apply Insights in Power BI to Explain Fluctuations in Visuals.* https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-insights

5. NIST. *AI Risk Management Framework.* https://www.nist.gov/itl/ai-risk-management-framework

6. NIST. *AI Risks and Trustworthiness.* https://airc.nist.gov/airmf-resources/airmf/3-sec-characteristics/

7. Singh, R. and Gill, S. S. (2023). *Edge AI: A Survey.* Internet of Things and Cyber-Physical Systems. https://doi.org/10.1016/j.iotcps.2023.02.004
