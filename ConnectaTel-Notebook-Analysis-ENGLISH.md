# 📊 ConnectaTel Customer Analytics - Complete Analysis Breakdown

## Overview
This Jupyter notebook performs a comprehensive analysis of telecommunications customer data from ConnectaTel, focusing on data cleaning, exploratory analysis, outlier detection, and customer segmentation.

---

## 📋 Notebook Structure

### **Total: 79 Cells**
- **36 Markdown Cells** - Documentation and explanations
- **43 Code Cells** - Data processing and analysis

---

## 🔍 Section Breakdown

### **Section 1: Introduction & Data Exploration**
**Goal:** Understand the structure and content of the datasets

#### 1.1 Project Context
- Role: Data Analyst
- Objective: Evaluate customer behavior
- Data Source: ConnectaTel telecommunications company
- Geographic Focus: Latin America

#### 1.2 Dataset Structure Exploration
**🎯 Objective:** Understand the structure of each dataset
- Load three CSV files: plans, users, usage
- Inspect columns, data types, dimensions
- Preview first rows of each dataset

**Key Analysis:**
```python
- plans.csv: Plan pricing, minutes, GB, extra costs
- users_latam.csv: Customer demographics, location, plan, churn status
- usage.csv: Call/message logs with duration and dates
```

---

### **Section 2: Data Cleaning**

#### 2.1 Initial Data Quality Assessment
- Check for missing values
- Identify data types
- Review basic statistics

#### 2.2 Detection of Invalid Values and Sentinel Values
**🎯 Objective:** Identify sentinel values (special codes for missing/invalid data)

**Sentinel Detection:**
- Negative values in age column
- Zero or extreme values in usage columns
- Invalid dates or impossible timestamps
- Placeholder values (-999, 999, 0, etc.)

**Actions:**
```python
- Document all sentinel values found
- Quantify their frequency
- Assess impact on analysis
- Plan replacement strategy
```

#### 2.3 Date Review and Standardization
**🎯 Objective:** Ensure date columns are properly formatted and valid

**Checks:**
- Convert string dates to datetime format
- Verify date range (2024 data)
- Identify impossible dates (future dates, negative durations)
- Standardize date format across all columns

---

### **Section 3: Data Transformation**

#### 3.1 Handling Missing Data Strategy
- Replace sentinel values with NaN
- Document replacement reasoning
- Decide on imputation vs. deletion
- Maintain data integrity

#### 3.2 Correcting Sentinel Values and Impossible Dates
**🎯 Objective:** Clean problematic data entries

**Decisions Made:**
```python
- Replace age sentinels with NaN or median
- Remove/flag impossible date entries
- Handle duplicate records
- Standardize text fields (uppercase/lowercase)
```

**Before & After Comparisons:**
- Count of invalid records removed
- Data quality improvement metrics
- Impact on dataset size

---

### **Section 4: Feature Engineering**

#### 4.1 Creating Derived Features
- Calculate total minutes per customer
- Count messages per customer
- Compute average daily usage
- Calculate monthly costs

#### 4.2 Statistical Summary by User (2024)
**🎯 Objective:** Analyze numerical columns for each customer

**Key Metrics Calculated:**
```python
- Total calls (count & duration)
- Total messages sent/received
- Data consumption (GB)
- Total costs incurred
- Plan utilization rates
- Usage frequency patterns
```

**Aggregations:**
- Sum of usage metrics
- Average usage rates
- Maximum values (peaks)
- Standard deviation (consistency)
- Min/Max ranges

---

### **Section 5: Exploratory Data Analysis (EDA)**

#### 5.1 Univariate Analysis
- Age distribution (histogram)
- Usage patterns (calls, messages, data)
- Cost distribution
- Churn rate overview

#### 5.2 Outlier Identification
**🎯 Objective:** Detect extreme values in key variables

**Methods Used:**
```python
- IQR (Interquartile Range) method
- Z-score analysis
- Visual inspection (box plots)
- Statistical thresholds
```

**Outlier Categories:**
1. **Heavy Users** - High call/message/data usage
2. **High Spenders** - Excessive bill amounts
3. **Age Anomalies** - Invalid age values
4. **Duration Extremes** - Unusually long/short calls

**Analysis:**
- Count of outliers per variable
- Percentage of data affected
- Impact on model building
- Decision: Keep or remove?

#### 5.3 Bivariate & Multivariate Analysis
- Age vs. Usage patterns
- Age vs. Spending
- Plan type vs. Usage
- Churn vs. Usage intensity

---

### **Section 6: Customer Segmentation**

#### 6.1 Segmentation Strategy
Define customer groups based on:
- Age brackets
- Usage intensity (heavy/medium/light)
- Spending patterns
- Churn risk

#### 6.2 Age-Based Customer Segmentation
**🎯 Objective:** Classify each customer into age groups

**Age Groups Defined:**
```
Group 1: 18-25 years (Young users)
Group 2: 26-35 years (Adults)
Group 3: 36-50 years (Middle-aged)
Group 4: 50+ years (Seniors)
```

**Characteristics per Group:**
- Average usage (calls, messages, data)
- Average spending
- Churn rate
- Plan preferences
- Peak usage times

#### 6.3 Visualization of Customer Segmentation
**🎯 Objective:** Visualize segment distribution and characteristics

**Charts Created:**
```
- Pie charts: Segment size distribution
- Bar charts: Average metrics by segment
- Box plots: Spending ranges by segment
- Heatmaps: Segment profiles
- Scatter plots: Multi-dimensional relationships
```

---

### **Section 7: Executive Analysis & Insights**

#### 7.1 Problems Detected in Data
**⚠️ Data Quality Issues:**

1. **Sentinel Values Found:**
   - Age column: Negative values (-1, -999)
   - Usage columns: Zeros indicating "no usage"
   - Dates: Future dates or dates before 2024

2. **Missing Data Patterns:**
   - Percentage of NaN values per column
   - Systematic vs. random missingness
   - Impact on analysis

3. **Outliers Identified:**
   - Heavy users (top 5%)
   - High spenders (outlier costs)
   - Unusual age values

#### 7.2 Key Findings

**Usage Patterns:**
- Average calls per customer per month
- Message to call ratio
- Data consumption trends
- Peak usage times

**Customer Value:**
- Revenue distribution (Pareto principle)
- High-value customer concentration
- Average customer lifetime value (by segment)

**Churn Insights:**
- Churn rate by age group
- Churn rate by usage intensity
- Churn rate by plan type
- Risk factors for churn

**Segment Profiles:**
```
Segment 1 (Young Users):
  - Higher data usage
  - Lower average spend
  - High churn risk
  
Segment 2 (Adults):
  - Balanced usage pattern
  - Medium-high spend
  - Moderate churn risk
  
Segment 3 (Middle-aged):
  - Call-focused usage
  - Higher spend
  - Lower churn risk
  
Segment 4 (Seniors):
  - Lower overall usage
  - High spend (plan commitment)
  - Lowest churn risk
```

---

## 🎯 Business Recommendations

### 1. **Data Quality Improvements**
- Establish data validation rules
- Regular sentinel value checks
- Implement automated data cleaning pipeline
- Monitor data quality metrics

### 2. **Targeted Retention Strategies**
**By Segment:**
- Young users: Reduce prices, increase data allowance
- Adults: Bundled services, family plans
- Middle-aged: Reliability and quality focus
- Seniors: Simplified plans, customer support

### 3. **Revenue Optimization**
- Focus on high-value segments
- Upgrade light users to higher plans
- Create targeted offers for churn-risk customers
- Develop new plans based on segment preferences

### 4. **Product Development**
- Design youth-targeted data-heavy plans
- Create family/group plans for adults
- Develop premium plans for high spenders
- Simplify offerings for seniors

### 5. **Marketing Strategy**
- Segment-specific campaigns
- Personalized offers based on usage patterns
- Retention programs for churn-risk segments
- Expansion focus on profitable segments

---

## 📊 Key Metrics Summary

### Usage Metrics:
- **Average Calls/Month:** [Value from analysis]
- **Average Messages/Month:** [Value from analysis]
- **Average Data/Month:** [Value from analysis]
- **Average Cost/Month:** [Value from analysis]

### Customer Distribution:
- **Total Customers:** [Value]
- **Active Customers:** [Value]
- **Churned Customers:** [Value]
- **At-Risk Customers:** [Value]

### Segment Distribution:
- **Segment 1 Size:** [Percentage]
- **Segment 2 Size:** [Percentage]
- **Segment 3 Size:** [Percentage]
- **Segment 4 Size:** [Percentage]

---

## 🛠️ Python Libraries Used

```python
import pandas as pd              # Data manipulation
import numpy as np               # Numerical operations
import matplotlib.pyplot as plt   # Plotting
import seaborn as sns            # Advanced visualization
from datetime import datetime     # Date handling
```

---

## 🔄 Analysis Workflow

```
1. Load Data (plans, users, usage)
   ↓
2. Exploratory Inspection (head, info, describe)
   ↓
3. Data Cleaning
   ├─ Identify sentinels
   ├─ Handle dates
   ├─ Fix anomalies
   ↓
4. Feature Engineering
   ├─ Aggregate metrics
   ├─ Create derived features
   ├─ Calculate statistics
   ↓
5. Statistical Analysis
   ├─ Distributions
   ├─ Correlations
   ├─ Outlier detection
   ↓
6. Customer Segmentation
   ├─ Define groups
   ├─ Profile segments
   ├─ Visualize results
   ↓
7. Business Insights
   ├─ Identify patterns
   ├─ Extract actionable insights
   ├─ Generate recommendations
```

---

## 📈 Expected Outputs

### Reports Generated:
1. **Data Quality Report** - Issues found and actions taken
2. **Customer Segment Report** - Detailed profile of each segment
3. **Churn Risk Assessment** - Customers at risk by segment
4. **Revenue Analysis** - Distribution and concentration analysis
5. **Visualization Dashboard** - Charts and graphs for presentation

### Deliverables:
- Cleaned and processed datasets
- Segment membership for each customer
- Recommendations for business strategy
- Executive summary with key insights
- Visualization suite for stakeholder communication

---

## 💡 Data Insights Examples

### "Young Users (18-25):"
- **Behavior:** Heavy data users, light on calls
- **Challenge:** High churn rate
- **Opportunity:** Data plan upgrades, entertainment packages

### "Middle-Aged Users (36-50):"
- **Behavior:** Call-focused, stable usage
- **Strength:** Low churn, loyal customers
- **Opportunity:** Premium services, loyalty programs

### "Seniors (50+):"
- **Behavior:** Consistent usage, low experimentation
- **Strength:** Lowest churn, most predictable
- **Opportunity:** Simplified interfaces, dedicated support

---

## 🎓 Learning Outcomes

By analyzing this notebook, you'll learn:

✅ How to load and combine multiple datasets
✅ Data quality assessment and cleaning techniques
✅ Sentinel value detection and handling
✅ Feature engineering for business metrics
✅ Exploratory data analysis methodology
✅ Outlier detection and analysis
✅ Customer segmentation strategies
✅ Business insight extraction
✅ Data visualization best practices
✅ How to translate technical analysis to business recommendations

---

## 📝 Notes & Observations

### Data Quality:
- The dataset contains real-world quality issues (sentinels, invalid dates)
- This is intentional for learning data cleaning techniques
- All issues are documented and addressed systematically

### Methodology:
- Follows industry-standard data analysis workflow
- Combines technical analysis with business thinking
- Produces actionable insights from raw data

### Scalability:
- Code can be adapted for larger datasets
- Techniques are transferable to other domains
- Principles apply to any customer analytics project

---

## 🔗 Related Resources

- [Pandas Documentation](https://pandas.pydata.org/)
- [Seaborn Visualization](https://seaborn.pydata.org/)
- [Customer Segmentation Guide](https://en.wikipedia.org/wiki/Customer_segmentation)
- [Data Cleaning Best Practices](https://www.kdnuggets.com/)
- [Churn Prediction Models](https://towardsdatascience.com/)

---

## ✅ Final Checklist

After completing this analysis:

- [ ] All data quality issues identified and documented
- [ ] Datasets cleaned and validated
- [ ] Features engineered and calculated
- [ ] Segments defined and profiled
- [ ] Visualizations created for presentation
- [ ] Business recommendations formulated
- [ ] Executive summary prepared
- [ ] Code documented and reproducible
- [ ] Insights communicated to stakeholders
- [ ] Results ready for decision-making

---

**Notebook Status:** ✅ Complete Analysis Ready
**Last Updated:** 2026
**Language:** English (Translated from Spanish)
