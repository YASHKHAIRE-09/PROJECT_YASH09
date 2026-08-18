# PROJECT_YASH09


# 🏋️ Data Cleaning & Visualization – Powerlifting Meets Analysis

## 📌 Project Overview

This project focuses on **Data Cleaning, Processing, Visualization, and Data Storytelling** using a dataset of powerlifting meets.

The main objective was to work with a real-world dataset, identify and handle data-quality issues, prepare the data for analysis, and create meaningful visualizations to discover patterns and insights.

The project was completed using **Python, Pandas, Matplotlib, and Seaborn**.

---

## 🎯 Project Objectives

The project was developed according to the following data-cleaning and visualization objectives:

* Understand and inspect the dataset
* Identify duplicate records
* Handle missing values
* Convert and process date information
* Prepare the dataset for visualization
* Analyze trends and distributions
* Create meaningful visualizations
* Present insights through data storytelling

---

## 📂 Dataset

The dataset used in this project is **`meets.csv`**.

It contains information about powerlifting competitions and includes:

| Column        | Description                                           |
| ------------- | ----------------------------------------------------- |
| `MeetID`      | Unique identification number of the powerlifting meet |
| `MeetPath`    | Path or identifier associated with the meet           |
| `Federation`  | Powerlifting federation conducting the meet           |
| `Date`        | Date on which the meet was conducted                  |
| `MeetCountry` | Country where the meet was held                       |
| `MeetState`   | State/region where the meet was held                  |
| `MeetTown`    | Town/city where the meet was held                     |
| `MeetName`    | Name of the powerlifting meet                         |

### Dataset Size

* **Rows:** 8,482
* **Original Columns:** 8
* **Duplicate Rows:** 0
* **Missing values:** Present in `MeetState` and `MeetTown`

---

## 🧹 Data Cleaning & Preprocessing

The first stage of the project involved examining the quality and structure of the dataset.

### 1. Dataset Inspection

The dataset was loaded using Pandas and inspected using functions such as:

* `head()`
* `describe()`
* `columns`
* `info()`

This helped understand the dataset structure, columns, data types, and statistical information.

### 2. Duplicate Detection

Duplicate records were checked using:

```python
df.duplicated()
df.duplicated().sum()
```

The dataset contained **no complete duplicate rows**.

Duplicate removal was also demonstrated using:

```python
df.drop_duplicates()
```

and by checking duplicates based on the `MeetID` column.

### 3. Missing Value Analysis

Missing values were identified using:

```python
df.isnull().sum()
```

The main missing values were found in:

* `MeetState`
* `MeetTown`

Instead of removing all records containing missing values, missing categorical values were replaced with **`Unknown`**:

```python
df['MeetState'] = df['MeetState'].fillna('Unknown')
df['MeetTown'] = df['MeetTown'].fillna('Unknown')
```

This helped preserve useful records while making the dataset more suitable for analysis.

### 4. Date Processing

The `Date` column was converted into a proper datetime format:

```python
df['Date'] = pd.to_datetime(df['Date'])
```

The year was then extracted into a new column:

```python
df['Year'] = df['Date'].dt.year
```

This enabled year-wise analysis of powerlifting meets.

---

## 📊 Data Visualization

Three major visualizations were created to transform the cleaned data into meaningful insights.

### 📈 1. Growth of Powerlifting Meets Over Time

A line chart was created to analyze how the number of powerlifting meets changed over the years.

**Purpose:**

* Identify growth patterns
* Observe changes in the number of meets hosted
* Understand the development of powerlifting competitions over time

The analysis focused on meet counts by year up to 2018.

---

### 🏆 2. Top 10 Most Active Powerlifting Federations

A bar chart was created to identify the **10 federations with the highest number of recorded meets**.

**Purpose:**

* Compare federation activity
* Identify the most frequently represented federations
* Understand the distribution of meets across federations

---

### 🌍 3. Geographical Distribution of Powerlifting Meets

A pie chart was created using the top 5 countries based on the number of recorded meets.

**Purpose:**

* Understand the geographical distribution of powerlifting competitions
* Identify countries with the largest representation
* Present the country distribution in an easy-to-understand format

---

## 🛠️ Technologies & Libraries Used

### Programming Language

* **Python**

### Libraries

* **Pandas** – Data loading, cleaning, preprocessing, and analysis
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical and categorical visualizations

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Load Dataset using Pandas
     ↓
Explore Dataset
     ↓
Check Data Types & Statistics
     ↓
Check Duplicate Records
     ↓
Identify Missing Values
     ↓
Handle Missing Values
     ↓
Convert Date Column
     ↓
Extract Year
     ↓
Analyze Powerlifting Meets
     ↓
Create Visualizations
     ↓
Identify Trends & Patterns
     ↓
Data Storytelling
```

---

## 💡 Key Insights

The visual analysis helps answer questions such as:

* How has the number of powerlifting meets changed over time?
* Which powerlifting federations hosted the most meets?
* Which countries have the highest representation of powerlifting meets?
* How are powerlifting competitions distributed geographically?
* What patterns can be observed from the historical meet data?

These visualizations transform the raw dataset into an easier-to-understand story about the **growth, federation activity, and geographical distribution of powerlifting competitions**.


---

## 📌 Expected Learning Outcomes

Through this project, the following skills were developed:

* Understanding real-world datasets
* Data exploration using Pandas
* Identifying missing values
* Handling missing categorical data
* Detecting duplicate records
* Date and time preprocessing
* Creating meaningful visualizations
* Using Matplotlib and Seaborn
* Identifying trends and patterns
* Presenting findings through data storytelling

---

## 🚀 Conclusion

This project demonstrates a complete basic **data cleaning and visualization workflow** using a real-world powerlifting meets dataset.

Starting from raw data, the project involved **data exploration, duplicate checking, missing-value handling, date processing, visualization, and interpretation of patterns**.

The final visualizations provide a clear view of the **historical growth of powerlifting meets, the activity of different federations, and the geographical distribution of competitions**.

This project helped demonstrate how data cleaning and visualization can turn raw datasets into meaningful and understandable insights.

---





This project was completed as part of a **Data Cleaning & Visualization Project**.
