# 🚗✨ Auto Analytics & Visualization Project ✨🚗

**Author**: Chance Angelo C. Tan

Welcome to the **Auto Analytics Project**, where we harness the power of Python and the Pandas library for effective data wrangling and visualization. This repository features scripts designed to clean, process, and visualize automotive data, revealing insights into key features such as **model**, **cylinders**, and **gear type**. Dive in and unlock the potential of data-driven analysis! 🚀

---

## 📝 Project Overview

### 📋 **Problem Description**

#### **Intended Learning Outcomes**
- Master the functions within the **Pandas library** for data analysis.
- Implement various programming techniques to develop efficient **data wrangling** and **visualization** solutions.

#### **Instructions**
- Develop your Python scripts in Jupyter Notebook to address the tasks outlined below.

---

## 📈 Data Wrangling & Visualizations

### **Problems**

#### **PROBLEM 1: Initial Data Exploration**
- **Task**:
  - Load the CSV data into a DataFrame named `cars` using Pandas.
  - Display the first and last five rows of the `cars` DataFrame.

#### **PROBLEM 2: Advanced Data Manipulation**
- **Task Details**:
  1. Save your work as `Surname_Pandas-P.py`:
     - Extract and present the first five rows with odd-numbered columns.
  2. Save your findings as `Surname_Pandas-P2.py`:
     - Locate the row pertaining to the car model "Mazda RX4".
     - Retrieve and display the cylinder count ('cyl') for "Camaro Z28".
     - Extract and summarize the cylinders ('cyl') and gear types ('gear') for "Mazda RX4 Wag", "Ford Pantera L", and "Honda Civic".

---

## ⚙️ Setup & Installation

To execute the Python scripts within this project, perform the following steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/TanTan-Angelo/Experiment-3---CompProg

pip install pandas jupyter matplotlib
jupyter notebook


import pandas as pd

# PROBLEM 1: Load data into a DataFrame
cars = pd.read_csv('cars.csv')
print(cars.head())  # Display the first five rows
print(cars.tail())  # Display the last five rows

# PROBLEM 2: Advanced Manipulation
# a. Display rows with odd-numbered columns
odd_columns = cars.iloc[:, ::2]
print(odd_columns.head())

# b. Display the row for Mazda RX4
mazda_rx4 = cars[cars['Model'] == 'Mazda RX4']
print(mazda_rx4)

# c. Display the number of cylinders for Camaro Z28
camaro = cars[cars['Model'] == 'Camaro Z28']
print(camaro['cyl'])

# d. Display cylinders and gear type for specific models
specific_models = cars[cars['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic'])]
print(specific_models[['Model', 'cyl', 'gear']])



