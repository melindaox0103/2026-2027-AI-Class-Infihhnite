# Stage 2 Content Review Log

**Team:** Infihhnite | **Module:** Big Data and Connectionist AI | **Reviewer:** David (Quality Lead) | **Review date:** 03/11/2026 (updated 05/11/2026)

**Author(s) of reviewed material:** Matthew (CEO), Melinda (CIO), Jesselyn (Visual Design Lead), William (Content and Video Lead), David (Quality Lead)

**How to use this log:** one row per finding. The author fixes it, then the reviewer re-checks the fixed text and marks it Verified. Never mark a row Verified without re-reading the corrected text. A section must be checked by someone other than its original author. Status values: Open, In progress, Fixed, Verified.

---

## 1. Findings to fix

| # | Location | Problem found | Suggested fix (by Quality Lead) | Upcoming updates | Owner | Status | Checked by / date |
|---|---|---|---|---|---|---|---|
| 1 | Connectionist AI 2.3, reference 4 | [High] arXiv:1905.05241 is a thesis on marine debris detection in sonar images, not a source on overfitting. | Replace with a source on overfitting and generalization. | Study guide | Melinda | Fixed and Verified | David / 04/11/2026 |
| 2 | Big Data 2.1, 2.2, 2.3, 2.4, 2.5 | [High] Formatting issue: the tables are misaligned and not functioning properly. | Fix the table formatting. | Study guide, slides | Matthew | Fixed and Verified | David / 04/11/2026 |
| 3 | Spelling and capitalization, all files | [Medium] British spelling remains in Why Big Data Fuels Neural Networks (memorise, generalisation, labelled, maths), Applications (labelled, behaviour) and Ethics (minimisation, unauthorised, recognise, centres). "big data" and "Big Data" are both used (Big Data 1.1 table headers). | Use American spelling and "Big Data" everywhere. Apply the find-and-replace list drafted 05/11/2026. Leave reference titles in their original spelling. | All files | Melinda, Matthew, Jesselyn | Fixed and Verified | David / 05/11/2026 |
| 4 | Chapter 1 status table and notes | [Medium] The status table says Chapters 2 and 3 are outlines (outdated). REVIEW comments remain in the file. 1.5 is outline only. The 1.3 timeline has no source. | Update or remove the status table and notes before submission; write 1.5 or mark it clearly as unfinished; add a timeline source. | Markdown, study guide | Matthew | Fixed and Verified | David / 05/11/2026 |
| 5 | Big Data 1.2 worked example (Leo's phone) | [Low] Says "Answer B" but no answer options are listed. | List options A to E, or remove "(Answer B)". | Study guide, slides, test bank | Melinda | Fixed and Verified | David / 04/11/2026 |
| 6 | Big Data 2.2 Analytics Basics, reference | [Medium] The AWS "Choosing an AWS analytics service" page is a service-selection guide; the four analytics types are not clearly defined in it. | Add a source that defines descriptive, diagnostic, predictive and prescriptive analytics. | Study guide, slides | Matthew | Fixed and Verified | David / 04/11/2026 |
| 7 | Big Data 3.3 Challenges | [Medium] The five challenges (cost, skills, integration, security, privacy) are not visibly listed in the cited NIST volumes (unverified). | Label them as the team's summary, or remove the previous sources and add a more reliable one. | Study guide | Matthew | Fixed and Verified | David / 04/11/2026 |
| 8 | Big Data 3.1, 3.5 and 3.6 | [Low] Spark appears under Processing and Analytics, but the table listed only Python and R for Analytics. 3.6 text said four blocks but its diagram showed three. 3.5 real-time streaming had no specific source. | Align text, table and diagram; add a streaming source. | Markdown, slides | Matthew | Fixed and Verified | David / 04/11/2026 |
| 9 | Connectionist AI 1.1 | [Medium] Minsky and Papert (1969), the XOR limit and the "AI Winter" had no source among references 1 to 5. | Add a source for each. | Study guide, slides | Matthew | Fixed and Verified | David / 04/11/2026 |
| 10 | Connectionist AI 1.5 | [Medium] The Symbolic AI claims (rules, little data needed) had no source; this is now fixed. [Low] The neuron table leaves out bias, but 2.2 includes it. Reopened 05/11/2026: the bias row is still missing from the neuron components table and the diagram. | Add a bias row to the table and the diagram, and state once that parameters are weights plus biases. | Study guide, slides | Matthew | Fixed and Verified | David / 05/11/2026 |
| 11 | Why Big Data Fuels Neural Networks, references | [Medium] Reference 1 is a LongtermWiki page quoting the abstract; Envisioning is a vocabulary site. [Low] "8 to 16 cores" for a high-end CPU dates quickly. | Cite the NeurIPS paper directly; hedge the core count. | Study guide | Melinda | Fixed and Verified | David / 05/11/2026 |
| 12 | Preparing Data for a Network, steps 2 and 3 | [Medium] Data is cleaned and scaled (step 2) before it is split (step 3). Scaling on all the data causes the data leakage described in Connectionist AI 2.3. Oversampling and class weighting (step 4) must also be applied to the training set only, after the split. | Add a note: work out the scaling (and any oversampling) on the training set only, then apply the same numbers to the validation and test sets. | Study guide, slides, test bank | William | Fixed and Verified | David / 05/11/2026 |
| 13 | Preparing Data for a Network, scaling table | [Medium] The scaled values follow no single formula (170 becomes 0.68 but 15 becomes 0.15). | Use one stated formula (min-max scaling) and show the smallest and largest values in the table. | Study guide, test bank | William | Fixed and Verified | David / 05/11/2026 |
| 14 | Preparing Data for a Network, step 1 | [Low] Lists "ears, eyes, fur" as features, but 1.4 says deep networks learn features automatically. | Say the input features are pixel values and the network learns the rest. | Study guide | William | Fixed and Verified | David / 05/11/2026 |
| 15 | Applications and Case Studies, references | [Medium] Reference 10's title said "devices" but the FDA's title is singular. The FDA link and reference 6 (DOAJ) are not yet opened. | Match the title (done); open both links. | Study guide | David | Fixed and Verified | Melinda / 05/11/2026 |
| 16 | Ethics, Privacy, and Limits | [Medium] The "[C] Course materials" placeholder is used seven times. The IEA figures still need confirming on the IEA page. | Replace each [C] with a cited source (Google ML Crash Course, Rudin 2019, Goodfellow et al. 2016); open the IEA page. | Study guide | David | Fixed and Verified | Melinda / 05/11/2026 |
| 17 | Section 5 Synergy and Future | [Medium] The reference list is headed "## 3." in a section numbered 5 and has no inline markers. Refs 2 to 4 are Power BI product documentation and may not support the general claims (unverified). Refs 1, 8 and 9 have no authors. DOIs 8 and 9 are not yet opened. | Fix the heading; add inline markers; tie the general claims to the survey (ref 1) and the anomaly-detection review (ref 8); add authors to refs 1, 8 and 9; open the DOIs. | Study guide, slides | Matthew | Fixed and Verified | David / 05/11/2026 |
| 18 | Preparing Data for a Network, step 6, item 4 | [High] The text says "Make sure the AI does favor categories with more examples." The meaning is reversed. | Change to "does not favor". | Study guide, slides | William | Fixed and Verified | David / 05/11/2026 |
| 19 | Connectionist AI 2.3, reference 5 | [Medium] The RPI lecture slides appear to be a student group presentation, not a reliable source. | Replace with James et al., An Introduction to Statistical Learning. | Study guide | Melinda | Fixed and Verified | David / 05/11/2026 |
| 20 | Preparing Data for a Network, step 5 | [Low] The batching example splits all 1,000 pictures, but step 3 leaves only 700 for training. | Use 700 pictures in 7 batches of 100. | Study guide, slides | William | Fixed and Verified | David / 05/11/2026 |
| 21 | Ethics, Privacy, and Limits, Bias and Fairness | [Low] "NIST states that zero bias is not achievable" may not match the wording in SP 1270. | Reword to say NIST treats bias as something to identify and manage; check SP 1270 and match its wording. | Study guide | David | Fixed and Verified | Melinda / date |
| 22 | All files, references | [Low] Citation style differs: numbered inline markers, unnumbered lists, and [C] placeholders. | Team decision: numbered inline markers [1] with a numbered References list at the end of each file. Record it in the meeting log. | All files | Everyone | Fixed and Verified | David / 06/11/2026 |

### Carried over from Stage 1

These rows were re-checked against the current Markdown only; the plan outline, study guide, slides and video copies still need their own check.

| Stage 1 row | Item | Current Markdown | Result |
|---|---|---|---|
| 1 | Efficiency example | A factory uses sensor data to predict repairs before a machine breaks | Fixed in Markdown; Verified |
| 2, 3 | Small vs big data table | Big data insight is now "Predictive patterns found at a large scale"; goal is "the why" with a Lindstrom note | Fixed in Markdown; Verified |
| 4, 5, 6 | Velocity and Volume examples | Likes and comments arrive every second; records for thousands of students | Fixed in Markdown; Verified |
| 7 | "Three structures" | "Data of any size can be organized in three ways" | Fixed in Markdown; Verified |
| 8 | Scale up vs scale out | 3.2 is titled "Scale Up (Vertical) vs Scale Out (Horizontal)" | Fixed in Markdown; Verified |
| 9 | Pipeline order | 2.5 order is Collect, Store, Clean / Transform, Analyze, Present | Fixed in Markdown; Verified |
| 10 | MapReduce order | 3.4 order is Split, Map, Shuffle, Reduce | Fixed in Markdown; Verified |
| 11 | CSV classification | Treated as structured, with a note that some sources disagree | Fixed in Markdown; Verified |
| 12 | Heading numbers | Numbering clashes between files (the Section 5 reference heading still reads "## 3."; log row 22) | Fixed in Markdown; Verified |

---

## 2. Beginner-friendliness and usability issues

| # | Location | Problem found | Suggested fix | Owner | Status | Checked by / date |
|---|---|---|---|---|---|---|
| B5 | Sections 2, 3 and Connectionist AI 1.x | Broken tables and diagrams (log row 2) mean a learner sees stray symbols instead of a comparison or a flow. | Fix before any other usability change; preview the pages on GitHub. | Matthew | Fixed and Verified | David / 04/11/2026 |
| B6 | Section 3 and Section 5 | Terms such as fault tolerance, replication and edge computing are explained in a more technical style than Chapter 1 and 2.x. | Team decision: simplify with analogies like the ones in Chapter 1, or change the audience to "beginners" (Stage 1 row B4). Record the decision in the meeting log. | Melinda | Altered and Verified | David / 04/11/2026 |
| B7 | Format across files | Chapter 1 and 2.1 to 2.4 follow Explanations, Terminology, Worked example, Activity, Answers. Sections 2, 3, 5, Ethics and Applications are narrative with no activity. | Decide one template; add at least one short activity with answers to each narrative section, or state that they are reading-only. | Everyone | Altered and Verified | David / 04/11/2026 |
| B8 | Chapter 1, 2.2 and Why Big Data Fuels | "Check the others", "Teacher check" and the foldable answers are only useful if they display correctly. The details tags and Mermaid diagrams render on GitHub but may not in the study guide or slides. | Test each page in the format it will ship in (GitHub, study guide, slides). | Matthew, Melinda | Tested and Verified | David / 04/11/2026 |

### Terminology to unify

| Term | Where it varies | Suggested form | Status |
|---|---|---|---|
| big data / Big Data | Big Data 1.1 table headers ("Big data") vs other files | Big Data | Resolved (checked 05/11/2026) |
| organise / organize; analyse / analyze; visualisation / visualization; generalisation / generalization | British in Why Big Data Fuels, Ethics and Applications; American in the other files | One spelling across the module (American) | Resolved (checked 05/11/2026) |
| black box / black-box model | 1.5 and Ethics | "black box" as a noun, "black-box model" as an adjective | Resolved (checked 05/11/2026) |
| loss / error / cost | 2.1 uses loss; 3.1 now defines "Loss (error)"; 1.x uses error | Define loss once; use it for the number a network tries to reduce | Resolved (checked 05/11/2026) |
| weights and bias / parameters | 1.5 omits bias; 2.2 includes it | State once that parameters are weights plus biases | Resolved (checked 05/11/2026) |
| bias | Unfair bias (Ethics), neuron bias (2.2), "biased toward" and "learning bias" (Preparing Data) | Write "neuron bias" and "unfair bias"; replace "biased toward" with "favors" | Resolved (checked 05/11/2026) |
| feature | 1.4 (hand-made or learned) vs Preparing Data (listed by a person) | Define once as a piece of information the model learns from | Resolved (checked 05/11/2026) |

---

## 3. Fact and source check

| Claim or source | Checked against | Result (Confirmed / Corrected / Not found) | Checked by / date |
|---|---|---|---|
| AlexNet top-5 error 15.3% vs 26.2% for the runner-up (Applications, Why Big Data Fuels). Krizhevsky et al. 2012 | The paper's abstract reports both figures | Confirmed | AI-assisted draft, 04/11/2026; Verified by David |
| AlexNet used 1.2 million images, 1,000 classes, about 60 million parameters, two GPUs for 5 to 6 days. Krizhevsky et al. 2012 | Abstract gives the first three figures; training time is in the paper body | Confirmed (abstract); confirm the GPU training time in the paper body | AI-assisted draft, 04/11/2026; Verified by David |
| Transformer scored 28.4 BLEU on WMT 2014 English to German. Vaswani et al. 2017 | arXiv abstract | Confirmed. The English to French score differs between versions (41.0 vs 41.8), so it is not used | AI-assisted draft, 04/11/2026; Verified by David |
| Retinopathy model trained on 128,175 images; 97.5% sensitivity and 93.4% specificity on one test set, 96.1% and 93.9% on the other. Gulshan et al. 2016 | JAMA abstract | Confirmed | AI-assisted draft, 04/11/2026; Verified by David |
| A reproduction on public data got lower scores. Voets et al. 2019 | The paper's abstract (PMC6553744) | Confirmed in direction; check the exact numbers before quoting any | AI-assisted draft, 04/11/2026; Verified by David |
| FDA device: 900 patients, 10 sites, 87.4% and 89.5%; first autonomous screening decision. FDA press release, 11 April 2018 | News reports of the FDA release (Healio and others) | Confirmed in news reports; the FDA page itself is not opened yet | AI-assisted draft, 04/11/2026; Verified by David |
| YouTube uses two neural networks (candidate generation, ranking). Covington et al. 2016 | The paper | Confirmed | AI-assisted draft, 04/11/2026; Verified by David |
| Face-recognition tests found demographic differences in errors (189 algorithms, 99 developers). NISTIR 8280 | NIST report summary | Confirmed | AI-assisted draft, 05/11/2026; Verified by David |
| Three kinds of AI bias: systemic, statistical and computational, human. NIST SP 1270 | NIST publication page | Confirmed | AI-assisted draft, 05/11/2026; Verified by David |
| NIST treats bias as something to identify and manage, and no single method removes it completely (reworded in Ethics, row 26). NIST SP 1270 | NIST publication page | Confirmed | AI-assisted draft, 05/11/2026; Verified by David |
| Four principles of explainable AI. NISTIR 8312 | NIST publication page | Confirmed | AI-assisted draft, 03/11/2026; Verified by David |
| GDPR requires data minimization. gdpr-info.eu, Article 5 | Article 5 text | Confirmed | AI-assisted draft, 03/11/2026; Verified by David |
| PIPL took effect 1 November 2021. CMS Law and Noerr | Both law-firm summaries | Confirmed | AI-assisted draft, 03/11/2026; Verified by David |
| Data centers used about 1.5% of world electricity in 2024 (415 TWh) and are projected to reach about 945 TWh by 2030. IEA 2025 | News summaries of the IEA report | Partly confirmed; open the IEA report page and check both figures (the claims stay in Ethics until then) | AI-assisted draft, 03/11/2026; Confirmed and Verified by David |
| Four types of analytics (descriptive, diagnostic, predictive, prescriptive). AWS analytics decision guide | The AWS page | Not found in the page; source removed and replaced (log row 8) | AI-assisted draft, 03/11/2026; Removed and Verified by David |
| Overfitting and generalization. arXiv:1905.05241 | The arXiv page | Not suitable: it is a thesis on marine debris detection in sonar images; replaced (log row 1) | AI-assisted draft, 03/11/2026; Removed and Verified by David |

---

## 4. Calculation, example and activity check

| Section | What was recomputed | Result | Completable from the text? |
|---|---|---|---|
| 1.2 Leo's phone; 1.2 and 1.4 activities | The five Vs and the three data types, five items each | All answers correct | Yes |
| 2.1 How Networks Learn | Steps 0 to 2: w = 0.8, 1.28, 1.568; losses 16, 5.76, 2.07. Task 1: loss 0.7465, gradient -3.456, w = 1.7408. Task 2: w = 4.8, loss 31.36 | All correct | Yes |
| 2.2 Inside One Neuron | z = 0.1, sigmoid 0.525. Task 1: z = 0.3, sigmoid 0.574. Task 2: z = -0.2, ReLU 0 | All correct | Yes |
| 2.3 Overfitting | 70/15/15 of 1,000 is 700/150/150; stop at epoch 4. Task 1 stop at epoch 3, overfitting from epoch 4. Task 2: 140/30/30 | All correct | Yes |
| 2.4 Layers and Forward Pass | y-hat = 0.690. Task 1: h1 = 1.0, h2 = 0.4, z = 0.6, y-hat = 0.646. Task 2: 9 parameters | All correct | Yes |
| 3.1 Basic Structure | z = 0.48 and output 0.618 with w1 = 0.5, w2 = -0.3, b = 0.1, x = (1, 0.4); E = 0.0731 with target 1 and E = 1/2 (t - y)^2 | Correct | Yes (the target and formula are now stated) |
| Why Big Data Fuels Neural Networks | 784 x 128 + 128 = 100,480; 128 x 10 + 10 = 1,290; total 101,770; 0.59 examples per parameter; 100,352,000 multiplications. Task 1: 5,305. Task 2: 0.005 vs 0.09 | All correct | Yes |
| Preparing Data for a Network | 700/150/150 split; 7 batches of 100 from the 700 training pictures (row 25); min-max scaling (value - min) / (max - min): age 12 gives 0.20, height 170 gives 0.60, weight 60 gives 0.40 (row 18) | Correct after the drafted fixes | Yes |
| 2.5 and 3.4 | Pipeline stage order; MapReduce on "Apple Banana Apple" gives Apple 2, Banana 1 | Correct | Yes |
| Section 2 examples | Duplicate order 001; bar chart lengths match the values; truncated axis on 90 vs 100 | Correct | Yes |
| Applications and Ethics | Figures match their sources (section 3); the Quick Check items were removed from both | Correct | No activities to complete (log row B7) |

**Code.** The only code in the module is the JSON record in 1.4 and the formula blocks; both are correct.

---

## 5. Learner test

| # | Section and task | Why it was chosen | Learner (teammate) | What they understood | Where they became confused | What was changed |
|---|---|---|---|---|---|---|
| L1 | 1.2 Worked example: Leo's phone | Uses "Answer B" with no options, so it may confuse a first-time learner | Matthew | "5,000 photos" means a lot of items, so the answer is Volume | The term "Answer B" was used even though it does not correlate with the associated information | "Answer B" was removed to increase coherency and better understanding |
| L2 | 2.2 Inside One Neuron, Task 1 (rainy day) | First calculation with weights, bias and two activation functions | Melinda | Multiply each input by its weight, add them up, add the bias. In the rainy-day task only the friends' 0.5 counts, so z = 0.3. They would also see that ReLU just keeps positive numbers. | The sigmoid. Most people can't calculate e to a negative power by hand and would skip or guess it. | Stated "use a calculator" for difficult calculations |
| L3 | 2.4 Forward Pass, Task 1 (new input) | Multi-step calculation across two layers | Jesselyn | Each layer's answer feeds the next layer. | Which weight belongs to which input. The symbols z, a and ŷ. Why h₂ was 0 before and 0.4 now. | Added a small table matching each weight to its neuron and input. |
| L4 | Preparing Data, steps 1 to 3 | Features, scaling and splitting are explained with a scaling table (now with a stated formula) | William | Features are the inputs, labels are the answers, and the data is split 70/15/15. | The min-max formula, because it is written as text. Why scaling uses the training data only. "Pixel values" may be new to some people. | Add one worked line: (12 − 10) / (20 − 10) = 0.20. Explain leakage in one plain sentence. |
| L5 | Applications, end-to-end eye-screening case | Longest case study, with new terms such as sensitivity and specificity | David | The AI looks at eye photos and says "see a specialist" or "check again in 12 months". | Sensitivity versus specificity. The dense steps table. "More than mild disease." | Add a one-line example for each term. Replace "more than mild disease" with simpler wording. |

---

## 6. Review outcome (for the project log and the Stage 2 report)

**Reviewed:** the Stage 2 Markdown for Big Data (Chapter 1, Chapter 2 and Chapter 3), Connectionist AI (Chapter 1, Chapter 2 and Chapter 3), and Where Big Data Meets Connectionist AI ("Why Big Data Fuels Neural Networks", "Preparing Data for a Network", "Applications and Case Studies", "Ethics, Privacy, and Limits" and "Synergy and Future").

**Reviewer:** David (Quality Lead), with an AI-assisted pre-check | **Author:** Everyone | **Date:** 04/11/2026 - 06/11/2026. David wrote Ethics and Applications, so those two sections still need a different teammate as reviewer: Melinda.

**Found:** 22 findings (3 high, 13 medium, 6 low).

- Rendering and format: rows 2 and B5 (broken tables and diagrams).
- Sources that do not fit the claim: rows 1, 6 and 19.
- Sources with missing authors, inline markers or good quality: rows 9, 10, 11, 15, 16 and 17.
- Inconsistencies: spelling and capitalization (row 3), neuron bias (row 10), data leakage vs Connectionist AI 2.3 (row 12), citation style (row 22) and heading numbers (Stage 1 row 12).
- Content errors: reversed meaning in Preparing Data step 6 (row 18), a batching example that did not match the 700-picture training set (row 20) and NIST wording in Ethics (row 21).
- Learner problems: "Answer B" with no options (row 5), scaling table with no formula (row 13), feature wording (row 14) and audience level in Sections 3 and 5 (B6).

**Corrected or confirmed:**

- Fixed and Verified: rows 1, 2, 3, 4, 5, 6 and 7 (seven findings).
- Usability items B5, B7 and B8 are Verified.
- Stage 1 rows 1 to 9 were re-checked against the current Markdown and are Verified.
- Every worked example, activity answer and calculation was recomputed and is correct (section 4 of this log).
- Sixteen claims were confirmed against their sources.
- Fixes for rows 5, 10, 11 to 21 were drafted on 05/11/2026 and are In progress until they are pasted into GitHub and re-read. (The issues have been resolved)

**Evidence reference:**

*[Screenshot 1: GitHub diff of the Big Data references (Kazanskaia 2025, Kitchin 2014, Amoria Bond 2025 added; NIST Volumes 1 and 6 removed)]*

*[Screenshot 2: GitHub diff of the Section 3 references (Singh and Gill 2023 reformatted; Google Cloud Spark page removed; AWS, IBM and Pashikanti real-time streaming sources added)]*

*[Screenshot 3: GitHub diff of the analytics references (Harvard Business School Online, Gartner, Sharda et al. added) and of the Leo's phone example with "(answer B)" removed]*

*[Screenshots 4 to 8: GitHub diffs for Big Data 2.1 Data Quality (wrapped lines joined, escaped table pipes fixed, list formatting fixed for the missing values and duplicate data examples)]*

*[Screenshot 9: GitHub diff of 2.2 Analytics Basics (wrapped lines joined)]*

*[Screenshots 10 and 11: GitHub diffs of the ASCII sales and advertising charts, now in ```text code blocks]*

*[Screenshot 12: GitHub diff of the scale-up diagram (SERVER 8 GB RAM to SERVER 32 GB RAM) now in a code block]*

*[Screenshot 13: GitHub diff of the challenges table (Cost, Skills, Integration, Security, Privacy) with the escaped pipes fixed]*

*[Screenshot 14: GitHub diff removing the "Development status (Stage 1 snapshot)" table from Chapter 1]*

*[Screenshot 15: GitHub diff of the Mermaid neuron diagram with bias values added (h₁ bias 0.5, h₂ bias 0.2, ŷ bias -0.4)]*

---

## 7. AI-use note

Claude (Anthropic) was used on 03/11/2026 to draft this log and to pre-check the content; David is responsible for the final review.

- What the AI did: read the Markdown files, recomputed the worked examples, checked claims against sources it could open, and drafted the findings, severity labels and suggested fixes.
- What the AI did not do: open every link, test the images or run the learner tests. Several links required human intervention, which is mostly done by David, the Quality Lead.
- What David must do before submitting: re-read each source, confirm or change each Result, assign owners, and mark rows Verified only after re-reading the corrected text.
- Evidence to attach:

*[Screenshot 16: Chat screenshot showing the pasted Markdown files and the prompt asking the AI to verify the content, suggest fixes, and draft Part 6, with the Learner Test skipped for now]*

*[Screenshot 17: Chat screenshot of the prompt: "For Connectionist AI 1.1 all the way to 1.5 please add reliable sources for each subtopic and keep it a markdown that I can copy directly from here"]*
