# Task 03 - HR Analytics Dashboard using Power BI

## Objective

The objective of this project is to build an interactive HR Analytics Dashboard using Microsoft Power BI to analyze employee attrition. The dashboard helps identify employee turnover trends based on department, job role, gender, and age group, enabling better HR decision-making.

---

## Tools Used

- Microsoft Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)

---

## Dataset

Dataset Name: IBM HR Analytics Employee Attrition & Performance Dataset

The dataset contains information such as:

- Employee Number
- Age
- Gender
- Department
- Job Role
- Monthly Income
- Attrition
- Education
- Job Satisfaction
- Years at Company
- Business Travel
- Marital Status
- Overtime

---

## Data Preparation

The following preprocessing steps were performed before creating the dashboard:

- Imported the dataset into Power BI.
- Verified data types.
- Checked for missing values.
- Checked for duplicate records.
- Created a calculated column using DAX.
- Prepared the dataset for visualization.

---

## Dashboard Features

### KPI Cards

- Total Employees
- Average Age
- Average Monthly Income

### Visualizations

- Employee Attrition Overview
- Attrition by Department
- Attrition by Job Role

### Interactive Filters

- Department
- Gender
- Age Group

---

## DAX Formula

```DAX
Age Group =
SWITCH(
    TRUE(),
    'WA_Fn-UseC_-HR-Employee-Attrition'[Age] <= 30, "18-30",
    'WA_Fn-UseC_-HR-Employee-Attrition'[Age] <= 40, "31-40",
    'WA_Fn-UseC_-HR-Employee-Attrition'[Age] <= 50, "41-50",
    "51+"
)
```

---

## Key Insights

- The organization consists of 1470 employees.
- Research and Development has the highest number of employees.
- Most employees belong to the 31–40 years age group.
- Certain job roles experience higher employee attrition.
- Interactive filters allow users to analyze employee attrition by department, gender, and age group.

---

## Project Structure

```
Task-03-HR-Analytics-Dashboard/
│
├── HR_Analytics_Dashboard.pbix
├── Dashboard.png
├── README.md
├── Task03_Report.docx
└── WA_Fn-UseC_-HR-Employee-Attrition.csv
```

---

## Dashboard Preview

Add the dashboard screenshot in this folder and use the following code:

```markdown
![Dashboard](Dashboard.png)
```

---

## Learning Outcomes

This project helped me learn:

- Data Import in Power BI
- Data Cleaning using Power Query
- Creating KPI Cards
- Building Interactive Dashboards
- Creating Calculated Columns using DAX
- Dashboard Formatting
- Business Intelligence Reporting
- Interactive Data Visualization

---

## Conclusion

This project demonstrates how Microsoft Power BI can transform raw HR employee data into meaningful business insights. The dashboard provides interactive visualizations and filters that help HR professionals analyze employee attrition effectively. It also strengthened my practical knowledge of Power BI, DAX, and Business Intelligence concepts.

---

## Author

Ajitdada Gajanan Gharge

Data Analyst Intern

SkillCraft Technology
