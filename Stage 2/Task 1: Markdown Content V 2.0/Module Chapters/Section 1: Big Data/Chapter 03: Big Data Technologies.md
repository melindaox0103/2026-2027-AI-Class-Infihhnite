## Chapter 3: Big Data Technologies

Big Data technologies are tools and systems used to store, process, analyze, and visualize large amounts of data.

These technologies help organizations handle data that may be too large or complex for traditional systems.

---

### 3.1 Categories of Technology

Big Data technologies can be divided into four main categories: **Storage, Processing, Analytics, and Visualization**.

Each category has a different role in handling data.

**Storage Technologies**

Storage technologies are used to save and organize large amounts of data so that it can be accessed later.

They help manage data from different sources and support large-scale storage.

Examples include:

- Hadoop Distributed File System (HDFS).
- Cloud storage.
- Distributed databases.
- Data warehouses (for example Amazon Redshift, Google BigQuery, Snowflake).
- Data lakes on cloud object storage (for example Amazon S3).

**Processing Technologies**

Processing technologies are used to handle and process large amounts of data efficiently.

They help perform calculations, transform information, and process data across multiple computers.

Examples include:

- Apache Hadoop.
- Apache Spark.

Note: **Hadoop** is a software framework. It includes HDFS (storage), YARN (resource management), and MapReduce (processing), so it appears under both storage and processing.

**Analytics Technologies**

Analytics technologies help examine data to identify patterns, trends, and useful information.

They are used to support predictions, business decisions, and statistical analysis.

Examples include:

- Python.
- R.
- Apache Spark.

**Visualization Technologies**

Visualization technologies present data using charts, graphs, and dashboards.

They make complex information easier to understand.

Examples include:

- Tableau.
- Microsoft Power BI.
- Looker.

**Comparison Table:**

| Category | Purpose | Examples |
| --- | --- | --- |
| Storage | Stores large amounts of data. | HDFS, Cloud Storage, Data Warehouses, Data Lakes |
| Processing | Processes and transforms data. | Hadoop, Spark |
| Analytics | Examines data to find patterns. | Python, R, Spark |
| Visualization | Presents data using charts and dashboards. | Tableau, Power BI, Looker |

**Visual Representation:**

```text
        +------------------+
        |     BIG DATA     |
        |   TECHNOLOGIES   |
        +------------------+
                  |
   +--------------+--------------+--------------+
   |              |              |              |
   v              v              v              v
STORAGE       PROCESSING     ANALYTICS    VISUALIZATION
Save data     Transform      Find          Show
              and compute    patterns      results
```

Together, these technologies help turn raw data into useful information.

**References**

- Apache Hadoop. *HDFS Architecture.* https://hadoop.apache.org/docs/r3.3.0/hadoop-project-dist/hadoop-hdfs/HdfsDesign
- Google Cloud. *What Is Apache Spark?* https://cloud.google.com/learn/what-is-apache-spark
- Apache Spark. *Unified Engine for Large-Scale Data Analytics.* https://spark.apache.org/
- AWS. *Choosing an AWS Analytics Service.* https://docs.aws.amazon.com/decision-guides/latest/decision-guides/analytics-on-aws-how-to-choose.html

---

### 3.2 Scale Up (Vertical) vs Scale Out (Horizontal)

Scaling refers to increasing a system's capacity so that it can handle more data, users, or processing tasks.

There are two main approaches: **Vertical Scaling (Scale Up)** and **Horizontal Scaling (Scale Out)**.

**Vertical Scaling (Scale Up)**

Vertical scaling means improving the capacity of an existing computer by adding more resources to it.

This can include:

- Increasing RAM.
- Upgrading the CPU.
- Adding more storage.

For example, a company might upgrade its server from 8 GB of RAM to 32 GB so that it can handle more tasks.

**Visual Representation:**

```text
BEFORE                AFTER

+----------+          +----------+
|  SERVER  |          |  SERVER  |
|          |   ---->  |          |
|   8 GB   |          |  32 GB   |
|   RAM    |          |   RAM    |
+----------+          +----------+
```

The same server becomes more powerful.

**Horizontal Scaling (Scale Out)**

Horizontal scaling means increasing system capacity by adding more computers or servers to work together.

Instead of upgrading one computer, additional computers are connected to the system.

For example, an online shopping platform might add more servers to handle an increase in website visitors.

**Visual Representation:**

```text
BEFORE

+----------+
| SERVER 1 |
+----------+

AFTER

+----------+   +----------+   +----------+
| SERVER 1 |   | SERVER 2 |   | SERVER 3 |
+----------+   +----------+   +----------+
      |              |              |
      +--------------+--------------+
                     |
               MORE CAPACITY
```

**Comparison Table**

| Comparison | Vertical Scaling (Scale Up) | Horizontal Scaling (Scale Out) |
| --- | --- | --- |
| Meaning | Upgrades an existing computer. | Adds more computers or servers. |
| Method | Adds more CPU, RAM, or storage. | Connects additional machines. |
| Cost | Can be expensive when high-end hardware is needed. | Can start with cheaper machines, but costs increase as more are added. |
| Limits | Limited by the maximum capacity of one machine. | Can expand by adding more machines, although coordination becomes more complex. |
| Complexity | Usually simpler to manage. | Requires coordination between multiple machines. |
| Reliability | One machine failure can affect the whole system. | Can continue operating if other machines are available and the system is designed for fault tolerance. |
| Example | Upgrading a server's RAM. | Adding more servers to a website. |

**Simple Analogy:**

Imagine a restaurant experiencing more customers.

- **Vertical Scaling:** Make the existing kitchen larger and give it better equipment.
- **Horizontal Scaling:** Open additional kitchens to serve more customers.

Both approaches increase capacity, but they work in different ways.

**References**

- Google Cloud. *What Is Cloud Scalability?* https://cloud.google.com/discover/what-is-cloud-scalability
- NIST. (2019). *NIST Big Data Interoperability Framework: Volume 1, Definitions* (NIST SP 1500-1r2). https://doi.org/10.6028/NIST.SP.1500-1r2

---

### 3.3 Challenges

Although Big Data technologies provide many benefits, organizations may face several challenges when implementing and managing them.

Five common challenges are **Cost, Skills, Integration, Security, and Privacy**.

**Cost**

Big Data systems can be expensive to develop, operate, and maintain.

Organizations may need to spend money on:

- Servers and storage systems.
- Cloud computing services.
- Software and technology.
- System maintenance.

For example, a company handling millions of customer transactions may need additional storage and computing resources, increasing its operating costs.

**Skills**

Big Data requires people with technical knowledge and experience.

Organizations may struggle to find employees who understand data management, programming, analytics, and machine learning.

For example, a company may have large amounts of data but lack employees who know how to analyze it properly.

**Integration**

Integration means combining data from different sources and systems.

This can be difficult because different systems may use different formats, structures, or technologies.

For example, a business may store customer information in one database and sales records in another. Combining these datasets can require additional processing.

**Security**

Security refers to protecting data from unauthorized access, theft, or damage.

Big Data systems often store large amounts of valuable information, making them attractive targets for cyberattacks.

Organizations need security measures such as:

- Password protection.
- Access controls.
- Data encryption.
- Regular security updates.

**Privacy**

Privacy refers to protecting personal information and ensuring that it is collected and used responsibly.

For example, companies may collect customer names, addresses, purchasing histories, and other personal information.

If this information is misused or shared without proper permission, it can violate people's privacy.

Organizations should follow relevant data protection laws (for example the EU's GDPR, or Thailand's Personal Data Protection Act B.E. 2562) and handle personal information responsibly.

**Comparison Table:**

| Challenge | Meaning | Example |
| --- | --- | --- |
| Cost | Big Data systems can be expensive. | Paying for additional servers and storage. |
| Skills | Requires trained employees. | Lack of workers who understand data analytics. |
| Integration | Combining data from different sources can be difficult. | Merging customer data from different databases. |
| Security | Protecting data from unauthorized access. | Preventing cyberattacks and data theft. |
| Privacy | Protecting people's personal information. | Preventing misuse of customer information. |

**References**

- Gandomi, A., & Haider, M. (2015). Beyond the hype: Big data concepts, methods, and analytics. *International Journal of Information Management*, 35(2), 137–144. https://doi.org/10.1016/j.ijinfomgt.2014.10.007
- Sivarajah, U., Kamal, M. M., Irani, Z., & Weerakkody, V. (2017). Critical analysis of Big Data challenges and analytical methods. *Journal of Business Research*, 70, 263–286. https://doi.org/10.1016/j.jbusres.2016.08.001
- Kitchin, R. (2014). *The Data Revolution: Big Data, Open Data, Data Infrastructures and Their Consequences*. SAGE Publications. https://doi.org/10.4135/9781473909472
- European Union. (2016). *Regulation (EU) 2016/679 (General Data Protection Regulation).*

---

### 3.4 MapReduce

MapReduce is a programming model used to process large amounts of data across multiple computers. It was introduced by Google in 2004 and is best known today through Apache Hadoop.

It divides a large task into smaller tasks, processes them separately, and combines the results.

There are four main stages: **Split, Map, Shuffle, and Reduce**.

**Split**

The first stage divides a large dataset into smaller sections.

These sections can then be processed separately by different computers.

For example, a large collection of documents can be divided into several smaller groups.

**Map**

The Map stage processes each section and produces intermediate results.

For example, if the task is to count words in documents, the Map stage identifies each word and assigns it a value of 1.

**Example:**

```text
INPUT:
"Apple Banana Apple"

MAP OUTPUT:
(Apple, 1)
(Banana, 1)
(Apple, 1)
```

**Shuffle**

The Shuffle stage groups together intermediate results with the same key, and sorts them by key, so that each Reduce task receives all the values for its keys.

For example, all occurrences of the word "Apple" are grouped together, while all occurrences of "Banana" are placed in another group.

**Example:**

```text
BEFORE SHUFFLE:
(Apple, 1)
(Banana, 1)
(Apple, 1)

AFTER SHUFFLE:
Apple  -> (1, 1)
Banana -> (1)
```

**Reduce**

The Reduce stage combines the grouped values to produce the final result.

For example, it adds the values together to calculate how many times each word appears.

**Example:**

```text
REDUCE:
Apple  -> 1 + 1 = 2
Banana -> 1     = 1

FINAL RESULT:
Apple: 2
Banana: 1
```

**Complete MapReduce Process:**

```text
+----------------+
|   LARGE DATA   |
+----------------+
        |
        v
+----------------+
|     SPLIT      |
|  Divide Data   |
+----------------+
        |
        v
+----------------+
|      MAP       |
|  Process Data  |
+----------------+
        |
        v
+----------------+
|    SHUFFLE     |
| Group Results  |
+----------------+
        |
        v
+----------------+
|     REDUCE     |
| Combine Values |
+----------------+
        |
        v
+----------------+
| FINAL RESULTS  |
+----------------+
```

**Real-Life Example:**

Imagine a website wants to count how many times each word appears in millions of user comments.

1. **Split:** Divide the comments into smaller groups.
2. **Map:** Count each word in each group.
3. **Shuffle:** Group identical words together.
4. **Reduce:** Add the counts to calculate the total number of times each word appears.

MapReduce makes it possible to process large datasets by distributing smaller tasks across multiple computers.

**Today:** many organizations now use Apache Spark for jobs that once used MapReduce, because Spark keeps more data in memory. MapReduce remains the clearest way to learn the idea of splitting work across many machines.

**References**

- Dean, J., & Ghemawat, S. (2004). MapReduce: Simplified Data Processing on Large Clusters. *Proceedings of the 6th Symposium on Operating Systems Design and Implementation (OSDI '04).*
- Apache Hadoop. *MapReduce Tutorial.* https://hadoop.apache.org/docs/stable/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html

---

### 3.5 Future Trends

Big Data technologies continue to develop as organizations need faster, more flexible, and more efficient ways to handle information.

Three important trends are **Cloud Computing, Edge Computing, and Real-Time Streaming**.

**Cloud Computing**

Cloud computing allows organizations to store data and use computing resources through the internet instead of relying entirely on their own physical computers and servers.

This allows businesses to access storage and computing power when needed.

Benefits include:

- Flexible storage capacity.
- Access from different locations.
- Reduced need to maintain physical servers.
- Ability to increase or decrease resources based on demand.

For example, a company can use cloud storage to save customer information without building its own large data center.

**Edge Computing**

Edge computing processes data closer to where it is generated instead of sending everything to a distant central server.

This can reduce delays and allow faster responses.

For example, a smart security camera can process information locally to detect movement without sending every second of video to a central server.

**Benefits:**

- Faster data processing.
- Reduced network delays.
- Less data needs to be sent to central servers.
- Useful for devices that need quick responses.

**Real-Time Streaming**

Real-time streaming involves continuously collecting and processing data as it is generated.

Instead of waiting for data to be collected in large batches, the system processes information as it arrives.

For example, a navigation application can continuously receive traffic information and update its recommended routes.

**Benefits:**

- Provides up-to-date information.
- Allows faster decision-making.
- Helps detect changes as they happen.
- Useful for monitoring systems and live applications.

**Comparison Table:**

| Technology | Main Idea | Example |
| --- | --- | --- |
| Cloud Computing | Uses internet-based servers for storage and computing. | Storing files using cloud services. |
| Edge Computing | Processes data close to where it is generated. | Smart cameras detecting movement locally. |
| Real-Time Streaming | Processes data continuously as it arrives. | Live traffic updates. |

**Visual Summary:**

```text
        DATA GENERATION
              |
      +-------+-------+
      |       |       |
      v       v       v
   CLOUD     EDGE   REAL-TIME
      |       |       |
      v       v       v
   Store   Process  Process
   Data    Locally  Continuously
      |       |       |
      +-------+-------+
              |
              v
        USEFUL RESULTS
```

These technologies help make Big Data systems more flexible, responsive, and efficient.

**References**

- Mell, P., & Grance, T. (2011). *The NIST Definition of Cloud Computing* (NIST SP 800-145). https://doi.org/10.6028/NIST.SP.800-145
- Shi, W., Cao, J., Zhang, Q., Li, Y., & Xu, L. (2016). Edge computing: Vision and challenges. *IEEE Internet of Things Journal*, 3(5), 637–646. https://doi.org/10.1109/JIOT.2016.2579198
- Singh, R., & Gill, S. S. (2023). Edge AI: A survey. *Internet of Things and Cyber-Physical Systems*, 3, 71–92. https://doi.org/10.1016/j.iotcps.2023.02.004
- Amazon Web Services. (n.d.). *What Is Real-Time Data Streaming?* https://aws.amazon.com/what-is/real-time-data-streaming/
- Kleppmann, M. (2017). *Designing Data-Intensive Applications* (Chapter 11: Stream Processing). O'Reilly Media.

---

### 3.6 Distributed Storage Idea

Distributed storage is a method of storing data across multiple computers instead of keeping everything on a single machine.

This approach allows large amounts of information to be stored and accessed across a network.

It is commonly used in Big Data systems because one computer may not have enough storage capacity to handle extremely large datasets.

Three important concepts are **Blocks, Replication, and Fault Tolerance**.

**Blocks**

Large files can be divided into smaller pieces called blocks.

These blocks are then stored across different computers in a distributed storage system.

For example, in HDFS a large file is split into blocks of **128 MB** by default, and the blocks are stored on different machines. The diagram below uses four blocks to keep the idea simple.

**Visual Representation:**

```text
+----------------------+
|      LARGE FILE      |
+----------------------+
           |
           v
   DIVIDE INTO BLOCKS
           |
  +--------+--------+--------+
  |        |        |        |
  v        v        v        v
+------+ +------+ +------+ +------+
|Block1| |Block2| |Block3| |Block4|
+------+ +------+ +------+ +------+
  |        |        |        |
  v        v        v        v
 STORE ACROSS DIFFERENT MACHINES
```

Dividing files into blocks makes it easier to distribute and manage large amounts of data.

**Replication**

Replication means creating multiple copies of each block and storing them on different machines. HDFS keeps **three** copies of each block by default, and spreads them across machines (and, where possible, across racks) so the data survives the loss of a machine or even a whole rack.

This helps ensure that data remains available even if one machine becomes unavailable.

For example, if Block 1 is stored on Machine A, other copies may be stored on Machine B and Machine C.

**Visual Representation:**

```text
           ORIGINAL BLOCK
              Block 1
                 |
       +---------+---------+
       |         |         |
       v         v         v
 +-----------+ +-----------+ +-----------+
 | Machine A | | Machine B | | Machine C |
 |  Block 1  | |  Block 1  | |  Block 1  |
 +-----------+ +-----------+ +-----------+
     COPY          COPY          COPY
```

If one machine becomes unavailable, another machine may still have a copy of the data.

**Fault Tolerance**

Fault tolerance is the ability of a system to continue operating even when part of the system fails.

Distributed storage systems use techniques such as replication to reduce the risk of losing access to data.

For example, if one storage machine stops working, the system can retrieve the required information from another machine containing a copy.

**Why Is It Important?**

- Reduces the risk of data loss.
- Improves data availability.
- Allows systems to continue operating when machines fail.
- Supports the storage of large datasets.

**Comparison of the Three Concepts:**

| Concept | Meaning | Purpose |
| --- | --- | --- |
| Blocks | Divides large files into smaller pieces. | Makes data easier to distribute and store. |
| Replication | Creates multiple copies of data. | Keeps additional copies available. |
| Fault Tolerance | Allows a system to continue working when failures occur. | Improves system reliability. |

**Complete Distributed Storage Process:**

```text
+------------------+
|    LARGE FILE    |
+------------------+
          |
          v
   DIVIDE INTO BLOCKS
          |
   +------+------+------+
   |      |      |      |
   v      v      v      v
Block 1 Block 2 Block 3 Block 4
   |      |      |      |
   v      v      v      v
  DISTRIBUTE ACROSS MACHINES
          |
          v
    CREATE COPIES
    (REPLICATION)
          |
          v
    FAULT TOLERANCE
          |
          v
 DATA REMAINS AVAILABLE
```

Distributed storage allows Big Data systems to store large amounts of information while improving availability and reliability.

**References**

- Apache Hadoop. *HDFS Architecture.* https://hadoop.apache.org/docs/r3.3.0/hadoop-project-dist/hadoop-hdfs/HdfsDesign
- Ghemawat, S., Gobioff, H., & Leung, S.-T. (2003). The Google File System. *Proceedings of the 19th ACM Symposium on Operating Systems Principles (SOSP '03).*
- NIST. (2019). *NIST Big Data Interoperability Framework: Volume 1, Definitions* (NIST SP 1500-1r2). https://doi.org/10.6028/NIST.SP.1500-1r2
