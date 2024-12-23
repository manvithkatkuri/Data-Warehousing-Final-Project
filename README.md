# Data Warehousing Final Project

## **Project Title**
**Financial Transactions Analytics Platform**

---

## **1. Executive Summary**
The **Financial Transactions Analytics Platform** is a robust data warehouse designed to integrate, analyze, and visualize financial transaction data. By consolidating transactional, user, and card information into a dimensional data model, this project enables actionable insights for credit risk assessment, fraud detection, and customer segmentation.

Key features include:
- A **subject-oriented, integrated, and non-volatile data warehouse**.
- Efficient **dimensional modeling** for fast analytical queries.
- Real-world business applications such as fraud detection, customer profiling, and revenue optimization.

---

## **2. Problem Statement**
**Current Challenges**:
- Disparate and scattered financial data sources impede decision-making.
- Difficulty in assessing credit risk, predicting fraud, and creating targeted marketing strategies.

**Proposed Solution**:
The project consolidates data into a unified data warehouse to enable:
1. **Fraud detection** by analyzing transactional anomalies.
2. **Customer segmentation** based on demographics and spending patterns.
3. **Credit risk profiling** using predictive modeling.

---

## **3. Objectives**
- Design a robust and scalable **data warehouse** using best practices in dimensional modeling.
- Implement an **ETL process** to extract, clean, and load financial datasets.
- Conduct **exploratory data analysis (EDA)** to uncover key insights.
- Build a **credit risk prediction model** for classifying users into risk categories.

---

## **4. Data Sources**
The project utilizes **three primary datasets**:
1. **Transactions Dataset**:
   - Includes transaction ID, amount, merchant, date, and associated card ID.
2. **Users Dataset**:
   - Contains demographic data such as age, income, and credit score.
3. **Cards Dataset**:
   - Details card attributes like card brand, type, credit limit, and expiry date.

**Source**: Kaggle’s Financial Transactions Fraud Dataset.

---

## **5. ETL (Extract, Transform, Load) Process**
### **Extraction**
- Data was sourced from Kaggle in CSV format.

### **Transformation**
- **Data Cleaning**:
  - Standardized date formats and currency values.
  - Removed duplicates and handled missing values.
- **Enrichment**:
  - Derived additional features like transaction month and risk categories.
  - Aggregated metrics for customer profiling.

### **Loading**
- Transformed data was loaded into an **SQL-based relational schema**, with a star schema designed for efficient querying.

---

## **6. Database Design**
### **Transactional Model (OLTP)**
**Tables**:
- **Transactions**: Contains real-time transactional data.
- **Users**: Stores customer demographic details.
- **Cards**: Includes information about issued cards.

### **Dimensional Model (OLAP)**
The dimensional model uses a **star schema**:
- **Fact Table**: `Transaction_Facts`, containing measures like transaction amount, risk score, and fraud flags.
- **Dimension Tables**:
  - `Users` Dimension: User demographics.
  - `Cards` Dimension: Card details.
  - `Merchants` Dimension: Merchant categories.

This schema supports fast aggregations and queries for analytics.

---

## **7. Exploratory Data Analysis (EDA)**
### **Key Insights**
- **Customer Analysis**:
  - Average customer age: **45.39 years**.
  - Highest recorded credit limit: **$151K**.
- **Transaction Trends**:
  - Total transactions: **250,116**.
  - Average transaction amount: **$44.05**.
  - Most popular merchant categories: **Food & Retail**.
- **Fraud Indicators**:
  - Higher fraud likelihood in transactions exceeding **$10K**.

---

## **8. Predictive Analytics: Credit Risk Assessment**
The credit risk model classifies customers into **four risk categories**:
1. **Low Risk**
2. **Moderate Risk**
3. **High Risk**
4. **Very High Risk**

### **Model Development**
- **Algorithm**: Logistic Regression.
- **Features**:
  - Income
  - Credit score
  - Transaction amount
  - Spending patterns
- **Evaluation Metrics**:
  - Accuracy: **98%**.
  - Cross-validation: **97%-98% consistency**.
  - F1-Score:
    - Low Risk: **0.98**.
    - Very High Risk: **0.94**.

---

## **9. Business Applications**
### **Fraud Detection**
- Identify and flag unusual transaction patterns using historical data.

### **Customer Segmentation**
- Group customers by demographics and spending behavior for targeted marketing.

### **Credit Risk Profiling**
- Mitigate risk by classifying customers into risk categories, enabling the creation of customized financial products.

---

## **10. Visualization and Reporting**
The project features **interactive dashboards** to provide actionable insights:
- **Customer Risk Dashboard**:
  - Displays the distribution of customers across risk categories.
- **Transaction Trends Dashboard**:
  - Visualizes daily, monthly, and yearly transaction volumes.
- **Merchant Analysis Dashboard**:
  - Highlights top-performing merchants and fraud-prone categories.

### **Tools Used**
- **Power BI**: For creating dynamic visualizations.
- **SQL**: For querying the data warehouse.

---

## **11. Challenges and Learnings**
### Challenges:
- Handling large datasets with inconsistent formats.
- Designing a schema that balances storage efficiency and query performance.

### Learnings:
- Effective data cleaning improves downstream model accuracy.
- Dimensional modeling enhances query speed for analytics use cases.

---

## **12. Conclusion**
The project successfully delivers:
- A scalable data warehouse for financial analytics.
- Actionable insights for fraud detection, risk profiling, and customer segmentation.
- A predictive model that helps financial institutions mitigate risks.

---

## **13. References**
1. W.H. Inmon - *Building the Data Warehouse.*
2. R. Kimball - *The Data Warehouse Toolkit.*
3. Oracle SQL Documentation.
4. Kaggle - *Transactions Fraud Dataset.*

---

## **14. Future Scope**
- Incorporate real-time streaming data for fraud detection.
- Explore advanced models like XGBoost or Neural Networks for credit risk analysis.
- Extend the system to include additional financial datasets for more comprehensive insights.
