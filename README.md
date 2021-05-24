# Exploratory-Data-Analysis---Retail-
Exploratory Data Analysis - Retail  (Level - Beginner)
## Exploratory Data Analysis

Technically, The primary motive of EDA is to
- Examine the data distribution
- Handling missing values of the dataset(a most common issue with every dataset)
- Handling the outliers
- Removing duplicate data
- Encoding the categorical variables
- Normalizing and Scaling

## Understanding EDA
To understand the steps involved in EDA, we will use Python as the programming language and Jupyter Notebooks because it’s open-source, and not only it’s an excellent IDE but also very good for visualization and presentation.

- Step 1
First, we will import all the python libraries that are required for this, which include NumPy for numerical calculations and scientific computing, Pandas for handling data, and Matplotlib and Seaborn for visualization.
- Step 2
Then we will load the data into the Pandas data frame. For this analysis, we will use a dataset of “World Happiness Report”, which has the following columns: GDP per Capita, Family, Life Expectancy, Freedom, Generosity, Trust Government Corruption, etc. to describe the extent to which these factors contribute to evaluating the happiness.
- Step 3
We can observe the dataset by checking a few of the rows using the head() method, which returns the first five records from the dataset.
- Step 4
Using shape, we can observe the dimensions of the data.
- Step 4
Using shape, we can observe the dimensions of the data.
- Step 5
info() method shows some of the characteristics of the data such as Column Name, No. of non-null values of our columns, Dtype of the data, and Memory Usage.
- Step 7
Handling missing values in the dataset. Luckily, this dataset doesn’t have any missing values, but the real world is not so naive as our case.

So I have removed a few values intentionally just to depict how to handle this particular case.

We can check if our data contains a null value or not by the following command features have 1 missing values each.

So, now we can handle the missing values by using a few techniques, which are

- Drop the missing values – If the dataset is huge and missing values are very few then we can directly drop the values because it will not have much impact.
- Replace with mean values – We can replace the missing values with mean values, but this is not advisable in case if the data has outliers.
- Replace with median values – We can replace the missing values with median values, and it is recommended in case if the data has outliers.
- Replace with mode values – We can do this in the case of a Categorical feature.
- Regression – It can be used to predict the null value using other details from the dataset.
For our case, we will handle missing values by replacing them with the median value.
And, now we can see that our dataset doesn’t have any null values now.
- Step 8

We can check for duplicate values in our dataset as the presence of duplicate values will hamper the accuracy of our ML model.As we can see that the duplicate values are now handled.
- Step 9
Handling the outliers in the data, i.e. the extreme values in the data. We can find the outliers in our data using a Boxplot.
 boxplot that the normal range of data lies within the block and the outliers are denoted by the small circles in the extreme end of the graph.
So to handle it we can either drop the outlier values or replace the outlier values using IQR(Interquartile Range Method).
IQR is calculated as the difference between the 25th and the 75th percentile of the data. The percentiles can be calculated by sorting the selecting values at specific indices. The IQR is used to identify outliers by defining limits on the sample values that are a factor k of the IQR. The common value for the factor k is the value 1.5.
- Step 10
Normalizing and Scaling – Data Normalization or feature scaling is a process to standardize the range of features of the data as the range may vary a lot. So we can preprocess the data using ML algorithms. So for this, we will use StandardScaler for the numerical values, which uses the formula as x-mean/std deviation.
- Step 11
We can find the pairwise correlation between the different columns of the data using the corr() method. (Note – All non-numeric data type column will be ignored.)

happinessData.corr() is used to find the pairwise correlation of all columns in the data frame. Any ‘nan’ values are automatically excluded.

The resulting coefficient is a value between -1 and 1 inclusive, where:

- 1: Total positive linear correlation
- 0: No linear correlation, the two variables most likely do not affect each other
- -1: Total negative linear correlation
Pearson Correlation is the default method of the function “corr”.
- Step 12
Now, using Seaborn, we will visualize the relation between Economy (GDP per Capita) and Happiness Score by using a regression plot. And as we can see, as the Economy increases, the Happiness Score increases as well as denoting a positive relation.



