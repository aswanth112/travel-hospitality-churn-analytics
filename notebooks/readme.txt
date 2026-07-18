# Travel & Hospitality — Customer Churn Analysis
### Data Analytics Internship Project | Infotact Solutions | Batch 17.1

---

## Project Overview

This project analyzes real-world hotel booking data to understand and 
predict customer cancellations (churn). Using exploratory data analysis 
and machine learning, we identify key drivers of cancellations and 
provide actionable business recommendations to help hotels reduce 
revenue loss.

**Intern:** Aswanth Chandran  
**Organization:** Infotact Solutions  
**Duration:** May 2026 – July 2026  
**Domain:** Travel & Hospitality  

---

## Dataset

- **Source:** Hotel Booking Demand Dataset (Kaggle)
- **Raw Records:** 119,390 rows × 32 columns
- **Clean Records:** 87,396 rows × 33 columns
- **Date Range:** 2015 – 2017
- **Hotel Types:** City Hotel, Resort Hotel

---

## Project Structure
travel-hospitality-churn-analytics/
├── data/
│   ├── raw/                          ← raw dataset (gitignored)
│   └── processed/
│       └── hotel_bookings_cleaned.csv ← cleaned dataset
├── notebooks/
│   └── week1_data_cleaning.ipynb     ← complete analysis notebook
├── dashboard/
│   ├── hotel_churn_dashboard.pbix    ← Power BI dashboard
│   ├── page1_overview.png            ← Page 1 screenshot
│   ├── page2_cancellation.png        ← Page 2 screenshot
│   └── page3_pricing.png             ← Page 3 screenshot
├── reports/                          ← final project report
├── .gitignore
└── README.md

---

## 📊 Dataset Summary
| Metric | Value |
|--------|-------|
| Raw Records | 119,390 rows |
| Clean Records | 87,396 rows |
| Duplicates Removed | 31,994 |
| Total Features | 32 columns |
| Cancellation Rate | 37% |
| Date Range | 2015 – 2017 |
| Hotel Types | City Hotel, Resort Hotel |

---

## 🗓️ Week by Week Progress

### ✅ Week 1 — Data Cleaning & Feature Engineering
- Downloaded Hotel Booking Demand dataset from Kaggle (119,390 records)
- Removed 31,994 duplicate rows
- Fixed missing values — agent filled with 0, country with Unknown, children with 0
- Fixed negative ADR values and capped extreme outliers above 3500
- Converted month names to numerical format (January = 1, December = 12)
- Created unified arrival_date column by combining year, month and day
- Saved cleaned dataset of 87,396 rows to processed folder
- Initialized GitHub repository with proper folder structure and gitignore

### ✅ Week 2 — Exploratory Data Analysis
- Calculated overall cancellation rate — 37% of all bookings
- Analysed cancellation by hotel type — City Hotel 42% vs Resort Hotel 28%
- Analysed cancellation by market segment — Online TA has highest volume
- Analysed cancellation by deposit type — No Deposit has highest rate
- Analysed cancellation by customer type — Transient customers cancel most
- Lead time analysis — cancelled bookings average 145 days vs 72 days
- Booking type analysis — Early Planners cancel more than Last Minute bookers
- Generated correlation heatmap across all 20 numerical features

### ✅ Week 3 — Machine Learning Model Building
- Selected 8 basic features for baseline models
- Expanded to 14 features including encoded categorical variables
- Built and compared 6 machine learning models
- Applied SMOTE to handle class imbalance
- Improved cancellation Recall from 48% to 66%
- Plotted ROC-AUC curve and Feature Importance chart

#### 🏆 Model Comparison Results
| Model | Features | Accuracy |
|-------|----------|----------|
| Logistic Regression | 8 | 74.00% |
| Decision Tree | 8 | 70.49% |
| Random Forest | 8 | 75.15% |
| Decision Tree | 14 | 74.47% |
| Random Forest | 14 | 78.89% |
| Gradient Boosting | 14 | 80.09% |
| **XGBoost ✅ Best** | **14** | **80.49%** |
| XGBoost + SMOTE | 14 | 75.81% (Recall 66%) |

### ✅ Week 4 — Dashboard & Documentation
- Built 3-page interactive Power BI dashboard
- Page 1 — Executive Overview with KPI cards and hotel comparison
- Page 2 — Cancellation Analysis with market segment and deposit type breakdown
- Page 3 — Pricing Trends and Lead Time Analysis with seasonal ADR patterns
- Added hotel type and year slicers for interactive filtering
- Wrote final business recommendations based on analysis findings
- Completed project report and README documentation

---

## 🔍 Key Findings
- **37%** overall cancellation rate — 1 in 3 bookings never arrives
- **City Hotels** cancel 42% vs **Resort Hotels** only 28%
- Cancelled customers book **2x further in advance** — 145 days vs 72 days
- **No Deposit** bookings have the highest cancellation tendency
- **Online TA** segment drives the most cancellation volume
- **Early Planners** (90+ days lead time) cancel more than Last Minute bookers
- **lead_time** and **deposit_type** are the strongest cancellation predictors

---

## 💡 Business Recommendations
1. Introduce mandatory deposit policies for online bookings
2. Send retention campaigns to customers booking 90+ days in advance
3. City Hotels should revise and strengthen cancellation policies
4. Offer direct booking discounts to reduce OTA dependency
5. Deploy XGBoost model to automatically flag high-risk bookings at reservation

---

## 🛠️ Technology Stack
| Component | Technology |
|-----------|------------|
| Data Processing | Python, Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn, XGBoost |
| Class Imbalance | SMOTE (imbalanced-learn) |
| Dashboard | Power BI Desktop |
| Version Control | Git, GitHub |
| Development | Jupyter Notebook |

