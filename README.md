# Pandas Data Analysis Examples

This repository contains a Google Colab notebook (**Pandas.ipynb**) demonstrating fundamental data manipulation and analysis techniques using the **Pandas** library in Python.  

It is designed as an interactive guide for beginners to understand common Pandas operations, using a sample `student.csv` dataset.

---

## 📂 Files in this Repository

- **Pandas.ipynb** — Google Colab notebook with Python code examples.
- **student.csv** — Sample dataset used in the notebook.

---

## 🚀 How to Use

### 1️⃣ Open in Google Colab

- Navigate to the `Pandas.ipynb` file in this GitHub repository.
- Click the _Open in Colab_ badge (if available), or copy the URL of the notebook.
- Alternatively:
  - Go to [Google Colab](https://colab.research.google.com/).
  - Click **File** → **Open notebook** → **GitHub** tab → Paste the repository URL.

### 2️⃣ Upload `student.csv`

- Once the notebook is open in Colab:
  - Locate the cell containing:

    ```python
    from google.colab import files
    uploaded = files.upload()
    ```

  - Run this cell to upload the `student.csv` file from your local machine.

### 3️⃣ Run Cells

- Execute each code cell sequentially by clicking the **Play** button next to it or pressing `Shift + Enter`.
- Observe the outputs to understand how each Pandas function works.

---

## 🧑‍🏫 Key Concepts Covered

The `Pandas.ipynb` notebook covers the following essential Pandas functionalities:

### 📦 Installation & Import

- Checking Pandas version
- Standard import:

    ```python
    import pandas as pd
    ```

### 📄 DataFrame Creation

- Creating DataFrames from Python dictionaries

### 📥 Data Loading

- Reading data from CSV: `pd.read_csv()`
- Mentioned: Reading from Excel: `pd.read_excel()`

### 🔍 Initial Data Inspection

- Viewing first/last rows: `df.head()`, `df.tail()`
- Sampling random rows: `df.sample()`
- DataFrame dimensions: `df.shape`
- Column names: `df.columns`
- Descriptive statistics: `df.describe()`
- Data types: `df.dtypes`
- Missing values: `df.isnull().sum()`

### 📌 Column Selection

- Single column: `df["column_name"]`
- Multiple columns: `df[["column1", "column2"]]`

### 🔎 Row & Column Selection (`.loc` & `.iloc`)

- By label: `df.loc[row_label, column_label]`
- By integer position: `df.iloc[row_index, column_index]`

### 🗂️ Data Filtering (Conditional Selection)

- Single condition example: `df[df["gender"] == "male"]`
- Multiple conditions using `&` (AND), `|` (OR)

### 📊 Aggregation & Grouping

- Mean: `df["column"].mean()`
- Max/Min: `df["column"].max()`, `df["column"].min()`
- Grouping and aggregation:

    ```python
    df.groupby("gender")["mark"].mean()
    ```

### 📝 String Operations

- Substring search:

    ```python
    df["column"].str.contains("text", na=False)
    ```

### 🔃 Sorting Data

- Ascending sort: `df.sort_values(by="column_name")`
- Descending sort:

    ```python
    df.sort_values(by="column_name", ascending=False)
    ```

- Example: Sorting by gender.

### 🧮 Value Counts

- Counting unique values:

    ```python
    df["column"].value_counts()
    ```

---

## 📌 Summary

This notebook provides hands-on examples of common Pandas operations that are essential for data analysis in Python. It is a great starting point for beginners looking to build confidence working with tabular data using the Pandas library.

---

## ⭐ Future Improvements (Suggestions)

- Add examples of merging and joining DataFrames
- Include visualization examples with `matplotlib` or `seaborn`
- Cover handling of missing data in more depth
- Demonstrate exporting data to CSV/Excel
