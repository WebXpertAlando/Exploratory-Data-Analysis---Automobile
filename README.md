# Exploratory-Data-Analysis---Automobile
## Introduction
Exploratory Data Analysis or EDA is an approach to analyze data data in order to:

- Summerize main characteristics of data.
- Gain better understanding of the dataset.
- Uncover relationships between variables and extract important variables for the problem we are trying to solve.
### Objectives:
  What are the characteristics that have the most impact on the car price?

 We will learn:
 - Descriptive statistics which describes basic features of dataset and obtain a short summery about the sample and measures of the data.
 - Perform Data Preprocessing e.g. Data Cleaning by checking Missing Values, Duplicates, Outliers.
 - Perform  Data Visualization on th dataset.
 - Basic grouping of data using GroupBy and how this can help to transform the dataset.
 - The correlation between different variables
 - Advanced correlation, where we can introduce various correlation statistics method, namely:

   1. **Pearson correlation**
   2. **Correlation Heatmaps**
   3. **Predicting Price Using Linear Regression**
  - Predict Price using the famous model Linear Regression from scikit learn.

# Python Implementation of Exploratotry Data Analysis(EDA)
### Libray Used:
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit Learn
- Scipy

### Data Source: Kaggle (Automobile)

```Python
# Load dataset
df = pd.read_csv("automobileEDA.csv")
df
```
<img width="1000" height="398" alt="Screenshot at 2025-09-18 14-09-44" src="https://github.com/user-attachments/assets/8f71b691-ec2e-4a01-b74e-dcb9a7855081" />

# Data Preprocessing
### Data Cleaning
##### Check for Missing Values




# Descriptive Statistics and Short Summary of the data. 
```Python
df.describe(include = "all")
```
<img width="999" height="362" alt="Screenshot at 2025-09-18 14-17-00" src="https://github.com/user-attachments/assets/1578e80d-5fc2-49cd-926d-cf58ac4a5544" />

There are variables that can be divided up into different categories or grouped and have discrete values e.g in our dataset, we have drive system as a categorical value which consists of categories forward wheel-drivel, rear wheel-drive and four wheel-drive.

One way of summerizing the categorical data is by using the function call **value_counts()**

```Python
# Count of Categorical Column Drive-Wheels
drive_wheel_col_counts = df['drive-wheels'].value_counts()
drive_wheel_col_counts
```

<img width="989" height="80" alt="Screenshot at 2025-09-18 14-41-12" src="https://github.com/user-attachments/assets/82e98aad-7712-4197-9444-7a9d7dca9578" />

As we can see there are 118 cars with the front wheel-drive category, 75 cars in the rear wheel-drive category and finally 8 cars in the four wheeel-drive category. We can perform as many as summary as we want provided that we already know our categorical columns with discrete values. 

```Python
# Count of Categorical Column engine-type
engine_type_col_counts = df['engine-type'].value_counts()
engine_type_col_counts 
```
<img width="996" height="127" alt="Screenshot at 2025-09-18 15-02-36" src="https://github.com/user-attachments/assets/3b402c39-bd81-4e76-b0ad-27561ee2b18c" />


  
## Data Visualization  
