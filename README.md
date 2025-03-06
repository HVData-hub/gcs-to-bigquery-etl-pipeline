# End-to-End Data Pipeline: Data Cleaning, Storage, and Visualization with GCS, BigQuery & Power BI

## Overview  
This project builds an **end-to-end data pipeline** that takes raw data, cleans it, stores it in the cloud, processes it using BigQuery, and visualizes insights with Power BI. The pipeline is designed to handle data efficiently using **Python, Google Cloud Storage (GCS), BigQuery, and Power BI**, ensuring scalability, security, and ease of analysis.

## Architecture Diagram  
The following diagram illustrates the entire pipeline from **data ingestion to visualization**:  

![Data Pipeline Diagram](/Images/ProjectFlow.jpeg)  

## Workflow Steps  

### **1. Data Loading (Jupyter Notebook)**
- The raw dataset is first **loaded into Jupyter Notebook** for initial exploration and analysis.  
- Python’s **pandas library** is used to read, manipulate, and process structured data efficiently.  
- The data is stored in a CSV format, ensuring compatibility with various tools for further processing.  

### **2. Data Cleaning**  
- The dataset undergoes **cleaning and transformation** to handle missing values, remove duplicates, and standardize formats.  
- Data cleaning is performed in **Jupyter Notebook**, leveraging Python’s pandas library for structured manipulation.  
- The cleaned dataset is then **saved and exported** for further processing in cloud storage.  

### **3. Google Cloud Authentication**  
- To interact with **Google Cloud Storage (GCS) and BigQuery**, authentication is required via **Google Cloud SDK**.  
- A **service account** is created to provide secure, role-based access to cloud resources.  
- The authentication is done using **Google Cloud CLI (`gcloud auth login`)** and necessary Python libraries.  

### **4. Uploading Data to Google Cloud Storage (GCS)**  
- A **Google Cloud Storage (GCS) bucket** is created to store the cleaned dataset.  
- The processed dataset is **uploaded from the local machine to GCS**, ensuring a secure and scalable data repository.  
- Cloud storage helps in **efficiently managing large datasets** before they are loaded into BigQuery.  

### **5. Creating a Service Account for BigQuery**  
- A **service account** is created in **Google Cloud IAM (Identity and Access Management)** for managing permissions.  
- Necessary **IAM roles** are assigned to the service account, allowing it to interact with BigQuery and GCS.  
- A **JSON key** file is generated for authentication when accessing BigQuery from external tools like Power BI.  

### **6. Assigning IAM Roles and Permissions**  
- Proper **permissions** are assigned to ensure secure access to **BigQuery and Google Cloud Storage**.  
- The **service account** is granted necessary roles such as **BigQuery Admin** and **Storage Admin**.  
- IAM policies ensure that **only authorized users and tools** can access the cloud resources.  

### **7. Loading Data into BigQuery**  
- The dataset is **imported from GCS to BigQuery**, enabling fast querying and analysis.  
- **Google Cloud SDK CLI (`bq load` command)** is used to transfer data from GCS to BigQuery tables.  
- This step enables efficient **data warehousing and analysis** using **SQL-based querying**.  

### **8. Running SQL Queries in BigQuery**  
- SQL queries are used to **validate and process** the imported data inside BigQuery.  
- Data is checked for accuracy and completeness using **SELECT queries** and basic aggregations.  
- This step ensures that the dataset is **ready for visualization and reporting**.  

### **9. Assigning BigQuery Permissions for Power BI**  
- The **service account** is configured to allow Power BI to fetch data from BigQuery securely.  
- IAM roles and permissions are updated to **grant access to Power BI** using the JSON key file.  
- This ensures seamless data transfer between **BigQuery and Power BI**.  

### **10. Linking BigQuery to Power BI**  
- Power BI’s **"Get Data"** option is used to establish a connection with BigQuery.  
- Authentication is done using the **service account JSON key**, allowing secure data retrieval.  
- This step allows Power BI to directly **query and fetch data from BigQuery** for visualization.  

### **11. Creating Data Visualizations in Power BI**  
- Power BI is used to create **interactive dashboards and reports** for data analysis.  
- Various visualization techniques, including **charts, graphs, and tables**, are used to represent insights.  
- The final output is a **business-ready dashboard** that helps in decision-making based on the processed data.  

## Technologies Used  
- **Python (Jupyter Notebook)**
- **Google Cloud Storage (GCS)**
- **Google BigQuery**
- **Google Cloud IAM (Identity & Access Management)**
- **Google Cloud SDK (gcloud CLI)**
- **Power BI for Visualization**  

References:

# **Key References for GCP & Python Integration**

1. **Google Cloud Storage (GCS) Overview & Python Integration:**
   - [Google Cloud Storage Docs](https://cloud.google.com/storage/docs)  
   - [Python SDK for GCS](https://googleapis.dev/python/storage/latest/index.html)

2. **Google BigQuery Overview & Python Integration:**
   - [Google BigQuery Docs](https://cloud.google.com/bigquery/docs)  
   - [Python SDK for BigQuery](https://googleapis.dev/python/bigquery/latest/index.html)  
   - [Loading Data into BigQuery with Python](https://cloud.google.com/bigquery/docs/loading-data-cloud-storage-python)

3. **Using Jupyter Notebook with Python:**
   - [Jupyter Notebook Documentation](https://jupyter.org/documentation)  
   - [Using Jupyter with Python](https://realpython.com/jupyter-notebook-introduction/)
