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

---

## 1. Data structure

- **Warehouse:** neat, planned tables (rows and columns), such as `Date | Toy | Number sold`.
- **Big data:** any kind of data: tables, photos, videos, messages, sensor readings, even messy ones.

## 2. How data is stored

- **Warehouse: organize first, store second.** Like a library, every book gets a labeled shelf *before* it goes in.
- **Big data: store first, organize later.** Like a giant storage room, boxes go in as they are and get sorted when needed.

## 3. Typical use

- **Warehouse:** clear reports for known questions. *"How many toys did we sell in May?"*
- **Big data:** exploring huge, varied data to find new patterns. *"What do kids like that we haven't noticed?"*

---

## Visual: at a glance

| | Data Warehouse | Big Data Storage |
|---|---|---|
| **Data structure** | Neat, planned tables | Any kind, even messy |
| **How stored** | Organized *before* storing | Raw first, organized *later* |
| **Typical use** | Reports and decisions | Finding new patterns |

## Worked example: Happy Toys

| Step | Warehouse path | Big data path |
|---|---|---|
| 1 | Take only the neat sales receipts | Save everything: receipts, comments, photos, videos |
| 2 | Clean and fit them into a planned table | Leave them as they are |
| 3 | Make a report | A data scientist later reads the comments |
| **Result** | "Teddy bears sold 120 in May." | "Kids keep mentioning dinosaurs, so order more dinosaur toys." |

The warehouse answered a **known question**. Big data helped the store **discover something new**.

---

## References

1. Splunk. *Data Lake vs. Data Warehouse.* https://splunk.com/en_us/blog/learn/data-warehouse-vs-data-lake.html
2. TechTarget. *Data lake vs. data warehouse: Key differences explained.* https://www.techtarget.com/data-technologies/feature/Data-lake-vs-data-warehouse-Key-differences-explained
3. BMC Software. *Data Lake vs. Data Warehouse vs. Database.* https://www.bmc.com/blogs/data-lake-vs-data-warehouse-vs-database-whats-the-difference/


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

# 2. Big Data Processing and Analytics

Big Data refers to extremely large and complex sets of data that
traditional data-processing methods may struggle to handle.

Big Data Processing involves collecting, organizing, cleaning, and
transforming data so it can be used effectively.

Big Data Analytics involves examining this data to discover patterns,
understand information, and support decision-making.

# 2.1 Data Quality

Data quality refers to how accurate, complete, consistent, and reliable
data is. High-quality data is important because incorrect or incomplete
information can lead to misleading results.

Two common data quality problems are **missing values** and **duplicate
data**.

**Missing Values**

Missing values occur when certain information is not recorded or is
unavailable in a dataset.

For example, an online shopping platform may collect customer
information, but some customers might not provide their phone numbers or
addresses.

**Example:**

| Customer ID \| Name \| Age \| Phone Number \|

\|---\|---\|---\|---\|

| 001 \| Alice \| 20 \| 0812345678 \|

| 002 \| Bob \| 22 \| Missing \|

| 003 \| Charlie \| Missing \| 0898765432 \|

Missing values can cause problems because:

-   Some calculations may become inaccurate.

-   Important information may be unavailable.

-   Certain analysis methods may not work properly.

**How to Handle Missing Values:**

1.  **Remove the Data:** Delete records with missing information if they
    are not important.

2.  **Fill in the Missing Values:** Replace missing information with a
    suitable value, such as the average or median.

3.  **Use a Placeholder:** Mark the information as "Unknown" or "Not
    Available" when the actual value cannot be determined.

**Duplicate Data**

Duplicate data occurs when the same information appears more than once
in a dataset.

For example, an online shopping platform might accidentally record the
same customer or transaction multiple times.

**Example:**

| Order ID \| Customer \| Product \|

\|---\|---\|---\|

| 001 \| Alice \| Laptop \|

| 002 \| Bob \| Phone \|

| 001 \| Alice \| Laptop \|

| 003 \| Charlie \| Tablet \|

Order 001 appears twice, meaning it is a duplicate.

Duplicate data can cause problems because:

-   It may make the total number of records appear larger than it
    actually is.

-   Calculations and statistics may become inaccurate.

-   It can lead to incorrect business decisions.

**How to Handle Duplicate Data:**

1.  Identify records that contain the same information.

2.  Check whether they are actual duplicates or separate transactions.

3.  Remove unnecessary duplicate records.

**Simple Data Cleaning Process:**

    RAW DATA

       \|

       v

    Check Missing Values

       \|

       v

    Handle Missing Information

       \|

       v

    Check Duplicate Records

       \|

       v

    Remove Unnecessary Duplicates

       \|

       v

    CLEAN DATA

Data cleaning helps ensure that information is more reliable before it
is used for analysis.

**References**

-   IBM. *What Is Data Quality?*
    https://www.ibm.com/think/topics/data-quality
-   IBM. *Data Quality Dimensions.*
    https://www.ibm.com/docs/en/watsonx/wdi/2.2.x?topic=quality-data-dimensions

------------------------------------------------------------------------

# 2.2 Analytics Basics

Big Data Analytics is the process of examining large amounts of data to
discover useful information and support decision-making.

There are four main types of analytics: **Descriptive, Diagnostic,
Predictive, and Prescriptive Analytics**.

**Descriptive Analytics**

Descriptive analytics explains what happened in the past by summarizing
historical data.

It is commonly used to identify trends, patterns, and overall
performance.

For example, a supermarket might analyze its sales records to discover
which products sold the most last month.

**Main Question:** What happened?

**Example:**

    SALES DATA

         \|

         v

    Summarize Sales

         \|

         v

    Identify Best-Selling Products

         \|

         v

    REPORT:

    Product A sold the most.

**Diagnostic Analytics**

Diagnostic analytics explains why something happened by examining data
and identifying possible causes.

For example, if a supermarket experiences a decrease in sales, it might
investigate whether the decrease was caused by higher prices, fewer
customers, or a lack of product availability.

**Main Question:** Why did it happen?

**Example:**

    SALES DECREASE

         \|

         v

    Examine Sales Data

         \|

         v

    Investigate Possible Causes

         \|

         v

    FINDING:

    Fewer customers visited the store.

**Predictive Analytics**

Predictive analytics uses historical data, patterns, and statistical
models to estimate what might happen in the future.

For example, a supermarket might use previous sales records to predict
how many products customers will buy next month.

**Main Question:** What might happen?

**Example:**

    HISTORICAL SALES DATA

             \|

             v

       Identify Patterns

             \|

             v

       Build Prediction

             \|

             v

    FORECAST:

    Sales may increase next month.

**Prescriptive Analytics**

Prescriptive analytics recommends actions that can help achieve a
desired result.

It uses information from data analysis and predictions to suggest
possible decisions.

For example, if a supermarket predicts that demand for a product will
increase, prescriptive analytics might recommend increasing its stock
before the demand rises.

**Main Question:** What should we do?

**Example:**

    PREDICTED SALES INCREASE

             \|

             v

       Evaluate Options

             \|

             v

       Recommend Action

             \|

             v

    DECISION:

    Increase product stock.

**Comparison Table**

| Type of Analytics \| Main Question \| Purpose \| Example \|

\|---\|---\|---\|---\|

| Descriptive \| What happened? \| Summarizes past data. \| Finding last
  month's best-selling product. \|

| Diagnostic \| Why did it happen? \| Identifies possible causes. \|
  Investigating why sales decreased. \|

| Predictive \| What might happen? \| Estimates future outcomes. \|
  Forecasting next month's sales. \|

| Prescriptive \| What should we do? \| Recommends possible actions. \|
  Increasing stock before demand rises. \|

**Visual Summary:**

    DESCRIPTIVE

    What happened?

          \|

          v

    DIAGNOSTIC

    Why did it happen?

          \|

          v

    PREDICTIVE

    What might happen?

          \|

          v

    PRESCRIPTIVE

    What should we do?

Together, these four types of analytics help businesses understand their
performance, identify problems, predict future situations, and make
better decisions.

**References**

-   AWS. *Choosing an AWS Analytics Service.*
    https://docs.aws.amazon.com/decision-guides/latest/decision-guides/analytics-on-aws-how-to-choose.html

------------------------------------------------------------------------

# 2.3 Data Visualisation and Challenges

Data visualisation is the process of presenting data using visual
elements such as charts, graphs, and diagrams.

It helps people understand large amounts of information more easily by
turning numbers into visual representations.

**Common Chart Types**

Different charts are suitable for different types of information.

| Chart Type \| Purpose \| Example \|

\|---\|---\|---\|

| Bar Chart \| Compares different categories. \| Comparing sales between
  products. \|

| Line Chart \| Shows changes over time. \| Tracking monthly revenue. \|

| Pie Chart \| Shows proportions of a whole. \| Displaying market share.
  \|

| Scatter Plot \| Shows relationships between two variables. \|
  Comparing advertising spending and sales. \|

| Histogram \| Shows the distribution of numerical data. \| Displaying
  the age distribution of customers. \|

**Visual Examples:**

**1. Bar Chart**

Used to compare values between different categories.

    SALES BY PRODUCT

    A \| ██████████  100

    B \| ██████       60

    C \| █████████    90

    D \| ████         40

**2. Line Chart**

Used to show changes or trends over time.

    SALES

      \^

      \|             \*

      \|         \*  /

      \|      \*  /

      \|   \*  /

      \| \*

      +--------------------\> TIME

**3. Pie Chart**

Used to show how different categories contribute to a whole.

For example, a company's market share:

| Company \| Market Share \|

\|---\|---\|

| A \| 50% \|

| B \| 30% \|

| C \| 20% \|

**4. Scatter Plot**

Used to show the relationship between two numerical variables.

For example, a business might compare advertising spending with sales
revenue.

    SALES

      \^

      \|             \*

      \|         \* \*

      \|       \*

      \|    \* \*

      \|  \*

      +--------------------\> ADVERTISING

**Misleading Charts**

A misleading chart is a visual representation that gives an incorrect or
confusing impression of the data.

This can happen when information is presented in a way that exaggerates
differences or hides important details.

Common examples include:

-   **Truncated Axis:** Starting a chart's vertical axis above zero can
    make small differences appear much larger.

-   **Distorted Scale:** Using inconsistent intervals can make the data
    difficult to compare.

-   **3D Effects:** Three-dimensional charts can distort the appearance
    and size of values.

-   **Missing Labels:** Leaving out titles, units, or labels can make
    information unclear.

**Example: Truncated Axis**

Imagine two companies have the following sales:

| Company \| Sales \|

\|---\|---\|

| A \| 90 \|

| B \| 100 \|

If the vertical axis starts at 80 instead of 0, the difference between
the companies may appear much larger than it really is.

**Too Much Data**

Too much data in a chart can make it difficult for people to understand
the main message.

For example, displaying 100 different product categories in one chart
may make the information crowded and confusing.

Common problems include:

-   Too many categories.

-   Too many colors.

-   Overlapping labels.

-   Too many data points.

-   Unnecessary information.

**How to Improve It:**

1.  Remove information that is not relevant.

2.  Group similar categories together.

3.  Use clear labels and titles.

4.  Highlight the most important information.

5.  Choose a suitable chart type.

**Choosing the Right Chart**

Choosing the correct chart is important because different charts
communicate different types of information.

| What You Want to Show \| Recommended Chart \|

\|---\|---\|

| Compare categories \| Bar Chart \|

| Show changes over time \| Line Chart \|

| Show proportions \| Pie Chart \|

| Show relationships \| Scatter Plot \|

| Show data distribution \| Histogram \|

**Simple Example:**

Imagine a company wants to understand its monthly sales.

-   To compare sales between different products, use a bar chart.

-   To track how sales change every month, use a line chart.

-   To show the percentage of total sales contributed by each product,
    use a pie chart.

The main goal of data visualisation is to communicate information
clearly and accurately, rather than simply making charts look
attractive.

**References**

-   Tableau. *Choose the Right Chart Type for Your Data.*
    https://help.tableau.com/current/pro/desktop/en-us/what_chart_example.htm
-   UK Government. *A Bite-Sized Guide to Visualising Data.*
    https://www.gov.uk/government/publications/a-bite-sized-guide-to-visualising-data-a-dstl-biscuit-book/a-bite-sized-guide-to-visualising-data

------------------------------------------------------------------------

# 2.4 ETL

ETL stands for **Extract, Transform, Load**. It is a process used to
collect data from different sources, prepare it, and store it in a
destination where it can be analyzed.

ETL is commonly used in data warehouses and Big Data systems.

**Extract**

Extract means collecting data from different sources.

Data can come from:

-   Databases.

-   Websites.

-   Mobile applications.

-   Sensors.

-   Business systems.

For example, an online shopping company might collect customer
information, product details, and transaction records from its platform.

**Transform**

Transform means cleaning and changing the collected data into a suitable
format.

This may involve:

-   Removing duplicate records.

-   Handling missing values.

-   Correcting inconsistent formats.

-   Combining information from different sources.

For example, a company might convert different date formats into one
standard format and remove unnecessary duplicate records.

**Load**

Load means storing the transformed data in a destination, such as a
database or data warehouse.

After loading, the data can be accessed and used for reporting and
analysis.

**ETL Process:**

    +-------------+

    \|   EXTRACT   \|

    \|             \|

    \| Collect Data\|

    +-------------+

           \|

           v

    +-------------+

    \|  TRANSFORM  \|

    \|             \|

    \| Clean Data  \|

    \| Change Format\|

    +-------------+

           \|

           v

    +-------------+

    \|    LOAD     \|

    \|             \|

    \| Store Data  \|

    +-------------+

           \|

           v

    +-------------+

    \| DATA        \|

    \| WAREHOUSE   \|

    +-------------+

           \|

           v

       ANALYSIS

**Example: Online Shopping Company**

Imagine an online shopping company that wants to analyze its sales.

1.  **Extract:** Collect customer information and transaction records
    from its website.

2.  **Transform:** Remove duplicate transactions and correct missing or
    inconsistent information.

3.  **Load:** Store the cleaned data in a data warehouse.

The company can then use the data to analyze customer behavior and sales
performance.

ETL helps ensure that data is organized and ready for further analysis.

**References**

-   AWS. *What Is ETL?* https://aws.amazon.com/what-is/etl/
-   AWS. *What Is an ETL Pipeline?*
    https://aws.amazon.com/what-is/etl-pipeline/

------------------------------------------------------------------------

# 2.5 The Data Pipeline

A data pipeline is a series of steps that moves data from its original
source to its final destination, where it can be analyzed or used.

It helps automate the process of collecting, storing, cleaning,
analyzing, and presenting data.

**Main Stages of a Data Pipeline**

**Collect**

The first step is gathering data from different sources.

Examples include:

-   Websites.

-   Sensors.

-   Mobile applications.

-   Databases.

-   Social media platforms.

**Store**

After collection, the data is stored in a suitable storage system, such
as a database or data warehouse.

This allows the data to be accessed and processed later.

**Clean / Transform**

The collected data is cleaned and converted into a suitable format.

This may include removing duplicates, handling missing values, and
correcting errors.

**Analyze**

The cleaned data is examined to discover useful information, patterns,
and trends.

For example, a business might analyze customer purchases to identify its
most popular products.

**Present**

Finally, the results are presented using reports, dashboards, charts, or
graphs.

This allows people to understand the information and make decisions.

**Visual Representation:**

    +-------------+

    \|   COLLECT   \|

    \|             \|

    \| Gather Data \|

    +-------------+

           \|

           v

    +-------------+

    \|    STORE    \|

    \|             \|

    \| Save Data   \|

    +-------------+

           \|

           v

    +-------------+

    \| CLEAN /     \|

    \| TRANSFORM   \|

    \|             \|

    \| Prepare Data\|

    +-------------+

           \|

           v

    +-------------+

    \|   ANALYZE   \|

    \|             \|

    \| Find Patterns\|

    +-------------+

           \|

           v

    +-------------+

    \|   PRESENT   \|

    \|             \|

    \| Show Results\|

    +-------------+

           \|

           v

       DECISIONS

**Example: Supermarket Data Pipeline**

Imagine a supermarket wants to understand customer purchasing behavior.

| Stage \| Example \|

\|---\|---\|

| Collect \| Collect customer transactions and product purchases. \|

| Store \| Save the information in a database. \|

| Clean / Transform \| Remove duplicate transactions and organize the
  data. \|

| Analyze \| Identify popular products and purchasing patterns. \|

| Present \| Display the results in a sales dashboard. \|

**ETL vs. Data Pipeline**

ETL and data pipelines are related, but they are not exactly the same.

| ETL \| Data Pipeline \|

\|---\|---\|

| Focuses on Extract, Transform, and Load. \| Covers the movement and
  processing of data through multiple stages. \|

| Usually prepares data before loading it into a destination. \| Can
  include storage, analysis, and presentation. \|

| Is a specific data-processing process. \| Is a broader workflow that
  can include ETL. \|

A data pipeline may use ETL as part of its process.

**References**

-   AWS. *What Is a Data Pipeline?*
    https://aws.amazon.com/what-is/data-pipeline/
-   AWS. *What Is an ETL Pipeline?*
    https://aws.amazon.com/what-is/etl-pipeline/

------------------------------------------------------------------------

# 3. Big Data Technologies

Big Data technologies are tools and systems used to store, process,
analyze, and visualize large amounts of data.

These technologies help organizations handle data that may be too large
or complex for traditional systems.

# 3.1 Categories of Technology

Big Data technologies can be divided into four main categories:
**Storage, Processing, Analytics, and Visualisation**.

Each category has a different role in handling data.

**Storage Technologies**

Storage technologies are used to save and organize large amounts of data
so that it can be accessed later.

They help manage data from different sources and support large-scale
storage.

Examples include:

-   Hadoop Distributed File System (HDFS).

-   Cloud storage.

-   Distributed databases.

**Processing Technologies**

Processing technologies are used to handle and process large amounts of
data efficiently.

They help perform calculations, transform information, and process data
across multiple computers.

Examples include:

-   Apache Hadoop.

-   Apache Spark.

**Analytics Technologies**

Analytics technologies help examine data to identify patterns, trends,
and useful information.

They are used to support predictions, business decisions, and
statistical analysis.

Examples include:

-   Python.

-   R.  

-   Apache Spark.

**Visualisation Technologies**

Visualisation technologies present data using charts, graphs, and
dashboards.

They make complex information easier to understand.

Examples include:

-   Tableau.

-   Microsoft Power BI.

-   Looker.

**Comparison Table:**

| Category \| Purpose \| Examples \|

\|---\|---\|---\|

| Storage \| Stores large amounts of data. \| HDFS, Cloud Storage \|

| Processing \| Processes and transforms data. \| Hadoop, Spark \|

| Analytics \| Examines data to find patterns. \| Python, R \|

| Visualisation \| Presents data using charts and dashboards. \|
  Tableau, Power BI \|

**Visual Representation:**

    +------------------+

    \|   BIG DATA       \|

    \|   TECHNOLOGIES   \|

    +------------------+

             \|

     +-------+-------+

     \|       \|       \|

     v       v       v

    STORAGE PROCESSING ANALYTICS

                             \|

                             v

                       VISUALISATION

Together, these technologies help turn raw data into useful information.

**References**

-   Apache Hadoop. *HDFS Architecture Guide.*
    https://hadoop.apache.org/docs/stable1/hdfs_design.html
-   Google Cloud. *What Is Apache Spark?*
    https://cloud.google.com/learn/what-is-apache-spark
-   Apache Spark. *Unified Engine for Large-Scale Data Analytics.*
    https://spark.apache.org/
-   AWS. *Choosing an AWS Analytics Service.*
    https://docs.aws.amazon.com/decision-guides/latest/decision-guides/analytics-on-aws-how-to-choose.html

------------------------------------------------------------------------

# 3.2 Scale Up (Vertical) vs Scale Out (Horizontal)

Scaling refers to increasing a system's capacity so that it can handle
more data, users, or processing tasks.

There are two main approaches: **Vertical Scaling (Scale Up)** and
**Horizontal Scaling (Scale Out)**.

**Vertical Scaling (Scale Up)**

Vertical scaling means improving the capacity of an existing computer by
adding more resources to it.

This can include:

-   Increasing RAM.

-   Upgrading the CPU.

-   Adding more storage.

For example, a company might upgrade its server from 8 GB of RAM to 32
GB so that it can handle more tasks.

**Visual Representation:**

    BEFORE                  AFTER

    +----------+            +----------+

    \| SERVER   \|            \| SERVER   \|

    \|          \|            \|          \|

    \|  8 GB    \|   ----\>    \|  32 GB   \|

    \|  RAM     \|            \|  RAM     \|

    +----------+            +----------+

The same server becomes more powerful.

**Horizontal Scaling (Scale Out)**

Horizontal scaling means increasing system capacity by adding more
computers or servers to work together.

Instead of upgrading one computer, additional computers are connected to
the system.

For example, an online shopping platform might add more servers to
handle an increase in website visitors.

**Visual Representation:**

    BEFORE

    +----------+

    \| SERVER 1 \|

    +----------+

    AFTER

    +----------+   +----------+   +----------+

    \| SERVER 1 \|   \| SERVER 2 \|   \| SERVER 3 \|

    +----------+   +----------+   +----------+

         	          \|             /

         	          \|            /

            +-----------+-----------+

                        \|

                   MORE CAPACITY

**Comparison Table**

| Comparison \| Vertical Scaling (Scale Up) \| Horizontal Scaling (Scale
  Out) \|

\|---\|---\|---\|

| Meaning \| Upgrades an existing computer. \| Adds more computers or
  servers. \|

| Method \| Adds more CPU, RAM, or storage. \| Connects additional
  machines. \|

| Cost \| Can be expensive when high-end hardware is needed. \| Can
  start with cheaper machines, but costs increase as more are added. \|

| Limits \| Limited by the maximum capacity of one machine. \| Can
  expand by adding more machines, although coordination becomes more
  complex. \|

| Complexity \| Usually simpler to manage. \| Requires coordination
  between multiple machines. \|

| Reliability \| One machine failure can affect the whole system. \| Can
  continue operating if other machines are available and the system is
  designed for fault tolerance. \|

| Example \| Upgrading a server's RAM. \| Adding more servers to a
  website. \|

**Simple Analogy:**

Imagine a restaurant experiencing more customers.

-   **Vertical Scaling:** Make the existing kitchen larger and give it
    better equipment.

-   **Horizontal Scaling:** Open additional kitchens to serve more
    customers.

Both approaches increase capacity, but they work in different ways.

**References**

-   Google Cloud. *What Is Cloud Scalability?*
    https://cloud.google.com/discover/what-is-cloud-scalability
-   NIST. *NIST Big Data Interoperability Framework: Volume 6, Reference
    Architecture.*
    https://www.nist.gov/publications/nist-big-data-interoperability-framework-volume-6-reference-architecture

------------------------------------------------------------------------

# 3.3 Challenges

Although Big Data technologies provide many benefits, organizations may
face several challenges when implementing and managing them.

Five common challenges are **Cost, Skills, Integration, Security, and
Privacy**.

**Cost**

Big Data systems can be expensive to develop, operate, and maintain.

Organizations may need to spend money on:

-   Servers and storage systems.

-   Cloud computing services.

-   Software and technology.

-   System maintenance.

For example, a company handling millions of customer transactions may
need additional storage and computing resources, increasing its
operating costs.

**Skills**

Big Data requires people with technical knowledge and experience.

Organizations may struggle to find employees who understand data
management, programming, analytics, and machine learning.

For example, a company may have large amounts of data but lack employees
who know how to analyze it properly.

**Integration**

Integration means combining data from different sources and systems.

This can be difficult because different systems may use different
formats, structures, or technologies.

For example, a business may store customer information in one database
and sales records in another. Combining these datasets can require
additional processing.

**Security**

Security refers to protecting data from unauthorized access, theft, or
damage.

Big Data systems often store large amounts of valuable information,
making them attractive targets for cyberattacks.

Organizations need security measures such as:

-   Password protection.

-   Access controls.

-   Data encryption.

-   Regular security updates.

**Privacy**

Privacy refers to protecting personal information and ensuring that it
is collected and used responsibly.

For example, companies may collect customer names, addresses, purchasing
histories, and other personal information.

If this information is misused or shared without proper permission, it
can violate people's privacy.

Organizations should follow relevant data protection laws and handle
personal information responsibly.

**Comparison Table:**

| Challenge \| Meaning \| Example \|

\|---\|---\|---\|

| Cost \| Big Data systems can be expensive. \| Paying for additional
  servers and storage. \|

| Skills \| Requires trained employees. \| Lack of workers who
  understand data analytics. \|

| Integration \| Combining data from different sources can be difficult.
  \| Merging customer data from different databases. \|

| Security \| Protecting data from unauthorized access. \| Preventing
  cyberattacks and data theft. \|

| Privacy \| Protecting people's personal information. \| Preventing
  misuse of customer information. \|

**References**

-   NIST. *NIST Big Data Interoperability Framework: Volume 1,
    Definitions.*
    https://www.nist.gov/publications/nist-big-data-interoperability-framework-volume-1-definitions
-   NIST. *NIST Big Data Interoperability Framework: Volume 6, Reference
    Architecture.*
    https://www.nist.gov/publications/nist-big-data-interoperability-framework-volume-6-reference-architecture

------------------------------------------------------------------------

# 3.4 MapReduce

MapReduce is a programming model used to process large amounts of data
across multiple computers.

It divides a large task into smaller tasks, processes them separately,
and combines the results.

MapReduce is commonly associated with Apache Hadoop.

There are four main stages: **Split, Map, Shuffle, and Reduce**.

**Split**

The first stage divides a large dataset into smaller sections.

These sections can then be processed separately by different computers.

For example, a large collection of documents can be divided into several
smaller groups.

**Map**

The Map stage processes each section and produces intermediate results.

For example, if the task is to count words in documents, the Map stage
identifies each word and assigns it a value of 1.

**Example:**

    INPUT:

    "Apple Banana Apple"

    MAP OUTPUT:

    (Apple, 1)

    (Banana, 1)

    (Apple, 1)

**Shuffle**

The Shuffle stage groups together intermediate results with the same
key.

For example, all occurrences of the word "Apple" are grouped together,
while all occurrences of "Banana" are placed in another group.

**Example:**

    BEFORE SHUFFLE:

    (Apple, 1)

    (Banana, 1)

    (Apple, 1)

    AFTER SHUFFLE:

    Apple  -\> (1, 1)

    Banana -\> (1)

**Reduce**

The Reduce stage combines the grouped values to produce the final
result.

For example, it adds the values together to calculate how many times
each word appears.

**Example:**

    REDUCE:

    Apple  -\> 1 + 1 = 2

    Banana -\> 1 = 1

    FINAL RESULT:

    Apple: 2

    Banana: 1

**Complete MapReduce Process:**

    +----------------+

    \|   LARGE DATA   \|

    +----------------+

            \|

            v

    +----------------+

    \|     SPLIT      \|

    \| Divide Data    \|

    +----------------+

            \|

            v

    +----------------+

    \|      MAP       \|

    \| Process Data   \|

    +----------------+

            \|

            v

    +----------------+

    \|    SHUFFLE     \|

    \| Group Results  \|

    +----------------+

            \|

            v

    +----------------+

    \|     REDUCE     \|

    \| Combine Values \|

    +----------------+

            \|

            v

    +----------------+

    \| FINAL RESULTS  \|

    +----------------+

**Real-Life Example:**

Imagine a website wants to count how many times each word appears in
millions of user comments.

1.  **Split:** Divide the comments into smaller groups.

2.  **Map:** Count each word in each group.

3.  **Shuffle:** Group identical words together.

4.  **Reduce:** Add the counts to calculate the total number of times
    each word appears.

MapReduce makes it possible to process large datasets by distributing
smaller tasks across multiple computers.

**References**

-   Apache Hadoop. *MapReduce Tutorial.*
    https://hadoop.apache.org/docs/current1/mapred_tutorial.html

------------------------------------------------------------------------

# 3.5 Future Trends

Big Data technologies continue to develop as organizations need faster,
more flexible, and more efficient ways to handle information.

Three important trends are **Cloud Computing, Edge Computing, and
Real-Time Streaming**.

**Cloud Computing**

Cloud computing allows organizations to store data and use computing
resources through the internet instead of relying entirely on their own
physical computers and servers.

This allows businesses to access storage and computing power when
needed.

Benefits include:

-   Flexible storage capacity.

-   Access from different locations.

-   Reduced need to maintain physical servers.

-   Ability to increase or decrease resources based on demand.

For example, a company can use cloud storage to save customer
information without building its own large data center.

**Edge Computing**

Edge computing processes data closer to where it is generated instead of
sending everything to a distant central server.

This can reduce delays and allow faster responses.

For example, a smart security camera can process information locally to
detect movement without sending every second of video to a central
server.

**Benefits:**

-   Faster data processing.

-   Reduced network delays.

-   Less data needs to be sent to central servers.

-   Useful for devices that need quick responses.

**Real-Time Streaming**

Real-time streaming involves continuously collecting and processing data
as it is generated.

Instead of waiting for data to be collected in large batches, the system
processes information as it arrives.

For example, a navigation application can continuously receive traffic
information and update its recommended routes.

**Benefits:**

-   Provides up-to-date information.

-   Allows faster decision-making.

-   Helps detect changes as they happen.

-   Useful for monitoring systems and live applications.

**Comparison Table:**

| Technology \| Main Idea \| Example \|

\|---\|---\|---\|

| Cloud Computing \| Uses internet-based servers for storage and
  computing. \| Storing files using cloud services. \|

| Edge Computing \| Processes data close to where it is generated. \|
  Smart cameras detecting movement locally. \|

| Real-Time Streaming \| Processes data continuously as it arrives. \|
  Live traffic updates. \|

**Visual Summary:**

    DATA GENERATION

          \|

     +----+----+

     \|    \|    \|

     v    v    v

    CLOUD EDGE REAL-TIME

    \|     \|       \|

    v     v       v

    Store Process Process

    Data  Locally Continuously

     \|     \|       \|

     +-----+-------+

           \|

           v

      USEFUL RESULTS

These technologies help make Big Data systems more flexible, responsive,
and efficient.

**References**

-   NIST. *Cloud Computing.*
    https://csrc.nist.gov/glossary/term/cloud_computing
-   Google Cloud. *What Is Cloud Scalability?*
    https://cloud.google.com/discover/what-is-cloud-scalability
-   Singh, R. and Gill, S. S. (2023). *Edge AI: A Survey.* Internet of
    Things and Cyber-Physical Systems.
    https://doi.org/10.1016/j.iotcps.2023.02.004
-   Google Cloud. *What Is Apache Spark?*
    https://cloud.google.com/learn/what-is-apache-spark

------------------------------------------------------------------------

# 3.6 Distributed Storage Idea

Distributed storage is a method of storing data across multiple
computers instead of keeping everything on a single machine.

This approach allows large amounts of information to be stored and
accessed across a network.

It is commonly used in Big Data systems because one computer may not
have enough storage capacity to handle extremely large datasets.

Three important concepts are **Blocks, Replication, and Fault
Tolerance**.

**Blocks**

Large files can be divided into smaller pieces called blocks.

These blocks are then stored across different computers in a distributed
storage system.

For example, a large file can be divided into four blocks and stored on
different machines.

**Visual Representation:**

    ORIGINAL FILE

    +----------------------+

    \|      LARGE FILE      \|

    +----------------------+

               \|

               v

         DIVIDE INTO BLOCKS

               \|

       +-------+-------+

       \|       \|       \|

       v       v       v

    +------+ +------+ +------+ +------+

    \|Block1\| \|Block2\| \|Block3\| \|Block4\|

    +------+ +------+ +------+ +------+

       \|       \|       \|       \|

       v       v       v       v

     STORE ACROSS DIFFERENT MACHINES

Dividing files into blocks makes it easier to distribute and manage
large amounts of data.

**Replication**

Replication means creating multiple copies of data and storing them on
different machines.

This helps ensure that data remains available even if one machine
becomes unavailable.

For example, if Block 1 is stored on Machine A, another copy may be
stored on Machine B.

**Visual Representation:**

       ORIGINAL BLOCK

          Block 1

             \|

       +-----+-----+

       \|           \|

       v           v

    +------+    +------+

    \|Machine A\|  \|Machine B\|

    \| Block 1 \|  \| Block 1 \|

    +------+    +------+

       COPY        COPY

If one machine becomes unavailable, another machine may still have a
copy of the data.

**Fault Tolerance**

Fault tolerance is the ability of a system to continue operating even
when part of the system fails.

Distributed storage systems use techniques such as replication to reduce
the risk of losing access to data.

For example, if one storage machine stops working, the system can
retrieve the required information from another machine containing a
copy.

**Why Is It Important?**

-   Reduces the risk of data loss.

-   Improves data availability.

-   Allows systems to continue operating when machines fail.

-   Supports the storage of large datasets.

**Comparison of the Three Concepts:**

| Concept \| Meaning \| Purpose \|

\|---\|---\|---\|

| Blocks \| Divides large files into smaller pieces. \| Makes data
  easier to distribute and store. \|

| Replication \| Creates multiple copies of data. \| Keeps additional
  copies available. \|

| Fault Tolerance \| Allows a system to continue working when failures
  occur. \| Improves system reliability. \|

**Complete Distributed Storage Process:**

    +------------------+

    \|    LARGE FILE    \|

    +------------------+

             \|

             v

       DIVIDE INTO BLOCKS

             \|

             v

    +--------+--------+

    \|        \|        \|

    v        v        v

  Block 1  Block 2  Block 3

    \|        \|        \|

    v        v        v

  DISTRIBUTE ACROSS MACHINES

             \|

             v

        CREATE COPIES

         (REPLICATION)

             \|

             v

       FAULT TOLERANCE

             \|

             v

       DATA REMAINS

        AVAILABLE

Distributed storage allows Big Data systems to store large amounts of
information while improving availability and reliability.

**References**

-   Apache Hadoop. *HDFS Architecture Guide.*
    https://hadoop.apache.org/docs/stable1/hdfs_design.html
-   NIST. *NIST Big Data Interoperability Framework: Volume 6, Reference
    Architecture.*
    https://www.nist.gov/publications/nist-big-data-interoperability-framework-volume-6-reference-architecture




