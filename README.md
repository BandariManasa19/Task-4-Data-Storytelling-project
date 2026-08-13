# Task 4: Data Storytelling - Gender and Transaction Sales Analysis

## Overview

This project performs a comprehensive statistical analysis to determine whether there is a significant difference in average transaction sales between male and female customers. The analysis combines exploratory data analysis, hypothesis testing, and data visualization to provide data-driven insights for business decision-making.

## Project Objective

To validate whether the observed difference in average transaction sales between male and female customers is **statistically significant** using rigorous statistical testing.

### Key Question
**Does average transaction sales differ significantly between male and female customers?**

## Key Findings

- **Male Average Sales:** $141,807.34
- **Female Average Sales:** $136,883.21
- **Difference:** $4,924.13
- **Statistical Test:** Welch's Independent Two-Sample T-Test
- **P-value:** 0.4950
- **Significance Level:** 0.05
- **Conclusion:** **No statistically significant difference** (p-value > 0.05)

Although males show a higher average transaction value, the difference is **not statistically meaningful** at the 5% significance level.

## Project Structure

```
Task4/
├── README.md                              # This file
├── requirements.txt                       # Python dependencies
├── analysis/
│   ├── hypothesis_testing.py             # Statistical hypothesis testing script
│   ├── statistical_visualization.py      # Visualization generation script
│   └── statistical_results.csv           # Test results summary
├── data/
│   └── cleaned_dataset.csv               # Cleaned dataset (1,001 records)
├── visuals/
│   ├── gender_comparison.png             # Gender-wise sales comparison chart
│   └── confidence_interval.png           # Confidence interval visualization
├── report/
│   └── Hypothesis_Testing_Summary.md     # Detailed analysis report
└── presentation/                          # Presentation materials
```

## Methodology

### 1. **Hypotheses**

- **Null Hypothesis (H₀):** There is no statistically significant difference in average transaction sales between male and female customers.
- **Alternative Hypothesis (H₁):** There is a statistically significant difference in average transaction sales between male and female customers.

### 2. **Statistical Test**

**Welch's Independent Two-Sample T-Test** was used because:
- It compares means between two independent groups
- It doesn't assume equal variances
- It's robust for slightly unequal sample sizes

### 3. **Sample Information**

| Group | Sample Size |
|-------|------------|
| Male | 511 |
| Female | 489 |
| **Total** | **1,000** |

### 4. **Test Parameters**

- **Significance Level:** α = 0.05
- **Test Statistic (T):** 0.6826
- **P-value:** 0.4950
- **95% Confidence Interval:** -$9,231.58 to $19,079.85

## Getting Started

### Prerequisites

- Python 3.x
- Required packages (see `requirements.txt`)

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Task4
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

### Running the Analysis

1. **Run hypothesis testing:**
```bash
python analysis/hypothesis_testing.py
```

2. **Generate visualizations:**
```bash
python analysis/statistical_visualization.py
```

## Key Files

- **`analysis/hypothesis_testing.py`** - Performs Welch's t-test and generates statistical results
- **`analysis/statistical_visualization.py`** - Creates comparison charts and confidence interval plots
- **`data/cleaned_dataset.csv`** - Source data for analysis (1,001 transaction records)
- **`report/Hypothesis_Testing_Summary.md`** - Comprehensive analysis report with detailed findings

## Visualizations

### Gender Comparison Chart
Visual comparison of average transaction sales between male and female customers.

### Confidence Interval Plot
95% confidence interval visualization showing the range of mean differences.

## Business Insights

### Conclusion
While descriptive analysis showed males had higher average transaction sales ($4,924.13 more), **this difference is not statistically significant**. Therefore:

✗ Do **NOT** make major business decisions based solely on gender  
✓ Consider stronger predictors such as:
- Product and category performance
- City and regional performance
- Customer-level revenue patterns
- Monthly sales trends
- Multiple customer characteristics

## Dependencies

- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **scipy** - Scientific computing and statistics
- **matplotlib** - Data visualization

See `requirements.txt` for specific version requirements.

