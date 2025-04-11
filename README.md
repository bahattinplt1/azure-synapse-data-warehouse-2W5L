# 🚀 Azure Synapse Analytics – Data Warehouse Project

This project showcases a practical data engineering workflow using **Azure Synapse Analytics**, focusing on building and loading a **relational data warehouse** with CSV-based product and customer data.

The work follows the exercises from the **DP-203: Data Engineering on Microsoft Azure** course, including SQL pool provisioning, data ingestion, staging, transformation, and slowly changing dimension (SCD) logic.

---

## 🧱 Key Steps Performed

### 1. 🔧 Provisioned Synapse SQL Pool  
Created a dedicated SQL pool and linked it with a Data Lake Storage Gen2 account using an ARM template and PowerShell.

### 2. 📥 Loaded CSV Data into Staging Tables  
Used `COPY INTO` statements to load `Product.csv` and `Customer.csv` files into `StageProduct` and `StageCustomer`.

### 3. 📊 Created Dimension Tables with CTAS  
Used a `CREATE TABLE AS SELECT (CTAS)` to generate `DimProduct`, with `ROW_NUMBER()` used to create surrogate keys.

### 4. 🔁 Implemented Slowly Changing Dimensions  
Inserted new customers, applied Type 1 updates for name/email/phone changes, and Type 2 inserts for address changes in `DimCustomer`.

### 5. ⚙️ Optimized Tables  
Rebuilt indexes and created column statistics for query performance improvement.

### 6. 🧪 Validated Errors  
Reviewed rejected rows from `Customer.csv` — included error and row log files.

---

## 📄 Included Files

- `Customer.csv`
- `Product.csv`
- `QIDxxx_1_1.Row.Txt`
- `QIDxxx_1_1.Error.Txt`
- (Screenshots of Synapse Studio steps)

---

## 📌 Technologies Used

- Microsoft Azure Synapse Analytics
- Azure Data Lake Storage Gen2
- T-SQL (Transact-SQL)
- GitHub

---

## ✅ Project Status

- ✔️ All tasks completed successfully
- 🗑️ Resources deleted to avoid Azure billing
- 📁 Data and logs archived in this repository
