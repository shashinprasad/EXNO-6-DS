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
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/1b5ce4e3-5cb2-437d-96f2-61600f5444bc)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/af4a29a9-6aa7-472a-945a-cc2d9e716354)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/21df4270-ca53-45f9-aafd-4ffb8d650b71)
```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/a7f1dc36-df3b-4ba6-8679-15759309e5e5)
```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/4f93be52-db5d-46b6-a056-9e055f8e8273)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/64ae7a1a-56ad-4ce9-8889-11ef84121014)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/895eb59e-21af-459d-b20e-99b5db4e0672)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/3aac7616-329b-44b4-b8d7-ad51d1ed4bdf)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/24f7f2eb-9bda-4446-a39f-77aaaab3bd75)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/e4572c14-0e5c-4835-9b3f-3914d82ddbbd)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/fcf51fa9-9ee6-46a1-82ae-fe6ee1396244)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/af8e2013-2c59-44c1-b7ad-9872eefd86d9)
```
num_var = np.random.randn(1)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/d5c2e2ce-7b82-43c0-9e94-a06f89dac028)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/4ae184a6-3e55-4f10-8127-9d984727251d)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/02200da3-50a6-4d5d-9c5c-04df9a023b7d)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/eb020490-1ad1-4624-bacf-96b2ce3e169a)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/d7953012-dffe-4bbe-ae79-310ebda397ab)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/463d06cd-612b-4232-9c5e-b7364d4cd52d)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/a269eb9f-7a43-4094-8978-bbdb5df610f6)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/5273bb01-dfb4-47e1-a965-4050f11e5530)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/4725aea4-296e-49d6-b092-9c9863bf4aeb)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/5e9669d5-efc0-406a-8580-9fa8be2ac850)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/c19b8c08-aa7b-473d-b298-ee83d8cf9c9d)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/8cbb34f5-0b9e-4dd8-94b2-ea0a9df31512)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/783bbb37-edc5-43ce-9403-cddc70b2e2cc)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/d63dbda4-42b7-4622-90e6-f5845e6f9775)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/guru14789/EXNO-6-DS/assets/151705853/b83e6929-cea3-4d6b-8aa7-1654409f32a3)

# Result:

Thus, all the data visualization techniques of Seaborn has been implemented.
