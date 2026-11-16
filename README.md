# Home Credit Default Risk Prediction 🏦📊

## 1. Project Overview
This project aims to predict the probability of a client defaulting on a loan based on their demographic data, external credit history, and previous applications. By effectively identifying high-risk applicants, financial institutions can minimize default losses while safely approving creditworthy clients.

## 2. Tech Stack & Tools
* **Language:** Python
* **Libraries:** Pandas, Scikit-learn, Seaborn, Matplotlib
* **Data Processing:** Apache Parquet, Missing Value Imputation, Outlier Handling
* **Modeling:** Random Forest Classifier, Cost-Sensitive Learning

## 3. Key Technical Implementations
* **Data Ingestion:** Processed and merged 3 large-scale relational datasets (over 3.69 million records), converting raw CSVs to Parquet format to optimize I/O performance and memory efficiency.
* **EDA & Cleaning:** Eliminated 41 high-missingness features (>50%) and rectified extreme system-generated employment anomalies (`DAYS_EMPLOYED = 365243`) affecting 18% of the applicant records.
* **Feature Engineering:** Extracted 11 domain-specific historical credit features via aggregations (e.g., maximum historical debt, past loan refusals) resulting in a robust 90-feature dataset.
* **Imbalanced Data Handling:** Mitigated a severe 8.07% minority class imbalance using stratified sampling (`stratify=y`) and balanced class weighting (`class_weight='balanced'`).

## 4. Business Impact & Results
The Random Forest model achieved the following performance on a 61,503-record test set:
* **ROC-AUC Score:** 0.7404
* **Overall Accuracy:** 78%
* **Safe Loan Precision:** 95% (Highly reliable approvals for creditworthy applicants)
* **Default Recall:** 53% (Successfully flagged more than half of the actual defaulters, minimizing capital loss).

Key drivers of default risk identified via Feature Importance include normalized external credit scores (`EXT_SOURCE_2`, `EXT_SOURCE_3`), client age, and historical loan rejection counts.

## 5. Contact
* **Author:** Đào Đức Nam
* **Email:** daonam2k5@gmail.com
* **LinkedIn:** [Insert Your LinkedIn Link Here]
