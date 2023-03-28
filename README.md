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

# CODE 1
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

# EDA - SuperStore.csv

![31](https://user-images.githubusercontent.com/120620842/228266559-c5ee7866-5a27-47eb-876d-ec2456fb941d.png)

# Displaying information about Dataset

![32](https://user-images.githubusercontent.com/120620842/228266646-b6ddcdbb-a235-41d9-8dc7-1397f2106963.png)

![33](https://user-images.githubusercontent.com/120620842/228266830-003e4d11-dc2c-468a-90e6-d014897649d0.png)

![34](https://user-images.githubusercontent.com/120620842/228266920-57ed130b-9696-4752-8112-b55377f843cc.png)

# Finding null values and cleaning it

![35](https://user-images.githubusercontent.com/120620842/228267110-21e89b81-c4b4-4352-90b3-528ee177ee36.png)

# Value counts of "Postal Code"

![36](https://user-images.githubusercontent.com/120620842/228267334-691608a2-305d-40dc-8ec2-9ef7494d05af.png)

# Distribution of Data

![37](https://user-images.githubusercontent.com/120620842/228267490-07d07778-520b-408a-8c4c-308ba2cc1873.png)

# Univariate Analysis

![38](https://user-images.githubusercontent.com/120620842/228267753-4202b9aa-5192-4402-a2f9-fb7c8b8ef812.png)

![39](https://user-images.githubusercontent.com/120620842/228267856-96eccc3f-728f-440c-83cd-b90652853948.png)

![40](https://user-images.githubusercontent.com/120620842/228267965-e07cd661-a42c-4408-a728-a9e6f6e542c7.png)

![41](https://user-images.githubusercontent.com/120620842/228268601-566ea5f5-fe07-4691-9182-696e4e48d979.png)

![42](https://user-images.githubusercontent.com/120620842/228268656-4d2f127a-e8ba-4dc0-a7e7-c233576e3617.png)

# CODE 2

```
import pandas as pd
import seaborn as sns
df1=pd.read_csv("diabetes.csv")
print(df1)
df1.info()
df1.dtypes
df1.skew()
df1.describe()
sns.boxplot(x='Glucose',data=df1)
sns.countplot(x="Glucose",data=df1)
sns.displot(df1["Glucose"]) 
sns.histplot(x="Glucose",data=df1)
df1.skew()
df1.kurtosis()
sns.boxplot(x="Insulin",data=df1)
```
# EDA - diabetes.csv

![WhatsApp Image 2023-03-28 at 10 07 04 PM](https://user-images.githubusercontent.com/120620842/228314134-19535e94-c39d-4d15-b2fe-b357273fb9a4.jpeg)

# Displaying information about Dataset

![WhatsApp Image 2023-03-28 at 10 07 04 PM (1)](https://user-images.githubusercontent.com/120620842/228314504-1780e4d4-a19f-49b4-8ed8-9fef1d60f681.jpeg)

![WhatsApp Image 2023-03-28 at 10 07 04 PM (2)](https://user-images.githubusercontent.com/120620842/228315268-7fc67009-3b43-4d2b-bbb1-967f5ad4fb60.jpeg)

![WhatsApp Image 2023-03-28 at 10 07 04 PM (5)](https://user-images.githubusercontent.com/120620842/228316400-51e096fb-6a3e-4efa-b73a-2f7d3121b2d3.jpeg)

## Univariate analysis

![WhatsApp Image 2023-03-28 at 10 07 04 PM (6)](https://user-images.githubusercontent.com/120620842/228316621-442cd182-b6cc-4763-8443-af3de270a8a6.jpeg)

![WhatsApp Image 2023-03-28 at 10 07 04 PM (7)](https://user-images.githubusercontent.com/120620842/228316784-83efbfb2-497b-49f7-b96a-49e150dbad83.jpeg)

![WhatsApp Image 2023-03-28 at 10 07 04 PM (8)](https://user-images.githubusercontent.com/120620842/228317002-0cc9c2d6-04b1-4772-81f3-aa94516ef83c.jpeg)

![WhatsApp Image 2023-03-28 at 10 45 12 PM](https://user-images.githubusercontent.com/120620842/228318019-83e3cf21-edf2-4833-b6cb-19d3e3d36dd7.jpeg)

## Distribution of data

![WhatsApp Image 2023-03-28 at 10 07 04 PM (9)](https://user-images.githubusercontent.com/120620842/228317642-ec99a504-31e0-482a-a023-b5e9e698b2d4.jpeg)

![WhatsApp Image 2023-03-28 at 10 07 04 PM (10)](https://user-images.githubusercontent.com/120620842/228317786-96a18279-e431-4de0-9d94-fe28011ea003.jpeg)

![WhatsApp Image 2023-03-28 at 10 07 04 PM (11)](https://user-images.githubusercontent.com/120620842/228317874-31237d6f-66d3-4afa-956a-8abab05c93be.jpeg)

# RESULT
Thus the program to perform EDA on the given data set is successfully executed.
