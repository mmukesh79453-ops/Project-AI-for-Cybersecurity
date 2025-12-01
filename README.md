Credit Fraud Dataset – Cleaning and Exploration

This project focuses on cleaning and performing basic exploratory analysis on a credit card transaction dataset. The goal is to prepare the data for fraud detection tasks by ensuring that the dataset is consistent, clean, and ready for modeling.


---

📌 Dataset Overview

The dataset contains 5657 transactions with the following columns:

TransactionID – Unique ID for each transaction

TransactionDate – Time of the transaction (HH:MM:SS)

Amount – Transaction amount

MerchantID – Merchant identifier

TransactionType – purchase or refund

Location – City of transaction

IsFraud – Fraud label (1 = fraud, 0 = not fraud)



---

🧹 Data Cleaning Steps

The following cleaning steps were performed:

1. Loaded the Excel file

Used pd.read_excel() to correctly load .xlsx data.

2. Checked data structure

df.head()

df.tail()

df.describe()

df.info()


3. Checked for missing values

df.isnull().sum()

✔ No missing values.

4. Checked and removed duplicates

df.duplicated().sum()
df = df.drop_duplicates()

✔ No duplicate rows found.

5. Column Cleanup

Stripped column names to avoid accidental whitespace issues:

df.columns = df.columns.str.strip()


---

📊 Exploratory Data Analysis

1. Transaction Type Distribution

Analysed how many transactions are purchase vs refund.

2. Amount Statistics

Looked at min, max, average, and distribution of transaction amounts.

3. Time Trend Plot

Converted transaction time into seconds and plotted:

Amount vs Time of Day


4. Amount Distribution

Histogram of transaction amounts:

plt.hist(df['Amount'], bins=30)


---

🛠 Tools & Libraries Used

Python

pandas

matplotlib

Google Colab



---

🎯 Project Goal

The primary purpose of this project is to prepare the dataset for fraud-detection modeling by ensuring that the data is:

clean

consistent

free from errors

ready for ML preprocessing


✔ Future Improvements

Feature engineering (hour, day, location encoding)

Fraud prediction model (Logistic Regression, Random Forest, XGBoost)

Handling class imbalance (SMOTE, undersampling)

More visualizations
