# 🌍 World Happiness Report Analysis

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Latest-green.svg)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Exploring global happiness patterns through data analysis and visualization**

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Features](#-features)
- [Installation](#-installation)
- [Usage](#-usage)
- [Analysis Sections](#-analysis-sections)
- [Key Findings](#-key-findings)
- [Visualizations](#-visualizations)
- [Technologies Used](#-technologies-used)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 Overview

This project presents a comprehensive **Exploratory Data Analysis (EDA)** of the World Happiness Report dataset. The analysis investigates what factors contribute to happiness across different countries and regions worldwide.

### 🎯 Objectives

| # | Objective |
|---|-----------|
| 1 | Understand the structure and quality of the dataset |
| 2 | Identify the happiest and least happy countries |
| 3 | Compare happiness levels across different regions |
| 4 | Discover correlations between happiness and various factors |
| 5 | Analyze happiness trends over time |

---

## 📊 Dataset

### Source Information

| Property | Value |
|----------|-------|
| **Name** | World Happiness Report |
| **Records** | 1,232 |
| **Features** | 13 |
| **Time Period** | 2015 - 2019 |
| **Format** | CSV |

### 📁 Dataset Columns

| Column | Description | Type |
|--------|-------------|------|
| `Country` | Name of the country | String |
| `Region` | Geographic region | String |
| `Happiness Rank` | Rank based on happiness score | Integer |
| `Happiness Score` | Overall happiness score (0-10) | Float |
| `Standard Error` | Standard error of the score | Float |
| `Economy (GDP per Capita)` | GDP contribution to happiness | Float |
| `Family` | Family/social support contribution | Float |
| `Health (Life Expectancy)` | Health contribution | Float |
| `Freedom` | Freedom to make life choices | Float |
| `Trust (Government Corruption)` | Perception of corruption | Float |
| `Generosity` | Generosity contribution | Float |
| `Dystopia Residual` | Unexplained happiness component | Float |
| `year` | Year of the record | Integer |

---

## ✨ Features

- [x] **Data Cleaning** - Handle missing values and data types
- [x] **Descriptive Statistics** - Summary statistics for all variables
- [x] **Regional Analysis** - Compare happiness across regions
- [x] **Correlation Analysis** - Identify key happiness factors
- [x] **Time Series Analysis** - Track happiness trends over years
- [x] **Data Visualization** - Beautiful charts and graphs

---

## 🛠 Installation

### Prerequisites

Make sure you have **Python 3.8+** installed on your system.

### Step 1: Clone the Repository
bash
git clone https://github.com/farzadjenab/World-Happiness-Report---Exploratory-Data-Analysis
cd world-happiness-analysis

### Step 2: Create Virtual Environment (Optional but Recommended)

bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate

### Step 3: Install Dependencies

bash
pip install -r requirements.txt

### 📦 Required Libraries

text
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0

---

## 🚀 Usage

### Running the Notebook

bash
jupyter notebook World_Happiness_Analysis.ipynb

### Quick Start

python
# Import libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv('world_happiness_report.csv')

# View first rows
df.head()

---

## 📈 Analysis Sections

### 1️⃣ Data Loading & Exploration

python
# Basic exploration
df.shape          # Dataset dimensions
df.info()         # Column info
df.describe()     # Statistical summary

### 2️⃣ Missing Values Analysis

python
# Check missing values
df.isnull().sum()

### 3️⃣ Regional Comparison

python
# Average happiness by region
df.groupby('Region')['Happiness Score'].mean()

### 4️⃣ Correlation Analysis

python
# Correlation matrix
df.corr()

### 5️⃣ Time Trend Analysis

python
# Yearly trends
df.groupby('year')['Happiness Score'].mean()

---

## 🔍 Key Findings

### 🏆 Top 5 Happiest Regions

| Rank | Region | Avg. Score |
|------|--------|------------|
| 🥇 | Australia and New Zealand | 7.30 |
| 🥈 | North America | 7.23 |
| 🥉 | Western Europe | 6.97 |
| 4 | Latin America and Caribbean | 6.07 |
| 5 | Eastern Asia | 5.63 |

### 📊 Correlation with Happiness Score

| Factor | Correlation |
|--------|-------------|
| Economy (GDP) | **0.78** 📈 |
| Health (Life Expectancy) | **0.77** 📈 |
| Family | **0.74** 📈 |
| Freedom | **0.57** 📈 |
| Trust (Government) | **0.40** 📈 |
| Generosity | **0.18** 📈 |

### 💡 Key Insights

> 1. **Economic prosperity** is strongly linked to happiness
> 2. **Western European countries** consistently rank among the happiest
> 3. **Sub-Saharan Africa** shows the lowest happiness scores
> 4. **Generosity** has minimal impact on national happiness levels
> 5. **Health and family** are crucial happiness determinants

---

## 📊 Visualizations

### Sample Visualizations Included

| Visualization | Description |
|--------------|-------------|
| 📊 Histogram | Distribution of happiness scores |
| 📦 Box Plot | Happiness variation by region |
| 🔥 Heatmap | Correlation between variables |
| 📈 Line Chart | Happiness trends over time |
| 📊 Bar Chart | Top/Bottom countries ranking |
| 🔵 Scatter Plot | GDP vs Happiness relationship |

### Preview


┌─────────────────────────────────────────┐
│     Happiness Score Distribution        │
│                                         │
│    ▓▓▓                                  │
│   ▓▓▓▓▓▓                               │
│  ▓▓▓▓▓▓▓▓▓▓                            │
│ ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓                        │
│▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓                    │
├─────────────────────────────────────────┤
│  3    4    5    6    7    8  (Score)   │
└─────────────────────────────────────────┘

---

## 🔧 Technologies Used

| Technology | Purpose |
|------------|---------|
| ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white) | Programming Language |
| ![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat&logo=pandas&logoColor=white) | Data Manipulation |
| ![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat&logo=numpy&logoColor=white) | Numerical Computing |
| ![Matplotlib](https://img.shields.io/badge/-Matplotlib-11557c?style=flat) | Data Visualization |
| ![Seaborn](https://img.shields.io/badge/-Seaborn-3776AB?style=flat) | Statistical Visualization |
| ![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=flat&logo=jupyter&logoColor=white) | Interactive Notebook |

---

## 📁 Project Structure


world-happiness-analysis/
│
├── 📁 data/
│   └── 📄 world_happiness_report.csv
│
├── 📁 notebooks/
│   └── 📓 World_Happiness_Analysis.ipynb
│
├── 📁 images/
│   ├── 🖼 correlation_heatmap.png
│   ├── 🖼 happiness_distribution.png
│   └── 🖼 regional_comparison.png
│
├── 📄 README.md
├── 📄 requirements.txt
└── 📄 LICENSE

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Steps to Contribute

1. **Fork** the repository
2. **Create** a new branch
   
bash
   git checkout -b feature/YourFeature
   
3. Commit your changes

bash
   git commit -m "Add: YourFeature"
4. Push to the branch

bash
   git push origin feature/YourFeature
5. Open a Pull Request
### 📌 Contribution Guidelines
[ ] Follow PEP 8 coding standards
[ ] Add comments to your code
[ ] Update documentation if needed
[ ] Test your changes before submitting
## 📜 License
This project is licensed under the MIT License.

MIT License

Copyright © 2025

Permission is hereby granted, free of charge, to any person obtaining a copy

of this software and associated documentation files (the “Software”), to deal

in the Software without restriction, including without limitation the rights

to use, copy, modify, merge, publish, distribute, sublicense, and/or sell

copies of the Software.

## 📞 Contact
│ Platform │	Link │
│📧 Email │	your.email@example.com │
│💼 LinkedIn │	Your Profile │
│🐙 GitHub │	Your GitHub │
## ⭐ Show Your Support
If you found this project helpful, please give it a ⭐!

⭐ Star this repo if you like it! ⭐

┌─────────────────────────────────────┐

│ Thanks for visiting! Happy coding! │

└─────────────────────────────────────┘

<div align=“center”>

Made with ❤️ for Data Science Enthusiasts





</div>


