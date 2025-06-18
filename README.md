# PowerBI-Healthcare-Dashboard-and-report

# 🧠 US Mental Healthcare Analysis Dashboard – Power BI Project

This Power BI project provides a comprehensive analysis of mental healthcare facilities in the United States using a dataset of 1,500 records. It covers key metrics such as facility type, patient satisfaction, staffing levels, Covid-19 compliance, and service quality.

---

## 📌 Project Objectives

- Clean and transform messy healthcare facility data
- Analyze the distribution and performance of mental health centers
- Visualize key KPIs such as accreditation percentage, patient satisfaction, and staff-to-patient ratio
- Provide actionable insights to improve mental healthcare delivery

---

## 📊 Dashboard Features

### ✅ Key Metrics
- **Total Facilities**
- **Average Patient Satisfaction Rating**
- **Total Patients Served Annually**
- **Average Cost per Visit**
- **Accredited Facilities Percentage (Gauge)**
- **Covid-19 Compliance Rate**

### 📍 Regional Insights
- State-wise facility distribution
- Comparison of satisfaction ratings by state and type of facility

### ⚙️ Operational Insights
- Staff-to-patient ratio
- Emergency services availability
- 24/7 operational status
- Primary mental health issues treated (e.g., anxiety, depression, addiction)

### 💡 Insights Cards & Recommendations
- Accreditation gaps
- Understaffed facility identification
- Cost vs. satisfaction analysis
- Covid-19 safety compliance vs. public trust

---

## 🧹 Data Cleaning & Transformation

Performed using **Power Query Editor**:
- Removed nulls, fixed typos, and unified category formats
- Filled missing values (e.g., satisfaction rating filled with average)
- Converted cost fields to numeric
- Created DAX measures for KPIs and ratios
- Added calculated columns for classification

---

## 📁 Files Included

| File Name | Description |
|-----------|-------------|
| `mental_health_us.csv` | Raw dataset (1500 rows × 26 columns) |
| `US_Mental_Health.pbix` | Power BI dashboard report file |
| `A_Power_BI_dashboard_visualizing_US_Mental_Health.png` | Screenshot of dashboard |
| `README.md` | This documentation file |

---

## 📌 Technologies Used

- **Power BI Desktop**
- Power Query (ETL)
- DAX for custom measures
- Data modeling (relationships, lookups)

---

## 📈 Sample Measures (DAX)

```dax
Accredited Percentage = 
DIVIDE(
    CALCULATE(COUNTROWS(Mental_Health), Mental_Health[Accredited] = "Yes"),
    COUNTROWS(Mental_Health)
) * 100

Patients per Staff = 
DIVIDE(SUM(Mental_Health[Number_of_Patients_Annually]), SUM(Mental_Health[Number_of_Staff]), 0)
