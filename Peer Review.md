# Infihhnite — Stage 3 Peer Review

**Reviewing team:** Infihhnite
| Members | Student ID | Position | 
|---|---|---|
| Matthew Reinhart Dermawan  | 1820262296 | CEO |
| Melinda Odelia Xie  | 1820262300 |  CIO |
| Jesselyn Febriana Surjana  | 1820262302 | Visual Design Lead |
| William Dharma Hadikusumo  | 1820262047 |Content and Video Lead |
| David Starlie Suwandi  | 1820262333 | Quality Lead |


---

# Assigned Team: Team Name: Not Found

**Topic:** "Inside the Machine": Hardware, Network Infrastructure and Behaviourist AI (16 chapters, 16 "cases")

**Versions reviewed (Stage 2, V1.0)**
- Study Guide V1.0: `1_1__StudyGuide_V1.pdf`, 519 pages
- Test Bank V1.0: `1_2__TestBank_V1.pdf`, 36 pages, 75 questions (32 T/F, 32 MC, 11 open-ended)
- Simulators: `Simulators_V1.zip`, 14 simulators plus an index page
- PPT Slides V1.0: `2__PPT_V1_pptx.pdf`, 78 slides (PDF export; presenter notes [checked / not checked: edit]) 
- Video Tutorials V1.0: Section0_Intro (1:33), Section1_Hardware (8:48), Section2_Networks (8:54), Section3_BehavioristAI (8:17), Section4_PuttingItTogether (8:53), plus `VideoGuide_V1.pdf`. The Video Guide lists the files as `TeamNameNotFound_VideoXX_*.mp4`; the posted names differ, but the file sizes match the guide byte for byte.

## Overall impression
The three deliverables share one idea: every chapter is a "case" that the learner predicts, tries, and closes. The same sixteen cases, numbers and characters (Nova and Byte) appear in the guide, slides, videos, simulators and Test Bank, and the numbers we checked are reproducible. That coherence is the team's biggest strength. The main risks before Nov 28 are (1) video fixes that the team's own guide says are not yet applied, (2) differing wording for the same prediction question and unlabeled single-run vs. average numbers, and (3) image-source quality and slide legibility.

## Scores (provisional; remap to the published rubrics)
| Deliverable | Coverage (20) | Format (20) | Content (40) | Overall (20) | Total |
|---|---|---|---|---|---|
| Study Guide and Test Bank | 18 | 17 | 35 | 18 | **88 / 100** |
| PPT Slides | 17 | 18 | 34 | 17 | **86 / 100** |
| Video Tutorials | 17 | 15 | 34 | 16 | **82 / 100** |

Study Guide bonus (reported separately): all 14 simulators run and reproduce the module's numbers; award per the published bonus rule [add value].

---

## 1. Study Guide and Test Bank V1.0

### Strength to preserve: predict-first activities with reasoned answers
Study Guide Ch 1, Activity 1.2 (p. 17): learners predict, trace a 4 + 9 program by hand, swap two steps, then open an answer that explains why ("the 4 is overwritten and lost, because the accumulator holds only one value"). The mistake becomes the lesson, and the answer explains reasoning, not only "13 / 18". Keep this in every chapter. It recurs across the guide: 97 Activity boxes, 23 Lab boxes and 17 Predict First boxes.

![Guide p.17](screenshots/07_Guide_p17_Activity_1_2.png)

### Strength to preserve: an answer key that teaches
Test Bank Answer Key B, Q51 (p. 26): the key shows the arithmetic (−5 + 100 − 20 = 75) and explains why distractor C (74) is wrong. Q34 and Q41 explain wrong options the same way. The open-ended key (p. 28 onward) gives key points plus a sample answer. We recomputed Q8, Q14, Q30, Q40, Q41, Q45, Q47, Q51, Q57, Q67, Q68, Q69, Q72, Q73, Q74 and Q75, and all key answers are correct.

### Strength to preserve: simulators that reproduce every number on screen
We opened all 14 simulators in Simulators_V1.zip. They run offline with no errors, and the numbers in the videos, slides and Test Bank can be reproduced: thermal throttling at 40 °C (140 °C, 45% speed), the 70%-men fairness test (ratio 0.75), the cook-off (60 s vs. 25 s), and the Q70 ε-greedy table. A learner can check any claim in the module themselves. Keep the "Run the comparison" button and the seed field, since they make results reproducible.

### Most important improvement: the Study Guide cites unreliable image sources
Study Guide p. 36 (Fig 1.9 Wikipedia, Fig 1.11 a TikTok post) and p. 64 (Fig 2.9 Wikipedia), plus stock-photo and blog pages elsewhere. For a course module, replace them with museum, university, Britannica or manufacturer sources, or the team's own figures. The text references (Princeton, MIT, IBM Research, p. 35) are strong, so image sources should meet the same standard. Check the image tables at the end of each chapter for the same pattern.

![Guide p.36](screenshots/09_Guide_p36_image_sources_Wikipedia_TikTok.png)

### Other issues
1. **Guide p. 20, Fig 1.14–1.17 (Activity 1.3):** The screenshots show a program that stores into FIRST and SECOND, while the text program uses NUM. A beginner comparing their Little Man Computer screen with the figure will see different names and addresses. The caption admits this, but it adds friction. Re-shoot the figures with the text program.
   ![Guide p.20](screenshots/08_Guide_p20_LMC_figure_differs_from_text_program.png)
2. **Guide p. 10 and p. 31, Test Bank Q1 (True):** "Four core hardware components: processor, memory, network and storage." A network is not usually listed as a core component of a computer; input/output devices are, and the guide's own chapter-end Q1 answer (p. 32) mentions I/O devices as a wrong option. Rephrase ("four main parts a computer uses") or treat the network as a connection. **[VERIFY with Content Lead]**
3. **Single run vs. 300-game average (Video 3 4:23–5:07, Slide 50, Test Bank Q70):** The numbers are consistent: we reproduced the Test Bank table with the Lab 11.1 simulator's "Run the comparison" button. However, the video and slide show one run (seed 1: ε = 0% → $1,000, ε = 20% → $1,490), while Q70 shows 300-game averages ($1,114, $1,309). A learner may think they disagree. Add "in this run (seed 1)" to the video and slide, and "average of 300 games (Lab 11.1, Run the comparison)" to the Q70 table caption.
   ![Test Bank p.19](screenshots/10_TestBank_p19_Q70_table.png)
   ![Simulator comparison](screenshots/12_Simulator_epsilon_comparison_matches_TestBank_Q70.png)
4. **Workload:** The guide states 70–120 minutes per chapter (p. 8), so 16 chapters take roughly 19–32 hours, in one 519-page, 100 MB PDF. Mark a "core path" of required activities per chapter, and consider chapter-level PDFs.
5. **Zip housekeeping:** The Video Guide names the supporting file `TeamNameNotFound_Stage2_SupportingFiles.zip`, but the posted file is `Simulators_V1.zip`, and it includes an unbuilt `src/` folder that learners don't need. [Mention only if the authors posted a different file.]

---

## 2. PPT Slides V1.0

### Strength to preserve: one repeatable, low-text lesson loop
Slides 6–9, 10–13, etc.: every case runs Predict (3 options, "raise your hand") → Idea (one diagram) → See it work (one number) → Case closed (cause, fix, vote answer). Most slides carry 5–35 words, so a prepared teammate can teach the lesson and the room can follow it. Slide 8 ("Trace it: what does PRINT show?", bonus: swap steps 2 and 3) turns Activity 1.2 into a 90-second classroom task.

![Slide 8](screenshots/06_Slide08_trace_it_strength.png)

### Most important improvement: simulator screenshots are too small to read from the back
Slide 16 (battery budget): the chart axes and the sentence "Of the average current, 91% comes from the awake time…" are far below readable size. The same pattern recurs on the other "See it work" slides (e.g., 12, 20, 25, 29, 33, 37, 42, 46, 50, 59, 63, 67, 71). Crop each screenshot to the single number or bar the slide is about, and enlarge it (at least 18 pt equivalent). The large red result already on the slide (37.9 days) is the right size; the screenshot should support it, not compete with it.

![Slide 16](screenshots/05_Slide16_small_simulator_text.png)

### Other issues
1. **Case #001 asks three different prediction questions.** Slide 6 offers (A) CPU too slow / (B) waits for data from storage / (C) screen too small. Video 0 (1:04) asks "memory, storage, or the network?", and the Video 1 reveal (2:23) says "if you guessed memory, you were close", while the Case Closed slide says storage. Use one wording everywhere (for example, "RAM fills up, data spills to storage, the CPU waits").
2. **Slide 7** introduces register, cache, RAM and SSD with no definition on the slide. The team's review record (Video Guide p. 29) says definitions were added to Video 1; make sure the slide or its notes carry them too. **[VERIFY in the PPTX notes]**
3. **Presenter notes:** Not inspected (PDF export only). Confirm every slide has teaching notes, since the slides are deliberately short. **[VERIFY]**

---

## 3. Video Tutorials V1.0

### Strength to preserve: pause-and-predict with the reveal withheld
Video 1, 1:05–1:25: the narration sets up the swapped program, a "PAUSE & PREDICT" badge appears, the accumulator and OUTPUT boxes stay empty ("?"), and the answer (18) comes only afterwards with its reason ("the second get erased the four"). Learners commit to a guess first. The narration explains instead of reading slides, and the numbers we checked (6.2 MB frame, 187 MB/s, 37.9 days, 4.1 days, 0.56 m vs. 1.95 m, 90 vs. 66) match the simulators and the Test Bank.

### Most important improvement: apply the fixes the team's own guide lists as "planned"
Video Guide p. 29 says the revisions for Videos 0, 1, 3 and 4 are "planned and not yet applied", while its table says all five were "Revised after peer review". Make the guide and the files agree. Evidence that fixes are still needed:

- **Video 0, 0:30–0:33:** The narration says "six students, six roles", but the slide shows five cards. Falent Ananta Christanto (Quality Lead) is missing, and "Nemindhara Naththarampotha" has no surname.
  ![Video 0 at 0:31](screenshots/01_Video0_0031_team_slide_five_of_six.png)
- **Video 1, 3:04–3:19 and 3:42–4:05:** A dark caption band covers about the bottom 40% of the cook-off simulator, hiding the chart the narrator describes, and the top heading is clipped. At the 4:05 reveal ("about four percent") the viewer cannot see the tie point on the chart.
  ![Video 1 at 3:10](screenshots/02_Video1_0310_caption_band_covers_simulator.png)
- **Video 2, 4:58–5:20 (latency pause):** The simulator already shows "WAITING (LATENCY) 50 ms" during the pause, so part of the answer is visible, and the caption band still covers the lower half.
  ![Video 2 at 5:08](screenshots/03_Video2_0508_latency_value_visible_during_pause.png)
- **Video 3, 4:36–4:56 (epsilon pause):** A nearly empty screen with a stray empty red rectangle; the options ("$1,000 / machine B") exist only in the caption.
  ![Video 3 at 4:45](screenshots/04_Video3_0445_near_empty_pause_screen.png)

### Other issues
1. **Density:** Each lesson video covers four chapters in about 8.5 minutes (about 2 minutes per chapter). The team's own review counts about 20 terms in Video 2 (Video Guide p. 30). Keep the rule "define each term once, in one sentence."
2. **Pause length:** 10 seconds is short for calculation questions (Video 3 at 2:42, maze score; Video 4 at 6:33, car stopping). Add an on-screen "Pause the video now" line.
3. **Audio:** Both voices are Kokoro text-to-speech (Video Guide p. 28), and the guide says not every member has listened to them. **[VERIFY by ear: pronunciation of "ε", "TCP/UDP", "QoS", large numbers]**
4. **Housekeeping:** Video Guide p. 29 lists Video 3 as 8:16 and Video 4 as 8:52; the files are 8:17 and 8:53.

---

## 4. How the three deliverables work together

**Concept traced: Case #001 (the idle processor / bottleneck).**
- **Introduced:** Video 0 (0:00–0:14) and Study Guide Ch 1 Case File (p. 9), with the Task Manager screenshot (Fig 1.1, p. 10).
- **Seen in action:** Slides 6–9; Video 1 (0:29–2:34), including the memory ladder.
- **Practiced and checked:** Guide Activities 1.2–1.5 (pp. 17–30); Test Bank Q2, Q34, Q65.

Every deliverable points to the next with exact references (Slide 5, the Video Guide connection tables), and the simulators let learners reproduce the numbers.

**Gaps and contradictions**
- Three different prediction wordings for Case #001 (see PPT issue 1).
- Single-run vs. average ε-greedy numbers are not labeled (Guide issue 3).
- The Test Bank assesses ideas that the videos and slides do not teach: jitter and corruption (Q10, Q42; Video 2 teaches only "three enemies"), local maximum (Q22, Q70b), sensor fusion (Q7, Q74c), zero-sum (Q73a), systolic array (Q4). They are taught in the guide, but a learner who only watches the videos meets them first in the Test Bank. Add one sentence in the video or slide, or mark these questions "Study Guide only".

---

## 5. Revision priorities (in order)
1. **Fix and re-export the videos, and make the Video Guide match.** Add the missing sixth member to Video 0; move captions off the simulators (Videos 1, 3, 4); hide the answers in every pause (Video 2 latency pause); fill the empty Video 3 pause screen; then correct Video Guide p. 29 so it states what was actually applied.
2. **Make wording and labels identical across deliverables.** Use one Case #001 prediction question; label the ε-greedy figures as "this run" vs. "300-game average"; add the Test-Bank-only terms to a slide or video, or label the questions.
3. **Raise source quality and slide legibility.** Replace the Wikipedia, TikTok and stock image sources (Guide pp. 36, 64); re-shoot Fig 1.14–1.17 with the text program; crop the simulator screenshots on slides 12–71 to one readable number each.

---

# Team of Our Choice: Team Hao Xiang Lai

**Topic:** "AI Overview": a nine-chapter beginner module, from "What is AI?" through learning, chatbots, everyday applications, embodied AI and alignment. The module is wrapped in a story: Lai Lai, Bit and Elder Mochi defeat nine "Myth Bosses" to relight the Lantern of Truth.

**Versions reviewed (Stage 2, V1.0)**
- Study Guide V1.0: `Hao_Xiang_Lai_Stage2_StudyGuide_V1.pdf`, 216 pages, 13.8 MB. The page footer reads "Study Guide v2.0"; please make the version label and the filename agree.
- Test Bank V1.0: `Hao_Xiang_Lai_Stage2_TestBank` (the file has no extension; its content is Markdown). 61 questions: 26 T/F, 27 MC, 8 open-ended.
- Study game: `Hao_Xiang_Lai_Stage2_LaiLaiAIAdventure_V1.html`, a 3D quiz adventure with 143 questions, one battle per chapter, 9 levels in total.
- PPT Slides V1.0: `Hao_Xiang_Lai_Stage2_PPT_V1.pdf`, 99 slides (PDF export; presenter notes [not available in the export / check the PPTX: edit]).
- Video Tutorials V1.0: `Hao_Xiang_Lai__Video1_Lai_Lais_AI_Adventure.mp4` (3:50, 960×544), `Video_Timeline_…txt` (subtitle file), and `Video_Guide_…pdf` (8 pages). **Only one video was posted.**

## Overall impression
The module has a strong identity. The same characters, the same nine bosses and the same "myth → facts" pattern appear in the guide, slides, video and game, and the visual design is consistent and friendly for beginners. The numbers we recomputed in the guide, slides and Test Bank are correct. The main risks before Nov 28 are: (1) the Test Bank is written against a 13-chapter outline, while the guide has 9 chapters, so some questions test content the guide never teaches; (2) the video collection is one 3:50 film that covers about one chapter's worth of the module; and (3) the guide's "Check your understanding" boxes have no answers.

## Scores (provisional; remap to the published rubrics)
| Deliverable | Coverage (20) | Format (20) | Content (40) | Overall (20) | Total |
|---|---|---|---|---|---|
| Study Guide and Test Bank | 17 | 18 | 33 | 18 | **86 / 100** |
| PPT Slides | 18 | 16 | 35 | 17 | **86 / 100** |
| Video Tutorials | 11 | 17 | 29 | 15 | **72 / 100** |

Study Guide bonus (reported separately): the 143-question study game loads and runs offline from one HTML file, and its questions carry explanations and difficulty tiers; award per the published bonus rule [add value]. [VERIFY: we confirmed that the game loads and read its question data, but could not play every battle; whoever on the team plays through all nine levels should confirm the bonus.]

---

## 1. Study Guide and Test Bank V1.0

### Strength to preserve: worked examples with hand-checkable numbers, followed by "What this shows"
Study Guide Worked Example 1.1 (p. 16; also Slide 10) and Worked Example 1.4 (p. 23): the navigation-app example asks the learner to compute 33 min vs. 40 min, then changes the goal ("must arrive within 45 minutes") so that the "rational" choice flips. The spam-filter example builds word scores from labelled emails. Each ends in a short "What this shows" box that states the lesson in one sentence. The numbers are small enough to do by hand, and the lesson is explained, not just stated. Keep this pattern; it recurs throughout all nine chapters. Slide 53 (Learning One Number, w = 2 → 4 → 5, then "Step too big? w = 9") is the best single example of how it carries over to the slides.

![Slide 53](screenshots/06_Slide53_worked_example_strength.png)

### Strength to preserve: a test bank made of scenarios and calculations with keys that explain wrong options
Test Bank M3, M4, M5, M8, M9, M18, M19, M24, M25, M26 and open-ended O2, O6, O7, O8: we solved these before reading the key, and every answer is correct (for example: M3 gives Fail 2–1 with distances B 2.00, C 2.24, D 2.24; M9 gives gradient −20 and new w = 1.0; M18 gives accuracy 96.25%, precision 60%, recall 75%; O2's divergence limit is a learning rate below about 0.21). The key names the likely mistake behind a wrong option (M9: "C misses the double negative"; M16: "A swaps those two figures"), and each open-ended answer lists key points and "valid alternatives". That is feedback a beginner can learn from.

![Test Bank M16 and key](screenshots/05_TestBank_M16_embeddings_and_key.png)

### Most important improvement: the Test Bank tests a 13-chapter module, but the guide has 9 chapters
The Test Bank header says "61 questions on Chapters 1–13", and its coverage table lists Ch. 8 "AI-powered research and search", Ch. 9 "AI in industry", Ch. 10 "Environmental systems and forecasting", and Ch. 11–13. The guide's table of contents (p. 3–4) has only nine chapters, and its Ch. 8 and Ch. 9 are "AI Behaviour, Decision-Making and Embodied AI" and "Real-World Risks, Governance and AI Alignment". We searched the guide's text for the key terms of the questions and found these with no matches: *embedding* (M16), *semantic search* (T15), *predictive maintenance* (T17), *concept drift* (O5), *ensemble* (O6), *break-even* (T20, M21, O6c), *physics-informed* (M20), and the five RAG stages (O4 and M17; the guide mentions RAG once, in one sentence, on p. 131). About 14 questions (roughly T15–T20, M16–M21, O4–O6) cannot be answered from the guide alone, and a beginner who studied the guide would meet these terms for the first time in the Test Bank. Also, the Test Bank tags questions with "Activity 1C", "Activity 8", "Activity 13G", but the guide has no activities with those names; it has Worked Examples (1.1–9.x) and Check your understanding boxes. Suggested fix: re-tag all questions to the guide's real chapters and section numbers (for example "Ch. 5, Worked Example 5.2"), then either add a short section for the missing topics or replace those questions with ones on content the guide teaches (the guide's Ch. 7–9 have plenty of material that has no question, such as SAE levels, handover and the three-layer defence in Ch. 9).

![Test Bank header](screenshots/04_TestBank_header_Chapters_1-13_coverage_table.png)
*(Image rendered from the Test Bank's Markdown source.)*

### Other issues
1. **Guide p. 19 (also p. 24, and every "Check your understanding" box; 35 boxes in total): no answers.** Question 1 ("In your own words, why is 'AI' hard to define precisely?") and Question 4 ("Name one AI system that is not machine learning…") are good, but a learner who is unsure has nowhere to check. Add a short "suggested answer" at the end of each chapter, or point each question to the page where its answer is built. The same applies to the "Before you battle: quick check" on the Boss Battle pages (for example p. 30).
   ![Guide p.19](screenshots/02_Guide_p19_Check_your_understanding_no_answers.png)
   ![Guide p.30](screenshots/03_Guide_p30_Boss_Battle_quick_check.png)
2. **Guide p. 3–4 (table of contents) and pp. 209–216 (references): the references are complete and well formatted, but they are not listed in the table of contents, and there is no module-wide glossary.** Each chapter ends with "Key terms", which is good. A beginner revising for the Test Bank has to search 216 pages for a term. Add "References" to the contents and consider one alphabetical glossary page that points to the section where each term is introduced.
   ![Guide p.4](screenshots/01_Guide_p04_TOC_no_glossary_or_references.png)
3. **Test Bank file housekeeping:** the file has no extension, so it will not open by double-click on most computers. When read as plain text, the title shows an `&#32;` artefact and the tags show raw backslashes (`\[Ch. 1, §1.3\]`). Export it as a PDF or .docx, and check the coverage table's open-ended column: O1, O3, O4 and O7 each appear under two chapters, which is accurate but may confuse a reader who is counting.
4. **Workload:** 216 pages is manageable, and the "⏱ 4 min" tags on slides help, but the guide itself has no suggested study time per chapter. Add one line to each Chapter Overview.

---

## 2. PPT Slides V1.0

### Strength to preserve: a consistent chapter rhythm that a teammate could teach from
Slides 7–18 (Chapter 1) and the same pattern in each later chapter: opening question ("Where did you meet AI today?") → definitions in short blocks → a Worked Example slide → "Guess the AI!" with a pair activity (slide 15) and its answer slide (16) → "Myth Busted" with the chapter's boss (slide 18) → a bridge to the next chapter. Each slide has one idea, colour-coded boxes (Surprise / Change the objective / What this shows) and a Lai Lai speech bubble for the teaching tip. The numbers on the slides we checked (slides 10 and 53) are correct, and the layout is the same in all nine chapters, so students always know where to look.

![Slide 10](screenshots/07_Slide10_dense_worked_example.png)

### Most important improvement: the answer is on the slide before the learner has tried; body text is small for the back of the room
Slide 10: the question ("Was the choice irrational?") and its answer ("No. It was the best choice with the information available.") are both visible at the same moment, in the "Surprise" box. The same happens on Slide 53 ("Step too big?" shows w = 9 and +16 with the table). If the deck uses animation to reveal these boxes, this is a non-issue; in the PDF export we cannot see that. [VERIFY in the PPTX.] If it does not, split each Worked Example into two slides (set-up, then reveal) so the room can predict first. Separately, the tables and the right-hand boxes use about 14–16 pt equivalent text. Text extraction shows about 130 words per slide on average, and some slides are close to 200 words, so a student at the back of a large room cannot read them. Where a slide has a table plus several boxes (by word count the fullest are slides 10, 53, 87, 92 and 96), move the box text into the presenter notes and enlarge the table.

### Other issues
1. **Section numbers do not match the guide.** Slide 96 is labelled "Section 9.4: AI Alignment", but in the guide 9.4 is "Deconstructing Pop Culture Myths" and alignment is 9.5 (p. 199). The slides also number Chapter 8 as 8.1–8.6, while the guide has 8.1–8.3 plus "Designing Safe and Trustworthy Embodied AI". Use the guide's numbers so learners can jump between the two.
   ![Slide 96](screenshots/08_Slide96_Section_9.4_vs_guide_9.5.png)
2. **Presenter notes:** not inspected (PDF export only). With slides this full, the notes decide whether a teammate can teach each slide in the 4 minutes it is tagged for. [VERIFY in the PPTX: every slide has notes.]
3. **Team slides (2–3), minor:** check that each photograph has a readable name and role caption, matching the guide's team page (p. 2), which lists seven members and roles.

---

## 3. Video Tutorials V1.0

### Strength to preserve: a story that teaches the history and corrects myths in short, visual beats
`Video1`, 0:51–2:08 and 2:11–2:37: dates appear as labelled cards (1943 McCulloch & Pitts, 1948 Wiener, 1950 Turing, 1956 Dartmouth), the narration says each in one sentence, and the burned-in subtitle repeats it in a high-contrast box. Myth Bosses then appear for the myths those dates correct (Ruledrax at 1:19: "Every program is just rules a human wrote!", answered by the perceptron and Samuel's checkers program at 1:25–1:30). At 2:07 the film states "Bit is a story metaphor — real AI doesn't evolve like a creature", and the 2:32 frame keeps a "Story metaphor" reminder on screen while Bit becomes the "Generative AI Bit". It is a brave and honest choice to stop a story from teaching a wrong picture. The dates and facts we checked (1943, 1948, 1950, 1956, 1958, 1959, 1966, 1997, 2012, 2017, 2020, 2022) are accurate.

![Video 2:32](screenshots/09_Video_0152_Stage5_Generative_AI_Bit.png)

### Most important improvement: one 3:50 film cannot carry a nine-chapter module
The assignment asks us to watch "every submitted tutorial", but only one video was posted. It covers the history (Ch. 3) and the "AI / ML / DL / generative AI" relationship (Ch. 2) in depth. The other seven chapters appear only as one-line rebuttals by a boss: Overfitz (Ch. 5) at 1:52–1:59, Scrollazar (Ch. 7) at 2:56–3:01, Defectron (Ch. 8) at 3:01–3:06, and Spectaculon (Ch. 9) at 3:08–3:14. Learning from data, chatbots, everyday applications, embodied AI and alignment have no video at all, and there is no moment where the learner has to stop and try something (the guide's worked examples, or the "Guess the AI!" slide, would translate well to a pause-and-predict). Suggested fix: add two to four short videos (about 3 minutes each) for the chapters with the most calculation or demonstration, such as Ch. 5 (the "Learning One Number" example from Slide 53 as a screen demo), Ch. 6 (the four chatbot generations) and Ch. 8–9 (deterministic rules vs. neural decisions; latency). Each can reuse the film's characters.

### Other issues
1. **Bit's stages and the boss order do not match the rest of the module.** The video narrates "Stage 1: Basic Bit" and "Stage 2: Learning Bit" (2:11–2:23), but the screen then shows "Stage 3 Deep Learning Bit", "Stage 4 Advanced Bit" and "Stage 5 Generative AI Bit" (2:32 frame above) without narration. The guide (p. 8), slides (slide 6) and game use four forms named Bit, Byte, Neuro and Omni, and those names never appear in the video. The boss order also differs: the video shows Knarlox as "Myth Boss 5/9" and Parrotex as "2/9", while the guide's levels are Ruledrax 1, Knarlox 2, Kryolith 3, Kludgemor 4, Overfitz 5, Parrotex 6. Pick one numbering and one set of Bit forms for all five deliverables.
   ![Video 2:05](screenshots/10_Video_0205_Myth_Boss_5of9_Knarlox.png)
2. **Small on-screen labels.** The file is 960×544. At 2:53–2:56 (AI winters) the labels "slow computers" and "scarce data" are small and sit far from the characters, and the AI-winter chart at 2:48–2:52 uses similarly small chart text. Export at 1080p, and enlarge chart labels to at least the size of the subtitles.
   ![Video 2:55](screenshots/11_Video_0255_small_labels_AI_winters.png)
3. **The Video Guide describes a different video.** The 8-page guide is the original script (the narrator-led version with timings such as "Scene 3, 0:45–1:20"); the final video has all nine bosses speaking, different Elder Mochi lines, and slightly different timings (the Scene 4 range "1:20–2:00" vs. the film's 1:19–2:37). It does not list the video files, a recommended watching order, or how the video links to the guide chapters, slides and game. Replace it with a one-page guide: file name, length, chapters covered, timestamps (the subtitle file already has them), and which guide page and game level follow each segment.
4. **Audio:** the track is present (mean −17 dB, peak −1 dB, so no obvious clipping), but we could not judge voice quality, pacing or pronunciation from extracted frames. [VERIFY by ear: pace of the 1943–1956 date run at 0:51–1:12, which has four dates in 21 seconds.]
5. **Pause points:** the film has no "pause and try" moments. Even one, such as before the 1:22 reveal that "some programs learn from data" (ask: "can a program learn from examples?"), would turn watching into practice.

---

## 4. How the three deliverables work together

**Concept traced: "Every program is just rules a human wrote" (Ruledrax) versus learning from data.**
- **Introduced:** Study Guide §1.2 (p. 20–22, traditional programming vs. machine learning) and Slide 13.
- **Seen in action:** Worked Example 1.4 (p. 23), the spam filter whose word scores come from labelled emails; Video 1:19–1:30 (Ruledrax, then the perceptron and Samuel's checkers).
- **Practised and checked:** Check your understanding 1.2 (p. 24), the Boss Battle page (p. 30), the Slide 18 myth card, the Level 1 game battle, and Test Bank T2 and M2 (M2 reuses the guide's word-score spam filter, so it assesses what Worked Example 1.4 teaches).

This is the best path through the module: every deliverable names the same boss, the same myth and the same fact. The gaps are the following.

**Gaps and contradictions**
- The Test Bank covers topics the guide does not teach (see §1), and cites "Activities" that do not exist in the guide.
- Bit's forms, the boss order and several section numbers differ between the video, slides and guide (§2 issue 1; §3 issue 1).
- The video covers one chapter's worth of the module, so most of the guide has no video (§3).
- The guide's practice boxes have no answers, so the only place a learner can check an answer is the game or the Test Bank key.

---

## 5. Revision priorities (in order)
1. **Align the Test Bank with the guide.** Re-tag every question to the guide's nine chapters and real worked-example or section numbers; for the roughly 14 questions on topics the guide never teaches (embeddings, semantic search, predictive maintenance, concept drift, ensemble forecasts, break-even probability, RAG stages), either add a short section to the guide or replace them. Export the file with an extension.
2. **Expand the video collection and rewrite the Video Guide.** Add two to four short tutorials for the chapters that have none, with at least one pause-and-predict moment each; re-export at 1080p; replace the script-style Video Guide with a one-page guide that matches the files and links each video to guide pages and game levels.
3. **Make practice self-checkable and the numbering consistent.** Add suggested answers to the 35 "Check your understanding" boxes and the Boss Battle quick checks; use one set of Bit forms, one boss order and the guide's section numbers on all slides and in the video; split the Worked Example slides so the reveal comes after the prediction.
