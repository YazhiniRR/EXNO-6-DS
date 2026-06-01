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

# Name: A.Rafshaan ahmed
# Reg.no: 212224230214
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
# 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="489" height="382" alt="image" src="https://github.com/user-attachments/assets/29b9b7ac-b7c4-45ec-b4f3-58d4774ad35c" />

# 2.Multi Line Plot
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

<img width="479" height="391" alt="image" src="https://github.com/user-attachments/assets/02324c6d-fec7-4931-990d-5c6e2c7a66aa" />

# TO VISUALIZE RELATIONSHIPS
# 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="680" height="405" alt="image" src="https://github.com/user-attachments/assets/75b6f58c-524c-489c-af01-1754f2d9e030" />

# 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="538" height="392" alt="image" src="https://github.com/user-attachments/assets/fdcb9c98-cce4-48e8-aea0-28635ff8fff9" />

# 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="556" height="397" alt="image" src="https://github.com/user-attachments/assets/4cd7edd4-4056-4485-8085-d17266303014" />

# TO CAPTURE DISTRIBUTIONS
# 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="577" height="383" alt="image" src="https://github.com/user-attachments/assets/366d6144-4646-44c9-ad5a-846adc5d2238" />

# 2.Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="544" height="385" alt="image" src="https://github.com/user-attachments/assets/a2adc478-5b06-43fe-b053-547a85a57400" />

# 3.Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="516" height="397" alt="image" src="https://github.com/user-attachments/assets/2b37a898-bbaf-40be-b5e8-a16f6ed10fc4" />

# 4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="512" height="393" alt="image" src="https://github.com/user-attachments/assets/a4f62626-fee3-478a-9dd3-1558fe06f28c" />

# 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="596" height="440" alt="image" src="https://github.com/user-attachments/assets/5dca8b12-9691-49c7-8f3b-fa11de0b6f5f" />


# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
