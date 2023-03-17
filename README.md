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

# CODE:
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
 
# OUTPUT:
![image](https://user-images.githubusercontent.com/113017853/190085557-810d3d45-503b-4fe7-a1bc-d0e6fa18f2da.png)

![image](https://user-images.githubusercontent.com/113017853/190085599-8ee1fd70-9381-4307-972f-8e480488b6d0.png)

![image](https://user-images.githubusercontent.com/113017853/190085648-3703b56d-bd84-44e9-9cc5-489dd5c748d3.png)

![image](https://user-images.githubusercontent.com/113017853/190085718-a76aee47-7dda-4dae-91f4-a3ea69630d7b.png)

![image](https://user-images.githubusercontent.com/113017853/190085773-afbf9a0a-5c6a-4710-80ff-19b2dc3ac729.png)

![image](https://user-images.githubusercontent.com/113017853/190085860-ba59732c-6af9-4910-bdf3-0302fa717f6b.png)

![image](https://user-images.githubusercontent.com/113017853/190085921-7a3d9efa-f14f-41da-b9d8-d36c44e6aa99.png)

##RESULT:

Hence the given data is read and perform data cleaning and save the cleaned data to a file.
