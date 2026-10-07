# AeroFit Treadmill Customer Analysis

Descriptive analysis of AeroFit treadmill purchases to understand how customer characteristics relate to the three models: KP281, KP481, and KP781. The project uses Python, Pandas, and visualization to build customer profiles and inform product recommendations.

## Business Objective

AeroFit wants to better understand the customers purchasing each treadmill model and use those patterns to recommend a suitable product to future customers. This analysis compares demographics, income, fitness, planned usage, and expected weekly miles across the products.

## Business Questions

- What are the customer and product characteristics in the purchase dataset?
- How do customer profiles differ across KP281, KP481, and KP781?
- Which characteristics are associated with each model purchase?
- What are the joint and conditional purchase probabilities across customer segments?
- How can the findings support product recommendations and inventory planning?

## Dataset

The project dataset contains **180 customer records and 9 fields**: `Product`, `Age`, `Gender`, `Education`, `MaritalStatus`, `Usage`, `Fitness`, `Income`, and `Miles`. Each row represents a customer who purchased an AeroFit treadmill during the three-month period described in the notebook.

The notebook reports no missing values or duplicate records. Potential outliers were reviewed and retained because they appeared to reflect plausible customer characteristics rather than data errors.

## Key Findings

- **Product mix:** KP281 accounts for 44.4% of purchases (80 customers), KP481 for 33.3% (60), and KP781 for 22.2% (40).
- **Distinct premium-model profile:** KP781 customers have higher average income (about $75,442), fitness rating (4.62/5), planned weekly usage (4.78 sessions), and expected weekly miles (166.9) than customers of the other models.
- **Fitness and model choice:** 94% of customers with a fitness rating of 5 purchased KP781. None of the customers rated 1 or 2 purchased KP781.
- **Planned usage:** All 9 customers in the high-usage group (6–7 sessions per week) purchased KP781. This group is small, so treat the pattern as directional.
- **KP281 and KP481 profiles overlap:** Their average ages, fitness ratings, and planned usage are similar; the notebook recommends differentiating them by product features and price rather than by customer demographics.
- **Gender pattern:** 33 of 40 KP781 purchases were by men. This is a sample pattern to investigate, not evidence of why the difference exists.
- **Age and marital status:** The analysis found little product differentiation by these characteristics compared with fitness and planned usage.

These are descriptive associations in a small historical purchase dataset. The project does not build or validate a predictive recommendation model, and the findings do not establish cause and effect.

## Recommendations from the Analysis

- Lead product guidance with a customer's self-rated fitness and planned weekly use.
- Treat income as a secondary conversation point, not a strict rule for recommending the premium model.
- Avoid pushing KP781 to customers with low fitness or low planned usage without first understanding their needs.
- Investigate the gender mix of KP781 buyers with additional customer research before changing marketing.
- Explain concrete feature and price differences between KP281 and KP481 because their observed customer profiles overlap.
- Use the observed 44% / 33% / 22% product mix as an initial inventory reference, then confirm it with ongoing sales data.
- Collect more purchase data before making major decisions based on small high-usage or higher-income groups.

## Skills and Tools

- Python, Pandas, NumPy, Matplotlib, and Seaborn
- Data inspection, descriptive statistics, and data-quality checks
- Categorical and numerical data analysis
- Cross-tabulations and conditional probability
- Customer segmentation and profile comparison
- Visual analysis with histograms, count plots, box plots, and relationship plots
- Translating descriptive patterns into practical recommendations

## Repository Structure

```text
aerofit-treadmill-customer-analysis/
├── README.md
├── aerofit_analysis.ipynb
└── aerofit_treadmill.csv
```

The notebook is the analysis source. The CSV is the dataset it reads. Rename the downloaded dataset from `aerofit_treadmill.csv.txt` to `aerofit_treadmill.csv` before uploading; the notebook expects that CSV filename.

## How to Review

1. Read this README for the project question and headline findings.
2. Open `aerofit_analysis.ipynb` to review the code, visualizations, probability analysis, and customer profiles.
3. Use `aerofit_treadmill.csv` as the notebook's input dataset.

## Author

**Aravinth Baskar**
