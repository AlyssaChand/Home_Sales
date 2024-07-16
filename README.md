# Home_Sales

These are the sources I used to help write my code: google and BCS — watching our cloud recordings, using instructor activity solutions and the class activities as references. I also used ChatGPT for guidance and clarification of concepts.

For this challenge, the task is to use SparkSQL to determine key metrics about home sales data. I used Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

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

    ![image](https://github.com/user-attachments/assets/3a3609ca-2105-4c30-bbd5-17c4a9969d0d)

    ![image](https://github.com/user-attachments/assets/6ad247c1-c127-42fe-b05c-d68271ce0411)

6. Uncache the Table and Verify

    ![image](https://github.com/user-attachments/assets/57b64003-b08a-40bb-87ae-e05970469d8a)

## Analysis
Uncached Data Runtime

   ![image](https://github.com/user-attachments/assets/36b504ab-2f94-4ca7-bab5-f22aa3645415)

Cached Data Runtime

   ![image](https://github.com/user-attachments/assets/b51148dd-4726-43ee-a97b-ccb4948d1d11)

Parquet Data Runtime

   ![image](https://github.com/user-attachments/assets/e54c08e1-e7b7-43b4-b2ac-8114985d1556)






