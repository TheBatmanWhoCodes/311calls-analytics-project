# 311calls-analytics-project

# Project Description: Descriptive Analysis of 311 Calls 

**Dataset:** [311 Calls](https://opendata.vancouver.ca/explore/dataset/3-1-1-contact-centre-metrics/table/)

## Objective
The 311 Calls Data Analytic Platform objective is to gain insights about the Service Level of the people who call 311 using statistical measures such as counts, averages, and distributions, to provide a clear overview of 311 calls. The project is structured using AWS Services to perform data ingestion, storage, preparation, cleaning, transformation, and visualization tasks.

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/684ae10b-f1d2-4ee4-8545-df0b0f8da7f9">

## Data Discovery

Below is a list of all the features of the dataset:
1. **Date** -> Date of the Call
2. **CallsOffered** -> Total Number of Calls Received that day at the 311 call center. 
3. **CallsHandled** -> Number of calls that were successfully answered.
4. **CallsAbandoned** -> Number of calls that hung up before reaching a live agent.
5. **AverageSpeedOfAnswer** -> Average time it takes from the start to transfer to a live agent. 
6. **ServiceLevel** -> The level of service provided by the live agent measured between 0-1.

## Methodology

### 1: Data Storage Design
- **Storage Method:** The dataset was stored in a structured Excel format.
- **S3 Bucket :** For storage, the data is stored in S3 buckets with folders for different reporting years (2023 and 2024).


<img width="1000" alt="image" src="https://github.com/user-attachments/assets/241ffbe5-fac4-44f1-8a10-3490563d87e3">

![image](https://github.com/user-attachments/assets/4ba0cde4-9785-4f85-bee1-ef366c998c8f)

### 2: Dataset Preparation
**Tool Used:** AWS Glue Databrew

Tasks:
- Removing duplicates. 
- Conversion of categorical fields to numerical ones.

![image](https://github.com/user-attachments/assets/dd0ce9ee-6a4a-41a2-8b10-dedb9009d09f)

### 3: Data Ingestion, Storage, Pipeline Design, Cleaning, Pipeline Implementation
**Tool Used:** AWS Glue

Tasks:
- Changed schema and replaced null values.
- Cleaning to remove duplicates, standardize entries, and ensure consistent formatting.
- Removal of irrelevant columns.
- Final filtered data was stored in the curated S3 folder.

![image](https://github.com/user-attachments/assets/ff96721c-c18f-40e2-8849-90a0375837c1)

### 4: Data Structuring
**Tool Used:** AWS Athena

- Data was structured into SQL-based tables

![image](https://github.com/user-attachments/assets/1db4a327-887c-40cc-bda3-a117163591e8)

### 5: Data Analysis and Visualization

- The data was then analyzed and charts were created for better understanding.

<img width="452" alt="image" src="https://github.com/user-attachments/assets/6efa860e-54a0-4b63-8e17-f629c51b2736">

### 6: Data Protection
**Encryption Tool:** AWS KMS

- The key was created to provide access only to specific users who needed the 311 call records for analysis. Additionally, a replication rule was created so that if the bucket gets deleted, the data is still safe and secure. 

![image](https://github.com/user-attachments/assets/c3da67b3-62e3-48a5-b4b0-76c381ff51ba)
![image](https://github.com/user-attachments/assets/d573379a-93a2-4059-83c2-792e62ddca34)


### 8: Data Monitoring
**Monitoring Tools:** AWS CloudWatch 

- Used for real time monitoring.
![image](https://github.com/user-attachments/assets/608c8946-b9f7-41c6-bc43-44d62e4f985f)


## **Tools and Techniques:**
- **Athena**
- **Excel**
- **AWS S3**
- **EC2**
- **KMS**
- **Cloudwatch**
- **Cloudtrail**
- **Glue**
- **Glue Databrew**

## **Deliverables:**
1. **Data Analytical Questions and Discovery**
2. **Data Storage Structure**
3. **Cleaned Dataset**
4. **Data Visualization**
5. **Data Encryption for security**
6. **Data Monitoring**
7. **ETL Pipeline**
8. **Structured SQL Queries**

## Conclusion

This data analytics initiative helps the City of Vancouver make informed decisions about the 311 contact centre and helps them refine the service. By analyzing trends in calls abandoned and average service level, the city can look to make changes and improve their service. 
