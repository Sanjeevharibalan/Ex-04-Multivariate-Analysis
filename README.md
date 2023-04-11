# Ex-04-Multivariate-Analysis

## AIM:

   To Perform Multivariate Analysis
## ALGORITHM:

1.Read the given data

2.Get information from the data

3.Perform the Multivariate Analysis

4.Save the clean data to file

## PROGRAM:

1.reading the file

import pandas as pd

import seaborn as sns

df=pd.read_csv("/content/SuperStore.csv")

data=df

2.Scatterplot

import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

sns.scatterplot (df['Postal Code'],df['Sales'])


3.Barplot

import pandas as pd

import seaborn as sns

sns.barplot (x=df["Postal Code"], y=df["Sales"], data=df)




4. Scatterplot

import pandas as pd

import seaborn as sns

sns.scatterplot(df["Postal Code"], y=df["Sales"], hue=df['Row ID'])



5.
  df.info()
  

  
 6. 
 
 states=df.loc[:,["Postal Code","Sales"]]

states=states.groupby(by=["Postal Code"]).sum().sort_values(by="Sales")

sns.barplot(x=states.index,y="Sales",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Postal Code")

plt.ylabel=("SALES")

plt.show()



7.

states=df.loc[:,["Segment","Sales"]]

states=states.groupby(by=["Segment"]).sum().sort_values(by="Sales")

#plt.figure(figsize=(10,7))

sns.barplot(x=states.index,y="Sales",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Segment")

plt.ylabel=("Sales")

plt.show()



8.



## OUTPUT:

![Screenshot (165)](https://user-images.githubusercontent.com/86832944/194208499-d28a7e1b-9e25-4f0e-881a-79af9dd58c30.png)
![Screenshot (167)](https://user-images.githubusercontent.com/86832944/194209071-a2100cbc-db7d-4229-86ae-a10854bd7b46.png)
![Screenshot (171)](https://user-images.githubusercontent.com/86832944/194209468-d244fd02-d863-436d-868c-aff2852430ef.png)
![Screenshot (168)](https://user-images.githubusercontent.com/86832944/194209230-233a9588-6690-4364-be0d-9178ee616727.png)
![Screenshot (169)](https://user-images.githubusercontent.com/86832944/194209587-2ce61dd3-3a22-4b7f-8faa-ca6b883ffc35.png)
![Screenshot (172)](https://user-images.githubusercontent.com/86832944/194209698-5e4bf0c6-a315-4309-bf25-5b5de3a714ad.png)
![Screenshot (173)](https://user-images.githubusercontent.com/86832944/194209735-ff63adcc-3898-4587-bd2c-b6d42045fe30.png)

## RESULT: 
 
Thus, Multivariate-Analysis is performed on given data and saved successfully.












