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
Yelp Academic Dataset:

Official Link – not included in this repo due to size.
We filter data for Arizona (state = 'AZ').
business_id & user_id are common across the business, review, user, checkin, tip JSON files.
Data Files
yelp_academic_dataset_business.json
yelp_academic_dataset_user.json
yelp_academic_dataset_review.json
yelp_academic_dataset_checkin.json
yelp_academic_dataset_tip.json

