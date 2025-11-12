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
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
<img width="569" height="400" alt="image" src="https://github.com/user-attachments/assets/94fb23c6-3035-48dc-8f1d-0f8f4d45b4a6" />

```
df=sns.load_dataset("tips")
df
```
<img width="399" height="328" alt="image" src="https://github.com/user-attachments/assets/1ac66c7f-e466-41ee-9a55-add7545259ec" />

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
<img width="589" height="406" alt="image" src="https://github.com/user-attachments/assets/68f385da-5d80-4efc-a74a-2d6eede09bd5" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-:Line Plot')
plt.xlabel('X-Label')
plt.ylabel('Y-Label')
```
<img width="591" height="418" alt="image" src="https://github.com/user-attachments/assets/fa1e9cd5-e68d-4447-9162-2c2bdb350c52" />

```
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
<img width="729" height="518" alt="image" src="https://github.com/user-attachments/assets/8507603e-4dd5-4e99-aa66-c218fb0792ac" />

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
<img width="657" height="440" alt="image" src="https://github.com/user-attachments/assets/224284ab-d48e-4cbc-894e-907ddf2c4869" />

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```
<img width="597" height="407" alt="image" src="https://github.com/user-attachments/assets/c21ca2f3-e7b0-4991-b18f-2ea095bac4a0" />

```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
<img width="640" height="428" alt="image" src="https://github.com/user-attachments/assets/fe123417-8b94-4ec8-b849-f17e9d36ee28" />

```
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset (2).csv")
tit
```
<img width="751" height="455" alt="image" src="https://github.com/user-attachments/assets/cdddfe9d-5a1d-4fad-acee-bb7a156c91ee" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
<img width="686" height="442" alt="image" src="https://github.com/user-attachments/assets/dfbc3a93-4496-4ae3-920b-1d21fd35c3d9" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')
plt.title("Fare of Passenger by Embarked Town,Divided by Class")
```
<img width="750" height="446" alt="image" src="https://github.com/user-attachments/assets/362f52c6-ee2d-4a93-abe2-0ff7fd9b7807" />

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
<img width="680" height="432" alt="image" src="https://github.com/user-attachments/assets/09e0b808-d690-4f16-a175-e81c2dbf7fa3" />

```
import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical Variable")
num_var
```
<img width="420" height="206" alt="image" src="https://github.com/user-attachments/assets/966c14c3-3c17-4afb-a3f9-5476281e31cb" />

```
sns.histplot(data=num_var,kde=True)
```
<img width="580" height="411" alt="image" src="https://github.com/user-attachments/assets/6949722a-92f3-478e-a96d-3c2561126bec" />

```
sns.histplot(data=tit,x="Pclass",hue="Survived",kde=True)
```
<img width="685" height="405" alt="image" src="https://github.com/user-attachments/assets/4a06ca61-5121-4643-b4a5-331b315e312f" />

```
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
```
<img width="616" height="336" alt="image" src="https://github.com/user-attachments/assets/0b6f7d93-0a60-4c06-8b68-a88e5533ba17" />

```
sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of Student Marks')
```
<img width="624" height="421" alt="image" src="https://github.com/user-attachments/assets/504c1b0e-4e06-4a19-b2f3-087a8f2d9095" />

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```
<img width="604" height="418" alt="image" src="https://github.com/user-attachments/assets/d2ee8ebb-9209-4df3-931c-6e26ca656a56" />

```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
            whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
<img width="630" height="405" alt="image" src="https://github.com/user-attachments/assets/7ab41462-3dd3-4ce2-a7f4-465f75c67e7c" />

```
sns.boxplot(x='Pclass',y='Age',data=tit,palette='rainbow')
plt.title("Age by Passenger Class,Titanic")
```
<img width="631" height="428" alt="image" src="https://github.com/user-attachments/assets/540b2dc2-371b-4beb-8c59-206656be736d" />

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set3",inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
<img width="729" height="424" alt="image" src="https://github.com/user-attachments/assets/1ee71f91-9b11-4807-8793-4e6c13d5acd9" />

```
import seaborn as sns
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip)
```
<img width="731" height="424" alt="image" src="https://github.com/user-attachments/assets/561a73d6-f35f-40c9-b4b1-a612b0dca9e0" />

```
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
<img width="561" height="429" alt="image" src="https://github.com/user-attachments/assets/4e84b2ec-7fdd-4774-a81f-5b5813089a12" />

```
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x="tip",y="day",data=tip)
```
<img width="603" height="422" alt="image" src="https://github.com/user-attachments/assets/da20ce05-6f61-4f88-8da2-13e1c1636df5" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set3',alpha=0.8)
```
<img width="669" height="421" alt="image" src="https://github.com/user-attachments/assets/aa181474-2b0c-46af-95d9-85fc2bf46d63" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
```
<img width="695" height="407" alt="image" src="https://github.com/user-attachments/assets/c53015d7-5d08-475b-b4e6-fa5c556d204d" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
```
<img width="587" height="408" alt="image" src="https://github.com/user-attachments/assets/3a2405f8-b615-46f8-9521-748f36713fbf" />

```
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted:\n")
print(data)
```
<img width="310" height="210" alt="image" src="https://github.com/user-attachments/assets/9f9aa793-4495-4816-bdeb-ef6529dd8668" />

```
hm = sns.heatmap(data=data, annot=True, fmt=".1f", cmap="coolwarm")
```
<img width="493" height="379" alt="image" src="https://github.com/user-attachments/assets/5e5521da-cb05-4ff9-9b4c-442ae4549966" />

```
tips=sns.load_dataset('tips')
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap="plasma",linewidth=0.5)
```
<img width="574" height="399" alt="image" src="https://github.com/user-attachments/assets/f56c02b7-51e0-485c-96f2-26384b978c0f" />


# Result:
 Data Visualization using seaborn python library for the given datas has been performed successfully.
