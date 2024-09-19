# **Operating Permit Data Analytical Platform**
Dataset: Operating Permit Data

**Operating Permit Data URL:** [(https://opendata.vancouver.ca/explore/dataset/operating-permits-water-systems-water-quality-reports/information/)]

---

## **Objectives:**
The Operating Permit Data Analytical Platform project is designed to analyze mechanical system permits issued in Vancouver. The project aims to evaluate trends in system types, permit statuses, and geographic distribution of systems. We utilized data cleaning, transformation, and visualization techniques to address key analytical questions through descriptive, diagnostic, predictive, and prescriptive analysis.

![Data Analytical Question Formulation](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Analytical%20Question%20Formulation.png)

---

## **Data Analytical Question Formulation:**
To evaluate the operating permit dataset, the following types of analytical questions were formulated:

- **Descriptive:** “What types of mechanical systems (e.g., cooling towers, decorative water features) are most common in Vancouver?”
- **Diagnostic:** “Are there any geographic regions where permits are more frequently issued?”
- **Predictive:** “What is the trend for the issuance of permits over the next year?”
- **Prescriptive:** “How can permit renewal processes be improved to ensure timely compliance?”

---

## **Data Discovery:**
Key dataset variables include:

- **Operating Permit Number:** A unique identifier for each permit.
- **Permit Status:** Current status of the permit (e.g., Issued, Active).
- **Address:** Location where the system is installed.
- **Mechanical System Type:** The type of mechanical system covered by the permit (e.g., Cooling Tower, Decorative Water Feature).
- **System Report Date:** The date on which the system was last reported or inspected.
- **System Status:** The operational status of the mechanical system.

---

## **Methodology:**

### 1: Data Storage Design
- **Storage Method:** The dataset was stored in a structured Excel format.
- **S3 Bucket:** For scalable storage, the data stored in S3 buckets with folders for different reporting years.

![Data Storage](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Storage.png)

---

### 2: Dataset Preparation
**Tool Used:** Databrew for data manipulation and cleaning.

Key tasks:
- Removal of duplicate rows (multiple entries for the same permit).
- Convert categorical fields (e.g., permit status) to numerical values for analysis.

![Data Cleaning](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Cleaning.png)

---

### 3: Data Ingestion, Storage, Pipeline Design, Cleaning, Pipeline Implementation

AWS Glue ETL Job: Proptax-ETL-job
Imported 2023 and 2024 datasets from the raw S3 folder.
Adjusted schema, filtered out irrelevant data, and removed null values.
Applied join and aggregate functions to merge datasets, focusing on Zoning Classification.
AWS Glue's ETL process cleaned and transformed the data:

The final cleaned dataset was saved in CSV format in the curated S3 folder.

The ETL pipeline was executed with AWS Glue, and the processed data was stored in the curated S3 bucket folder.

![Data Pipeline Implementation](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Pipeline%20Implementation.png)

---

### 4: Data Structuring
**Tool Used:** AWS Athena.

- Data was structured into SQL-based tables using Athena for easy querying and further analysis.

![Data Structuring](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Structuring.png)

---

### 5: Data Analysis and Visualization

- **Key Visualizations:** A bar chart was created to display the number of "Issued" vs "Active" permits from AWS Athena in CSV format.

    ![Data Analysis](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Analysis.png)


---

### 6: Data Protection
- **Encryption Tool:** AWS KMS (Key Management Services)
- **Versioning and Replication:** To avoid accidental data deletion and multiple region accessbility, S3 Versioning and Cross-Region Replication is enabled.

![Data Protection](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Protection%201.png)

![Data Protection](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Protection%202.png)

---

### 7: Data Monitoring
**Monitoring Tools:** AWS CloudWatch and AWS CloudTrail

![Data Monitoring](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Monitoring.png)

![Data Monitoring](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Monitoring%202.png)

---

## **Tools and Techniques:**
AWS S3 Bucket
AWS Glue
AWS Glue DataBrew
AWS Athena
AWS EC2
AWS KMS (Key Management Services)
AWS CloudWatch
AWS CloudTrail


---

## **Deliverables:**
1. **Data Questions and Discovery**
2. **S3 Storage Structure**
3. **Cleaned Datasets for 2023 and 2024**
4. **ETL Pipeline Design and Implementation (AWS Glue)**
5. **Structured SQL Queries in AWS Athena**
6. **Visualizations (Charts in MS Excel)**
7. **Data Published on General and Web Servers (EC2 Instances)**
8. **Data Protection (AWS KMS encryption)**
9. **S3 Versioning for data history**
10. **Cross-Region Replication for data availability**

These deliverables provide a framework for analyzing operating permit data, ensuring data is securely processed, stored, and published while maintaining accuracy and availability.
