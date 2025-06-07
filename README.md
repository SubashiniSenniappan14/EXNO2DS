EXNO2DS
Name : Subashini S
Reg No : 212222240106
AIM:
To perform Exploratory Data Analysis on the given data set.

EXPLANATION:
The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

CODING AND OUTPUT:
Importing required libraries:
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
Replacing the null values using mode/median/mean:
# Check for nulls
print(df.isnull().sum())

# Replace any found nulls (none found here, but example for median replacement)
# df['column_name'] = df['column_name'].fillna(df['column_name'].median())
Boxplot to analyze outliers
plt.figure(figsize=(12, 6))
sns.boxplot(data=df[['area', 'bedrooms', 'bathrooms', 'stories', 'parking']])
plt.title("Boxplot for Numeric Features")
plt.show()
Output:
image

Countplot for categorical features:
plt.figure(figsize=(12, 6))
sns.countplot(x='furnishingstatus', data=df)
plt.title("Count of Furnishing Status")
plt.show()
Output:
image

Displot for univariate distribution:
sns.displot(df['price'], kde=True, bins=30)
plt.title("Distribution of House Prices")
plt.show()
Output:
image

Cross-tabulation analysis:
cross_tab = pd.crosstab(df['furnishingstatus'], df['airconditioning'])
print(cross_tab)
Output:
image

Heatmap to show relationships:
plt.figure(figsize=(10, 6))
sns.heatmap(df.select_dtypes(include=np.number).corr(), cmap='coolwarm', annot=True, linewidths=0.5)
plt.title('Correlation Heatmap')
plt.show()
Output:
image

RESULT
I cleaned the dataset by checking for missing values and removing outliers using IQR. I performed visual and statistical EDA using boxplots, countplots, displot, crosstab, and heatmap to understand variable distributions and
