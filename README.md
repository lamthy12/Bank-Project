# 💰 Bank Marketing Data Cleaning | MySQL

## Project Overview

This project primarily focuses on evaluating data quality, categorizing customer subscription information from a Portuguese bank's direct marketing campaign 💵 by using MySQL. By analyzing data 🖥️, cleaning data 🔋 and standardizing subscription outcomes 🔥 are to improve the accuracy of subscription information, and prepare a structured data for further banking and customer employees

---

## 1. Project Problems

Before analyzing the effectiveness of a marketing campaign, it is important to understand whether the underlying customer data is reliable and consistent.

📌 This project focuses on three main questions:

- Are there missing values, duplicate records, or unusual data values?
- How can customer subscription outcomes be presented more clearly?
- How can customer age information be organized for future analysis?

---

## 2. Dataset

📎**Source:** [UCI Machine Learning Repository – Bank Marketing]
(https://archive.ics.uci.edu/dataset/222/bank+marketing)

**File:** `bank-full.csv`

| Dataset Information | Details |
|---|---|
| Industry | Banking and Financial Services |
| Records | 45,211 |
| Original Columns | 17 |
| Database | MySQL |
| Target Variable | `y` (Term Deposit Subscription) |

- Variables Table in BankMarketing_Dataset includes:

Age
Job 
Marital Status
Education
Credit Default
Balance
Housing Loan 
Personal Loan
Contact
Day_of_week
Month
Duration
Campaign
Pdays
Previous 
Poutcome
(y) Term Deposit Subscription

---

## 3. Tools & SQL Skills 📚📊

**Tools:** MySQL Workbench, Tableau, Visual Studio Code

- Used `COUNT()`, `DISTINCT`, `MIN()` and `MAX()`
- Applied `CASE WHEN` to categorize and organize data
- Used `ALTER TABLE` and `UPDATE` for data transformation
- Used `GROUP BY` and aggregate functions to review and
- Created line and bar charts in Tableau to compare customer data and subscription trends.

---

## 4. Data Preparation Process

### a. Data Quality Estimation:

- Checked missing values, duplicate data and `unknown` categories.
- Reviewed unusual values in age, account balance, call duration, and campaign contacts.
- Kept the negative balance and other rare values because they could either error or not, needing more exploration.

### b. Subscription Status Standardization

- Created `bank_marketing_clean` to keep the original dataset.
- Set `subscription_status`  from yes/no into subscribed/not subscribed to identify the amount easier.

### c. Customer Age Segmentation

- Used SQL `CASE WHEN` to create 5 ages groups such as: 18–29, 30–39, 40–49, 50–59, and 60+.

### d. Final Data Validation

- Confirmed all 45,211 customer records were retained.
- Verified successfully there are no NULL values in columns: subscription_status and age_group. 

---

## 5. Key Findings
<img width="2048" height="1450" alt="1f65f657-a788-4430-95c0-11a8eb7971e4" src="https://github.com/user-attachments/assets/c7c83bd5-a6a0-4c13-b849-45ba7d8caadc" />

**Subscription outcomes**

| Subscription Status | Customers | Share |
|---|---:|---:|
| Subscribed | 5,289 | 11.7% |
| Not Subscribed | 39,922 | 88.3% |
| **Total** | **45,211** | **100%** |

Approximately 11.7% of the customer records show a successful term deposit subscription.

**Customer age distribution**

| Age Group | Customers |
|---|---:|
| 18–29 | 5,273 |
| 30–39 | 18,089 |
| 40–49 | 11,655 |
| 50–59 | 8,410 |
| 60+ | 1,784 |

Customers aged 30–39 represent the largest age group, accounting for approximately 40% of the dataset.

These findings describe the overall dataset and do not establish which customer characteristics caused subscription outcomes.

---

## Project Files

- `bank_marketing_cleaning.sql` 
- `bank-full.csv` 
- `tableau.pdf` 

---

## What I learned 📝
Throughout this project, I am able to:
- 🖌️ Write SQL queries to explore and better understand a real-world banking dataset
- 📁 Get familiar with GROUP BY, ORDER BY and COUNT() and aggregate functions to summarize customer information 
- 👀 Identify missing values, duplicate records and unusual data values
- 📈 Prepare a professional dashboard

---

## Closing Thoughts & Conclusion 🔐

This project has reflected my skills for writing complex SQL queries, managing database, providing a clear vision of business insights and at first, I did not know much about it. I learned by asking difficult questions of my dataset and eventually managed to write queries by myself. Also, building an interactive dashboard from Tableau is really helpful to have a more comprehensive perspective on the project. 

Overall, the Bank Marketing project helps me have a better understanding of how many customers subscribed for term deposits from a bank marketing campaign. By checking and cleaning data from various groups of customers, including age ranges, job types, subscription statuses and personal loans, it allows users to locate data patterns easily. To wrap up, this analysis could assist a bank to track and analyze which type of groups may have potential subscribers for their term deposits and improve future marketing campaigns. 
