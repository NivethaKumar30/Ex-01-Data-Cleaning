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
import pandas as pd
df=pd.read_csv("/content/Data_set.csv")
print(df)
df.head(5)
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
```
#loan_data
import pandas as pd
df = pd.read_csv("/content/Loan_data.csv")
df.head(5)
df.info()
df.isnull().sum()
#MODE:
df['Gender'] = df['Gender'].fillna(df['Gender'].mode()[0])
df['Self_Employed'] = df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Dependents'] = df['Dependents'].fillna(df['Dependents'].mode()[0])
#MEAN and MEDIAN:
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].median())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].mean())
df.isnull().sum()
```
# OUPUT
First File:

Data_Set.csv FILE

![ds6](https://user-images.githubusercontent.com/119559844/226415678-e6eab64a-1054-4c70-9028-0c874e56dfd3.png)


INFO

![ds7](https://user-images.githubusercontent.com/119559844/226415997-af8c9b49-f88d-419f-835c-ffccb546ae27.png)

Isnull.().sum() before cleaning

![ds 3](https://user-images.githubusercontent.com/119559844/229988412-0d5e2523-e86a-4222-bae4-d15d9203cb13.png)


MODE,MEAN and FORWARD METHOD


![frwd](https://user-images.githubusercontent.com/119559844/229993986-0b9d82d7-e471-4820-b997-4a3afaa78fcd.png)



isnull().sum() after cleaning

![ds 2](https://user-images.githubusercontent.com/119559844/226420112-f0d55253-947f-4d7a-90e3-51f7ab31f55e.png)



Second File:

Loan_Data.csv FILE

![ds 2 2](https://user-images.githubusercontent.com/119559844/229989582-9f95bcfd-3b93-47a4-bf88-8777b84e7df4.png)


INFO

![df info1](https://user-images.githubusercontent.com/119559844/229991179-183c6343-713b-4c5b-934d-5e38b6634720.png)


Isnull.().sum() before cleaning

![isnull](https://user-images.githubusercontent.com/119559844/229991358-7b2815d6-3493-416f-855d-68c675528d83.png)


MODE,MEAN and MEDIAN

![mean and median ](https://user-images.githubusercontent.com/119559844/229991439-b42a5d66-7cd4-4d58-8c33-5633011ec5cd.png)

isnull().sum() after cleaning

![isnull1](https://user-images.githubusercontent.com/119559844/229991478-945212e6-0508-44b9-86bd-2d22920f55b7.png)


# RESULT :

Thus the given data is read,cleansed and cleaned data is saved into the file.


