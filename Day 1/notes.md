# What I Learned

## 1️. Why Databricks over Pandas / Hadoop?

- **Pandas** works well for small, local datasets but struggles with large-scale data
- **Hadoop (MapReduce)** is powerful but complex and slow to develop with
- **Databricks (Spark-based)** offers:
  - **In-memory processing** → faster execution
  - **Unified platform** for Data Engineering, Analytics, and AI
  - Less boilerplate, more productivity
  - Easy scalability for big data workloads

**Databricks sits in the sweet spot between performance and developer experience.**

## 2️. Lakehouse Architecture – Basics

Combines the best of:
- **Data Lakes** (cheap storage, scalability)
- **Data Warehouses** (structured data, performance, reliability)

**Key idea:** One data platform for:
- Batch + Streaming
- BI + ML
- Structured + Semi-structured data

Uses **Delta Lake** to add reliability (ACID transactions) on top of cloud storage.

## 3️. Databricks Workspace Overview

Understood the core components of the UI:
- **Workspace** → Where notebooks, folders, and repos live
- **Compute** → Clusters used to run Spark jobs
- **Catalog** → Tables, schemas, and data assets

This helped me understand where code runs and where data lives.

## 4️. Industry Use Cases

Real-world companies using Databricks:
- **Netflix** → Data processing, recommendations
- **Shell** → Energy data analytics
- **Comcast** → Customer and streaming data insights

This made it clear that Databricks is built for production-scale systems.

---

## Tasks Completed

* Created Databricks Community Edition account  
* Explored:
  - Workspace
  - Compute
  - Data Explorer 
* Created my first Databricks notebook  
* Ran basic PySpark commands successfully

---

## Hands-on Practice

```python
# Create simple DataFrame
data = [("iPhone", 999), ("Samsung", 799), ("MacBook", 1299)]
df = spark.createDataFrame(data, ["product", "price"])
df.show()

# Filter expensive products
df.filter(df.price > 1000).show()
```

**Key takeaway from this:**
- Spark DataFrames feel similar to Pandas but are distributed by design
- Operations are lazy, meaning execution happens only when required (like `.show()`)
--- 




![day 1 code image](day1-code.png)

#DatabricksWithIDC



