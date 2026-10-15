# Environmental Toxin Analysis in River Systems

**Author:** Darren Van Der Velde  
**License:** MIT  

---

An in-depth exploratory data analysis examining heavy metal concentrations, water chemistry parameters, and pollutant variations across major river systems worldwide.

This project uses Python and Jupyter Notebook to explore toxin levels (Lead, Mercury, Arsenic), water quality indicators (pH, Temperature, Dissolved Oxygen, Nitrates, Phosphates) in major global river systems including the Amazon, Nile, Yangtze, Mississippi, Danube and others over the period 2018–2023.

---

## Project Overview

The analysis investigates global river system water quality and toxin concentrations using the **National_River_Toxin_Dataset_1** dataset. The exploratory data analysis (EDA) covers **1,305 records** across **10 attributes** and maps the distribution and statistical characteristics of key environmental indicators.

### What this project covers
- Loading and cleaning of river toxin monitoring data
- Handling of missing values in numeric columns
- Calculation of average toxin levels per river system
- Identification of the most polluted river systems (especially by Lead)
- Time-series visualization of toxin levels from 2018 to 2023
- Statistical hypothesis testing (independent two-sample t-test)
- Linear regression analysis exploring the relationship between pH and Lead concentrations
- Clear visual summaries (bar charts, line graphs) stored in the `Assets` folder
- A full PDF report of the analysis available in the `Docs` folder
- Detailed documentation of the full analysis approach and methodology

---

## Repository Structure

```
Evironmentak-Toxin-Analysis-In-River-Systems/
│
├── Assets/                          # Screenshots and visual outputs from the analysis
│   ├── ALLBRS.png
│   ├── CH.png
│   └── LLOT.png
│
├── Dataset/
│   ├── Clean/                       # Cleaned version of the dataset
│   │   └── National_River_Toxin_Dataset_1.csv
│   └── Raw/                         # Original / raw version of the dataset
│       └── National_River_Toxin_Dataset_1.csv
│
├── Docs/                            # Project documentation and reports
│   ├── ANALYSIS_APPROACH.md         # Detailed step-by-step analysis methodology
│   └── Environmental Toxin Analysis in River Systems (4).pdf
│
├── Notebooks/                       # Jupyter Notebook containing the full analysis
│   └── Environmental Toxin Analysis in River Systems.ipynb
│
├── .gitignore                       # Git ignore rules
├── LICENSE                          # MIT License
├── README.md                        # Project overview and documentation
└── requirements.txt                 # Python dependencies
```

---

## Analysis Approach

A complete step-by-step breakdown of the analytical methodology used in this project is available here:

**→ [Docs/ANALYSIS_APPROACH.md](Docs/ANALYSIS_APPROACH.md)**

This document covers:
- Data loading and cleaning process
- Missing value handling strategy
- Descriptive statistics and ranking of polluted river systems
- Time-series visualization approach
- Hypothesis testing (t-test) methodology and results
- Linear regression analysis between pH and Lead
- Key takeaways and interpretation of findings

---

## Dataset Information

**File:** `National_River_Toxin_Dataset_1.csv`

| Column              | Description                                      |
|---------------------|--------------------------------------------------|
| Date                | Sampling date (2018-01-01 onwards)               |
| River_System        | Name of the river system                         |
| pH_Level            | Acidity / alkalinity of the water                |
| Temperature         | Water temperature                                |
| Lead                | Lead concentration                               |
| Mercury             | Mercury concentration                            |
| Arsenic             | Arsenic concentration                            |
| Nitrates            | Nitrate levels                                   |
| Phosphates          | Phosphate levels                                 |
| Dissolved_Oxygen    | Dissolved oxygen concentration                   |

The dataset contains measurements from multiple major river systems over several years, allowing both cross-sectional and temporal analysis.

---

## Key Findings from the Analysis

### Overall Toxin Levels
- **Arsenic** (~3.598) and **Lead** (~3.011) show the highest overall average concentrations.
- **Mercury** (~0.596) is significantly lower on average than the other heavy metals.

### Most Polluted River Systems (by Lead)
- **Yangtze** recorded the highest average lead level (~4.011).
- **Mississippi** followed closely (~3.478).
- **Amazon** showed one of the lower average lead concentrations among the top entries (~2.031).

### Statistical Insights
- An independent two-sample t-test between the **Amazon** and **Nile** river systems for Lead levels produced a T-statistic of approximately **-20.24** and a near-zero p-value, confirming a statistically significant difference in pollutant burden between the two basins.
- Linear regression between **pH_Level** and **Lead** indicated a positive relationship (coefficient ≈ 0.803), suggesting that higher (more basic) pH values tend to be associated with higher lead concentrations in this dataset.

### Implications
The results highlight the importance of continuous monitoring of heavy metal accumulation and nutrient pollution in major global waterways. Differences in toxin profiles across river systems indicate that environmental policies and remediation efforts should be tailored to local industrial, agricultural, and geographical conditions rather than applying one-size-fits-all strategies.

---

## How to Run the Analysis

1. Clone the repository:
   ```bash
   git clone https://github.com/Darrenvandervelde/Evironmentak-Toxin-Analysis-In-River-Systems.git
   cd Evironmentak-Toxin-Analysis-In-River-Systems
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook "Notebooks/Environmental Toxin Analysis in River Systems.ipynb"
   ```

4. The notebook loads the dataset from the same directory (or adjust the path to point to `Dataset/Clean/National_River_Toxin_Dataset_1.csv`).

---

## Technologies Used

- **Python**
- **Pandas** – data loading and manipulation
- **NumPy** – numerical operations
- **Matplotlib & Seaborn** – data visualization
- **SciPy** – statistical tests (t-test)
- **Scikit-learn** – linear regression
- **Statsmodels** – time-series seasonal decomposition
- **Jupyter Notebook** – interactive analysis and documentation

---

## Visual Outputs

Graph screenshots and key visualizations from the notebook are stored in the `Assets/` folder.  
A complete written report (including both code explanations and visuals) is available as a PDF in the `Docs/` folder.  
A detailed explanation of the full analysis methodology can be found in [`Docs/ANALYSIS_APPROACH.md`](Docs/ANALYSIS_APPROACH.md).

---

## License

This project is released under the **MIT License**. See the [LICENSE](LICENSE) file for full details.

---

## Author

**Darren Van Der Velde**  

Feel free to open issues or submit pull requests if you would like to extend the analysis or improve the documentation.
