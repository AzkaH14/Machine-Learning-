# Machine-Learning-
_____________
**Automobile Data Analysis**
Setup and Requirements
This project requires the following libraries:

**Python** 
Pandas
NumPy
Matplotlib
Seaborn
Installation
To set up and run this analysis:

**Dataset**
The dataset used in this project contains information on various automobiles, including attributes such as price, engine type, fuel type, and normalized losses.

**Objective**
The main objectives of this analysis are to:
Clean the data by handling missing values and inconsistent entries.
Explore the distribution of specific features.
Gain insights into the dataset through visualizations
_____________

**Steps**

1. Data Loading
The dataset is loaded with Pandas for easy handling:

data_frame = pd.read_csv('path/to/Automobile_data.csv')

2. Data Cleaning
Duplicate Detection: 
data_frame.duplicated()

3.Standardizing Missing Values: Replaced missing values, represented by ?, with NaN for consistent handling.
data_frame.replace('?', np.nan, inplace=True)


4.Data Type Conversion: Converted the normalized-losses column to numeric to enable accurate calculations.
data_frame['normalized-losses'] = pd.to_numeric(data_frame['normalized-losses'])


5.Imputation of Missing Values: Filled missing values in normalized-losses with the mean to reduce skewed data distribution.
mean_normalized_losses = data_frame['normalized-losses'].mean()
data_frame['normalized-losses'].fillna(mean_normalized_losses, inplace=True)


6. Data Analysis and Visualization
Box Plot for Outliers: Created a box plot for normalized-losses to spot any outliers.
sns.boxplot(x=data_frame['normalized-losses'])


7.Distribution of Symboling: Analyzed the distribution of symboling values to gain insights into risk factor ratings.
sns.histplot(data_frame['symboling'])





