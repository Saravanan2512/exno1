# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(5)
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'])
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
# OUTPUT
 READ_CSV
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/084ba31c-5460-4c42-9f56-701be0df9a3c)
 HEAD
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/dd8c11fa-4c18-4435-94fb-b8a96cf8a630)
 TAIL
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/083ecd66-7fd2-467c-bf31-3fcc23a1c87a)
 INFO
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/d44617a2-bdc2-4437-9530-14911f38f3b4)
 ISNULL
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/5dcc0aa0-9370-4757-a277-9eba1ba97cf9)
 ISNULL_SUM
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/b82b82fa-d2e2-46ab-81ef-f3025a2ff1df)
 MEAN
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/0037257f-f2b6-472b-976a-b512d2d0a6d8)
 DROPNA
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/471b7f77-6502-4f20-a5de-640c3504f26c)
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/04bb7e1c-c436-468d-9261-4a6f41fccdb1)
 FILLNA
 ![image](https://github.com/Saravanan2512/exno1/assets/144979117/6eeb76bb-dee5-4bc9-9818-a46a8ad8e2c5)

# RESULT
The data clearning has beeen done successfully.

 






         
