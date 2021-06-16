# Exploratory-Data-Analysis
Good practices comes here. (EDA is all about making sense of data in hand, before getting them dirty with it.)

[Link to post](https://towardsdatascience.com/exploratory-data-analysis-8fc1cb20fd15)
---

> Exploratory Data Analysis refers to the critical process of performing initial investigations on data so as to discover patterns,to spot anomalies,to test hypothesis and to check assumptions with the help of summary statistics and graphical representations.

```
df = pd.read_csv('link.csv')
df.head()

df.shape

df.info()

df.describe()

df.quality.unique()

df.quality.value_counts()
```

[Blog link](https://towardsai.net/p/data-analysis/exploratory-data-analysis-in-python-ebdf643a33f6)

# Exploratory Data Analysis

### Steps in Data Exploation and Preprocessing:
1. Identification of variables and data types
2. Analyzing the basic matrics
3. Non-Graphical Univariate Analysis
4. Graphical Univariate Analysis
5. Bivariate Analysis
6. Variable transformations
7. Missing value treatment
8. Outlier treatment
9. Correlation Analysis
10. Dimensionality Reduction

> Variable identification:

Variable are of two types -Numetical and Categorical. They can be farther classified as follows.
```
Variable
|__Numerical
     |__Discreate	# whole number eg. number of students
     |__Continuous   # any value in range eg. Annual income
|__Categorical
     |__Orfinal    # that can be ordered eg. Grades
     |__Nominal    # no intrinsic order of labels eg. Country
```
The next step is to identify the Predictor(Inputs) and Target(Output) variables.

> Importing Libraries:

```
import pandas as pd   # data analysis tools
import numpy as np     # scientific computing
import matplotlib as plt    # data visualization
import seaborn as sns    # data visualization
```
> Importing Dataset
```
data = pd.read_csv("dataset.csv")

```

> Identification of data types:

The .dtypes method to identiry the data type on the variable in the dataset.
```
data.dtypes
```

> Size of the dataset:

The .shape method to get the size of the dataset
```
data.shape 
```

> Statistical Summary of Numeric Variables:

Pandas descirbe() is used to view some basic statistical details like count, percentile, mean, std and maximum value of a data frame or a series of numeric values.
```
data.describe()
```

> Non-Graphical Univariate Analysis

To get the count of unique values: The value_counts() method in pandas returns a series containing the counts of all the unique values in a column.
```
data['coulum'].value_counts()
```

> To get the list & number of unique values:

The nunique() function in Pandas returns a number of distinct observatins in a column
```
data['coulumn'].nunique()
```

The unique() function of Pandas returns the list of unique values in the dataset.
```
data['coulumn'].unique()

```

> Filtering based on Conditions:

Datasets can be filtered using different conditions using ligical operators in python ( and: &, or: | )


```
data[(data['column'] == 'Value')]

```

> Finding null values:

Pandas isnull() method is used to check and manage NULL values in a data frame.

```
data.apply(lambda x: sum(x.isnull()), axis=0)
```

> Graphical Univariate Analysis:

**Histogram**

Histograms shows the distribution of data and Identify outliers. 
```
data['column'].hist(bins=25)

```

**box Plots**

A box plot is the visual representation of the statistical summary of a given data set.
- Mimimum
- First Quartile
- Median (second quartile)
- Thired Quartile
- Maximum
```
data.boxplot(column = 'column_name')

```
```
data.boxplot(column= 'column_name', by = ‘column_name’)
```

**Count Plot**

A count plot can be thought of as a histogram across a categorical, instead of numeric, variable. It is used to find the frequency of each category.
```
sns.countplot(data.column)

```

> The above eda paractical is done in above jupyter notebook [link](www.google.com)
