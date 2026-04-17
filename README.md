
---

# Experiment 20: Covid Data Analysis Project

**Name:** Shravya Srivastava  
**PRN:** 25070123106

---

### Aim: Exploratory Data Analysis of a COVID-19 Dataset

---

### Theory

Exploratory Data Analysis (EDA) is a critical process in data science used to summarize the main characteristics of a dataset, often with visual methods. This experiment involves analyzing the **covid_19_data.csv** file to understand global trends in confirmed cases, deaths, and recoveries.

The project focuses on data wrangling—such as grouping data by country and province—and identifying statistical extremes, such as identifying the regions with the highest impact. By using these techniques, we can transform raw health data into actionable insights regarding the progression of the pandemic.

---

### Library and Module Descriptions

The following foundational libraries were imported to handle the data processing and numerical analysis:

| Import | One-Line Description |
| :--- | :--- |
| `import pandas as pd` | The primary library used for data manipulation and structured table analysis. |
| `import numpy as np` | Used for performing high-performance mathematical operations on arrays and handling missing data. |

---

### Command Descriptions

The following specific Pandas commands were used to explore and analyze the COVID-19 records:

| Command | One-Line Description |
| :--- | :--- |
| `pd.read_csv()` | Loads the external COVID-19 dataset into a DataFrame for analysis. |
| `df.head()` | Displays the first five rows of the data to inspect the available columns. |
| `df.info()` | Provides a concise summary of the dataset's structure, column names, and null values. |
| `df.isnull().sum()` | Identifies and counts missing values across the dataset, such as in the 'Province/State' column. |
| `df.describe()` | Generates descriptive statistics for numerical columns like Confirmed, Deaths, and Recovered. |
| `df.groupby('Col').sum()` | Aggregates data by a specific category (e.g., Country/Region) to calculate global totals. |
| `df['Col'].max()` | Finds the maximum value in a numerical series, used to identify peak infection counts. |
| `df[df['Col'] == val]` | Filters the dataset to isolate rows matching specific conditions, such as a particular province. |
| `.values[0]` | Extracts the raw value from a filtered DataFrame for clean output. |

---

### Functions and Analysis Logic

#### Data Inspection and Cleaning
* **Missing Value Check:** Using `.isnull().sum()` to identify that several entries for "Province/State" are missing, which is a common occurrence in global health reporting.
* **Statistical Overview:** Using `.describe()` to understand the range and standard deviation of cases, helping to identify the scale of the outbreak.

#### Aggregation and Filtering
* **Country-Wise Totals:** Using `.groupby('Country/Region')` to sum cases, allowing for a comparison of the pandemic's impact across different nations.
* **Peak Value Identification:** Logic used to find the maximum number of confirmed cases (`.max()`) and subsequently identifying the exact province associated with that peak.

---

### Conclusion

Through this experiment, I, **Shravya Srivastava**, successfully performed a project-level analysis of a real-world COVID-19 dataset. I learned how to clean and group large-scale data to extract meaningful statistics, such as global totals and regional maximums. These analytical skills are essential for public health monitoring and for making data-driven decisions during global crises.
