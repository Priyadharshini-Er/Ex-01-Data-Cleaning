# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
``` 
Name : Priyadharshini P
Register Number : 212222100039

*Data Cleaning - Data_set.csv*
import pandas as pd 
df = pd.read_csv("/content/Data_set.csv")
import numpy as np
import pandas as pd
import seaborn as sbn
df = pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on'] = df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network'] = df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] =df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers'] = df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```

# OUPUT
# OUTPUT FOR DATA 1
![image](https://user-images.githubusercontent.com/119558093/229698308-58fb51fe-d87f-4884-a3a8-4c0a8d1ed740.png)
# Before cleaning
![dsbeforecleaning1](https://user-images.githubusercontent.com/119558093/229698503-2340deec-1e75-4e59-b59e-a1aaeab4f584.png)
# Mode
![dsmode](https://user-images.githubusercontent.com/119558093/229698651-0d2984d2-1fed-4787-87ab-39b507e1b3c5.png)
# Mean
![dsmean](https://user-images.githubusercontent.com/119558093/229698745-7f6e9103-6020-4387-bf06-077f4e815a8d.png)
# Median
![dsmedian](https://user-images.githubusercontent.com/119558093/229698856-bf473fa6-5c87-4bea-91f9-ee88c4d5fd8d.png)
# After Cleaning
![dsaftercleaning](https://user-images.githubusercontent.com/119558093/229698968-0eb9232c-a5e6-4b90-a7e1-f298fee92754.png)

# CODE FOR DATA 2
```
Name :PRIYADHARSHINI P
Register Number : 212222100039
mport pandas as pd
import numpy as np
import seaborn as sns
from google.colab import files
uploaded = files.upload()
df = pd.read_csv("Loan_data.csv")
df
df.head(5)
df.describe()
df.info()
df.tail()
df.isnull()
df.isnull().sum()
df.shape
df.columns
df.duplicated()
df['Gender'] = df["Gender"].fillna(df['Gender'].mode()[0])
df['Married'] = df["Married"].fillna(df['Married'].mode()[0])
df['Self_Employed'] = df["Self_Employed"].fillna(df['Self_Employed'].mode()[0])
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].mean())
df['Loan_Amount_Term'] = df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['Credit_History'] = df['Credit_History'].fillna(df['Credit_History'].mean())
sns.boxplot(y="LoanAmount",data=df)
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].median())
df.head()
df.isnull().sum()
df.info()
```

# OUTPUT FOR DATA 2
![dsdata 2](https://user-images.githubusercontent.com/119558093/229699204-0eef5411-9392-4ce0-840e-0bc5ab247e21.png)
![dsdata20](https://user-images.githubusercontent.com/119558093/229699288-8234265e-3207-4ca6-9abd-334bf2043709.png)
# BEFORE CLEANING
![dsbeforecelaning2](https://user-images.githubusercontent.com/119558093/229699413-82c592a5-f80b-41b2-9880-b87009b6f58c.png)
![dsbeforeclea22](https://user-images.githubusercontent.com/119558093/229699545-a2bdbd55-fb74-4fca-b49c-0677d826c0e9.png)
![dsbeforeclean23](https://user-images.githubusercontent.com/119558093/229699576-59867284-c13c-4415-ad4c-18bb8db6e97e.png)
![dsbeforecelan24](https://user-images.githubusercontent.com/119558093/229699604-e47b1b80-445d-4463-8a23-ebd86583bca8.png)
# MODE
![dsmode2](https://user-images.githubusercontent.com/119558093/229699743-95aaefdb-49ed-439f-8648-5f19a94e4ee8.png)
# MEAN
![dsmean2](https://user-images.githubusercontent.com/119558093/229699861-c33bd93d-fe3c-4229-9f88-13438d30da66.png)
# MEDIAN
![dsmeadian2](https://user-images.githubusercontent.com/119558093/229699970-d8435cea-d4d8-4c46-ad1a-552376c46523.png)
# AFTER CLEANING
![dsafterclean](https://user-images.githubusercontent.com/119558093/229700123-b7d63c07-00c0-4150-b097-d3ad9125c6c0.png)

# RESULT
Thus the given data is read,cleansed and cleaned data is saved into the file
