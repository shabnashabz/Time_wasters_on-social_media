# Time-Wasters on Social Media Data Analysis
## Overview
This project analyzes a dataset of social media users to identify patterns in age distribution, gender distribution, income levels, and social media usage habits. The goal is to examine how time spent on social media correlates with different demographic factors.

This analysis was conducted using Python with a focus on exploratory data analysis (EDA) and visualization.


## Key Objectives
Understand the age and income distributions of social media users.
Examine the gender distribution of the dataset.
Visualize how time spent on social media relates to the number of sessions users participate in.
Derive meaningful insights about social media usage habits across different demographics.
## Dataset
Filename: Time-Wasters on Social Media Dataset
Source: Kaggle
Data fields:
Age: The age of the user.
Gender: The gender of the user (Male, Female, Other).
Income: The annual income of the user.
Time Spent: The total time the user spends on social media.
Sessions: The number of social media sessions a user participates in.
Tools & Technologies
Python: For data manipulation and visualization.
Pandas: Library used for data exploration and manipulation.
Seaborn & Matplotlib: For creating visualizations.
Jupyter Notebook: For performing interactive data analysis.
## Key Steps in the Analysis:
Data Loading:

```python
df = pd.read_csv('/kaggle/input/time-wasters-on-social-media/Time-Wasters on Social Media.csv')
df.head()
```
## Data Exploration:

Use df.info() and df.describe() to understand the data structure.
Check for missing values and data types.
## Data Visualization:

Age Distribution: Visualized using a histogram and KDE (Kernel Density Estimate) to observe the spread of ages.
Gender Distribution: Represented using a pie chart.
Income Distribution: A boxplot was used to show the spread and outliers in the income data.
Total Time Spent vs. Number of Sessions: A scatter plot was created to examine any correlation between these variables.
## Example code for visualizations:

```python

sns.histplot(df['Age'], kde=True)
plt.title('Age Distribution')
```
```python

plt.pie(df['Gender'].value_counts(), labels=df['Gender'].unique(), autopct='%1.1f%%')
plt.title('Gender Distribution')
```
```python

sns.boxplot(y='Income', data=df)
plt.title('Income Distribution')
```
## Insights Gained:

The largest group of users falls within the 20-30 and 40-50 age ranges.
Male users make up 51.4% of the total users, followed by Female and Other genders.
The income distribution is relatively even, but there are a few outliers with very high incomes.
Users who spend more time on social media tend to have more frequent sessions, indicating a possible positive correlation.
## Example Visualizations
** Age Distribution **

Displays how the user base is spread across different age groups.
** Gender Distribution **

A pie chart showing the breakdown of gender in the dataset.
** Income Distribution **

A boxplot to explore the range and spread of income values.
** Total Time Spent vs Number of Sessions **

A scatter plot to investigate the relationship between the total time spent on social media and the number of sessions.
## Conclusion
The analysis provides insights into the typical social media user demographics, showing how factors such as age, income, and time spent on social media are distributed. Understanding these patterns can help in better targeting and engaging different user segments on social media platforms.
