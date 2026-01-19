# Pandas 

## What is Pandas?

Pandas is a Python library used for **data manipulation and analysis**. It provides fast, flexible data structures for handling **structured data** like tables.

Built on top of **NumPy**.

---

## Why Pandas?

* Easy handling of **tabular data**
* Powerful **data cleaning** tools
* Fast data analysis
* Essential for **ML, Data Science, AIML**

---

## Installation & Import

```bash
pip install pandas
```

```python
import pandas as pd
```

---

## Core Data Structures

### 1. Series (1D)

```python
s = pd.Series([10, 20, 30])
```

* Like a column
* Has **index + values**

---

### 2. DataFrame (2D)

```python
df = pd.DataFrame({
    'Name': ['A', 'B'],
    'Age': [20, 21]
})
```

* Rows + Columns
* Most used Pandas object

---

## Reading Data

```python
pd.read_csv('file.csv')
pd.read_excel('file.xlsx')
pd.read_json('file.json')
```

---

## Writing Data

```python
df.to_csv('file.csv', index=False)
df.to_excel('file.xlsx', index=False)
```

---

## DataFrame Attributes

```python
df.shape
df.size
df.columns
df.index
df.dtypes
```

---

## Viewing Data

```python
df.head()
df.tail()
df.info()
df.describe()
```

---

## Selecting Data

### Column Selection

```python
df['Age']
df[['Name', 'Age']]
```

### Row Selection

```python
df.loc[0]
df.iloc[0]
df.loc[0:3]
df.iloc[0:3]
```

---

## Filtering Data

```python
df[df['Age'] > 20]
```

Multiple conditions:

```python
df[(df['Age'] > 20) & (df['Age'] < 30)]
```

---

## Adding & Removing Columns

```python
df['Marks'] = [80, 90]
df.drop('Marks', axis=1, inplace=True)
```

---

## Handling Missing Values

```python
df.isnull()
df.isnull().sum()

df.dropna()
df.fillna(0)
```

---

## Sorting Data

```python
df.sort_values('Age')
df.sort_values('Age', ascending=False)
```

---

## GroupBy (Very Important)

```python
df.groupby('Age').mean()
```

Common aggregations:

* mean()
* sum()
* count()
* max(), min()

---

## Merging & Joining

```python
pd.merge(df1, df2, on='id')
pd.concat([df1, df2])
```

---

## Apply Function

```python
df['Age'].apply(lambda x: x + 1)
```

---

## Pandas vs NumPy

| Feature   | NumPy       | Pandas             |
| --------- | ----------- | ------------------ |
| Data Type | Homogeneous | Heterogeneous      |
| Structure | ndarray     | Series / DataFrame |
| Labels    | No          | Yes                |

---

## Where Pandas is Used

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Machine Learning Preprocessing

---

## One-Line Summary

**Pandas = Data Handling + Cleaning + Analysis Made Easy** 🚀
