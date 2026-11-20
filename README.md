# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 28.10.26
NAME: KANNADHASAN J
REG NO : 212224240071


DATASET:BMW SALES(2010-2024)

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("/content/BMW sales data (2010-2024).csv")

# Check columns
print(data.columns)

# Plot BMW sales volume by year
yearly_sales = data.groupby('Year')['Sales_Volume'].sum()

plt.figure(figsize=(12, 6))
plt.plot(yearly_sales.index, yearly_sales.values, marker='o', linewidth=2)

plt.title('BMW Sales Volume (2010–2024)')
plt.xlabel('Year')
plt.ylabel('Sales Volume')
plt.grid(True)
plt.xticks(yearly_sales.index, rotation=45)
plt.tight_layout()
plt.show()


```
# OUTPUT:

<img width="1211" height="626" alt="image" src="https://github.com/user-attachments/assets/190cc666-bf29-46ac-9d3a-a736cfdcb1fa" />


# RESULT:
Thus we have created the python code for plotting the time series of given data.
