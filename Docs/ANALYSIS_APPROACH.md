# Analysis Approach – Environmental Toxin Analysis in River Systems

**Author:** Darren Van Der Velde  
**Project:** Environmental Toxin Analysis in River Systems  
**Dataset:** National_River_Toxin_Dataset_1.csv  

---

## 1. Objective

The goal of this analysis was to perform a comprehensive exploratory data analysis (EDA) on water quality and toxin concentrations across major global river systems. The focus was on understanding heavy metal pollution (Lead, Mercury, Arsenic), nutrient levels, and key water chemistry parameters, and identifying statistically meaningful differences between river systems.

---

## 2. Dataset Overview

- **Source File:** `National_River_Toxin_Dataset_1.csv`
- **Records:** 1,305 observations
- **Time Period:** 2018 – 2023
- **Key Variables:**
  - Date
  - River_System
  - pH_Level
  - Temperature
  - Lead
  - Mercury
  - Arsenic
  - Nitrates
  - Phosphates
  - Dissolved_Oxygen

---

## 3. Analysis Workflow

### Step 1: Environment Setup & Imports
Required libraries were imported for data manipulation, visualization, and statistical analysis:

- `pandas` & `numpy` → data handling
- `matplotlib` & `seaborn` → visualization
- `scipy.stats` → hypothesis testing
- `sklearn.linear_model` → linear regression
- `statsmodels` → time-series decomposition

### Step 2: Data Loading
The dataset was loaded using `pd.read_csv()`.

### Step 3: Initial Data Exploration
- Examined the first few rows with `.head()`
- Checked data types and basic statistics with `.info()` and `.describe()`
- Identified the shape and structure of the data

### Step 4: Missing Value Handling
- Checked for missing values across all columns
- Filled missing values in numeric columns only (using appropriate imputation methods) to preserve data integrity without introducing bias into categorical or date fields

### Step 5: Data Type Conversion
- Converted the `Date` column to proper datetime format to enable time-based analysis and visualization

### Step 6: Descriptive Statistics – Average Toxin Levels
Calculated the mean concentration of each toxin (Lead, Mercury, Arsenic) across the entire dataset to establish a global baseline.

**Key Observation:**
- Arsenic and Lead showed the highest average concentrations
- Mercury levels were substantially lower

### Step 7: Ranking Most Polluted River Systems
Grouped the data by `River_System` and calculated average Lead concentrations. Sorted the results in descending order to identify the top polluted systems.

**Key Observation:**
- Yangtze and Mississippi ranked highest in average Lead levels
- Amazon showed relatively lower Lead concentrations

### Step 8: Visualization of Average Lead Levels
Created a bar chart to visually compare average Lead concentrations across river systems. This provided a clear, stakeholder-friendly view of pollution disparities.

### Step 9: Time-Series Analysis (2018–2023)
Plotted toxin levels over time using line graphs to observe trends, seasonality, or unusual spikes across the multi-year period.

### Step 10: Hypothesis Testing (T-Test)
Performed an independent two-sample t-test comparing Lead levels between the **Amazon** and **Nile** river systems.

**Results:**
- T-statistic ≈ -20.24
- Extremely low p-value (near zero)
- Conclusion: Statistically significant difference in Lead concentrations between the two river systems

### Step 11: Linear Regression Analysis
Fitted a simple linear regression model to examine the relationship between `pH_Level` and `Lead` concentration.

**Results:**
- Positive regression coefficient (≈ 0.803)
- Indicates that higher (more basic) pH values are associated with higher Lead levels in this dataset

### Step 12: Conclusion & Interpretation
Synthesized all findings into clear insights:
- Confirmed structural differences in pollutant burdens across river basins
- Highlighted the need for localized environmental management strategies rather than generalized approaches
- Emphasized the value of continuous monitoring of heavy metals and nutrients

---

## 4. Tools & Techniques Used

| Technique                        | Purpose                                      |
|----------------------------------|----------------------------------------------|
| Descriptive Statistics           | Baseline understanding of toxin levels       |
| GroupBy Aggregation              | Compare river systems                        |
| Bar Charts & Line Graphs         | Visual communication of findings             |
| Independent Two-Sample T-Test    | Test for significant differences             |
| Linear Regression                | Explore relationship between pH and Lead     |
| Missing Value Imputation         | Ensure data quality                          |
| Datetime Conversion              | Enable temporal analysis                     |

---

## 5. Key Takeaways from the Approach

1. **Data Quality First** – Cleaning and handling missing values was performed early to ensure reliable results.
2. **Progressive Analysis** – Started with global averages → moved to system-level comparisons → applied statistical tests.
3. **Visualization + Statistics** – Combined visual storytelling with rigorous statistical testing.
4. **Actionable Insights** – Focused on findings that support real-world environmental decision-making.

---

## 6. Files Related to This Analysis

- Full interactive analysis: `Notebooks/Environmental Toxin Analysis in River Systems.ipynb`
- PDF report: `Docs/Environmental Toxin Analysis in River Systems (4).pdf`
- Visualization screenshots: `Assets/`
- Cleaned dataset: `Dataset/Clean/National_River_Toxin_Dataset_1.csv`

---

*This document outlines the structured analytical approach followed throughout the project.*
