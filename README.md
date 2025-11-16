# Exploratory Data Analysis

A comprehensive exploratory data analysis (EDA) project that uncovers insights from GlobalMart's customer purchase data through statistical analysis, data visualization, and business intelligence reporting.

## Overview

This Jupyter notebook performs an in-depth exploratory analysis of GlobalMart's sales dataset, examining performance across multiple dimensions including products, geography, customer segments, sales teams, and time periods. The analysis provides actionable insights to drive strategic decision-making and optimize sales operations.

## Table of Contents

- [Project Goals](#project-goals)
- [Business Value](#business-value)
- [Key Features](#key-features)
- [Technical Stack](#technical-stack)
- [Dataset Description](#dataset-description)
- [Installation](#installation)
- [Usage](#usage)
- [Analysis Sections](#analysis-sections)
- [Key Insights](#key-insights)
- [Visualizations](#visualizations)
- [Business Recommendations](#business-recommendations)
- [Next Steps](#next-steps)

## Project Goals

### Primary Objectives

1. **Understand Sales Performance**: Analyze revenue, targets, and achievement rates
2. **Identify Top Performers**: Discover best products, regions, and sales representatives
3. **Uncover Patterns**: Detect trends, seasonality, and customer behavior
4. **Support Decision Making**: Provide data-driven recommendations
5. **Visualize Insights**: Create compelling charts and graphs for stakeholders

### Focus Areas

- **Data Quality**: Clean and prepare data for analysis
- **Performance Metrics**: Calculate KPIs and success indicators
- **Segmentation Analysis**: Break down performance by key dimensions
- **Temporal Trends**: Identify time-based patterns and seasonality
- **Conversion Analysis**: Understand deal progression and win rates

## Business Value

### Strategic Benefits

1. **Revenue Optimization**: Identify high-performing products and segments
2. **Resource Allocation**: Direct investment to profitable areas
3. **Performance Management**: Benchmark sales team effectiveness
4. **Market Intelligence**: Understand regional and customer dynamics
5. **Risk Mitigation**: Identify underperforming areas needing attention

### Operational Benefits

1. **Data-Driven Culture**: Build foundation for analytics-driven decisions
2. **Baseline Establishment**: Set performance benchmarks
3. **Opportunity Identification**: Spot expansion and growth opportunities
4. **Best Practice Sharing**: Replicate successful strategies
5. **Forecasting Foundation**: Prepare data for predictive modeling

## Key Features

### 📊 Comprehensive Data Analysis

- **Univariate Analysis**: Single variable distributions and statistics
- **Bivariate Analysis**: Relationships between two variables
- **Multivariate Analysis**: Complex interactions across multiple dimensions
- **Statistical Summaries**: Mean, median, mode, standard deviation
- **Distribution Analysis**: Histograms, box plots, density plots

### 🔍 Multi-Dimensional Insights

1. **Product Analysis**
   - Category performance comparison
   - Product-level revenue breakdown
   - Win rate by product type
   - Units sold and deal sizes

2. **Geographic Analysis**
   - Regional revenue distribution
   - Country-level performance
   - Geographic conversion rates
   - Market penetration analysis

3. **Customer Segmentation**
   - Segment revenue contribution
   - Average deal sizes by segment
   - Customer lifetime patterns
   - Segment-specific win rates

4. **Sales Team Performance**
   - Individual representative rankings
   - Team-level comparisons
   - Performance distribution
   - Success rate analysis

5. **Temporal Patterns**
   - Monthly revenue trends
   - Quarterly performance
   - Day-of-week patterns
   - Seasonal variations

### 📈 Rich Visualizations

- Revenue distribution charts
- Performance comparison bar charts
- Trend line graphs
- Correlation heatmaps
- Box plots for outlier detection
- Pie charts for composition
- Scatter plots for relationships

### 💡 Actionable Insights

- Executive summary report
- Key performance indicators
- Top performer identification
- Improvement recommendations
- Strategic next steps

## Technical Stack

### Core Libraries

```python
# Data Manipulation
import pandas as pd
import numpy as np

# Visualization
import matplotlib.pyplot as plt
import seaborn as sns

# Utilities
from datetime import datetime
import warnings
```

### Visualization Configuration

```python
# Professional styling
plt.style.use('seaborn-v0_8-darkgrid')
sns.set_palette("husl")
plt.rcParams['figure.figsize'] = (12, 6)
plt.rcParams['font.size'] = 10
```

## Dataset Description

### Data Structure

**Total Records**: 5,000 customer transactions  
**Features**: 15 columns  
**Date Range**: Full calendar year (2021)  
**Data Quality**: Clean dataset with no missing values

### Column Descriptions

| Column | Description | Data Type | Sample Values |
|--------|-------------|-----------|---------------|
| **Order_ID** | Unique transaction identifier | Integer | 4971, 2347, 2588 |
| **Order_Date** | Date of transaction | Date | 2021-01-01 |
| **Region** | Geographic region | Categorical | North, South, East, West |
| **Country** | Country name | Categorical | USA, Brazil, China, Canada |
| **Sales_Rep** | Sales representative name | Categorical | David Lee, Alice Johnson |
| **Team** | Sales team assignment | Categorical | Team A, Team B, Team C |
| **Customer_ID** | Unique customer identifier | String | C3971, C1347 |
| **Customer_Segment** | Customer category | Categorical | Corporate, SME, Retail |
| **Product_Category** | Product type | Categorical | Furniture, Electronics, Appliances |
| **Product_Name** | Specific product | Categorical | Office Chair, Laptop Pro, Refrigerator |
| **Stage** | Deal stage status | Categorical | Won, Lost, Opportunity |
| **Units_Sold** | Quantity of items sold | Integer | 0-20 |
| **Revenue** | Actual sales revenue | Float | $0 - $2,000 |
| **Target** | Sales target amount | Float | $200 - $2,000 |
| **Deal_Size** | Total deal value | Float | $0 - $2,000 |

### Deal Stages

- **Won**: Successfully closed deals with revenue
- **Lost**: Failed opportunities with no revenue
- **Opportunity**: Active prospects (potential deals)

### Sample Data

```csv
Order_ID,Order_Date,Region,Country,Sales_Rep,Team,Customer_ID,Customer_Segment,Product_Category,Product_Name,Stage,Units_Sold,Revenue,Target,Deal_Size
4971,2021-01-01,North,USA,David Lee,Team C,C3971,Corporate,Furniture,Office Chair,Won,6,1662,1447,1665
2347,2021-01-02,South,Brazil,Alice Johnson,Team B,C1347,SME,Appliances,Microwave Max,Opportunity,2,464,875,928
```

## Installation

### Prerequisites

- Python 3.7 or higher
- Jupyter Notebook or JupyterLab
- Basic understanding of Python and data analysis

### Installation Steps

1. **Create Virtual Environment**

```bash
python -m venv globalmart_env
source globalmart_env/bin/activate  # Windows: globalmart_env\Scripts\activate
```

2. **Install Required Packages**

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. **Launch Jupyter Notebook**

```bash
jupyter notebook globalmart_eda.ipynb
```

### Required Packages

```txt
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
```

### Quick Start

```bash
# One-line installation
pip install pandas numpy matplotlib seaborn jupyter

# Start analysis
jupyter notebook globalmart_eda.ipynb
```

## Usage

### Running the Analysis

1. **Prepare Your Data**
   - Ensure your CSV file matches the required format
   - Update the file path in the notebook:
     ```python
     df = pd.read_csv('your_sales_data.csv')
     ```

2. **Execute Cells**
   - Run cells sequentially from top to bottom
   - Each section builds on previous analysis
   - Review outputs, charts, and insights

3. **Customize Analysis**
   - Modify date ranges for specific periods
   - Filter by region, product, or segment
   - Adjust visualization parameters

### Notebook Structure

The notebook is organized into logical sections:

1. **Section 1**: Load and inspect data
2. **Section 2**: Data cleaning and preparation
3. **Section 3**: Analysis and visualization
4. **Section 4**: Insights report generation

### Customization Examples

#### Filter by Date Range

```python
# Analyze Q1 2021 only
df_q1 = df_clean[df_clean['Quarter'] == 1]
```

#### Focus on Specific Region

```python
# Analyze North region performance
df_north = df_clean[df_clean['Region'] == 'North']
```

#### Custom Visualizations

```python
# Create custom chart
plt.figure(figsize=(14, 7))
sns.barplot(data=df_clean, x='Product_Category', y='Revenue', hue='Customer_Segment')
plt.title('Revenue by Product and Segment')
plt.show()
```

## Analysis Sections

### 1. Load and Inspect Data

**Objectives**: 
- Load dataset into pandas DataFrame
- Display basic information and structure
- Check data types and dimensions
- Identify any data quality issues

**Key Operations**:
```python
# Load data
df = pd.read_csv('supermarket_sales.csv')

# Basic inspection
df.shape          # Dimensions
df.info()         # Data types and non-null counts
df.describe()     # Statistical summary
df.head()         # First few rows
```

**Outputs**:
- Dataset shape and size
- Column data types
- Statistical summaries
- Missing value analysis
- Duplicate record check

### 2. Clean the Data

**Objectives**:
- Handle missing values (if any)
- Remove duplicates
- Format dates properly
- Create derived features
- Prepare data for analysis

**Feature Engineering**:
```python
# Date features
df['Year'] = df['Order_Date'].dt.year
df['Month'] = df['Order_Date'].dt.month
df['Month_Name'] = df['Order_Date'].dt.strftime('%B')
df['Quarter'] = df['Order_Date'].dt.quarter
df['Day_of_Week'] = df['Order_Date'].dt.day_name()

# Business metrics
df['Is_Won'] = (df['Stage'] == 'Won').astype(int)
df['Achievement_Rate'] = (df['Revenue'] / df['Target']) * 100
```

**New Features Created**:
- Temporal: Year, Month, Quarter, Day of Week
- Performance: Is_Won, Achievement_Rate
- Segmentation: Enhanced categorization

### 3. Analyze and Visualize

**3.1 Sales Performance Overview**

Calculates and displays:
- Total revenue generated
- Overall achievement rate
- Win rate percentage
- Average deal size
- Units sold totals

**3.2 Product Analysis**

Examines:
- Revenue by product category
- Top-selling products
- Category-level win rates
- Units sold distribution
- Product mix contribution

**3.3 Geographic Analysis**

Explores:
- Regional revenue distribution
- Country performance rankings
- Geographic win rates
- Market coverage
- Territory comparisons

**3.4 Customer Segment Analysis**

Investigates:
- Segment revenue contributions
- Average deal sizes by segment
- Segment-specific conversion rates
- Customer lifetime patterns
- Segment growth trends

**3.5 Sales Team Performance**

Evaluates:
- Representative rankings
- Team comparisons
- Individual win rates
- Performance distribution
- Top performer identification

**3.6 Temporal Analysis**

Analyzes:
- Monthly revenue trends
- Quarterly performance
- Day-of-week patterns
- Seasonal variations
- Time-based correlations

**3.7 Deal Stage Analysis**

Studies:
- Stage distribution (Won, Lost, Opportunity)
- Conversion funnel
- Stage-specific metrics
- Win/loss ratios
- Opportunity value

**3.8 Statistical Distributions**

Examines:
- Revenue distributions
- Deal size patterns
- Achievement rate spreads
- Box plots for outliers
- Histogram analysis

### 4. Insights Report

Generates comprehensive executive summary including:
- Overall performance metrics
- Top performer identification
- Key insights by dimension
- Strategic recommendations
- Action items and next steps

## Key Insights

### Performance Metrics

**Overall Achievement**:
- Total revenue vs. target comparison
- Win rate calculation
- Average deal size
- Total units sold
- Revenue per transaction

**Top Performers**:
- Best-performing product category
- Highest revenue region
- Top customer segment
- Leading sales representative
- Most successful team

### Pattern Discoveries

**Product Insights**:
- Which categories drive revenue
- Product-level win rates
- Pricing effectiveness
- Volume vs. value products
- Category growth trends

**Geographic Insights**:
- Regional performance gaps
- Country-specific patterns
- Market maturity indicators
- Expansion opportunities
- Geographic risk factors

**Customer Insights**:
- Segment profitability
- Deal size by segment
- Loyalty indicators
- Segment-specific needs
- Cross-selling potential

**Temporal Insights**:
- Seasonal patterns
- Monthly variations
- Quarterly trends
- Day-of-week effects
- Time-to-close analysis

**Team Insights**:
- Performance variation
- Win rate differences
- Territory assignments
- Skill gaps
- Training needs

## Visualizations

### Chart Types Created

1. **Bar Charts**
   - Revenue by category
   - Regional comparisons
   - Team performance
   - Monthly trends

2. **Pie Charts**
   - Revenue distribution
   - Stage composition
   - Segment contribution
   - Category mix

3. **Line Charts**
   - Monthly revenue trends
   - Quarterly progression
   - Time-series patterns
   - Growth trajectories

4. **Box Plots**
   - Revenue distribution by stage
   - Deal size outliers
   - Performance spread
   - Variability analysis

5. **Histograms**
   - Revenue distributions
   - Deal size frequency
   - Achievement rate spread
   - Units sold patterns

6. **Heatmaps**
   - Correlation matrices
   - Cross-tabulation
   - Pattern identification
   - Relationship strength

7. **Scatter Plots**
   - Revenue vs. target
   - Deal size relationships
   - Correlation exploration
   - Trend identification

### Visualization Customization

```python
# Professional color palette
colors = ['#2ecc71', '#e74c3c', '#3498db', '#f39c12', '#9b59b6']

# Custom chart template
plt.figure(figsize=(12, 6))
sns.set_style("whitegrid")
plt.title('Your Title', fontsize=14, fontweight='bold')
plt.xlabel('X Label')
plt.ylabel('Y Label')
plt.legend()
plt.tight_layout()
plt.show()
```

## Business Recommendations

### Strategic Initiatives

1. **Product Strategy**
   - Expand high-performing categories
   - Phase out low-performing products
   - Optimize product mix
   - Enhance pricing strategies
   - Bundle complementary products

2. **Geographic Expansion**
   - Replicate success in underperforming regions
   - Allocate resources to high-potential markets
   - Conduct market research in new territories
   - Adapt strategies to local preferences
   - Build regional partnerships

3. **Customer Segmentation**
   - Focus on high-value segments
   - Develop segment-specific offerings
   - Tailor marketing messages
   - Optimize sales approach by segment
   - Enhance customer experience

4. **Sales Team Development**
   - Share best practices from top performers
   - Provide targeted training
   - Optimize territory assignments
   - Implement performance incentives
   - Enhance collaboration

5. **Process Optimization**
   - Improve conversion from Opportunity to Won
   - Reduce lost deals
   - Streamline sales cycle
   - Enhance qualification criteria
   - Automate routine tasks

### Tactical Actions

**Immediate (Week 1-2)**:
- Share analysis results with stakeholders
- Identify quick wins
- Set up performance dashboards
- Launch pilot programs

**Short-term (Month 1-3)**:
- Implement recommended strategies
- Monitor performance changes
- Gather feedback
- Refine approaches

**Long-term (Quarter 2-4)**:
- Scale successful initiatives
- Develop predictive models
- Build advanced analytics
- Establish continuous improvement

## Next Steps

### Analytics Roadmap

1. **Deep Dive Analysis**
   - Customer lifetime value analysis
   - Cohort analysis
   - Churn prediction
   - Market basket analysis

2. **Predictive Modeling**
   - Sales forecasting model
   - Win probability estimation
   - Demand prediction
   - Trend forecasting

3. **Advanced Segmentation**
   - RFM analysis
   - Clustering customers
   - Persona development
   - Behavioral segmentation

4. **Real-time Dashboards**
   - Power BI integration
   - Tableau visualizations
   - Automated reporting
   - Alert systems

5. **A/B Testing**
   - Test pricing strategies
   - Evaluate marketing campaigns
   - Optimize sales processes
   - Measure initiatives

### Technical Enhancements

- Automate data pipeline
- Integrate with CRM systems
- Build interactive dashboards
- Implement version control
- Create documentation

## Project Structure

```
globalmart-eda/
│
├── globalmart_eda.ipynb           # Main analysis notebook
├── supermarket_sales.csv          # Input dataset
├── README.md                      # This documentation
├── requirements.txt               # Python dependencies
├── visualizations/                # Saved charts
│   ├── revenue_by_category.png
│   ├── regional_performance.png
│   └── monthly_trends.png
├── reports/                       # Generated reports
│   ├── executive_summary.pdf
│   └── detailed_findings.docx
└── scripts/                       # Utility scripts
    ├── data_loader.py
    └── visualization_helpers.py
```

## Best Practices

### Data Analysis
- ✅ Start with data quality checks
- ✅ Document assumptions and decisions
- ✅ Validate findings with stakeholders
- ✅ Use consistent naming conventions
- ✅ Comment code for clarity

### Visualization
- ✅ Choose appropriate chart types
- ✅ Use consistent color schemes
- ✅ Add clear titles and labels
- ✅ Include legends when needed
- ✅ Avoid chart junk

### Reporting
- ✅ Focus on actionable insights
- ✅ Support claims with data
- ✅ Present clearly to non-technical audience
- ✅ Prioritize key findings
- ✅ Provide recommendations

### Collaboration
- ✅ Version control notebooks
- ✅ Share reproducible analysis
- ✅ Document methodology
- ✅ Gather feedback iteratively
- ✅ Update analysis regularly

## Troubleshooting

### Common Issues

**Issue**: File not found error
```python
# Solution: Check file path
import os
print(os.getcwd())  # Current directory
df = pd.read_csv('path/to/your/file.csv')
```

**Issue**: Date parsing errors
```python
# Solution: Specify date format
df['Order_Date'] = pd.to_datetime(df['Order_Date'], format='%Y-%m-%d')
```

**Issue**: Visualization not displaying
```python
# Solution: Add display command
%matplotlib inline
plt.show()
```

**Issue**: Memory errors with large datasets
```python
# Solution: Read in chunks
chunk_size = 10000
chunks = pd.read_csv('large_file.csv', chunksize=chunk_size)
df = pd.concat(chunks, ignore_index=True)
```

## Frequently Asked Questions

**Q: Can I use this with my own data?**  
A: Yes! Just ensure your data matches the expected format and column names.

**Q: How do I export charts?**  
A: Use `plt.savefig('chart_name.png', dpi=300, bbox_inches='tight')`

**Q: Can I schedule automatic reports?**  
A: Yes, convert the notebook to a Python script and schedule with cron/Task Scheduler.

**Q: How do I share findings?**  
A: Export notebook as HTML/PDF or create a presentation deck with key charts.

**Q: What if I have missing values?**  
A: The notebook includes handling logic. Uncomment and adjust as needed.

## References

### Documentation
- [pandas Documentation](https://pandas.pydata.org/docs/)
- [matplotlib Gallery](https://matplotlib.org/stable/gallery/index.html)
- [seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)

### Books
- "Python for Data Analysis" by Wes McKinney
- "Storytelling with Data" by Cole Nussbaumer Knaflic

### Online Resources
- Kaggle notebooks for inspiration
- Towards Data Science blog
- Real Python tutorials

## License

This project is provided as-is for educational and commercial use.

## Contributing

Contributions welcome! To enhance this analysis:
1. Fork the repository
2. Create feature branch
3. Add improvements
4. Submit pull request

## Support

For questions or issues:
- Review the troubleshooting section
- Check documentation links
- Validate data format
- Ensure all packages installed

---

**Version**: 1.0  
**Last Updated**: 2025  
**Python**: 3.7+  
**Level**: Beginner to Intermediate  
**Status**: Complete Analysis Ready
