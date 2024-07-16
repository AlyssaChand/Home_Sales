# Home_Sales

These are the sources I used to help write my code: google and BCS — watching our cloud recordings, using instructor activity solutions and the class activities as references. I also used ChatGPT for guidance and clarification of concepts.

For this challenge, the task is to use SparkSQL to determine key metrics about home sales data. I used Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Overview

This notebook demonstrates how to perform data analysis on home sales data using PySpark in a Google Colab environment. The steps include installing necessary dependencies, reading data from an S3 bucket, performing SQL queries, caching data for performance improvements, and leveraging Parquet for optimized storage.

## Steps

1. Install Dependencies and Set Up Environment
   
    ![image](https://github.com/user-attachments/assets/eac04449-cdfb-4fff-a39e-be441b730c6f)

    ![image](https://github.com/user-attachments/assets/18bffb6e-be7c-467f-b8eb-7bff7fa06256)

2. Load Data from S3 Bucket

    ![image](https://github.com/user-attachments/assets/56e84141-51db-418d-aa49-e20ca982b0ad)

    ![image](https://github.com/user-attachments/assets/4373883a-53e3-4c28-8710-60f611ca173f)

3. Perform SQL Queries

    ![image](https://github.com/user-attachments/assets/9c10491a-0636-4528-82c8-67f99f1f712b)

4. Cache the Table and Measure Performance

    ![Screenshot 2024-07-15 181646](https://github.com/user-attachments/assets/97029245-f6fd-4b67-af13-82fe6c87539c)

    ![image](https://github.com/user-attachments/assets/e3042f71-c305-4ae5-96f5-4b7d2812d7aa)

5. Partition and Read Parquet Data

    ![image](https://github.com/user-attachments/assets/a84643b0-b496-47f7-92b7-737b1491dc67)

    ![image](https://github.com/user-attachments/assets/6ad247c1-c127-42fe-b05c-d68271ce0411)

6. Uncache the Table and Verify

    ![image](https://github.com/user-attachments/assets/57b64003-b08a-40bb-87ae-e05970469d8a)

## Analysis
Uncached Data Runtime: The query took approximately 1.31 seconds to execute. When the data is not cached, each query execution involves reading data from disk. This disk I/O process is relatively slow and can significantly impact the query performance.

   ![image](https://github.com/user-attachments/assets/07589c56-ab4b-4074-b96a-ecf337e0fd96)

Cached Data Runtime: Caching the data reduced the query time to approximately 0.67 seconds, because the data was stored in memory instead of being read from disk each time. This reduces the query execution time since Spark can quickly retrieve the data from memory without repeated disk I/O operations.

   ![image](https://github.com/user-attachments/assets/ad520cf9-adfc-4c38-a91d-1b2ca7e84ff0)

Parquet Data Runtime: Reading from Parquet format took approximately 1.30 seconds. Although Parquet optimizes read performance with effective data compression and encoding, it took longer than cached data. This indicates that, while Parquet optimizes storage and query performance, accessing data from memory (cached data) is inherently faster than reading from disk, even with Parquet's optimizations.

   ![image](https://github.com/user-attachments/assets/ddd293d5-55f5-42c9-8d4e-fce1d6769c05)

Both caching and Parquet storage can be crucial in big data scenarios to enhance performance, reduce query latency, and make data processing more efficient. Understanding when to use these techniques based on the specific context and requirements is key to optimizing performance in big data environments.

 
