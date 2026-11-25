## Chapter 2: Big Data Processing and Analytics
> **Before you start:** This chapter builds on the basic ideas of Big Data (volume, variety, velocity, and common data types/sources from Chapter 1). No prior programming or database background is required.
Big Data refers to extremely large and complex sets of data that traditional data-processing methods may struggle to handle.

Big Data Processing involves collecting, organizing, cleaning, and transforming data so it can be used effectively.

Big Data Analytics involves examining this data to discover patterns, understand information, and support decision-making.

---

### 2.1 Data Quality

Data quality refers to how accurate, complete, consistent, and reliable data is. High-quality data is important because incorrect or incomplete information can lead to misleading results.

Two common data quality problems are **missing values** and **duplicate data**. They link to common data quality dimensions: **missing values** break *completeness*, and **duplicate data** breaks *uniqueness*. Other common dimensions include accuracy, consistency, timeliness, and validity.

**Missing Values**

Missing values occur when certain information is not recorded or is unavailable in a dataset.

For example, an online shopping platform may collect customer information, but some customers might not provide their phone numbers or addresses.

**Example:**

| Customer ID | Name | Age | Phone Number |
| --- | --- | --- | --- |
| 001 | Alice | 20 | 0812345678 |
| 002 | Bob | 22 | Missing |
| 003 | Charlie | Missing | 0898765432 |

Missing values can cause problems because:

- Some calculations may become inaccurate.
- Important information may be unavailable.
- Certain analysis methods may not work properly.

**How to Handle Missing Values:**

1. **Remove the Data:** Delete records with missing information if they are not important.
2. **Fill in the Missing Values:** Replace missing information with a suitable value, such as the average or median.
3. **Use a Placeholder:** Mark the information as "Unknown" or "Not Available" when the actual value cannot be determined.

**Caution:** deleting records is only safe when the missing data is rare and the pattern is random. If a particular group is more likely to leave a field empty, deleting those records can bias the results. When the data has extreme values, the median is often safer than the average for filling gaps.

**Duplicate Data**

Duplicate data occurs when the same information appears more than once in a dataset.

For example, an online shopping platform might accidentally record the same customer or transaction multiple times.

**Example:**

| Order ID | Customer | Product |
| --- | --- | --- |
| 001 | Alice | Laptop |
| 002 | Bob | Phone |
| 001 | Alice | Laptop |
| 003 | Charlie | Tablet |

Order 001 appears twice, meaning it is a duplicate.

Duplicate data can cause problems because:

- It may make the total number of records appear larger than it actually is.
- Calculations and statistics may become inaccurate.
- It can lead to incorrect business decisions.

**How to Handle Duplicate Data:**

1. Identify records that contain the same information.
2. Check whether they are actual duplicates or separate transactions.
3. Remove unnecessary duplicate records.

**Simple Data Cleaning Process:**

```text
RAW DATA
   |
   v
Check Missing Values
   |
   v
Handle Missing Information
   |
   v
Check Duplicate Records
   |
   v
Remove Unnecessary Duplicates
   |
   v
CLEAN DATA
```

Data cleaning helps ensure that information is more reliable before it is used for analysis.

**References**

- IBM. *What Is Data Quality?* https://www.ibm.com/think/topics/data-quality
- IBM. *Data Quality Dimensions.* https://www.ibm.com/docs/en/watsonx/wdi/2.2.x?topic=quality-data-dimensions

---

### 2.2 Analytics Basics

Big Data Analytics is the process of examining large amounts of data to discover useful information and support decision-making.

There are four main types of analytics: **Descriptive, Diagnostic, Predictive, and Prescriptive Analytics**.

**Descriptive Analytics**

Descriptive analytics explains what happened in the past by summarizing historical data.

It is commonly used to identify trends, patterns, and overall performance.

For example, a supermarket might analyze its sales records to discover which products sold the most last month.

**Main Question:** What happened?

**Example:**

```text
SALES DATA
    |
    v
Summarize Sales
    |
    v
Identify Best-Selling Products
    |
    v
REPORT:
Product A sold the most.
```

**Diagnostic Analytics**

Diagnostic analytics explains why something happened by examining data and identifying possible causes.

For example, if a supermarket experiences a decrease in sales, it might investigate whether the decrease was caused by higher prices, fewer customers, or a lack of product availability.

**Main Question:** Why did it happen?

**Example:**

```text
SALES DECREASE
    |
    v
Examine Sales Data
    |
    v
Investigate Possible Causes
    |
    v
FINDING:
Fewer customers visited the store.
```

**Predictive Analytics**

Predictive analytics uses historical data, patterns, and statistical models to estimate what might happen in the future.

For example, a supermarket might use previous sales records to predict how many products customers will buy next month.

**Main Question:** What might happen?

**Example:**

```text
HISTORICAL SALES DATA
    |
    v
Identify Patterns
    |
    v
Build Prediction
    |
    v
FORECAST:
Sales may increase next month.
```

**Prescriptive Analytics**

Prescriptive analytics recommends actions that can help achieve a desired result.

It uses information from data analysis and predictions to suggest possible decisions.

For example, if a supermarket predicts that demand for a product will increase, prescriptive analytics might recommend increasing its stock before the demand rises.

**Main Question:** What should we do?

**Example:**

```text
PREDICTED SALES INCREASE
    |
    v
Evaluate Options
    |
    v
Recommend Action
    |
    v
DECISION:
Increase product stock.
```

**Comparison Table**

| Type of Analytics | Main Question | Purpose | Example |
| --- | --- | --- | --- |
| Descriptive | What happened? | Summarizes past data. | Finding last month's best-selling product. |
| Diagnostic | Why did it happen? | Identifies possible causes. | Investigating why sales decreased. |
| Predictive | What might happen? | Estimates future outcomes. | Forecasting next month's sales. |
| Prescriptive | What should we do? | Recommends possible actions. | Increasing stock before demand rises. |

**Visual Summary:**

```text
DESCRIPTIVE
What happened?
      |
      v
DIAGNOSTIC
Why did it happen?
      |
      v
PREDICTIVE
What might happen?
      |
      v
PRESCRIPTIVE
What should we do?
```

Together, these four types of analytics help businesses understand their performance, identify problems, predict future situations, and make better decisions.

**References**

- Harvard Business School Online. (2021). *4 Types of Data Analytics to Improve Decision-Making.* https://online.hbs.edu/blog/post/types-of-data-analysis
- Gartner. (n.d.). *Business Analytics* [Glossary entry]. Gartner Information Technology Glossary. https://www.gartner.com/en/information-technology/glossary/business-analytics
- Sharda, R., Delen, D., & Turban, E. (2018). *Business Intelligence, Analytics, and Data Science: A Managerial Perspective* (4th ed.). Pearson.

---

### 2.3 Data Visualization and Challenges

Data visualization is the process of presenting data using visual elements such as charts, graphs, and diagrams.

It helps people understand large amounts of information more easily by turning numbers into visual representations.

**Common Chart Types**

Different charts are suitable for different types of information.

| Chart Type | Purpose | Example |
| --- | --- | --- |
| Bar Chart | Compares different categories. | Comparing sales between products. |
| Line Chart | Shows changes over time. | Tracking monthly revenue. |
| Pie Chart | Shows proportions of a whole. | Displaying market share. |
| Scatter Plot | Shows relationships between two variables. | Comparing advertising spending and sales. |
| Histogram | Shows the distribution of numerical data. | Displaying the age distribution of customers. |

**Visual Examples:**

**1. Bar Chart**

Used to compare values between different categories.

```text
SALES BY PRODUCT

A | ██████████ 100
B | ██████      60
C | █████████   90
D | ████        40
```

**2. Line Chart**

Used to show changes or trends over time.

```text
SALES
  ^
  |                     *
  |                 *
  |             *
  |         *
  |     *
  +----------------------> TIME
```

**3. Pie Chart**

Used to show how different categories contribute to a whole.

For example, a company's market share:

| Company | Market Share |
| --- | --- |
| A | 50% |
| B | 30% |
| C | 20% |

**4. Scatter Plot**

Used to show the relationship between two numerical variables.

For example, a business might compare advertising spending with sales revenue.

```text
SALES
  ^
  |                   *
  |              *  *
  |          *
  |      *  *
  |   *
  +----------------------> ADVERTISING
```

**Misleading Charts**

A misleading chart is a visual representation that gives an incorrect or confusing impression of the data.

This can happen when information is presented in a way that exaggerates differences or hides important details.

Common examples include:

- **Truncated Axis:** Starting a chart's vertical axis above zero can make small differences appear much larger.
- **Distorted Scale:** Using inconsistent intervals can make the data difficult to compare.
- **3D Effects:** Three-dimensional charts can distort the appearance and size of values.
- **Missing Labels:** Leaving out titles, units, or labels can make information unclear.

**Example: Truncated Axis**

Imagine two companies have the following sales:

| Company | Sales |
| --- | --- |
| A | 90 |
| B | 100 |

If the vertical axis starts at 80 instead of 0, the difference between the companies may appear much larger than it really is.

With an axis that starts at 0, the bars are 90 and 100 tall, so B is about 11% taller than A. With an axis that starts at 80, the bars are 10 and 20 tall, so B looks **twice** as tall as A. The data is the same. Only the axis changed.

**Too Much Data**

Too much data in a chart can make it difficult for people to understand the main message.

For example, displaying 100 different product categories in one chart may make the information crowded and confusing.

Common problems include:

- Too many categories.
- Too many colors.
- Overlapping labels.
- Too many data points.
- Unnecessary information.

**How to Improve It:**

1. Remove information that is not relevant.
2. Group similar categories together.
3. Use clear labels and titles.
4. Highlight the most important information.
5. Choose a suitable chart type.

**Choosing the Right Chart**

Choosing the correct chart is important because different charts communicate different types of information.

| What You Want to Show | Recommended Chart |
| --- | --- |
| Compare categories | Bar Chart |
| Show changes over time | Line Chart |
| Show proportions | Pie Chart |
| Show relationships | Scatter Plot |
| Show data distribution | Histogram |

**Simple Example:**

Imagine a company wants to understand its monthly sales.

- To compare sales between different products, use a bar chart.
- To track how sales change every month, use a line chart.
- To show the percentage of total sales contributed by each product, use a pie chart.

The main goal of data visualization is to communicate information clearly and accurately, rather than simply making charts look attractive.

**References**

- Tableau. *Choose the Right Chart Type for Your Data.* https://help.tableau.com/current/pro/desktop/en-us/what_chart_example.htm
- UK Government. *A Bite-Sized Guide to Visualising Data.* https://www.gov.uk/government/publications/a-bite-sized-guide-to-visualising-data-a-dstl-biscuit-book/a-bite-sized-guide-to-visualising-data

---

### 2.4 ETL

ETL stands for **Extract, Transform, Load**. It is a process used to collect data from different sources, prepare it, and store it in a destination where it can be analyzed.

ETL is commonly used in data warehouses and Big Data systems.

**Extract**

Extract means collecting data from different sources.

Data can come from:

- Databases.
- Websites.
- Mobile applications.
- Sensors.
- Business systems.

For example, an online shopping company might collect customer information, product details, and transaction records from its platform.

**Transform**

Transform means cleaning and changing the collected data into a suitable format.

This may involve:

- Removing duplicate records.
- Handling missing values.
- Correcting inconsistent formats.
- Combining information from different sources.

For example, a company might convert different date formats into one standard format and remove unnecessary duplicate records.

**Load**

Load means storing the transformed data in a destination, such as a database or data warehouse.

After loading, the data can be accessed and used for reporting and analysis.

**ETL Process:**

```text
+----------------+
|    EXTRACT     |
|  Collect Data  |
+----------------+
        |
        v
+----------------+
|   TRANSFORM    |
|   Clean Data   |
| Change Format  |
+----------------+
        |
        v
+----------------+
|      LOAD      |
|   Store Data   |
+----------------+
        |
        v
+----------------+
| DATA WAREHOUSE |
+----------------+
        |
        v
    ANALYSIS
```

**Example: Online Shopping Company**

Imagine an online shopping company that wants to analyze its sales.

1. **Extract:** Collect customer information and transaction records from its website.
2. **Transform:** Remove duplicate transactions and correct missing or inconsistent information.
3. **Load:** Store the cleaned data in a data warehouse.

The company can then use the data to analyze customer behavior and sales performance.

ETL helps ensure that data is organized and ready for further analysis.

**ETL and ELT**

In some modern systems, especially those built on cloud storage or data lakes, data is **loaded first and transformed afterwards**. This order is called **ELT** (Extract, Load, Transform). ETL transforms the data *before* storing it. ELT stores the raw data first and transforms it when needed. Both are in common use.

**References**

- AWS. *What Is ETL?* https://aws.amazon.com/what-is/etl/
- AWS. *What Is an ETL Pipeline?* https://aws.amazon.com/what-is/etl-pipeline/

---

### 2.5 The Data Pipeline

A data pipeline is a series of steps that moves data from its original source to its final destination, where it can be analyzed or used.

It helps automate the process of collecting, storing, cleaning, analyzing, and presenting data.

**Main Stages of a Data Pipeline**

**Collect**

The first step is gathering data from different sources.

Examples include:

- Websites.
- Sensors.
- Mobile applications.
- Databases.
- Social media platforms.

**Store**

After collection, the data is stored in a suitable storage system, such as a database or data warehouse.

This allows the data to be accessed and processed later.

**Clean / Transform**

The collected data is cleaned and converted into a suitable format.

This may include removing duplicates, handling missing values, and correcting errors.

**Analyze**

The cleaned data is examined to discover useful information, patterns, and trends.

For example, a business might analyze customer purchases to identify its most popular products.

**Present**

Finally, the results are presented using reports, dashboards, charts, or graphs.

This allows people to understand the information and make decisions.

**Visual Representation:**

```text
+----------------+
|    COLLECT     |
|  Gather Data   |
+----------------+
        |
        v
+----------------+
|     STORE      |
|   Save Data    |
+----------------+
        |
        v
+----------------+
|    CLEAN /     |
|   TRANSFORM    |
|  Prepare Data  |
+----------------+
        |
        v
+----------------+
|    ANALYZE     |
| Find Patterns  |
+----------------+
        |
        v
+----------------+
|    PRESENT     |
|  Show Results  |
+----------------+
        |
        v
    DECISIONS
```

**Note on order.** In the pipeline above, data is stored *before* it is cleaned. This matches **ELT** (see 2.4), where raw data is stored first. If the data is cleaned *before* it is stored, that step is **ETL**. Both can be part of a data pipeline.

**Example: Supermarket Data Pipeline**

Imagine a supermarket wants to understand customer purchasing behavior.

| Stage | Example |
| --- | --- |
| Collect | Collect customer transactions and product purchases. |
| Store | Save the information in a database. |
| Clean / Transform | Remove duplicate transactions and organize the data. |
| Analyze | Identify popular products and purchasing patterns. |
| Present | Display the results in a sales dashboard. |

**ETL vs. Data Pipeline**

ETL and data pipelines are related, but they are not exactly the same.

| ETL | Data Pipeline |
| --- | --- |
| Focuses on Extract, Transform, and Load. | Covers the movement and processing of data through multiple stages. |
| Usually prepares data before loading it into a destination. | Can include storage, analysis, and presentation. |
| Is a specific data-processing process. | Is a broader workflow that can include ETL. |

A data pipeline may use ETL as part of its process.

**References**

- AWS. *What Is a Data Pipeline?* https://aws.amazon.com/what-is/data-pipeline/
- AWS. *What Is an ETL Pipeline?* https://aws.amazon.com/what-is/etl-pipeline/
---

### Terminology

| Term | Meaning |
| --- | --- |
| **Data quality** | How accurate, complete, consistent, and reliable data is |
| **Missing values** | Unrecorded or unavailable entries in a dataset (affects *completeness*) |
| **Duplicate data** | Repeated records of the same information in a dataset (affects *uniqueness*) |
| **Descriptive analytics** | Summarizing past data to explain what happened |
| **Diagnostic analytics** | Examining data to find why something happened |
| **Predictive analytics** | Using historical patterns and models to estimate what might happen |
| **Prescriptive analytics** | Recommending actions to achieve a desired outcome |
| **Data visualization** | Presenting data through charts, graphs, and diagrams to aid understanding |
| **Truncated axis** | Starting a chart axis above zero, which can exaggerate visual differences |
| **ETL** | Extract, Transform, Load—collecting, cleaning/formatting, and storing data |
| **ELT** | Extract, Load, Transform—loading raw data first and transforming it afterward |
| **Data pipeline** | An end-to-end series of stages moving and processing data from source to presentation |
