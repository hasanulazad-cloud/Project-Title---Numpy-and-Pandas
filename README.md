# 📊 NumPy & Pandas Fundamentals

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Arrays-013243?logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-DataFrames-150458?logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> A hands-on walkthrough of the core data science toolkit: **NumPy arrays**, **Pandas Series** and **Pandas DataFrames**, practised on weekly temperature readings, student marks and retail sales transactions.

---

## 📌 Project Overview

This project covers the foundations every data analyst needs before moving to real datasets. Each section solves a set of practical tasks: creating data structures, inspecting them, slicing and filtering, transforming values, and summarising by group.

**What's inside**
- 🌡️ **NumPy:** weekly temperature data, unit conversion, statistics, 1D and 2D slicing
- 🎓 **Pandas Series:** student marks with custom labels, `loc` / `iloc` access, boolean filtering
- 🛒 **Pandas DataFrame:** 10 sales transactions explored, filtered, grouped and modified

---

## 📂 Repository Contents

| File | Description |
|---|---|
| `Python DA Assignment Numpy and Pandas.ipynb` | Complete notebook with all tasks and outputs |

---

## 🧩 Sections & Skills

### 1️⃣ NumPy Array Operations
| Task | Technique |
|---|---|
| Create a 1D array of daily temperatures | `np.array()` |
| Inspect properties | `.shape`, `.size`, `.dtype` |
| Convert Celsius to Fahrenheit | Vectorised arithmetic |
| Max, min and mean | `np.max()`, `np.min()`, `np.mean()` |
| First three days, weekend, middle days | Slicing (`[:3]`, `[-2:]`, `[2:5]`) |
| Two-week 2D array | Nested lists, `temperatures[:, -2:]` |

### 2️⃣ Pandas Series
| Task | Technique |
|---|---|
| Marks with labels `Rank1` to `Rank5` | `pd.Series(data, index)` |
| Access by position and label | `.iloc[]`, `.loc[]` |
| Marks above 90 | Boolean mask |
| Update, drop and rescale | `.loc` assignment, `.drop()`, division |

### 3️⃣ Pandas DataFrame
| Task | Technique |
|---|---|
| Build the transactions table | `pd.DataFrame(dict)` |
| Explore the data | `.head()`, `.tail()`, `.shape`, `.columns`, `.dtypes` |
| Select columns | `df[[...]]`, `.iloc[:, -3:]` |
| North region, amount over 200 | Combined boolean filter with `&` |
| Category counts and unique regions | `.value_counts()`, `.unique()` |
| Mean amount per region | `.groupby()` |
| Edit, add and delete data | `.loc`, new column, `.drop()` |

---

## 📊 Key Results

**Weekly temperatures (Week 1)**

| Statistic | Celsius | Fahrenheit |
|---|---|---|
| Maximum | 26.1°C | 78.98°F |
| Minimum | 20.8°C | 69.44°F |
| Mean | 23.54°C | 74.38°F |

**Sales transactions (10 records)**

| Region | Mean amount |
|---|---|
| East | 375.0 |
| North | 287.5 |
| South | 250.0 |
| West | 190.0 |

| Product category | Transactions |
|---|---|
| Electronics | 4 |
| Clothing | 3 |
| Furniture | 3 |

- 🔝 **East** has the highest average sale (375), driven by two Furniture transactions.
- 🔎 Three North transactions are above 200, and all are Electronics (IDs 103, 106, 110).
- 🎓 After updating Rank1 to 100 and removing Rank5, the CGPA values are 10.0, 9.2, 8.9 and 8.5.

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/hasanulazad-cloud/Project-Title---Numpy-and-Pandas.git
cd Project-Title---Numpy-and-Pandas

# 2. Install the dependencies
pip install numpy pandas jupyter

# 3. Open the notebook
jupyter notebook "Python DA Assignment Numpy and Pandas.ipynb"
```

---

## ⚠️ Known Limitations

- **Row removal not applied.** The step meant to remove TransactionID 109 stores its result in a separate variable and then prints the original table, so row 109 is still present (and counted in the figures above). Using `dataframe = dataframe[dataframe['TransactionID'] != 109]` removes it.
- **Table is changed in place.** `dataframe = transactions` points to the same object, so edits also change `transactions`. Use `.copy()` to keep the original.
- **Regional means were calculated before the edit.** After the Amount for transaction 102 was changed from 150 to 165, South's mean becomes 257.5.

---

## 🔮 Future Improvements

- Add charts (temperature trend, sales by region) with Matplotlib
- Load transactions from a CSV file instead of typing them in
- Add `groupby` summaries with multiple statistics using `.agg()`
- Extend to merging and pivot tables

---

## 👤 Author

**Hasanul H Azad**
Medical billing / RCM professional upskilling in Data Science, AI and Machine Learning
GitHub: [@hasanulazad-cloud](https://github.com/hasanulazad-cloud)

---

⭐ If you found this useful, consider starring the repo.
