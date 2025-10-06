# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas and matplot libraries.
2. import Kmeans algorithm to solve customer segmentation.
3. Using the for loop cluster the given data
4. Predict the output and plot data graphs.
5. Display the outputs

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Rogith J
RegisterNumber: 212224040280 
*/
import pandas as pd 
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
data.info()
print("Name:Rogith J")
print("Reg no:212224040280")
print("Name:Rogith J")
print("Reg no:212224040280")
data.head()
print("Name:Rogith J")
print("Reg no:212224040280")
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
    kmeans=KMeans(n_clusters=i,init="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
print("Name:Rogith J")
print("Reg no:212224040280")
plt.plot(range(1,11),wcss)
plt.xlabel("No.of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
KMeans(n_clusters=5)
y_pred=km.predict(df.iloc[:,3:])
y_pred
print("Name:Rogith J")
print("Reg no:212224040280")
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
```

## Output:
DATA.INFO()
<img width="539" height="332" alt="Screenshot 2025-10-06 114106" src="https://github.com/user-attachments/assets/9c1b6b6a-269e-481f-8504-5f47dcb04ad8" />
DATA.HEAD()
<img width="711" height="279" alt="Screenshot 2025-10-06 114115" src="https://github.com/user-attachments/assets/aa358e77-f727-45e3-8f49-7456acab30aa" />
DATA.ISNULL().SUM()
<img width="656" height="227" alt="Screenshot 2025-10-06 114121" src="https://github.com/user-attachments/assets/26da7678-d6e6-4352-80ff-9ee506ea79d0" />
ELBOW METHOD
<img width="959" height="671" alt="Screenshot 2025-10-06 114132" src="https://github.com/user-attachments/assets/15487ef1-901e-444c-b521-8a750b4c266d" />
Y_PRED
<img width="809" height="227" alt="Screenshot 2025-10-06 114153" src="https://github.com/user-attachments/assets/8cbecd53-b1b5-4fc0-9c46-3730333736e5" />
CUSTOMER SEGMENT
<img width="903" height="643" alt="Screenshot 2025-10-06 114203" src="https://github.com/user-attachments/assets/19dd6928-800b-4ddb-a4ac-a26ae8d62951" />

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
