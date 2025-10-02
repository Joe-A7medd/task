# PySpark Task Project

##  Overview
This project contains a PySpark task submitted as part of the assignment.  
It demonstrates multiple PySpark functionalities including:
- Creating RDDs and DataFrames
- Basic transformations and actions
- Aggregations (sum, average, min, max, count)
- Filtering and grouping
- Word count and stopword removal
- Working with text files and DataFrame schema operations

---

##  Task Code
The code is in the file: `pyspark_task.py`  

> You can open it directly to see the implementation.  

The task includes:
1. Creating an RDD from numbers 1–49 using `numpy`.
2. Calculating sum, average, max, min, and count.
3. Counting even vs. odd numbers.
4. Working with people data (age, name) for max age, average age, and grouping names by age.
5. Text analysis on `russia.txt`: line counts, word frequency, tokenization, removing stopwords.
6. Creating a DataFrame with schema `(id, name, age, salary)` and performing:
   - `select`
   - `filter`
   - `groupBy` with aggregation
   - counting distinct values

---

## How to Run (Using Docker Compose)

1. Make sure **Docker** and **Docker Compose** are installed.  

2. Start all services using Docker Compose:
   ```bash
   docker-compose up -d
    ```
   
This will start:

spark (Spark Master)

spark-worker (Spark Worker)

jupyter (Jupyter Notebook with PySpark)

namenode (Hadoop HDFS NameNode)

datanode (Hadoop HDFS DataNode)

##  Access Jupyter Notebook
Open your browser and go to: [http://localhost:8888](http://localhost:8888)

## Notes (Docker Version)

All project files are in ./shared on your host and mounted to /data inside containers.

Spark Master URL: spark://spark:7077.

Hadoop HDFS is running (NameNode: http://localhost:9870).

Make sure russia.txt and scripts are inside ./shared folder.

spark-submit commands must reference paths inside the container, e.g., /data/pyspark_task.py.

Jupyter Notebook can also be used to run and test scripts interactively.

The task demonstrates both RDD and DataFrame operations for learning purposes.

