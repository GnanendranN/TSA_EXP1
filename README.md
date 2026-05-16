# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 16-05-2026

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

```py
import pandas as pd
from matplotlib import pyplot as plt

df = pd.read_csv('/content/drive/MyDrive/Time_Series/nasa_exoplanet_intelligence.csv')
df.head(10)

df['disc_year'] = pd.to_datetime(df['disc_year'], format='%Y')

df.dtypes

yearly_data = df.groupby('disc_year')['star_temp_k'].mean()

yearly_data.plot(kind='line', marker='o')
plt.title('Average Temperature of Stars')
plt.xlabel('Year')
plt.ylabel('Average Temperature in Kelvin')
plt.grid(True)
plt.show()

```

# OUTPUT:
<img width="671" height="429" alt="image" src="https://github.com/user-attachments/assets/50c140c3-b6db-4a9d-9488-240d483a634a" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
