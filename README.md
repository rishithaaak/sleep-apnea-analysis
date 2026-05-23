# Sleep Efficiency & Lifestyle Factor Analysis

This project investigates how everyday habits, behaviors, and demographics impact baseline sleep quality. Using a dataset of 425 individuals, we cleaned missing data points, analyzed feature correlations, and built visualizations to isolate the primary lifestyle drivers behind sleep efficiency.

* **Project Presentation:** [BridgeUP Google Slides Link](https://docs.google.com/presentation/d/1rmoPrBiLIrEcYSMO0G9VlKKFpu8_xN3Z0kthT8RVUJo/edit?usp=sharing)
* **Team (Group 1 - Dr. Rong):** Anna, Annie, Amulya, Shivali, Rishitha

## Data Cleaning & Imputation Strategy

The raw dataset tracks 15 variables per individual, including sleep architecture percentages (REM, Deep, Light), sleep schedules, and lifestyle trackers (caffeine, alcohol, smoking, and exercise). 

To fix missing records without introducing distribution bias or data leakage, we applied the following cleaning steps:

* **Awakenings (20 missing values):** Filled missing rows using the dataset median to prevent extreme values from throwing off the distribution.
* **Caffeine Consumption (25 missing values):** Sorted the rows by age brackets and applied a backward fill (`bfill`) to keep age-group consumption habits intact.
* **Alcohol Consumption (14 missing values):** Sorted by age brackets and backward-filled (`bfill`) to maintain accurate generational habits.



## Key Analytical Insights

### 1. Correlation Analysis
We mapped a Pearson correlation matrix across all numeric features to find out what actually drives target sleep efficiency:
* **Age vs. Sleep Efficiency:** Surprisingly, we found no strong overall correlation between absolute age and sleep efficiency. 
* **Early Adulthood:** When breaking down age groups further, there is a slight positive correlation between younger age ranges and higher efficiency scores, which drops off as the cohort matures.

### 2. Gender Grouping & Distributions
We used box plots to see if sleep patterns varied significantly by biological sex:
* **The Data:** On average, men in this dataset maintained slightly higher sleep efficiency scores than women.
* **The Context:** Based on clinical literature, this baseline gap is frequently linked to hormonal fluctuations in women that inherently raise the statistical risk for insomnia.

### 3. Lifestyle Interactions
We generated scatterplots and bar charts to map individual habits directly against sleep quality. This allowed us to visualize exactly how compounding behaviors—like drinking alcohol close to bedtime versus higher weekly exercise frequencies—directly impact deep sleep and REM cycles.

