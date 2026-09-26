# industrial-predictive-maintenance-analytics

 Industrial Predictive Maintenance Analytics

 Project Overview

This project analyzes industrial machine operating data to identify patterns associated with machine failures and understand key operational factors that can support predictive maintenance and process improvement.

The analysis is performed using Python and focuses on exploratory data analysis (EDA), operational KPIs, failure-mode analysis, and correlation analysis.

> **Note:** The dataset used in this project is the publicly available AI4I 2020 Predictive Maintenance Dataset. It is a synthetic industrial dataset and is not data from any specific company.

---

##  Objectives

The main objectives of this project are:

- Analyze machine operating data using Python
- Calculate important operational KPIs
- Determine the overall machine failure rate
- Compare failure rates across product types
- Analyze operating conditions associated with machine failures
- Study different machine failure modes
- Identify relationships between operating variables
- Generate insights that can support maintenance and process-improvement decisions

---

##  Dataset

The project uses the **AI4I 2020 Predictive Maintenance Dataset**.

The dataset contains **10,000 observations** and includes variables related to machine operation and failure.

### Important Variables

| Variable | Description |
|---|---|
| Product ID | Unique product identifier |
| Type | Product quality/type category |
| Air temperature [K] | Air temperature |
| Process temperature [K] | Process temperature |
| Rotational speed [rpm] | Machine rotational speed |
| Torque [Nm] | Machine torque |
| Tool wear [min] | Tool wear duration |
| Machine failure | Indicates whether machine failure occurred |
| TWF | Tool Wear Failure |
| HDF | Heat Dissipation Failure |
| PWF | Power Failure |
| OSF | Overstrain Failure |
| RNF | Random Failure |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

##  Analysis Performed

### 1. Data Understanding

- Loaded the dataset using Pandas
- Examined dataset structure
- Checked data types
- Checked missing values
- Generated descriptive statistics

### 2. Operational KPI Analysis

The following KPIs were calculated:

- Total observations
- Total machine failures
- Overall machine failure rate
- Average torque
- Average tool wear

### 3. Failure Rate by Product Type

Machine failure rates were compared across product types.

Observed failure rates:

| Product Type | Failure Rate |
|---|---:|
| H | 2.09% |
| L | 3.92% |
| M | 2.77% |

These values describe the observed failure rates in this dataset and do not establish a causal relationship between product type and failure.

### 4. Operating Condition Analysis

Operating variables were compared between observations with and without machine failure.

#### Torque

- No failure: **39.63 Nm**
- Failure: **50.17 Nm**

#### Tool Wear

- No failure: **106.69 min**
- Failure: **143.78 min**

#### Rotational Speed

- No failure: **1540.26 rpm**
- Failure: **1496.49 rpm**

The analysis shows that failure observations were associated with higher torque and tool wear, while rotational speed was somewhat lower.

> These are observed associations and should not be interpreted as proof of causation.

### 5. Failure Mode Analysis

The major failure-mode flags were analyzed:

| Failure Mode | Count |
|---|---:|
| TWF | 46 |
| HDF | 115 |
| PWF | 95 |
| OSF | 98 |
| RNF | 19 |

The analysis also examined how torque and tool wear varied across different failure modes.

### 6. Correlation Analysis

Correlation analysis was performed to examine relationships between numerical variables.

Some notable relationships include:

- Air temperature ↔ Process temperature: **0.876**
- Rotational speed ↔ Torque: **-0.875**
- Torque ↔ Machine failure: **0.191**
- Tool wear ↔ Machine failure: **0.105**

Correlation measures association and does not establish causation.

---

## 📈 Key Findings

The analysis identified several patterns in the dataset:

- Overall machine failure rate was **3.39%**.
- Failure observations had higher average torque than non-failure observations.
- Failure observations had higher average tool wear.
- Failure observations had somewhat lower average rotational speed.
- Product types showed different observed failure rates.
- Different failure modes showed different operating patterns.
- Torque showed the strongest linear correlation with the machine-failure indicator among the analyzed operating variables.

These findings can be used as a starting point for further predictive-maintenance analysis.

---

## 📁 Project Structure

```text
industrial-predictive-maintenance-analytics/
│
├── Predictive_Maintenance_Analytics.ipynb
├── README.md
└── requirements.txt
