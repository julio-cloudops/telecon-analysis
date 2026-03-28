# 📊 ConnectaTel Customer Analytics

[![Python](https://img.shields.io/badge/Python-3.9-blue)](https://img.shields.io/badge/Python-3.9-blue)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
[![Seaborn](https://img.shields.io/badge/Visualization-Seaborn-green)](https://img.shields.io/badge/Visualization-Seaborn-green)
[![Status](https://img.shields.io/badge/Project-Completed-brightgreen)](https://img.shields.io/badge/Project-Completed-brightgreen)

---

## 🚀 Overview

This project analyzes customer behavior from a telecommunications company in Latin America (**ConnectaTel**) with the objective of identifying usage patterns, segmenting users, and detecting business opportunities.

👉 Applied Techniques:

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Customer Segmentation

---

## 🎯 Objectives

* Analyze real usage of calls and messages
* Identify high-value customers (heavy users)
* Detect outliers and their impact
* Segment customers by age and behavior
* Propose improvements to commercial plans

---

## 📂 Datasets

| Dataset | Description |
| --- | --- |
| `plans.csv` | Plan information (price, minutes, GB, extra costs) |
| `users_latam.csv` | Customer data (age, city, plan, churn) |
| `usage.csv` | Real usage (calls, messages, duration, dates) |

---

## ⚙️ Project Pipeline

```
graph LR
A[Load Data] --> B[Data Cleaning]
B --> C[Feature Engineering]
C --> D[EDA]
D --> E[Segmentation]
E --> F[Insights & Business Recommendations]
```

---

## 📋 Files in Repository

### Main Files:
- **README.md** - Project documentation
- **S7 Version-Estudiante-Project-ConnectaTel.ipynb** - Complete Jupyter Notebook with analysis and segmentation

### Technologies Used:
- **Python 3.9** - Programming language
- **Pandas** - Data manipulation and analysis
- **Seaborn** - Data visualization
- **Jupyter Notebook** - Interactive development environment

---

## 🔍 Project Structure

### 1. **Data Loading**
   - Read three CSV files: plans, users, and usage data
   - Combine datasets using merge operations

### 2. **Data Cleaning**
   - Handle missing values
   - Remove or treat outliers
   - Standardize data formats
   - Validate data integrity

### 3. **Feature Engineering**
   - Create new features from existing data
   - Calculate call and message statistics
   - Compute cost metrics
   - Extract temporal patterns

### 4. **Exploratory Data Analysis (EDA)**
   - Statistical summaries
   - Distribution analysis
   - Correlation analysis
   - Visualization of patterns

### 5. **Customer Segmentation**
   - Segment users by age groups
   - Identify heavy users vs. light users
   - Analyze behavior patterns by segment
   - Detect anomalies

### 6. **Business Insights**
   - Revenue optimization opportunities
   - Churn risk assessment
   - Product recommendations
   - Marketing strategy suggestions

---

## 💡 Key Insights Expected

- **Usage Patterns**: Understanding how customers use calls, messages, and data
- **High-Value Customers**: Identifying the most profitable customer segments
- **Plan Optimization**: Recommendations for improving current commercial plans
- **Churn Prediction**: Early detection of customers at risk of leaving
- **Market Opportunities**: New business segments to target

---

## 📊 Visualizations Included

- Distribution plots (histograms, density plots)
- Relationship plots (scatter plots, correlation heatmaps)
- Categorical analysis (bar charts, box plots)
- Time series analysis (trend plots)
- Segmentation results (cluster visualizations)

---

## 🛠️ Requirements

```python
python >= 3.9
pandas >= 1.3.0
numpy >= 1.21.0
matplotlib >= 3.4.0
seaborn >= 0.11.0
jupyter >= 1.0.0
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/julio-cloudops/telecom-analysis.git
cd telecom-analysis
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Open the Jupyter Notebook
```bash
jupyter notebook "S7 Version-Estudiante-Project-ConnectaTel.ipynb"
```

### 4. Run all cells to see the complete analysis

---

## 📈 Expected Outcomes

After running this analysis, you will obtain:

1. **Customer Segments** - Clearly defined groups based on behavior
2. **Usage Insights** - Understanding of consumption patterns
3. **Business Recommendations** - Actionable insights for decision-making
4. **Visualizations** - Clear charts for stakeholder presentations
5. **Statistical Reports** - Detailed metrics and KPIs

---

## 🤝 Contributing

This is an educational project. Contributions, suggestions, and improvements are welcome!

If you want to contribute:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/NewFeature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/NewFeature`)
5. Open a Pull Request

---

## 📝 License

This project is provided as-is for educational and analytical purposes.

---

## 👤 Author

**Julio CloudOps**

---

## 🙏 Acknowledgments

- ConnectaTel team for providing anonymized customer data
- Educational institutions for guidance in data analysis best practices
- Open source community for excellent tools and libraries

---

## 📧 Contact

For questions or suggestions about this project, feel free to reach out!

---

## 🎓 Learning Outcomes

By completing this project, you will learn:

✅ Data cleaning and preprocessing techniques
✅ Exploratory data analysis methodology
✅ Feature engineering for better insights
✅ Customer segmentation strategies
✅ Business intelligence application
✅ Data visualization best practices
✅ Statistical analysis and interpretation
✅ Actionable insights generation

---

## 📚 Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Data Science Best Practices](https://www.kdnuggets.com/)
- [Customer Segmentation Techniques](https://en.wikipedia.org/wiki/Customer_segmentation)

---

**Last Updated**: 2026
**Status**: ✅ Complete
