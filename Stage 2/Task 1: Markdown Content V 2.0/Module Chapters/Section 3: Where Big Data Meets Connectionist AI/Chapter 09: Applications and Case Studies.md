## Chapter 9: Applications and Case Studies

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
10. Healio (11 April 2018). *FDA allows marketing of IDx-DR artificial intelligence device for diabetic retinopathy detection.* (Secondary news report of.)
