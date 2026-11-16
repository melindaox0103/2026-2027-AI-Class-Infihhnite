# Infihhnite — Stage 3 Peer Review

**Reviewing team:** Infihhnite  |  **Members:** [add names]

---

# Assigned Team: Team Name: Not Found

**Topic:** "Inside the Machine": Hardware, Network Infrastructure and Behaviourist AI (16 chapters, 16 "cases")

**Versions reviewed (Stage 2, V1.0)**
- Study Guide V1.0: `1_1__StudyGuide_V1.pdf`, 519 pages
- Test Bank V1.0: `1_2__TestBank_V1.pdf`, 36 pages, 75 questions (32 T/F, 32 MC, 11 open-ended)
- PPT Slides V1.0: `2__PPT_V1_pptx.pdf`, 78 slides (PDF export; presenter notes [not checked / checked: edit])
- Video Tutorials V1.0: Section0_Intro (1:33), Section1_Hardware (8:48), Section2_Networks (8:54), Section3_BehavioristAI (8:17), Section4_PuttingItTogether (8:53), plus `VideoGuide_V1.pdf`. The Video Guide lists the files as `TeamNameNotFound_VideoXX_*.mp4`; the posted names differ, but the file sizes match the guide byte for byte.

## Overall impression
The three deliverables share one idea: every chapter is a "case" that the learner predicts, tries, and closes. The same sixteen cases, numbers and characters (Nova and Byte) appear in the guide, slides, videos and Test Bank. That coherence is the team's biggest strength. The main risks before Nov 28 are (1) video fixes that the team's own guide says are not yet applied, (2) a few numbers and prediction questions that differ between deliverables, and (3) source quality and slide legibility.

---

## 1. Study Guide and Test Bank V1.0

### Scores (provisional; remap to the published rubric)
| Criterion | Points |
|---|---|
| Coverage and completeness | 18 / 20 |
| Format and aesthetics | 17 / 20 |
| Quality of content | 35 / 40 |
| Overall impression | 18 / 20 |
| **Total** | **88 / 100** |

Study Guide bonus (reported separately): [pending rubric]. The guide includes 22 optional simulator Labs, but we did not run them, so we are not claiming the bonus.

### Strength to preserve: predict-first activities with reasoned answers
Study Guide Ch 1, Activity 1.2 (p. 17): learners predict, trace a 4 + 9 program by hand, swap two steps, and then open an answer that explains why ("the 4 is overwritten and lost, because the accumulator holds only one value"). The error becomes the lesson, and the Answer box explains the reasoning, not only "13 / 18". Keep this structure in every chapter. I confirmed it recurs across the chapters: 97 Activity boxes, 23 Lab boxes and 17 Predict First boxes.

![Guide p.17](screenshots/07_Guide_p17_Activity_1_2.png)

### Strength to preserve: an answer key that teaches
Test Bank Answer Key B, Q51 (p. 26): the key shows the arithmetic (−5 + 100 − 20 = 75) and explains why distractor C (74) is wrong. Q34 and Q41 explain each wrong option the same way. The open-ended key (p. 28 onward) gives key points and a sample answer. I recomputed Q8, Q14, Q30, Q40, Q41, Q45, Q47, Q51, Q57, Q67, Q68, Q69, Q72, Q73, Q74 and Q75, and all key answers are correct.

### Most important improvement: the Study Guide cites unreliable image sources
Study Guide p. 36 (Fig 1.9 Wikipedia, Fig 1.11 a TikTok post) and p. 64 (Fig 2.9 Wikipedia), plus stock-photo and blog pages elsewhere. For a course module, replace them with museum, university, Britannica or manufacturer sources, or the team's own figures. The text references (Princeton, MIT, IBM Research, p. 35) are strong, so the image sources should match that standard. Check the image tables at the end of each chapter for the same pattern.

![Guide p.36](screenshots/09_Guide_p36_image_sources_Wikipedia_TikTok.png)

### Other issues (location, what happened, fix)
1. **Guide p. 20, Fig 1.14–1.17 (Activity 1.3):** The screenshots show a program that stores into FIRST and SECOND, while the text program uses NUM. A beginner comparing their Little Man Computer screen with the figure will see different addresses (908/909 vs 908). The guide admits this in the caption, but it adds friction. Re-shoot the figures with the text program.
   ![Guide p.20](screenshots/08_Guide_p20_LMC_figure_differs_from_text_program.png)
2. **Guide p. 10 and p. 31, Test Bank Q1 (True):** "Four core hardware components: processor, memory, network and storage." A network is not usually listed as a core component of a computer; input/output devices are, and the guide's own answer to its chapter-end Q1 (p. 32) mentions I/O devices as a wrong option. Rephrase ("four main parts a computer uses") or treat the network as a connection. **[VERIFY with Content Lead]**
3. **Test Bank Q70 and Video 3 / Slide 50 disagree on the same experiment.** Test Bank p. 19: ε = 0% averages $1,114 and 83% of games get stuck on A; ε = 20% averages $1,309. Video 3 (4:23–4:56) and Slide 50 say ε = 20% earns $1,490 and ε = 0% earns exactly $1,000 with machine B "never" tried. Both are right (one run vs. a 300-game average), but a learner will think they contradict. Say "in this run" in the video and slide, and add one sentence on averages.
   ![TB p.19](screenshots/10_TestBank_p19_Q70_table.png)
   ![TB p.32](screenshots/11_TestBank_p32_Q70_key.png)
4. **Workload:** The guide states 70–120 minutes per chapter (p. 8), so 16 chapters take roughly 19–32 hours, in one 519-page, 100 MB PDF. Consider a "core path" that marks which activities are optional per chapter, and chapter-level PDFs.

---

## 2. PPT Slides V1.0

### Scores (provisional)
| Criterion | Points |
|---|---|
| Coverage and completeness | 17 / 20 |
| Format and aesthetics | 18 / 20 |
| Quality of content | 34 / 40 |
| Overall impression | 17 / 20 |
| **Total** | **86 / 100** |

(The 17/20 on coverage is partly because we could not check presenter notes. Adjust once a teammate has opened the PPTX.)

### Strength to preserve: one repeatable, low-text lesson loop
Slides 6–9, 10–13, etc.: every case runs Predict (3 options, "raise your hand") → Idea (one diagram) → See it work (one number) → Case closed (cause, fix, vote answer). Most slides carry 5–35 words, so a prepared teammate can teach the lesson and the room can follow it. Slide 8 ("Trace it: what does PRINT show?", bonus: swap steps 2 and 3) turns the guide's Activity 1.2 into a 90-second classroom task. This is the model the other cases should keep. This directly avoids the text-heavy problem hello_world flagged in many teams.

![Slide 8](screenshots/06_Slide08_trace_it_strength.png)

### Most important improvement: simulator screenshots are too small to read from the back
Slide 16 (battery budget): the chart axes and the sentence "Of the average current, 91% comes from the awake time…" are far below readable size. The same pattern recurs on the other "See it work" slides (e.g., 12, 20, 25, 29, 33, 37, 42, 46, 50, 59, 63, 67, 71). Crop each screenshot to the single number or bar the slide is about and enlarge it (at least 18 pt equivalent). The big red result already on the slide (37.9 days) is the right size; the screenshot should support it, not compete with it.

![Slide 16](screenshots/05_Slide16_small_simulator_text.png)

### Other issues
1. **Case #001 asks three different prediction questions.** Slide 6 offers (A) CPU too slow / (B) waits for data from storage / (C) screen too small. Video 0 (1:04) asks "memory, storage, or the network?" and the Video 1 reveal (2:23) says "if you guessed memory, you were close", while the Case Closed slide says storage. Use one wording everywhere (for example: "RAM fills up, data spills to storage, the CPU waits").
2. **Slide 7** introduces register, cache, RAM and SSD with no definition on the slide. The team's own review record (Video Guide p. 29) says these were added to Video 1; make sure the slide or its presenter notes carry the same definitions. **[VERIFY in the PPTX notes]**
3. **Presenter notes:** Not inspected (PDF export only). Confirm every slide has teaching notes, since the slides alone are deliberately short.

---

## 3. Video Tutorials V1.0

### Scores (provisional)
| Criterion | Points |
|---|---|
| Coverage and completeness | 17 / 20 |
| Format and aesthetics | 15 / 20 |
| Quality of content | 34 / 40 |
| Overall impression | 16 / 20 |
| **Total** | **82 / 100** |

(Audio, pacing and narration were not assessed by ear; adjust after a teammate has listened.)

### Strength to preserve: pause-and-predict with the reveal withheld
Video 1, 1:05–1:25: the narration sets up the swapped program, a "PAUSE & PREDICT" badge appears, the accumulator and OUTPUT boxes stay empty ("?"), and the answer (18) is only given afterwards, with the reason ("the second get erased the four"). Learners commit to a guess before they see the result. The narration also explains instead of reading slides, and I checked its numbers (6.2 MB frame, 187 MB/s, 37.9 days, 4.1 days, 0.56 m vs 1.95 m, 90 vs 66) against the Test Bank and found them consistent.

### Most important improvement: apply the fixes the team's own guide lists as "planned"
Video Guide p. 29 says the revisions for Videos 0, 1, 3 and 4 are "planned and not yet applied", while the same page's table says all five were "Revised after peer review". Please make the guide and the files agree. Evidence that the fixes are still needed:

- **Video 0, 0:30–0:33:** The narration says "six students, six roles", but the slide shows five cards. Falent Ananta Christanto (Quality Lead) is missing, and "Nemindhara Naththarampotha" has no surname.
  ![V0 0:31](screenshots/01_Video0_0031_team_slide_five_of_six.png)
- **Video 1, 3:04–3:19 and 3:42–4:05:** A dark caption band covers about the bottom 40% of the cook-off simulator, hiding the chart the narrator describes. The top heading is also clipped. During the 4:05 reveal ("about four percent") the viewer cannot see the tie point on the chart.
  ![V1 3:10](screenshots/02_Video1_0310_caption_band_covers_simulator.png)
- **Video 2, 4:58–5:20 (latency pause):** The simulator already shows "WAITING (LATENCY) 50 ms" during the pause, so part of the answer is visible. The caption band is also still over the lower half.
  ![V2 5:08](screenshots/03_Video2_0508_latency_value_visible_during_pause.png)
- **Video 3, 4:36–4:56 (epsilon pause):** Nearly empty screen with a stray empty red rectangle; the options "$1,000 / machine B" exist only in the caption.
  ![V3 4:45](screenshots/04_Video3_0445_near_empty_pause_screen.png)

### Other issues
1. **Density:** Each lesson video covers four chapters in about 8.5 minutes (about 2 minutes per chapter). Video 2 introduces roughly 20 terms by the team's own count (Video Guide p. 30). Keep the "define once, in one sentence" rule for every term.
2. **Pause length:** 10 seconds is short for calculation questions (Video 3 at 2:42, maze score; Video 4 at 6:33, car stopping). The guide says viewers can pause, but add an on-screen line such as "Pause the video now".
3. **Audio:** Both voices are Kokoro text-to-speech (Video Guide p. 28), and the guide says not every member has listened to them. **[VERIFY by ear: pronunciation of "ε", "TCP/UDP", "QoS", numbers]**
4. **Housekeeping:** Video Guide p. 29 lists Video 3 as 8:16 and Video 4 as 8:52; the files are 8:17 and 8:53.

---

## 4. How the three deliverables work together

**Concept traced: Case #001 (the idle processor / bottleneck).**
- **Introduced:** Video 0 (0:00–0:14) and Guide Ch 1 Case File (p. 9), Fig 1.1 Task Manager (p. 10).
- **Seen in action:** Slides 6–9; Video 1 (0:29–2:34), including the memory ladder.
- **Practice:** Guide Activities 1.2–1.5 (pp. 17–30); Test Bank Q2, Q34, Q65.

This is a strong chain: every deliverable points to the next one with exact references (Slide 5, Video Guide connection tables).

**Gaps and contradictions**
- The three prediction wordings for Case #001 (above).
- The ε-greedy numbers (Video 3 / Slide 50 vs Test Bank Q70).
- The Test Bank assesses ideas that the videos and slides do not teach: jitter and corruption (Q10, Q42; Video 2 teaches only "three enemies"), local maximum (Q22, Q70b), sensor fusion (Q7, Q74c), zero-sum (Q73a), systolic array (Q4). They are taught in the guide, but a learner who only watches the videos will meet them first in the Test Bank. Either add one sentence in the video or slide, or mark these questions "Study Guide only".

---

## 5. Revision priorities (in order)
1. **Fix and re-export the videos, and make the Video Guide match.** Add the missing sixth member on Video 0; move captions off the simulators (Videos 1, 3, 4) and hide the answers in every pause (Video 2 latency pause); fill the empty Video 3 pause screen; then correct Video Guide p. 29 so it states what was actually applied.
2. **Make the numbers and wording identical across the deliverables.** Use one Case #001 prediction question; add "in this run" or an average sentence for the ε-greedy figures (Video 3, Slide 50, Test Bank Q70); add the Test-Bank-only terms to a slide or video, or label them.
3. **Raise source quality and slide legibility.** Replace the Wikipedia/TikTok/stock image sources (Guide pp. 36, 64); re-shoot Fig 1.14–1.17 with the text program; crop the simulator screenshots on slides 12–71 to one readable number each.

---

# Team of Our Choice
[to be written by your team]
