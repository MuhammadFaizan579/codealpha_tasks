# Unemployment Analysis in India

A data analysis project focused on analyzing unemployment trends in India during 2020, particularly examining the impact of the COVID-19 pandemic using Python, Pandas, Matplotlib, and Seaborn.

## Project Overview

The objective of this project is to explore and analyze unemployment data collected from different regions of India. The analysis focuses on unemployment rates, employment levels, labour participation rates, regional differences, and changes during the COVID-19 period.

This project follows a complete data analysis workflow, starting from data loading and exploration to data cleaning, visualization, and extracting meaningful insights.

---

## Dataset

The dataset used in this project is:

**Unemployment_Rate_upto_11_2020**

The dataset contains unemployment-related information from different regions of India during 2020.

### Dataset Features

| Column                                  | Description                                                    |
| --------------------------------------- | -------------------------------------------------------------- |
| Region                                  | Name of the Indian state or region                             |
| Date                                    | Date of the recorded observation                               |
| Frequency                               | Frequency of data collection                                   |
| Estimated Unemployment Rate (%)         | Estimated percentage of unemployed people                      |
| Estimated Employed                      | Estimated number of employed people                            |
| Estimated Labour Participation Rate (%) | Percentage of the population participating in the labour force |
| Region.1                                | Geographical region of the state                               |
| longitude                               | Geographical longitude                                         |
| latitude                                | Geographical latitude                                          |

---

## Dataset Information

The dataset initially contained:

* **267 rows**
* **9 columns**
* Monthly unemployment observations
* Multiple regions across India
* Unemployment, employment, and labour participation data

The dataset contained no major data quality issues after the cleaning process.

---

## Technologies and Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab

---

## Data Analysis Workflow

The project followed the following workflow:

```text
Dataset
    ↓
Data Loading
    ↓
Data Exploration
    ↓
Data Cleaning
    ↓
Missing Value Analysis
    ↓
Statistical Analysis
    ↓
Data Sorting and Filtering
    ↓
Data Visualization
    ↓
Trend Analysis
    ↓
Regional Comparison
    ↓
Insights and Conclusion
```

---

## Data Exploration

The dataset was initially explored using:

```python
df.head()
df.tail()
df.shape
df.info()
df.describe()
```

These functions helped understand:

* Dataset size
* Column names
* Data types
* Number of non-null values
* Statistical summaries
* Minimum and maximum values
* Average unemployment rate
* Data distribution

---

## Data Cleaning

The data was checked for missing values using:

```python
df.isnull().sum()
```

Boolean values returned by `isnull()` were summed to determine the number of missing values in each column.

Rows containing missing values were removed using:

```python
df.dropna()
```

Since the percentage of missing data was relatively small, removing the incomplete rows was considered appropriate for this analysis.

---

## Statistical Analysis

Descriptive statistics were used to understand the distribution of the unemployment data.

Important statistical concepts explored included:

* Mean
* Median
* Standard Deviation
* Minimum value
* Maximum value

The mean helped identify the average unemployment rate, while the median provided the middle value of the data distribution.

Standard deviation was used to understand how widely the unemployment values varied from the average.

---

## Data Sorting and Filtering

The dataset was sorted to identify regions with higher and lower unemployment rates.

For example:

```python
df.sort_values(
    by="Estimated Unemployment Rate (%)",
    ascending=False
)
```

The parameter:

```python
ascending=False
```

sorts the values in **descending order**, meaning the highest values appear first.

This helped identify regions with the highest unemployment rates.

---

## Data Visualization

Multiple visualizations were created using Matplotlib and Seaborn.

### Unemployment Rate Distribution

Histograms were used to understand the distribution of unemployment rates across the dataset.

### Regional Comparison

Bar charts were used to compare unemployment rates across different regions.

### Monthly Trend Analysis

Line charts were used to analyze how unemployment rates changed over time.

### COVID-19 Impact Analysis

The unemployment rate during different months of 2020 was analyzed to understand the impact of the COVID-19 pandemic on employment conditions.

### Additional Visualizations

The project also used visualizations such as:

* Bar charts
* Line charts
* Histograms
* Boxplots
* Regional comparisons

These visualizations helped identify patterns and trends that were difficult to observe from raw data alone.

---

## Key Insights

### 1. COVID-19 significantly affected unemployment

The analysis showed noticeable changes in unemployment rates during the COVID-19 period. Lockdowns and restrictions affected businesses, industries, and employment opportunities.

### 2. Unemployment varied significantly across regions

Different regions experienced different unemployment levels. This indicates that the impact of the pandemic was not uniform across all states and regions.

### 3. Some regions experienced sharp increases

Certain regions showed significant increases in unemployment during specific periods, particularly during the initial months of the pandemic.

### 4. Unemployment rates changed over time

The monthly trend analysis demonstrated that unemployment was not constant. It changed considerably throughout 2020 as economic conditions evolved.

### 5. Employment and labour participation were important factors

The analysis also considered:

* Estimated employment
* Labour participation rate
* Unemployment rate

These metrics helped provide a broader understanding of the employment situation instead of focusing on unemployment alone.

### 6. Data visualization made patterns easier to understand

Charts and graphs made it easier to identify:

* Regional differences
* Monthly trends
* High and low unemployment periods
* Data distribution
* Potential outliers

---

## Conclusion

This project analyzed unemployment trends in India using Python and various data analysis libraries.

The analysis began with data loading and exploration using Pandas. The dataset structure, data types, statistical summaries, and missing values were examined. After cleaning the dataset, different statistical methods and visualizations were used to analyze unemployment patterns across regions and time periods.

The analysis demonstrated that unemployment rates varied significantly between different regions and changed considerably throughout 2020. The COVID-19 pandemic had a major impact on employment conditions, resulting in noticeable changes in unemployment levels in several regions.

Through this project, a complete data analysis workflow was implemented, including:

* Data loading
* Data exploration
* Data cleaning
* Missing value handling
* Statistical analysis
* Data sorting
* Data filtering
* Data visualization
* Trend analysis
* Regional comparison
* Insight generation

This project provided practical experience with Pandas, Matplotlib, and Seaborn while demonstrating how real-world data can be transformed into meaningful insights.

---

## Project Structure

```text
Unemployment-Analysis/
│
├── Unemployment Analysis.ipynb
├── Unemployment_Rate_upto_11_2020.csv
└── README.md
```

---

## Future Improvements

This project can be further improved by:

* Creating an interactive dashboard using Power BI
* Building a time-series forecasting model
* Predicting future unemployment rates
* Performing correlation analysis
* Creating an interactive geographical map
* Comparing unemployment trends with economic indicators
* Building a machine learning model for unemployment prediction

---

## Author

**Muhammad Faizan**

This project was developed as part of my learning journey in **Data Analysis, Data Science, and Machine Learning**.
