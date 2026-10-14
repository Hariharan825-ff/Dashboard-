# 📊 PhonePe Payment Insights Dashboard | Power BI

## 📌 Project Overview

The **PhonePe Payment Insights Dashboard** is an interactive data analytics project developed using Microsoft Power BI. It analyzes digital payment transactions to understand transaction volume, transaction value, user demographics, payment status, service categories, and weekday versus weekend usage.

The dashboard transforms raw transaction data into meaningful visual insights that help users explore digital payment trends and understand customer payment behaviour.

## 🎯 Project Objectives

* Analyze total transaction volume and transaction value.
* Track monthly transaction trends and growth.
* Understand user demographics across different age groups.
* Compare payment activity across service categories.
* Analyze successful, pending, and failed transactions.
* Compare weekday and weekend transaction patterns.
* Build an interactive dashboard for data-driven decision-making.

## 🛠️ Tools and Technologies

* **Microsoft Power BI Desktop** — Dashboard development and visualization.
* **Power Query** — Data cleaning and transformation.
* **DAX (Data Analysis Expressions)** — Calculations and KPI measures.
* **CSV / Excel** — Transaction dataset and data preparation.
* **Data Visualization** — Interactive charts, KPI cards, and slicers.

## ✨ Key Features

* **KPI Cards:** Displays total transactions, total transaction value, unique users, and successful transaction rate.
* **Monthly Transaction Analysis:** Visualizes monthly transaction count and value.
* **Age Group Analysis:** Compares Gen Z, Millennials, Gen X, and Boomers.
* **Service Category Analysis:** Examines Loans, Insurance, Money Transfer, and Recharge Bills.
* **Top 5 Users:** Identifies the five users with the highest transaction values.
* **Weekday vs. Weekend Analysis:** Compares transaction activity across different days.
* **Interactive Slicers:** Filters the dashboard by month and payment status.
* **Cross-filtering:** Allows users to explore relationships between different charts.
* **Custom Dashboard Design:** Uses a purple, PhonePe-inspired theme.

## 🧹 Data Cleaning and Preparation

The dataset was processed using Power Query to improve data quality and consistency.

The main steps included:

1. Importing the transaction dataset.
2. Keeping the raw data separate from the cleaned data.
3. Checking for null values, blank records, and duplicates.
4. Removing duplicate transactions.
5. Removing records with missing Transaction ID or Amount.
6. Standardizing payment status into Successful, Pending, and Failed.
7. Correcting column data types.
8. Extracting month and month number from transaction dates.
9. Creating a Weekday/Weekend classification.
10. Creating age segments for demographic analysis.
11. Validating data using column quality, column profile, and column distribution.
12. Loading the cleaned dataset into Power BI.

## 📐 DAX Measures

The following DAX measures were created for the dashboard.

### 1. Total Transactions

```dax
Total Transactions = COUNTROWS(Transactions)
```

### 2. Total Transaction Value

```dax
Total Value = SUM(Transactions[Amount])
```

### 3. Unique Users

```dax
Unique Users = DISTINCTCOUNT(Transactions[User ID])
```

### 4. Successful Transaction Rate

```dax
Successful Rate =
DIVIDE(
    CALCULATE(
        [Total Transactions],
        Transactions[Payment Status] = "Successful"
    ),
    [Total Transactions]
)
```

These measures respond dynamically to the dashboard's interactive filters.

## 📈 Dashboard Insights

Based on the project analysis:

* **Total Transactions:** Approximately 300K.
* **Total Transaction Value:** Approximately 3.47 billion in the dataset's reported amount units.
* **Transaction Growth:** Approximately 8.97%.
* **Transaction Value Growth:** Approximately 8.98%.
* **Monthly Trends:** Transaction activity peaks around July, with lower points around February and September.
* **Age Demographics:** Gen X and Millennials account for the largest shares of transactions.
* **Weekday Activity:** Approximately 215K transactions (71.6%) occur on weekdays.
* **Weekend Activity:** Approximately 85K transactions (28.4%) occur on weekends.
* **User Contribution:** The Top 5 Users chart highlights users contributing high transaction values.

*Note: These findings describe patterns in the analyzed dataset and do not establish causal relationships.*

## 🖥️ Dashboard Visualizations

| Visualization              | Chart Type        | Purpose                            |
| -------------------------- | ----------------- | ---------------------------------- |
| Transactions Over Time     | Area / Line Chart | Analyze monthly transaction trends |
| Age Segment Contribution   | Donut Chart       | Compare transactions by age group  |
| Service Transaction Value  | 100% Bar Chart    | Compare service categories         |
| Top 5 Users                | Column Chart      | Rank users by transaction value    |
| Weekday vs. Weekend Usage  | Donut Chart       | Compare transaction volumes        |
| Key Performance Indicators | KPI Cards         | Summarize important metrics        |

## 🚀 How to Use This Project

1. Clone or download this repository.
2. Download and install Microsoft Power BI Desktop.
3. Open the `.pbix` dashboard file included in the repository.
4. If prompted, update the source dataset path.
5. Refresh the data if the dataset is available.
6. Explore the dashboard using the month and payment status slicers.
7. Click chart segments to cross-filter other visualizations.

## 📂 Project Structure

```text
PhonePe-Payment-Insights-Dashboard/
│
├── README.md
├── PhonePe_Dashboard.pbix
├── dataset/
│   └── PhonePe_Transactions.csv
└── screenshots/
    └── dashboard.png
```

*The filenames above are suggested examples. Replace them with the actual filenames and folders in your repository.*

## 💡 What I Learned

Through this project, I gained practical experience in:

* Data cleaning and preprocessing.
* Data transformation using Power Query.
* Creating calculated measures using DAX.
* Building interactive dashboards in Power BI.
* Designing KPI cards and analytical visualizations.
* Analyzing transaction trends and customer demographics.
* Applying data visualization techniques to support data-driven decisions.

## 🔮 Future Improvements

* Add year-over-year and month-over-month comparisons.
* Include more detailed payment failure analysis.
* Develop additional user segmentation insights.
* Add geographical transaction analysis if location data is available.
* Improve drill-through reports and dashboard navigation.

## 👨‍💻 Author

**Hari Haran**

Third-Year B.Sc. Data Science

This project was developed as part of my data analytics and business intelligence learning journey.

## ⭐ Support

If you find this project useful, consider giving the repository a star on GitHub!

---

**Disclaimer:** This is an educational data analytics project. PhonePe is referenced to describe the payment platform being analyzed. This project is not an official PhonePe product or service.
