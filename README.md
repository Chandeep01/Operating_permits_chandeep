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
- **S3 Bucket (optional if used):** For scalable storage, the data could be stored in S3 buckets with folders for different reporting years.

![Data Storage](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Storage.png)

---

### 2: Dataset Preparation
**Tool Used:** Databrew for data manipulation and cleaning.

Key tasks:
- Removal of duplicate rows (multiple entries for the same permit).
- Conversion of categorical fields (e.g., permit status) to numerical values for analysis.
- Standardization of addresses and date formats for easier aggregation and analysis.

![Data Cleaning](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Cleaning.png)

---

### 3: Data Ingestion, Storage, Pipeline Design, Cleaning, Pipeline Implementation
- **Pipeline Design:** We designed a pipeline to import the Excel file, clean the data, and structure it for analysis.
- **Data Cleaning:** The dataset was cleaned to remove duplicates, standardize entries, and ensure consistent formatting.
- **Schema Changes:** Address and date columns were formatted for consistency.
- **Final Data Storage:** The cleaned dataset was saved in a structured format for easy querying and visualization.

![Data Pipeline Implementation](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Pipeline%20Implementation.png)

---

### 4: Data Structuring
**Tool Used:** SQL-based table queries for data structuring.

- Data was structured into SQL-based tables using Athena for easy querying and further analysis.

![Data Structuring](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Structuring.png)

---

### 5: Data Analysis and Visualization

- **Key Visualizations:** A bar chart was created to display the number of "Issued" vs "Active" permits.

    ![Data Analysis](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Analysis.png)


---

### 6: Data Protection
- **Encryption Tool:** AWS KMS (if used) can be implemented to ensure the dataset is encrypted and only accessible to authorized users.
- **Versioning and Replication:** To avoid data loss and ensure availability, S3 versioning and cross-region replication can be employed.

![Data Protection](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Protection%201.png)

![Data Protection](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Protection%202.png)

---

### 7: Data Monitoring
**Monitoring Tools:** AWS CloudWatch (if used) to enable real-time monitoring of the dataset and track any changes in system status or permits.

![Data Monitoring](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Monitoring.png)

![Data Monitoring](https://github.com/Chandeep01/Operating_permits_chandeep/blob/main/Data%20Monitoring%202.png)

---

## **Tools and Techniques:**
- **Pandas** - For data cleaning and structuring.
- **Matplotlib/Seaborn** - For data visualization.
- **SQL** - For querying structured data.
- **Excel** - For initial data handling (and visualization if applicable).
- **AWS S3, EC2, KMS (Optional)** - If using cloud-based storage, processing, and security services.

---

## **Deliverables:**
1. **Data Analytical Questions and Discovery**
2. **Data Storage Structure**
3. **Cleaned Dataset**
4. **Data Visualization (e.g., charts in Matplotlib/Seaborn)**
5. **Data Published on Web Server (if applicable)**
6. **Data Encryption for security (if applicable)**
7. **Data Monitoring and Alerts (if applicable)**

These deliverables provide a framework for analyzing operating permit data, ensuring data is securely processed, stored, and published while maintaining accuracy and availability.
