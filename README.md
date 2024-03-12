# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 21.02.2024

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
## POPULATION:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2015"].mean()
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()
```

## MARKET PRICE:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```

## TEMPERATURE:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```

# OUTPUT:
## POPULATION:
![1](https://github.com/saieswar1607/TSA_EXP1/assets/93427011/41ef6f2e-be9c-4310-b504-a4be6a9478cc)

## MARKET PRICE:
![2](https://github.com/saieswar1607/TSA_EXP1/assets/93427011/b873948f-22b3-4167-b0ca-e5842dfae927)
![3](https://github.com/saieswar1607/TSA_EXP1/assets/93427011/d6006f36-07e0-44fd-bda0-13bccf2b9951)

## TEMPERATURE:
![4](https://github.com/saieswar1607/TSA_EXP1/assets/93427011/bdc65c06-d5b7-4f5a-b848-07b057018115)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
