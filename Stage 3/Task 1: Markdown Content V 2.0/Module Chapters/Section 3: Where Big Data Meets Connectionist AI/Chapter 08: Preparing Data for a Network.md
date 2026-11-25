## Chapter 8: Preparing Data for a Network

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
