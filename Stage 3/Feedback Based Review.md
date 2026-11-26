# 📝 Feedback Based Review (Stage 3 Final Version)

**Purpose:** This document records the Stage 2 feedback that the instructor gave to all teams on the Markdown content, and explains how Team Infihhnite addressed each point in the final Markdown repository and the Stage 3 Final Verification Log. The final snapshot builds on the Stage 2 snapshot (commit `578aa5f`) and was verified between 25/11/2026 and 27/11/2026.

### 1. Content Coverage

* **Feedback received:** The Markdown did not fully cover the content it should have.

* **Action Taken in the Final Version:**
  * **Complete module structure.** The module contains 11 chapters in three sections (`Big Data`, `Connectionist AI`, and `Where Big Data Meets Connectionist AI`). Each chapter was checked for a worked example, a learner activity, and answers.
  * **Complete README.** The README now states prerequisites, learning outcomes, a recommended reading order, the location of assets and learning resources, how to open supporting materials, final version information, and known limitations. Each section uses relative links to the chapters.
  * **One consistent chapter template.** We agreed on a single template and added "Before you start" notes and terminology sections where a learner needs ideas from earlier chapters (for example, the terminology tables added to Chapters 3 and 4).
  * **Accurate cross-references.** References that used earlier numbering or topic names only were replaced with chapter and section numbers (Chapters 7, 8, and 9).
  * **Whole-module completeness check.** We checked 12 criteria: intended learners, prerequisites, measurable outcomes, logical sequence, no unfinished material, an example, activity, and answers in every chapter, references for borrowed material, labeled optional extensions, repeated explanations, consistent terminology, missing prerequisites, and transitions between chapters. All 12 are recorded as Verified.
  * **Verified accuracy.** Key claims in Chapters 7, 9, and 10 were rechecked against the primary sources (IEA, FDA, Krizhevsky et al., Voets et al., Kaplan et al.), and every worked calculation was recomputed from the text alone.

### 2. Supporting Resources and Image Assets

* **Feedback received:** The Markdown did not include enough resources, especially image resources, to support the production of the Study Guide, Test Bank, PowerPoint slides, and video.

* **Action Taken in the Final Version:**
  * **Assets are organized and documented.** The `assets/` folder is described in the README, including where each resource is and how to open it. The README previously stated that assets were referenced by relative paths without embedding any image from `assets/`. We fixed this by embedding the roadmap images, such as the module map, using relative paths, so every image shown is also available as a file for the other deliverables.
  * **Image inventory:** The final repository contains a number of images in `assets/`
  * **Reusable visual and structured content.** Mermaid diagrams (Chapters 5, 6, and 7), tables, worked numeric examples, and answer boxes provide ready-made material for slides, video storyboards, and test questions. The Chapter 7 diagram was rewritten so that it renders correctly.
  * **Rendering and portability verified.** Every image displays, local file paths were replaced with relative paths, Mermaid diagrams and answer boxes were confirmed on GitHub, and no private data appears in public content.
  * **Source tracking.** Every claim and image that borrows material has a marker and a listed source.

### 3. Verification of the Final Version

* **Feedback received:** Stage 2 results showed the need for a complete, checkable final package.

* **Action Taken in the Final Version:**
  * **Independent review.** Every file was checked by a team member other than its author, and the log records the reviewer and the date for each file.
  * **Findings resolved.** All seven findings in the Stage 3 Final Verification Log are marked Fixed or Verified, each re-read by a reviewer who did not make the fix.
  * **Package and snapshot checks.** We compared the rendered PDF with the Markdown source, confirmed that the repository matches the submitted snapshot, and tested the final package `Infihhnite_Stage3_FinalMarkdown_Repository.zip` on 27/11/2026.

### 4. Summary of Feedback and Response

| Feedback | Response in the final version | Where to verify |
| --- | --- | --- |
| Content not fully covered | 11 chapters with example, activity, and answers; complete README; one chapter template; terminology sections; corrected cross-references | Log Sections 2, 3, 4, 6 |
| Not enough resources, especially images | Documented `assets/` folder; roadmap images embedded with relative paths; Mermaid diagrams, tables, and worked examples ready for reuse | Log Sections 3 (finding 2) and 7 |
| Need for a checkable final package | Independent chapter reviews; PDF-to-Markdown comparison; repository-to-snapshot comparison; package test | Log Sections 8, 9, and 10 |

### 5. Evidence of Revisions

| Commit | File | Change |
| --- | --- | --- |
| `bfb60cc` | Chapter 03: Big Data Technologies | Added a terminology table |
| `0a69e21` | Chapter 04: Introduction to Connectionist AI | Added a terminology section |
| `2eb76f7` | Chapter 08: Preparing Data for a Network | Updated references to chapters and sections |
| `d78f2aa` | Chapter 09: Applications and Case Studies | Updated references to chapters |
| `63f41d4` | Chapter 07: Why Big Data Fuels Neural Networks | Standardized American spelling |
| `bdcbd18` | Chapter 07: Why Big Data Fuels Neural Networks | Reworked a diagram section that had rendering issues |

### 6. Status at Submission

At the time of submission, every finding in the Stage 3 Final Verification Log is marked Verified, and the final package has passed the checks recorded in Sections 7 to 10 of that log. The team will log and correct any further issue identified after submission.
