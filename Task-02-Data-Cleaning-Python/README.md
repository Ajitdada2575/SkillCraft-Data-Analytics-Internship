# Task 02 – Data Cleaning and Preparation using Python (Pandas)

##  Internship
**Company:** SkillCraft Technology

**Role:** Data Analyst Intern

**Task:** Task 02 – Data Cleaning and Preparation

---

# Project Overview

Data cleaning is one of the most important steps in the data analysis process. Raw datasets often contain missing values, duplicate records, inconsistent data types, and formatting issues that can affect analysis and decision-making.

In this project, I performed data cleaning and preparation using **Python** and the **Pandas** library in **Google Colab**. The objective was to prepare the dataset for future analysis by handling missing values, checking duplicate records, verifying data types, and exporting a clean dataset.

---

#  Objective

The main objectives of this task were:

- Import the dataset into Python
- Explore the dataset structure
- Identify missing values
- Remove missing values
- Check duplicate records
- Convert data types where necessary
- Export the cleaned dataset as a CSV file

---

#  Tools & Technologies

- Python 3
- Pandas
- Google Colab
- Microsoft Excel (Dataset Source)

---

#  Dataset

The dataset used in this project contains sales transaction records with information such as:

- Order ID
- Order Date
- Ship Date
- Customer Name
- Segment
- Country
- City
- State
- Region
- Category
- Sub-Category
- Product Name
- Sales

---

#  Steps Performed

## Step 1: Import Pandas Library

Imported the Pandas library for data manipulation.

```python
import pandas as pd
```

---

## Step 2: Load Dataset

Loaded the Excel dataset into a Pandas DataFrame.

```python
df = pd.read_excel('train.csv.xlsx', sheet_name='train')
```

---

## Step 3: Display First Five Records

Viewed the first five rows to understand the dataset structure.

```python
df.head()
```

---

## Step 4: Dataset Information

Checked the dataset information including:

- Number of rows
- Number of columns
- Data types
- Non-null values

```python
df.info()
```

### Result

- Total Rows: **9800**
- Total Columns: **18**

---

## Step 5: Identify Missing Values

Checked for missing values in every column.

```python
df.isnull().sum()
```

### Result

Only one column contained missing values:

| Column | Missing Values |
|----------|---------------|
| Postal Code | 11 |

---

## Step 6: Handle Missing Values

Removed rows containing missing values.

```python
df = df.dropna()
```

Verified the dataset again.

```python
df.isnull().sum()
```

### Result

All missing values were successfully removed.

---

## Step 7: Check Duplicate Records

Checked for duplicate rows.

```python
df.duplicated().sum()
```

### Result

```
0
```

No duplicate records were found.

---

## Step 8: Verify Data Types

Verified date columns.

```python
df['Order Date'] = pd.to_datetime(df['Order Date'])
df['Ship Date'] = pd.to_datetime(df['Ship Date'])
```

Both columns were successfully stored as **datetime** data type.

---

## Step 9: Export Clean Dataset

Saved the cleaned dataset.

```python
df.to_csv('cleaned_sales_data.csv', index=False)
```

---

#  Dataset Summary

| Description | Value |
|------------|------:|
| Original Rows | 9800 |
| Original Columns | 18 |
| Missing Values | 11 |
| Duplicate Rows | 0 |
| Cleaned Dataset | Yes |

---

#  Key Observations

- The dataset was mostly clean.
- Only the **Postal Code** column contained missing values.
- No duplicate records were found.
- Date columns were already stored correctly and verified using Pandas.
- The cleaned dataset is now ready for analysis and visualization.

---

# Skills Learned

During this project, I learned:

- Reading Excel files using Pandas
- Exploring datasets using `head()` and `info()`
- Identifying missing values
- Removing missing values
- Checking duplicate records
- Working with datetime columns
- Exporting cleaned datasets
- Data preprocessing techniques

---

# Project Files

```
Task_02_Data_Cleaning.ipynb
cleaned_sales_data.csv
README.md
```

---

# How to Run

1. Open Google Colab or Jupyter Notebook.
2. Upload the dataset (`train.csv.xlsx`).
3. Run all notebook cells sequentially.
4. A cleaned dataset named **cleaned_sales_data.csv** will be generated.

---

# Conclusion

This project demonstrates the complete data cleaning workflow using Python and Pandas. The dataset was explored, cleaned, validated, and exported successfully. Missing values were removed, duplicate records were checked, data types were verified, and the cleaned dataset was prepared for further analysis.

This task strengthened my understanding of data preprocessing techniques, which are essential for data analysis and machine learning projects.

---

## Author

**Ajitdada Gajanan Gharge**

**Data Analyst Intern**

**SkillCraft Technology**
