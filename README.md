<H3>ENTER YOUR NAME: JEEVANESH</H3>
<H3>ENTER YOUR REGISTER NO.: 212222243002</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
Import Libraries

```

from google.colab import files
import pandas as pd
import seaborn as sns
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
from scipy import stats
import numpy as np
```

Read the dataset

```
df=pd.read_csv("Churn_Modelling.csv")
```

Checking Data
```
df.head()
df.tail()
df.columns
```

Check the missing data
```
df.isnull().sum()
```

Check for Duplicates
```
df.duplicated()
```
Assigning Y
```
y = df.iloc[:, -1].values
print(y)
```

Check for duplicates
```
df.duplicated()
```

Check for outliers
```
df.describe()
```

Dropping string values data from dataset
```
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
data.head()
```

Normalize the dataset
```
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```

Split the dataset
```
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```

Training and testing model
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```

## OUTPUT:
Data:
![image](https://github.com/user-attachments/assets/d12e30e8-2ec6-4f3e-8071-71e0f29e59f5)

Data checking:
![image](https://github.com/user-attachments/assets/13eeaaa3-9779-4c75-8e2f-84639a200d5f)

Missing Data:
![image](https://github.com/user-attachments/assets/da80fe0e-90ac-42d2-aa35-03a018e163ab)


Duplicates identification:
![image](https://github.com/user-attachments/assets/f6cef794-19c2-43d8-ba72-176c279b928f)


Vakues of 'X':
![image](https://github.com/user-attachments/assets/7f37ec4b-28a4-447b-84df-07013fa5442b)

Values of 'Y':
![image](https://github.com/user-attachments/assets/27f4da99-bfb9-4039-b391-e93687fdd43a)


Outliers:
![image](https://github.com/user-attachments/assets/9465b38f-ac3e-4062-a46a-92e51666e820)

Checking datasets after dropping string values data from dataset:
![image](https://github.com/user-attachments/assets/f3554cb3-45cb-4b44-b821-80226a3d242a)

Normalize the dataset:
![image](https://github.com/user-attachments/assets/29e52780-79e9-4b17-9785-1402a8051f02)

Split the dataset:
![image](https://github.com/user-attachments/assets/871d3095-f1a0-4766-9e00-9324c3aee7e9)

Training and testing model:
![image](https://github.com/user-attachments/assets/747a9df9-e032-4c04-a650-310491c8b733)


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


