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
