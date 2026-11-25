## Chapter 1: Introduction to Big Data

**Terms used in this chapter**

- **Data**: facts such as numbers, words, pictures or sounds that a computer can store.
- **Analyze**: to look carefully at data to find patterns or answers.
- **Schema**: a plan for how data is organized, such as the column headings of a table.

---

### 1.1 Definition

Big Data is an important part of today's digital world. It helps businesses understand customers, schools improve learning, scientists study animals, sports teams analyze performance, and social media platforms recommend content.

To understand how Big Data works, we start with the 5 Vs (section 1.2), which describe its main characteristics. After that we look at how data has changed over time (1.3), the types of data and where they come from (1.4), and how Big Data storage differs from a data warehouse (1.5). Later chapters cover how data is processed and analyzed, and the technologies behind it.

#### What makes data "big"?

Big Data is a mix of organized, partly organized and unorganized data that organizations collect and then study to find useful insights [1]. Early descriptions of Big Data used three Vs: **volume** (how much), **velocity** (how fast) and **variety** (how many kinds) [1][4].

What counts as "big" is not a fixed number. It depends on the computing power available at the time [1].

#### Big Data examples

- A retail chain with hundreds of stores records millions of purchases every day [1].
- Hospital machines and wearable devices send health readings all the time, and the readings must be analyzed quickly [1].
- A video app receives likes, comments and uploads from millions of people.

#### Small data

Small data is data that is small enough for a person to read and understand. It is organized in a way that makes it easy to access and use [4][5].

A common way to explain the difference is: Big Data is about machines, small data is about people [3][5].

| Aspect | Small data | Big Data |
|---|---|---|
| **Focus** | People | Machines |
| **Typical goal** | Understanding the reason behind what people do (the *why*) | Finding patterns and links in huge amounts of data (the *what*) |
| **Volume** | Small enough to read and understand | Enormous, needs special tools |
| **Type of insight** | Qualitative: observations, habits, feelings [4] | Predictive patterns found at a large scale [4] |
| **Example** | Watching how a family uses its kitchen | Studying millions of online searches |

The "why versus what" contrast is the view of Martin Lindstrom, who popularized the term "small data" [3][5]. It is one expert's argument, not a rule everyone agrees on.

**Why small data matters**

- It can show feelings and context that numbers alone often miss [3].
- It started in marketing and is now used in many fields and by companies of any size [4].
- It works best together with Big Data: Big Data shows what is happening, and small data helps explain why [3][4].

---

### 1.2 The 5 Vs

The 5 Vs are five main features of Big Data: velocity, volume, value, variety and veracity [1].

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
3. **Choose.** The clue is about *how much*, so it is **Volume**.
4. **Check the others.** Nothing says the photos arrive quickly (not Velocity), that anything is wrong with them (not Veracity), or that they are used for something (not Value).

Note: one phone is not "Big Data" by itself. The example only shows what the word *volume* means.

#### Try it: which V is it?

Match each situation to a V.

1. A school stores twenty years of student records.
2. A live sports app updates scores and comments every second.
3. A survey has the same student's answers entered twice by mistake.
4. A library collects book titles, photos of covers and recordings of story time.
5. A cafeteria uses survey results to decide which snacks to sell.

**Answers**

1. **Volume.** The point is the *amount* of data stored.
2. **Velocity.** New data arrives constantly and must be handled quickly.
3. **Veracity.** Duplicate answers make the data less accurate and trustworthy.
4. **Variety.** Titles, photos and audio are different kinds of data.
5. **Value.** The data is used to make a useful decision.

---

### 1.3 Evolution and Benefits

#### Evolution of Big Data

- **Traditional databases:** people stored organized information, such as customer names and sales records.
- **Web and social media:** websites and social media created more data, such as comments, photos, videos and searches.
- **Cloud computing:** people could store data and use computer power over the internet.
- **Internet of Things (IoT):** devices such as smartwatches and sensors began collecting data automatically.
- **Today:** Big Data tools and AI help people analyze very large amounts of information.

Some milestones in this story: the idea of describing data by volume, velocity and variety was set out by Doug Laney in 2001 [13]. MapReduce, introduced in 2004, made it practical to process huge data sets across many ordinary computers [14]. The term "Internet of Things" was coined by Kevin Ashton in 1999 [15].

#### Benefits of Big Data

Organizations use Big Data to improve how they work, serve customers better and personalize marketing [1].

| Benefit | What it means | Example |
|:---|:---|:---|
| **Better decisions** | People choose better by looking at information and spotting patterns | A delivery company uses traffic data to find faster routes |
| **Efficiency** | People save time, money and resources | A factory uses sensor data to predict repairs before a machine breaks |
| **Personalization** | Apps and websites suggest things that match a person's interests | A video app recommends videos based on what you watch |

---

### 1.4 Types of Data and Sources

Data of any size, big or small, can be organized in three ways. The difference is how much *schema* (planned organization) the data has [1][2].

#### Structured data

Data organized in a fixed format, usually rows and columns, with a well-defined schema [2].

- Easiest of the three to search and analyze.
- Examples: sales figures, names, dates, prices, phone numbers.

| student_id | name | grade | books_borrowed |
|---|---|---|---|
| 11 | Mei | 5 | 4 |
| 12 | Omar | 6 | 7 |

#### Semi-structured data

Data that has some organization, such as tags or labels, but not a rigid format [2]. It sits between structured and unstructured data.

```json
{ "student": "Mei", "grade": 5, "club": "Chess" }
```

*What this shows:* every piece of information has a label (`student`, `grade`, `club`). The labels make the data easy to read, but a different record could have different labels.

#### Unstructured data

Data with no set format or model [2]. Examples: text documents, emails, photos, audio, video and social media posts.

| | Structured | Semi-structured | Unstructured |
|---|---|---|---|
| **Format** | Tables (rows and columns) | Labeled data such as JSON or XML | No fixed format |
| **Schema** | Well defined | Flexible | None |
| **Ease of analysis** | Easiest | In between | Hardest |

**A note on CSV files.** A CSV file stores values in rows and columns, so it is usually treated as structured data. The CSV format (RFC 4180 [8]) describes how values are separated, but it does not enforce a schema, which is why some sources call it semi-structured [6][7]. In this guide we treat a well-organized CSV file as structured.

#### Where data comes from

> **Note:** this mapping is a teaching guide based on the definitions above. Real data sources can fit more than one type.

| Source | Typical structure | What it looks like |
|---|---|---|
| **Transactions** | Structured | One customer's purchase history |
| **IoT sensors** | Structured / semi-structured | Temperature, wind speed, vibration, status readings |
| **Logs** | Semi-structured | App or server records with labels |
| **Surveys and forms** | Structured | Answers on a feedback form |
| **Emails and messages** | Semi-structured / unstructured | Customer complaints |
| **Observations and interviews** | Unstructured | Notes on how people use a product |

#### Try it: what type of data is it?

Classify each item as structured, semi-structured or unstructured.

1. A spreadsheet of class attendance with one row per student per day.
2. A photo of a child's drawing.
3. A labeled record such as `{ "pet": "Mochi", "age": 3 }`.
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

**Terms used in this section**

- **Data warehouse**: a central store of cleaned, organized data kept in planned tables, built mainly for reports [9][10].
- **Data lake**: a central store that keeps data in its original, raw form, whatever its type [9][10].
- **Schema-on-write**: the plan for the data (the schema) is decided *before* the data is stored.
- **Schema-on-read**: the plan for the data is decided *when* the data is read.

#### Comparing like with like

Big Data describes *the data itself*: its volume, velocity, variety, veracity and value (section 1.2). A data warehouse is *a place to keep data*. To compare fairly, we compare a data warehouse with the kind of storage that Big Data is usually kept in, called a **data lake** [9][10][11].

| | Data warehouse | Data lake (Big Data storage) |
|---|---|---|
| **Data structure** | Neat, planned tables (rows and columns) | Any kind: tables, photos, videos, messages, sensor readings, even messy data |
| **How it is stored** | Organized *before* storing (schema-on-write) | Stored raw first, organized *later* (schema-on-read) |
| **Typical use** | Clear reports for questions we already know | Exploring large, varied data to find new patterns |
| **Example question** | "How many toys did we sell in May?" | "What do children like that we have not noticed?" |

**Two ways to picture it**

- **Warehouse: organize first, store second.** Like a library, every book gets a labeled shelf *before* it goes in.
- **Data lake: store first, organize later.** Like a large storage room, boxes go in as they are and are sorted when someone needs them.

**In practice,** many organizations use **both**, and some modern platforms combine the two ideas (often called a *data lakehouse*) [12]. The two terms describe common designs, not strict rules.

**Link to Chapter 2.4:** data usually reaches a warehouse through **ETL** (transform, then load). Data usually reaches a lake through **ELT** (load raw, transform later).

#### Worked example: Happy Toys

| Step | Warehouse path | Data lake path |
|---|---|---|
| 1 | Take only the neat sales receipts | Save everything: receipts, comments, photos, videos |
| 2 | Clean the receipts and fit them into a planned table | Leave them as they are |
| 3 | Make a report | A data scientist later reads the comments |
| **Result** | "Teddy bears sold 120 in May." | "Children keep mentioning dinosaurs, so order more dinosaur toys." |

The warehouse answered a **known question**. The data lake helped the store **discover something new**.

#### Try it: warehouse or data lake?

1. A school needs a weekly attendance report with the same columns every week.
2. A school keeps student drawings, voice recordings and survey comments to study later.
3. Which one is "schema-on-read"?

**Answers**

1. **Data warehouse.** The question is known and the data fits a fixed table.
2. **Data lake.** The data is of many types and the questions are not yet decided.
3. **Data lake.** The structure is decided when the data is read.

---

## References

1. TechTarget. *5V's of Big Data.* https://www.techtarget.com/data-technologies/definition/5Vs-of-big-data
2. Educative. *Structured vs. semi-structured vs. unstructured data.* https://www.educative.io/answers/structured-vs-semi-structured-vs-unstructured-data
3. World Economic Forum (from Knowledge@Wharton). *Is small data the new Big Data?* https://www.weforum.org/stories/2016/04/is-small-data-the-new-big-data/
4. Iberdrola. *What is small data?* https://iberdrola.com/innovation/what-is-small-data
5. Lindstrom, M. (2016). *Small Data: The Tiny Clues That Uncover Huge Trends.* St. Martin's Press.
6. Coursera. *What Is Semi-structured Data?* https://www.coursera.org/articles/what-is-semi-structured-data
7. Surface. *Is CSV structured data?* https://withsurface.com/glossary/is-csv-structured-data
8. Shafranovich, Y. (2005). *Common Format and MIME Type for Comma-Separated Values (CSV) Files.* RFC 4180. https://www.rfc-editor.org/rfc/rfc4180
9. Splunk. *Data Lake vs. Data Warehouse.* https://splunk.com/en_us/blog/learn/data-warehouse-vs-data-lake.html
10. TechTarget. *Data lake vs. data warehouse: Key differences explained.* https://www.techtarget.com/data-technologies/feature/Data-lake-vs-data-warehouse-Key-differences-explained
11. BMC Software. *Data Lake vs. Data Warehouse vs. Database.* https://www.bmc.com/blogs/data-lake-vs-data-warehouse-vs-database-whats-the-difference/
12. Armbrust, M., Ghodsi, A., Xin, R., & Zaharia, M. (2021). *Lakehouse: A New Generation of Open Platforms that Unify Data Warehousing and Advanced Analytics.* Conference on Innovative Data Systems Research (CIDR 2021).
13. Laney, D. (2001). *3D Data Management: Controlling Data Volume, Velocity, and Variety.* META Group research note.
14. Dean, J., & Ghemawat, S. (2004). *MapReduce: Simplified Data Processing on Large Clusters.* OSDI '04.
15. Ashton, K. (2009). *That "Internet of Things" Thing.* RFID Journal.
