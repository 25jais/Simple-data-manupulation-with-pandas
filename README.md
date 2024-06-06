# Simple-data-manupulation-with-pandas
Q1:Learn how to read CSV files and manipulate
data frames using Pandas.
import pandas as pd

# Read CSV file into a DataFrame
df = pd.read_csv('data.csv')

# Display the first few rows of the DataFrame
print(df.head())
# Read CSV file into a DataFrame
df = pd.read_csv('data.csv')

# Display the first few rows of the DataFrame
print(df.head())

# Basic statistics of numerical columns
print(df.describe())

# Drop rows with missing values
df_cleaned = df.dropna()

# Fill missing values with 0
df_filled = df.fillna(0)

# Drop duplicate rows
df_no_duplicates = df.drop_duplicates()

# Accessing specific columns
print(df['column_name'])

# Accessing specific rows
print(df.loc[0])  # Access the first row
print(df.iloc[0]) # Access the row by index

# Slicing rows and columns
print(df.loc[0:5, 'column_name_1':'column_name_3'])


Q2:2. Perform simple data cleaning tasks such as
handling missing values and removing
duplicates.

import pandas as pd

# Sample DataFrame
data = {
    'A': [1, 2, None, 4, 5],
    'B': [None, 6, 7, 8, 9],
    'C': ['a', 'b', 'c', 'd', 'e']
}

df = pd.DataFrame(data)

# Handling missing values
df_cleaned = df.dropna()  # Remove rows with any missing values
# df_cleaned = df.dropna(subset=['A', 'B'])  # Remove rows with missing values in specific columns

# Removing duplicates
df_cleaned = df_cleaned.drop_duplicates()

print(df_cleaned)
3. Practice basic data manipulation operations
like filtering, sorting, and grouping data.

import pandas as pd

# Sample DataFrame
data = {
    'A': [1, 2, 3, 4, 5],
    'B': [6, 7, 8, 9, 10],
    'C': ['X', 'Y', 'X', 'Y', 'Z']
}

df = pd.DataFrame(data)

# Filtering Data
filtered_data = df[df['A'] > 2]  # Filter rows where column 'A' is greater than 2
print("Filtered Data:")
print(filtered_data)

# Sorting Data
sorted_data = df.sort_values(by='B', ascending=False)  # Sort DataFrame by column 'B' in descending order
print("\nSorted Data:")
print(sorted_data)

# Grouping Data
grouped_data = df.groupby('C')['A'].mean()  # Group data by values in column 'C' and calculate the mean of column 'A' for each group
print("\nGrouped Data:")
print(grouped_data)
