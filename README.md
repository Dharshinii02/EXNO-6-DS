# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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
df=pd.read_csv("C:\\Users\\admin\\Downloads\\titanic_dataset (1).csv")
df.head()
```

<img width="1416" height="456" alt="image" src="https://github.com/user-attachments/assets/4d7d2f5d-52fe-458b-825a-15f68ebbff5e" />


```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="1133" height="602" alt="image" src="https://github.com/user-attachments/assets/dd862ac0-0c7f-49b6-bf02-4efa894a9a68" />


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

<img width="813" height="613" alt="image" src="https://github.com/user-attachments/assets/b08664cb-50a4-474f-b8a3-0a49ad1d5953" />


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="851" height="558" alt="image" src="https://github.com/user-attachments/assets/12f84d14-96b2-48c9-bb2d-ffe773704a3c" />


```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="810" height="557" alt="image" src="https://github.com/user-attachments/assets/de252260-5c69-42f8-8541-361bf73b96c9" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

```

<img width="831" height="542" alt="image" src="https://github.com/user-attachments/assets/6e8060d3-d998-4053-bc14-5cdb4d8fcc44" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="855" height="582" alt="image" src="https://github.com/user-attachments/assets/8e4c8ca1-ba96-42e2-b734-c219685d3fff" />


```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="825" height="577" alt="image" src="https://github.com/user-attachments/assets/b508db40-8454-476f-8cce-8f9d5634fc22" />


```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```

<img width="836" height="577" alt="image" src="https://github.com/user-attachments/assets/d460987b-95bf-4a98-9f34-4bf96dd0a9e1" />


```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```


<img width="806" height="536" alt="image" src="https://github.com/user-attachments/assets/534d784f-82fb-4a9a-ae13-2907add3e24a" />



```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```


<img width="802" height="630" alt="image" src="https://github.com/user-attachments/assets/a3dbf2df-997f-4f93-b5d8-09a06a14583e" />







# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
