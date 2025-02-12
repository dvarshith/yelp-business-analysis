# Yelp Dataset Analysis for Arizona Businesses

<br/>

[![Hadoop](https://img.shields.io/badge/Big%20Data-Hadoop-blue)](https://hadoop.apache.org/)
[![Spark](https://img.shields.io/badge/Big%20Data-Spark-orange)](https://spark.apache.org/)
[![Python](https://img.shields.io/badge/Python-3.8+-green.svg)](https://www.python.org/)

<br/>

## Overview
This repository contains my **Yelp dataset** analysis project. The goal is to perform:
1. **Business-level analysis** (Milestone 1) – focusing on attributes, ratings, locations, etc.
2. **User-level analysis** (Milestone 2) – focusing on user behavior, sentiment, and user influence.

We use **Apache Hadoop** for distributed file storage and **Apache Spark** (PySpark) for data processing. 
The dataset is the [Yelp Academic Dataset](https://www.yelp.com/dataset) filtered to **Arizona** (AZ) businesses.

<br/>

## Requirements & Setup
### 1. Virtual Machine (Provided by Course)
- A pre-configured VM (Ubuntu 22.04) is available with Hadoop, Spark, and PySpark already installed.
- **Username/Password**: `dps`
- If you need instructions, see the `docs/VM-setup.md` or the course instructions for VirtualBox/UTM usage.
### 2. Hadoop & Spark
- **Hadoop**: v3.x 
  - Start services:  
    ```bash
    hdfs namenode -format   # first time only
    start-dfs.sh
    start-yarn.sh
    ```
  - Web UIs:  
    - HDFS: [http://localhost:9870](http://localhost:9870)  
    - Yarn: [http://localhost:8088](http://localhost:8088)
- **Spark**: v3.x
  - Interactive shell:
    ```bash
    spark-shell
    ```
  - PySpark:
    ```bash
    pyspark
    ```
### 3. Python / PySpark
- **Python** 3.8+ recommended
- `pyspark` installed in the VM
- Optionally Jupyter Notebook for an interactive environment:
  ```bash
  jupyter notebook
  # or: pyspark

<br/>

## Dataset
### Yelp Academic Dataset:
- [Official Link](https://www.yelp.com/dataset) – not included in this repo due to size.
- We filter data for Arizona (`state = 'AZ'`).
- `business_id` & `user_id` are common across the `business`, `review`, `user`, `checkin`, `tip` JSON files.
### Data Files
- `yelp_academic_dataset_business.json`
- `yelp_academic_dataset_user.json`
- `yelp_academic_dataset_review.json`
- `yelp_academic_dataset_checkin.json`
- `yelp_academic_dataset_tip.json`

<br/>

## How to Run
- Clone Repo:
  ```
  git clone https://github.com/<YourUser>/yelp-arizona-business-analysis.git
  cd yelp-arizona-business-analysis
  ```
- **Launch VM** (if using course-provided OVA/UTM).
- Start Hadoop & Spark (in the VM):
  ```
  hdfs namenode -format   # first time only
  start-dfs.sh
  start-yarn.sh
  pyspark
  ```
- Open the Notebook:
  ```
  cd Milestone1-Business
  jupyter notebook Project1Milestone1.ipynb
  ```
- Run cells to see queries & analysis. Similarly for `Milestone2-User`.

<br/>

## Milestone 1: Business-Level Analysis
- **Objective**: Analyze AZ businesses, focusing on attributes, ratings, categories, location patterns.
- **Approach**:
  - Convert JSON to Parquet or a suitable Spark format.
  - Filter to `state='AZ'`.
  - Perform SQL-like queries in Spark (e.g., spark.sql("SELECT ... FROM ... WHERE ...")).
  - Generate graphs & insights.
- **Queries**:
  - 5 total (minimum), at least 3 complex queries combining multiple datasets.
  - Example: “Top 10 highest-rated businesses in the ‘Restaurants’ category within Phoenix.”

<br/>

## Milestone 2: User-Level Analysis
- **Objective**: Analyze user behavior (reviews, tips, sentiment, influence).
**Approach**:
- Focus on users who reviewed the AZ businesses from Milestone 1.
- Possibly do sentiment analysis on `review.txt` or `tip.txt`.
- Check user attributes (average stars, friend count, compliment counts).
**Queries**:
- 10 total, 6 of which combine multiple datasets.
Example: “Which users have the most influence (highest fans or compliment counts) in a specific business category?”

<br/>

## Results
- Data filtering & approach
- Spark queries (with code snippets, no direct copy from provided notebooks)
- Graphs & figures
- Key insights from business-level and user-level analysis

</br>

## Acknowledgments
- Dataset, test cases, etc. provided by Dr. Samira Ghayekhloo from Arizona State University.

</br>

## License
This project is released under the `MIT License`. That means you’re free to use, modify, and distribute the code, but you do so at your own risk.

</br>

## Contact
Author: Varshith Dupati </br>
GitHub: @dvarshith </br>
Email: dvarshith942@gmail.com </br>
Issues: Please open an issue on this repo if you have questions or find bugs. </br>
