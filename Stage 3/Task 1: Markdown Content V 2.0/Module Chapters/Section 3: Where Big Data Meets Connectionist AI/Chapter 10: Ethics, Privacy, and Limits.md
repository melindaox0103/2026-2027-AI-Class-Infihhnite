## Chapter 10: Ethics, Privacy, and Limits

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
