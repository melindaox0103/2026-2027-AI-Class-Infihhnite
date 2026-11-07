# **Stage 1 Content Review Log**

**Team:** Infihhnite  \|  **Module:** Big Data and Connectionist AI  \|  **Reviewer:** David (Quality Lead)  \|  **Review date:** 26/10/2026

**Author(s) of reviewed material:** Matthew (CEO), Melinda (CIO), Jesselyn (Visual Design Lead), William( Content and Video Lead), David (Quality Lead)

*How to use this log: one row per finding. The author fixes it, then the reviewer re-checks the fixed text and marks it Verified. Never mark a row Verified without re-reading the corrected text. Status values: Open, In progress, Fixed, Verified.*

## **1\. Findings to fix**

| \# | Location | Problem found | Suggested fix by Quality Lead | Upcoming Updates | Owner | Status | Checked by / date |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | Evolution and benefits, benefits table | The Efficiency example repeats the Better Decisions example (delivery company and traffic data). | Give Efficiency its own example, such as a factory using sensor data to predict repairs before a machine breaks. | Study guide, slides | William | In Progress | David / 26/10/2026 |
| 2 | Small data vs big data table | Big Data insight type is labelled "Qualitative, predictive". | Change to "Quantitative, predictive". | Study guide, slides | Matthew | Verified | David / 26/10/2026 |
| 3 | Same table | Small data goal says "Finding causation (the why)", which overclaims. | "Understanding the context behind behaviour". | Study guide, slides | Matthew | Verified | David / 26/10/2026 |
| 4 | Definition, Velocity example | "1000 people trying to get inside" does not show data arriving quickly. | Use a data stream, such as thousands of messages or video views arriving every second. | Study guide, slides, video | Matthew | Verified | David / 26/10/2026 |
| 5 | Definition, Volume example | It is a question, not an example, and has a grammar error ("visits"). | Rewrite it as a statement, for example "Millions of people visit the square each year, and every visit produces records." | Study guide, slides | Matthew | verified | David / 26/10/2026 |
| 6 | 5 Vs table, Volume example | "Thousands of different types of students" mixes up volume and variety. | "Records for thousands of students". | Study guide, slides, video, test bank | Matthew | Verified | David / 26/10/2026 |
| 7 | Section 1.3 intro | "Small data can come in any of three structures" is wrong, because the three structures describe all data. | "Data can come in three structures". | Study guide, slides | David | Verified | David / 26/10/2026 |
| 8 | Plan outline, Technologies | "Scale UP vs Scale DOWN" is the wrong pair. | "Scale up (vertical) vs scale out (horizontal)". | Plan, study guide, slides, test bank | David | Verified | David / 26/10/2026 |
| 9 | Plan outline, Data pipeline | The order reads "Store, Collect, Analyze, Clean, transform, present". | Collect, store, clean/transform, analyse, present. | Plan, study guide, slides, video | David | Verified | David / 26/10/2026 |
| 10 | Plan outline, wording | "Notes and Outliers"; "AI configuration"; "Real-time sharing"; garbled visualisation cell. | "Noise and outliers"; "AI integration"; "Real-time streaming"; rewrite the visualisation cell clearly. | Plan | Matthew | Verified | David / 26/10/2026 |
| 11 | Semi-structured data | CSV is listed as semi-structured, but many sources call it structured. | Divert CSV’s classification from semi-structured to structured. | Study guide, test bank | Matthew | Verified | David / 26/10/2026 |
| 12 | Heading numbers | Numbers jump (1, 3, 4\) and are inconsistent ("1.3"). | Renumber all headings in order. | All files | Melinda | In Progress | David / 26/10/2026 |

## **2\. Beginner-friendliness issues**

| \# | Location | Problem found | Suggested fix | Owner | Status | Checked by / date |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| B2 | Big Data data-types section | SQL, JSON and XML code blocks conflict with the boundary "excludes in-depth programming". | Keep one tiny example or remove; or change the boundary. |  | Verified | David / 26/10/2026 |
| B3 | Learning goals | "Teach them how to use connectionist AI efficiently" and "spread the precautions and rules" are not things a learner can explain or do. | Rewrite as measurable goals, for example "explain the 5 Vs and give one example of each". | Melinda | Verified | David / 26/10/2026 |
| B4 | Target audience | Primary school audiences may not match topics such as gradient descent, backpropagation and MapReduce. | Team decision: simplify with analogies, or change the audience to "beginners". Record the decision in the meeting log. | Melinda | Verified | David / 26/10/2026 |

## 

## **3\. Fact and source check**

| Claim or source | Checked against | Result (Confirmed / Corrected / Not found) | Checked by / date |
| :---- | :---- | :---- | :---- |
| Scale up \= vertical, scale out \= horizontal. **CloudZero (cloudzero.com)**  | Scale up means a bigger machine (vertical) and scale out means more machines (horizontal).  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| Scale up and scale out can be used together. **O’Reilly (oreilly.com)**  | The two approaches aren’t mutually exclusive, and an application can use either, both or neither.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| “Scale down” is the wrong pair. **PingCAP (pingcap.com)**  | Scaling down is described as contraction, to reduce resources and costs.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| MapReduce step order. **Heather Miller course notes (heather.miller.am)**  | MapReduce has map and reduce phases, with shuffle and sort between them, and uses a word-count example.  | Confirmed. Plan’s “split, shuffle, map, reduce” is Corrected to split, map, shuffle, reduce  | AI-assisted draft, 27/10/2026; re-verified by David |
| MapReduce order. **Colorkrew blog (blog.colorkrew.com)**  | The steps are split, map, combine, shuffle, reduce.  | Confirmed (a simpler version is fine for beginners)  | AI-assisted draft, 27/10/2026; re-verified by David |
| MapReduce. **work-saas-media.com**  |  | Data was not Found | AI-assisted draft, 27/10/2026; re-verified by David |
| CSV classification. **thedataschool.co.uk**  | It treats CSV as a debated case, with the semi-structured side arguing that the format doesn’t enforce a schema.  | Sources disagree  | AI-assisted draft, 27/10/2026; re-verified by David |
| CSV classification. **Coursera**  | CSV counts as semi-structured when fields are flexible, and structured if it follows a strict tabular schema.  | Sources disagree  | AI-assisted draft, 27/10/2026; re-verified by David |
| CSV classification. **withsurface.com**  | CSV is usually treated as structured, though the format doesn’t enforce a schema.  | Corrected: use wording that says “usually structured; some sources say semi-structured because no schema is enforced”  | AI-assisted draft, 27/10/2026; re-verified by David |
| The 5 Vs definitions. **TechTarget (techtarget.com)**  | The page defines velocity, volume, value, variety and veracity as speed, amount, benefit, diversity of types, and quality and accuracy.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| Big data defined by 3 Vs (volume, velocity, variety). **TechTarget and Iberdrola**  | TechTarget says big data was first described with three Vs before value and veracity were added. Iberdrola also describes big data with three Vs.  | Confirmed | AI-assisted draft, 27/10/2026; re-verified by David |
| Structured, semi-structured and unstructured definitions and comparison table. **Educative (educative.io)**  | The page defines the three types, with semi-structured data using tags or markers, and compares format and schema.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| Structured, semi-structured and unstructured data. **Big Data Framework, CareerFoundry, Datamation**  | Data of Datamation was not found | The associated data has been removed | AI-assisted draft, 27/10/2026; re-verified by David |
| Small data definition (human-comprehensible, accessible, actionable). **Wikipedia: Small data**  | Small data is described as data small enough for human comprehension, in a volume and format that is accessible, informative and actionable.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| Big data is about machines, small data is about people. **Wikipedia**  | The page states this contrast, and gives five related data points or an eyewitness observation as small data examples.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| Big data finds correlations, small data finds causation. **Wikipedia and WEF**  | The WEF interview presents this as Martin Lindstrom’s argument.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| Small data is qualitative, big data is predictive. **Iberdrola**  | Iberdrola says big data analyses behaviours and predictive patterns at large scale, while small data provides qualitative information.  | Partly confirmed. “Quantitative” for big data isn’t stated in any source. | AI-assisted draft, 27/10/2026; re-verified by David |
| IoT sensor data as small data. **Wikipedia**  | One definition lists temperature, wind speed, vibration and status data from IoT as small data.  | Confirmed. The structure mapping (structured / semi-structured) is the team’s own and is labelled so  | AI-assisted draft, 27/10/2026; re-verified by David |
| Small data started in marketing and is now used in many sectors. **Iberdrola**  | Iberdrola says small data began in marketing and is increasingly important in all sectors and company sizes.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |
| Small data is faster and cheaper to collect. **WEF, Iberdrola, Wikipedia**  | Data was not found | Data not found and has been removed accordingly | AI-assisted draft, 27/10/2026; re-verified by David |
| Small data is context-rich and emotional. **WEF**  | Lindstrom says emotions are hard to describe with data, and presents small data as explaining the “why” behind what big data shows.  | Confirmed  | AI-assisted draft, 27/10/2026; re-verified by David |

## **5\. Review outcome (for the project log and Markdown V1.0 report)**

Fill in only what was actually done.

* **Reviewed:** Big Data Introduction content (Chapter 1, sections 1.1 to 1.5), the Stage 1 outline and table of contents (Big Data rows), the learning goals, the scope and boundaries.  
* **Reviewer:** David (Quality Lead)  \|  **Author:** Everyone  \|  **Date:** 27/10/2026

* **Found:**   
  * Weak or incorrect examples: rows 1, 4, 5, 6 (repeated Efficiency example, Velocity example not about data speed, Volume example written as a question, Volume example mixed up with Variety).   
  * Inaccurate or overclaimed statements: rows 2, 3, 7 ("Qualitative" for big data, causation claim unattributed, "small data can come in three structures").   
  * Outline errors: rows 8, 9, 10 (Scale up vs Scale down, pipeline order, wording errors). The source check also found that the MapReduce order in the outline (split, shuffle, map, reduce) is wrong, and that the pipeline order is still wrong in the latest outline.   
  * Sources that disagree: row 11 (CSV classification).   
  * Structure: row 12 (heading numbers)  
  * Beginner-friendliness: B2 (code blocks vs the boundary), B3 (learning goals not measurable), B4 (audience level).   
  * Source check (Section 3): "faster and cheaper to collect" and the "Quantitative" label were not supported by the sources opened, and the structured-data examples closely matched one source.   
* **Corrected or confirmed:**  
  * Corrected and re-read by David on 26/10/2026 (log rows marked Verified): rows 2, 3, 4, 5, 6, 7, 10, 11, B2, B3, B4. Row 8 is corrected in the outline, but the status table still shows the old "Scale UP vs Scale DOWN" title.   
  * Confirmed correct against sources: scale up (vertical) vs scale out (horizontal); the 5 Vs definitions; the small data definition and the machines vs people contrast; small data started in marketing.   
  * Still open: row 1 (in progress, William), row 12 (in progress), row 9 and the MapReduce order (the latest outline still shows the old order), and the status table title for 3.2.   
  * Overhauled the entirety of the content’s visuals as well as made necessary changes to the overall look of the project while keeping the   
* **Evidence reference:** The Picture below showcases before and after a section of the content specifically the 5Vs was revised.


## 

