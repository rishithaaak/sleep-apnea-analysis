# Human Sleep Efficiency & Behavioral Analytics

An end-to-end statistical data science study analyzing the demographic, physiological, and behavioral determinants of human sleep efficiency. Utilizing a clinical-style cohort dataset of 425 individuals across 15 biometric and lifestyle variables, this project builds a robust data preprocessing pipeline, handles non-random missingness through age-stratified backfilling, and executes advanced exploratory data analysis (EDA) to map the behavioral factors influencing sleep quality.

* **Slide Presentation:** [BridgeUP Research Presentation](https://docs.google.com/presentation/d/1rmoPrBiLIrEcYSMO0G9VlKKFpu8_xN3Z0kthT8RVUJo/edit?usp=sharing)
* **Research Team (Group 1 — Dr. Rong):** Anna, Annie, Amulya, Shivali, Rishitha

---

## Technical Core & Engineering Stack

* **Language:** Python 3
* **Data Ingestion & Engineering:** Pandas, NumPy
* **Statistical Modeling & Data Visualization:** Seaborn, Matplotlib

---

## Data Engineering Pipeline & Cleaning Strategy

The raw dataset tracks 425 patients across 15 multi-type attributes, spanning sleep architecture ratios (REM, Deep, and Light sleep percentages), temporal metrics (Bedtime, Wake-up time, total Sleep Duration), and routine lifestyle variables. 

To ensure statistical validity and prevent data leakage or distribution bias during subsequent modeling, a strict imputation and validation pipeline was developed:

| Feature Vector | Missing Records | Imputation Methodology & Engineering Rationale |
| :--- | :---: | :--- |
| **Awakenings** | 20 | **Median Imputation**: Utilized the sample median to preserve the structural distribution and mitigate the skewing impact of extreme outliers. |
| **Caffeine Consumption** | 25 | **Age-Stratified Backward Fill (bfill)**: Sorted the cohort chronologically by age to capture and preserve localized, generation-specific dietary habits. |
| **Alcohol Consumption** | 14 | **Age-Stratified Backward Fill (bfill)**: Maintained demographic alignment by sorting by age before imputation to reflect lifecourse consumption trends accurately. |

---

## Exploratory Data Analysis & Statistical Insights

### 1. Multi-Variable Feature Correlation
A Pearson correlation matrix was generated across all continuous numerical features to discover hidden co-dependencies and evaluate linear relationships with the target metric (`Sleep efficiency`):
* **Age vs. Efficiency:** Statistical analysis disproved the initial hypothesis of a strong linear decay; chronological age does not exhibit a dominant global correlation with sleep efficiency.
* **Granular Timeline Trends:** Segmenting the dataset revealed a localized, statistically minor positive correlation between younger age metrics and peak sleep efficiency specifically during early-stage adulthood.

### 2. Demographic Cohort Segmentation
Evaluating the target metric across gender boundaries highlighted systemic structural variations within the dataset population:
* **The Variance:** Comparative data visualizations via box plots demonstrated that male participants exhibited a marginally higher mean sleep efficiency score relative to female participants.
* **Domain Context:** This variance was contextualized using clinical literature regarding physiological and endocrine fluctuations in women, which historically introduces higher base-rate risks for idiopathic insomnia.
