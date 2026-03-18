# 🐼 Pandas Advanced Repository

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple)
![License](https://img.shields.io/badge/License-MIT-green)

A **high-performance data analysis repository** built using
Pandas — the most powerful Python library for **data manipulation, transformation, and analysis**.

This repository covers everything from **data wrangling → feature engineering → real-world analytics pipelines**.

---

# 📚 Table of Contents

* Introduction
* Repository Structure
* Installation
* Core Concepts
* Advanced Techniques
* Performance Optimization
* Data Pipelines
* Real-World Projects
* Visualization
* Contributing
* License

---

# 🧠 Introduction

Pandas provides:

* High-level **DataFrame abstraction**
* Powerful **data cleaning tools**
* Time-series analysis
* Missing data handling
* Grouping & aggregation
* SQL-like operations

This repo focuses on **writing efficient, scalable, and production-ready data workflows**.

---

# 📁 Repository Structure

```plaintext
pandas-mastery/
│
├── basics/
│   ├── series_dataframe.py
│   ├── indexing_selection.py
│   ├── data_types.py
│
├── data_cleaning/
│   ├── missing_values.py
│   ├── duplicates.py
│   ├── outlier_handling.py
│
├── transformation/
│   ├── apply_map.py
│   ├── lambda_functions.py
│   ├── feature_engineering.py
│
├── aggregation/
│   ├── groupby.py
│   ├── pivot_tables.py
│   ├── window_functions.py
│
├── time_series/
│   ├── datetime_index.py
│   ├── resampling.py
│   ├── rolling_analysis.py
│
├── performance/
│   ├── vectorization.py
│   ├── memory_optimization.py
│
├── projects/
│   ├── sales_analysis.py
│   ├── covid_analysis.py
│   ├── stock_market_analysis.py
│
└── README.md
```

---

# ⚙️ Installation

```bash
git clone https://github.com/yourusername/pandas-mastery.git
cd pandas-mastery
pip install pandas numpy matplotlib seaborn
```

Verify installation:

```python
import pandas as pd
print(pd.__version__)
```

---

# 🔹 Core Concepts

### DataFrame Creation

```python
import pandas as pd

data = {
    "Name": ["Umer", "Ali", "Sara"],
    "Age": [22, 23, 21]
}

df = pd.DataFrame(data)
```

---

### Data Selection

```python
df["Name"]
df.loc[0]
df.iloc[1]
```

---

### Filtering

```python
df[df["Age"] > 21]
```

---

# 🚀 Advanced Techniques

### GroupBy Operations

```python
df.groupby("Department")["Salary"].mean()
```

---

### Pivot Tables

```python
pd.pivot_table(df, values="Sales", index="Region", columns="Year")
```

---

### Apply & Lambda Functions

```python
df["Age"] = df["Age"].apply(lambda x: x + 1)
```

---

### Window Functions

```python
df["rolling_avg"] = df["Sales"].rolling(window=3).mean()
```

---

# ⚡ Performance Optimization

Best practices:

* Avoid loops → use vectorization
* Use `.values` or `.to_numpy()` when needed
* Use categorical data types
* Optimize memory with `astype()`

Example:

❌ Slow:

```python
for i in range(len(df)):
    df["Age"][i] += 1
```

✅ Fast:

```python
df["Age"] += 1
```

---

# 🔄 Data Pipelines

Example pipeline:

```python
df = (
    df.dropna()
      .query("Age > 20")
      .assign(Salary=lambda x: x["Salary"] * 1.1)
      .groupby("Department")
      .mean()
)
```

---

# 📊 Visualization

Works seamlessly with:

* Matplotlib
* Seaborn

```python
import matplotlib.pyplot as plt

df["Age"].hist()
plt.show()
```

---

# 🧪 Real-World Projects

| Project               | Description                         |
| --------------------- | ----------------------------------- |
| Sales Analysis        | Analyze trends and revenue patterns |
| COVID Data Analysis   | Time-series pandemic insights       |
| Stock Market Analysis | Financial data modeling             |

---

# 🤝 Contributing

1. Fork the repository
2. Create a branch

```bash
git checkout -b feature-branch
```

3. Commit changes

```bash
git commit -m "Added advanced pandas pipeline"
```

4. Push

```bash
git push origin feature-branch
```

5. Open Pull Request

---

# 📜 License

MIT License

---

# ⭐ Support

If you like this repository:

⭐ Star it
🍴 Fork it
📢 Share it

---

💡 *"Data is powerful, but only when you know how to transform it into insight."*

---

