# Spotify ETL Pipeline using AWS & Snowflake
This project implements an ETL (Extract, Transform, Load) pipeline to fetch global trending songs from Spotify's API and process the data using AWS and Snowflake.

## **Pipeline Overview:**

![Spotify ETL Architecture](images/arch.png)


### **1. Extraction**
- A **Python script** extracts data from **Spotify's API**.
- This process is automated using **AWS Lambda**, triggered daily by **Amazon CloudWatch**.
- The extracted raw data is stored in an **Amazon S3 bucket**.
![Extraction](images/extract.png)

### **2. Transformation**
- The raw data is retrieved from **S3** and transformed using **AWS Lambda**.
- The transformed data is then stored back in **S3**.
- **AWS triggers** automate the transformation process upon data arrival.

### **3. Loading**
- The transformed data is loaded into **Snowflake** using **Snowpipe**.
- AWS and Snowflake integration ensures seamless data transfer.
