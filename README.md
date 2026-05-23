sleep-apnea-analysis
BridgeUP: Sleep Efficiency Analysis
Link to Presentation

https://docs.google.com/presentation/d/1rmoPrBiLIrEcYSMO0G9VlKKFpu8_xN3Z0kthT8RVUJo/edit?usp=sharing

Group 1 - Dr.Rong Team Members: Anna, Annie, Amulya, Shivali, Rishitha

Project Overview
Our project explores sleep efficiency — how effectively a person sleeps — based on various factors such as age, gender, caffeine intake, alcohol consumption, and exercise frequency.

By analyzing this dataset, we aimed to answer the question:

How do lifestyle and demographic factors influence an individual’s sleep efficiency?

Motivation
Sleep plays a critical role in physical health, mental well-being, and daily performance. Understanding which habits or characteristics impact sleep efficiency can help individuals make better lifestyle choices and improve their sleep quality.

Dataset
Description: The dataset contains data for 425 individuals and includes 15 variables, such as:

Age Gender Bedtime / Wake-up Time Sleep Duration Sleep Efficiency REM / Deep / Light Sleep Percentages Awakenings Caffeine Consumption Alcohol Consumption Smoking Status Exercise Frequency

Data Cleaning
Column	Missing Values	Action Taken
Awakenings	20	Imputed with median
Caffeine Consumption	25	Sorted by age, backfilled
Alcohol Consumption	14	Sorted by age, backfilled
Data Modeling
🔹 Correlation Analysis

We created a correlation matrix to explore relationships among variables.

Found no strong correlation between age and sleep efficiency.

Observed a slight positive correlation between younger age and higher efficiency during early life stages.

🔹 Gender Comparison

Using box plots, we compared sleep efficiency between men and women.

On average, men exhibited slightly higher sleep efficiency.

Possible explanation: hormonal fluctuations in women may increase insomnia risk.

🔹 Visualizations

Scatterplots — to view trends between lifestyle factors and efficiency.

Box plots — to visualize differences by gender.

Correlation heatmap — to observe inter-variable relationships.
