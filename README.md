# Ex03-Univariate-Analysis

# AIM
To perform Univariate EDA on the given data set.

# Explanation
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

# ALGORITHM

## STEP 1
Import the built libraries required to perform EDA and outlier removal.

## STEP 2
Read the given csv file

## STEP 3
Convert the file into a dataframe and get information of the data.

## STEP 4
Return the objects containing counts of unique values using (value_counts()).

## STEP 5
Plot the counts in the form of Histogram or Bar Graph.

## STEP 6
Use seaborn the bar graph comparison of data can be viewed.

## STEP 7
Save the final data set into the file

# CODE
```

Name : S.Prema Latha
Register Number : 212222230112
**Univariate EDA - SuperStore.csv**
import pandas as pd
import numpy as np
import seaborn as snb
df = pd.read_csv('/content/SuperStore.csv')
df.head(10)
df.info()
df.describe()
df.dtypes
df.isnull().sum()
df['Postal Code'] = df["Postal Code"].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
df['Postal Code'].value_counts()
snb.boxplot(x="Sales",data=df)
snb.countplot(x="Sales",data=df)
snb.distplot(df["Sales"])
snb.histplot(x="Sales",data=df)
df.skew()
df.kurtosis()
snb.histplot(x="Postal Code",data=df)
snb.displot(x="Postal Code",data=df)
snb.boxplot(x="Postal Code",data=df)
snb.boxplot(x="Row ID",data=df)
snb.histplot(x="Ship Mode",data=df)
snb.countplot(x="Category",data=df)

```

# OUTPUT

EDA - SuperStore.csv

![31](https://user-images.githubusercontent.com/120620842/228266559-c5ee7866-5a27-47eb-876d-ec2456fb941d.png)

Displaying information about Dataset

![32](https://user-images.githubusercontent.com/120620842/228266646-b6ddcdbb-a235-41d9-8dc7-1397f2106963.png)

![33](https://user-images.githubusercontent.com/120620842/228266830-003e4d11-dc2c-468a-90e6-d014897649d0.png)

![34](https://user-images.githubusercontent.com/120620842/228266920-57ed130b-9696-4752-8112-b55377f843cc.png)

Finding null values and cleaning it

![35](https://user-images.githubusercontent.com/120620842/228267110-21e89b81-c4b4-4352-90b3-528ee177ee36.png)

Value counts of "Postal Code"

![36](https://user-images.githubusercontent.com/120620842/228267334-691608a2-305d-40dc-8ec2-9ef7494d05af.png)

Distribution of Data

![37](https://user-images.githubusercontent.com/120620842/228267490-07d07778-520b-408a-8c4c-308ba2cc1873.png)

Univariate Analysis

![38](https://user-images.githubusercontent.com/120620842/228267753-4202b9aa-5192-4402-a2f9-fb7c8b8ef812.png)

![39](https://user-images.githubusercontent.com/120620842/228267856-96eccc3f-728f-440c-83cd-b90652853948.png)

![40](https://user-images.githubusercontent.com/120620842/228267965-e07cd661-a42c-4408-a728-a9e6f6e542c7.png)

![41](https://user-images.githubusercontent.com/120620842/228268601-566ea5f5-fe07-4691-9182-696e4e48d979.png)

![42](https://user-images.githubusercontent.com/120620842/228268656-4d2f127a-e8ba-4dc0-a7e7-c233576e3617.png)

# RESULT
Thus the program to perform EDA on the given data set is successfully executed.
