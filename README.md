# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
## NAME: POOJASRI L
## REG.NO:212223220076

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1416" height="257" alt="image" src="https://github.com/user-attachments/assets/92fb7bb1-b6f5-4cdb-80c1-1fe5b4b9d55f" />


```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="723" height="580" alt="image" src="https://github.com/user-attachments/assets/69f487f5-9fba-487d-b728-5cead3798889" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="737" height="571" alt="image" src="https://github.com/user-attachments/assets/355ef598-92ad-4e0d-8eb5-00ca4df3caac" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="912" height="582" alt="image" src="https://github.com/user-attachments/assets/1f608446-9f50-421a-ab80-5ad2fdb86747" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="813" height="563" alt="image" src="https://github.com/user-attachments/assets/74c62b6f-117a-468f-be12-2ee7279169b2" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="830" height="585" alt="image" src="https://github.com/user-attachments/assets/e5f17d08-9d73-4dc2-81c7-3212788f18f3" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="812" height="577" alt="image" src="https://github.com/user-attachments/assets/8de8a99c-9f16-4a72-89ec-4a4681d7ed43" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="757" height="597" alt="image" src="https://github.com/user-attachments/assets/0831abf6-778b-484b-8b0c-a0545c46d8ce" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="772" height="572" alt="image" src="https://github.com/user-attachments/assets/a3f34177-ea06-4f3e-accb-963987b49176" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="827" height="612" alt="image" src="https://github.com/user-attachments/assets/484db00e-66ce-475e-ad23-8d799eaffea1" />


```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="835" height="637" alt="image" src="https://github.com/user-attachments/assets/dbea722b-6097-4dce-86a9-74a41fb45c45" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
