# Medical Insurance Cost Analysis
An exploratory data analysis and regression modelto understand which lifestyle  and personal factors drive medical insurance charges

## Question
What factors affect medical insurance charges and how accurately can charges be predicted?

## Dataset
**Source:** Medical Cost Personal Datasets(Kaggle)
**Size:** 1,338 records, 7 columns
**Columns:** age, sex, bmi, children, smoker, region, charges
**Data quality:** no missing values

## Tools
Python, pandas, matplotlib, skit-learn, Jupyter Notebook

## Method
1. Loaded and inspected the data('info', 'describe', missing values, duplicates)
2. Explored charges by smoking status, age, and BMI using charts
3. Grouped BMI into under25, 25-30, and over 30 to compare average charges
4. Built a linear regression model and improved it with an interaction feature(smoker, obese)

## Key Findings
**Smoking is the biggest cost driver:** smokers pay about $32,050 on average, roughly 4x average for non-smokers(about $8,400)
**Charges rise with age:** for everyone, steadily for non-smokers
**BMI over 30 rises cost sharply for smokers:** (about $22,500 up to $41,700) but only slightly for non-smokers ($8,200 TO $8,900)
Sex and region have very little effect on charges

## Model Results
|Model|R^2|Average error|
Linear regression(baseline)|0.807|$4,177|
|+ smoker-obese interaction feature|**0.907**|**$2,369**|
Adding one feature, built from a pattern found during exploration, raised R^2 by 0.10 and cut the average prediction error by about 43%

## Limitations
- The dataset is small (1,338 rows), and the data may not represent every population.
- Linear regression assumes straight line relationships. Other models might do better.
- The results show association, not proof of cause.

## Files
- 'insurance_analysis.ipynb': full analysis, charts, and model
- 'insurance.csv': the dataset

## How to run 
1. Download this repository
2. Install the libraries: 'pip install pandas matplotlib sckit-learn Jupyter'
3. Open 'insurance_analysis.ipynb' in Jupyter and run all cells
