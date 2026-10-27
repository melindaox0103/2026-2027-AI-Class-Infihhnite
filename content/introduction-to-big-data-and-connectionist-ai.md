# Section 1: Big Data

## Chapter 1: Introduction to Big Data

### Development status (Stage 1 snapshot)

| Section | Status | Notes |
|:---|:---|:---|
| 1.1 Definition | Drafted | Needs peer review |
| 1.2 The 5 Vs | Drafted | Includes worked example, activity and answers |
| 1.3 Evolution and Benefits | Drafted | Evolution timeline still needs a source |
| 1.4 Types of Data and Sources | Drafted | Includes activity and answers; examples rewritten |
| 1.5 Big Data vs Data Warehousing | Outline only | Not yet written |
| Chapters 2 and 3 | Outline only | See the outline file |

**Terms used in this chapter**

- **Data**: facts such as numbers, words, pictures or sounds that a computer can store.
- **Analyse**: to look carefully at data to find patterns or answers.
- **Schema**: a plan for how data is organised, such as the column headings of a table.

---

### 1.1 Definition

Big Data is an important part of today's digital world. It helps businesses understand customers, schools improve learning, scientists study animals, sports teams analyse performance, and social media platforms recommend content.

To understand how Big Data works, we start with the 5 Vs (section 1.2), which describe its main characteristics. After that we look at how data has changed over time (1.3), the types of data and where they come from (1.4), and how big data differs from a data warehouse (1.5). Later chapters cover how data is processed and analysed, and the technologies behind it.

#### What makes data "big"?

Big data is a mix of organised, partly organised and unorganised data that organisations collect and then study to find useful insights [1]. Early descriptions of big data used three Vs: **volume** (how much), **velocity** (how fast) and **variety** (how many kinds) [1][4].

What counts as "big" is not a fixed number. It depends on the computing power available at the time [1].

#### Big data examples

- A chain of shops with hundreds of stores records millions of purchases every day [1].
- Hospital machines and wearable devices send health readings all the time, and the readings must be analysed quickly [1].
- A video app receives likes, comments and uploads from millions of people.

#### Small data

Small data is data that is small enough for a person to understand. It is organised in a way that makes it easy to access and use [5]. Even five related pieces of data, or one eyewitness observation, can count as small data [5].

A common way to explain the difference is: big data is about machines, small data is about people [5].

| Aspect | Small data | Big data |
|---|---|---|
| **Focus** | People | Machines |
| **Typical goal** | Understanding the reason behind what people do (the *why*) | Finding patterns and links in huge amounts of data (the *what*) |
| **Volume** | Small enough to read and understand | Enormous, needs special tools |
| **Type of insight** | Qualitative: observations, habits, feelings [4] | Predictive patterns found at a large scale [4] |
| **Example** | Watching how a family uses its kitchen | Studying millions of online searches |

The "why versus what" contrast is the view of Martin Lindstrom, who popularised the term "small data" [3][5]. It is one expert's argument, not a rule everyone agrees on.

**Why small data matters**

- It can show feelings and context that numbers alone often miss [3].
- It started in marketing and is now used in many fields and by companies of any size [4].
- It works best together with big data: big data shows what is happening, and small data helps explain why [3][4].

<!-- REVIEW 27/10: removed "faster and cheaper to collect" and "useful for teams without big-data infrastructure". Not found in WEF, Iberdrola or Wikipedia. Re-add only with a source. -->

---

### 1.2 The 5 Vs

The 5 Vs are five main features of big data: velocity, volume, value, variety and veracity [1].

| V | What it means [1] | Everyday example |
|:---|:---|:---|
| **Volume** | How much data there is | A school system keeps attendance, grades and library records for thousands of students over many years |
| **Velocity** | How fast data is created and how fast it must be handled | Thousands of likes and comments arrive every second when a popular video goes live |
| **Variety** | The many different kinds of data | Photos, videos, text messages and call logs |
| **Veracity** | How accurate and trustworthy the data is | A teacher removes duplicate survey answers so the results are correct |
| **Value** | The useful benefit gained from the data | A school uses students' food preferences to choose snacks for an event |

Some sources add a sixth V, **variability**, which means inconsistency in how data is used or how it flows [1]. In this guide we keep to the five Vs.

#### Worked example: Leo's phone

Leo's family phone has 5,000 photos. Which V is this?

1. **Read the clue.** The clue is "5,000 photos", which is about a *number of items*.
2. **Match the clue to a question.** Volume asks "how much?", velocity asks "how fast?", variety asks "how many kinds?", veracity asks "is it true?", value asks "is it useful?".
3. **Choose.** The clue is about *how much*, so it is **Volume** (answer B).
4. **Check the others.** Nothing says the photos arrive quickly (not Velocity), that anything is wrong with them (not Veracity), or that they are used for something (not Value).

Note: one phone is not "big data" by itself. The example only shows what the word *volume* means.

#### Try it: which V is it?

Match each situation to a V.

1. A school stores twenty years of student records.
2. A live sports app updates scores and comments every second.
3. A survey has the same student's answers entered twice by mistake.
4. A library collects book titles, photos of covers and recordings of story time.
5. A canteen uses survey results to decide which snacks to sell.

**Answers**

1. **Volume.** The point is the *amount* of data stored.
2. **Velocity.** New data arrives constantly and must be handled quickly.
3. **Veracity.** Duplicate answers make the data less accurate and trustworthy.
4. **Variety.** Titles, photos and audio are different kinds of data.
5. **Value.** The data is used to make a useful decision.

---

### 1.3 Evolution and Benefits

#### Evolution of big data

- **Traditional databases:** people stored organised information, such as customer names and sales records.
- **Web and social media:** websites and social media created more data, such as comments, photos, videos and searches.
- **Cloud computing:** people could store data and use computer power over the internet.
- **Internet of Things (IoT):** devices such as smartwatches and sensors began collecting data automatically.
- **Today:** big data tools and AI help people analyse very large amounts of information.

<!-- REVIEW 27/10: timeline has no source yet. Add a reference before marking this section "checked". -->

#### Benefits of big data

Organisations use big data to improve how they work, serve customers better and personalise marketing [1].

| Benefit | What it means | Example (written by our team) |
|:---|:---|:---|
| **Better decisions** | People choose better by looking at information and spotting patterns | A delivery company uses traffic data to find faster routes |
| **Efficiency** | People save time, money and resources | A factory uses sensor data to predict repairs before a machine breaks |
| **Personalisation** | Apps and websites suggest things that match a person's interests | A video app recommends videos based on what you watch |

---

### 1.4 Types of Data and Sources

Data of any size, big or small, can be organised in three ways. The difference is how much *schema* (planned organisation) the data has [2].

#### Structured data

Data organised in a fixed format, usually rows and columns, with a well-defined schema [2].

- Easiest of the three to search and analyse.
- Examples: sales figures, names, dates, prices, phone numbers.

| student_id | name | grade | books_borrowed |
|---|---|---|---|
| 11 | Mei | 5 | 4 |
| 12 | Omar | 6 | 7 |

#### Semi-structured data

Data that has some organisation, such as tags or labels, but not a rigid format [2]. It sits between structured and unstructured data.

```json
{ "student": "Mei", "grade": 5, "club": "Chess" }
```

*What this shows:* every piece of information has a label (`student`, `grade`, `club`). The labels make the data easy to read, but a different record could have different labels.

#### Unstructured data

Data with no set format or model [2]. Examples: text documents, emails, photos, audio, video and social media posts.

| | Structured | Semi-structured | Unstructured |
|---|---|---|---|
| **Format** | Tables (rows and columns) | Labelled data such as JSON or XML | No fixed format |
| **Schema** | Well defined | Flexible | None |
| **Ease of analysis** | Easiest | In between | Hardest |

<!-- REVIEW 27/10: "Storage" row removed (not confirmed in sources). "Ease of analysis" row: check against Educative and Datamation. -->

**A note on CSV files.** A CSV file stores values in rows and columns, so it is usually treated as structured data. Some sources call it semi-structured, because the file format does not enforce a schema [6][7][8]. In this guide we treat a well-organised CSV file as structured.

#### Where data comes from

> The mapping below is our team's own classification, based on the definitions above.

| Source | Typical structure | What it looks like |
|---|---|---|
| **Transactions** | Structured | One customer's purchase history |
| **IoT sensors** | Structured / semi-structured | Temperature, wind speed, vibration, status readings [5] |
| **Logs** | Semi-structured | App or server records with labels |
| **Surveys and forms** | Structured | Answers on a feedback form |
| **Emails and messages** | Semi-structured / unstructured | Customer complaints |
| **Observations and interviews** | Unstructured | Notes on how people use a product |

#### Try it: what type of data is it?

Classify each item as structured, semi-structured or unstructured.

1. A spreadsheet of class attendance with one row per student per day.
2. A photo of a child's drawing.
3. A labelled record such as `{ "pet": "Mochi", "age": 3 }`.
4. A voice recording of a story.
5. A list of quiz scores saved as a CSV file.

**Answers**

1. **Structured.** Fixed rows and columns.
2. **Unstructured.** An image has no set format for its content.
3. **Semi-structured.** It has labels but is not a fixed table.
4. **Unstructured.** Audio has no predefined format.
5. **Structured** (usually). It is a tidy table, but some sources call CSV semi-structured, as noted above.

---

### 1.5 Big Data vs Data Warehousing

**Status: outline only.** Planned content:

- Data structure
- How data is stored
- Typical use

---

## References

Sources were opened and checked in the Stage 1 Content Review Log (Section 3).

1. TechTarget. *5V's of big data.* https://www.techtarget.com/data-technologies/definition/5Vs-of-big-data
2. Educative. *Structured vs. semi-structured vs. unstructured data.* https://www.educative.io/answers/structured-vs-semi-structured-vs-unstructured-data
3. World Economic Forum (from Knowledge@Wharton). *Is small data the new big data?* https://www.weforum.org/stories/2016/04/is-small-data-the-new-big-data/
4. Iberdrola. *What is small data?* https://iberdrola.com/innovation/what-is-small-data
5. Wikipedia. *Small data.* https://en.wikipedia.org/wiki/Small_data
6. Coursera. *What Is Semi-structured Data?* https://www.coursera.org/articles/what-is-semi-structured-data
7. The Data School. *Structured, Semi-structured, and Unstructured Data.* https://thedataschool.co.uk/anne-porciaaffi-asamani/structured-semi-structured-and-unstructured-data
8. Surface. *Is CSV structured data?* https://withsurface.com/glossary/is-csv-structured-data
