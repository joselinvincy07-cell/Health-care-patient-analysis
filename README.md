# README – Healthcare Data Analysis and Risk Prediction

## Project Title

**Healthcare Data Analysis and Patient Risk Classification Using Python**

---

## Project Description

This project generates a synthetic healthcare dataset containing 10,000 patient records and performs data analysis to identify patient health risks. The dataset includes age, gender, blood pressure, sugar level, cholesterol, and heart rate information.

The project uses data analytics and visualization techniques to classify patients into **Low**, **Medium**, and **High Risk** categories based on medical indicators.

---

## Objectives

* Generate a healthcare dataset using Python.
* Perform exploratory data analysis (EDA).
* Identify missing values and data quality issues.
* Classify patients based on health risk factors.
* Visualize patient health statistics.
* Analyze relationships among medical attributes.

---

## Technologies Used

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Random data generation and numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Advanced statistical visualizations

---

## Dataset Information

The dataset contains **10,000 patient records** with the following attributes:

| Column Name    | Description                    |
| -------------- | ------------------------------ |
| Patient_ID     | Unique patient identifier      |
| Age            | Patient age (20–80 years)      |
| Gender         | Male or Female                 |
| Blood_Pressure | Blood pressure level           |
| Sugar_Level    | Blood sugar level              |
| Cholesterol    | Cholesterol level              |
| Heart_Rate     | Heart rate (beats per minute)  |
| Risk_Level     | Predicted health risk category |

---

## Dataset Creation

The dataset is generated randomly using NumPy:

* Age: 20–80 years
* Blood Pressure: 80–180
* Sugar Level: 70–200
* Cholesterol: 150–300
* Heart Rate: 60–120

The dataset is saved as:

```text
healthcare_data.csv
```

---

## Data Preprocessing

### Missing Value Check

```python
data.isnull().sum()
```

Result:

```text
No missing values found
```

### Data Cleaning

```python
data = data.dropna()
```

Removes any incomplete records if present.

---

## Risk Level Classification

Patients are categorized based on health indicators.

### High Risk

* Blood Pressure > 140 OR
* Sugar Level > 160 OR
* Cholesterol > 240

### Medium Risk

* Blood Pressure > 120 OR
* Sugar Level > 120 OR
* Cholesterol > 200

### Low Risk

* Values within normal range

### Classification Function

```python
def risk_level(row):
    ...
```

---

## Statistical Analysis

The project calculates:

* Mean
* Standard Deviation
* Minimum Values
* Maximum Values
* Quartiles (25%, 50%, 75%)

### Sample Statistics

| Metric                 | Value  |
| ---------------------- | ------ |
| Average Age            | 50.29  |
| Average Blood Pressure | 129.67 |
| Average Sugar Level    | 135.62 |
| Average Cholesterol    | 224.57 |
| Average Heart Rate     | 89.89  |

---

## High Risk Patient Identification

```python
high_risk = data[data["Risk_Level"] == "High"]
```

### Result

```text
Total High Risk Patients: 7463
```

This helps healthcare providers identify patients requiring immediate attention.

---

## Data Visualizations

### 1. Histogram

**Age Distribution**
<img width="761" height="576" alt="Screenshot 2026-06-05 091312" src="https://github.com/user-attachments/assets/538a6307-596a-40e6-b590-0d4cb3a58036" />


* Shows the distribution of patient ages.

### 2. Bar Chart

**Risk Level Distribution**
<img width="792" height="562" alt="Screenshot 2026-06-05 091301" src="https://github.com/user-attachments/assets/61f4419b-a665-4187-a5b0-b1221343db7f" />


* Displays the count of Low, Medium, and High Risk patients.

### 3. Pie Chart

**Risk Percentage**
<img width="547" height="500" alt="Screenshot 2026-06-05 092204" src="https://github.com/user-attachments/assets/844adb79-3cf1-4f78-908c-a9607643d7af" />


* Shows the percentage of patients in each risk category.

### 4. Scatter Plot

**Age vs Blood Pressure**
<img width="731" height="511" alt="Screenshot 2026-06-05 091242" src="https://github.com/user-attachments/assets/f7ac99f3-55d4-4ad7-b815-eb38e4d8aa70" />


* Analyzes the relationship between age and blood pressure.

### 5. Box Plot

**Cholesterol Outliers**
<img width="650" height="546" alt="Screenshot 2026-06-05 091326" src="https://github.com/user-attachments/assets/71377fec-dedb-4c35-9d0f-0f1254f3a098" />


* Identifies extreme cholesterol values.

### 6. Correlation Heatmap

**Feature Relationships**
<img width="756" height="667" alt="Screenshot 2026-06-05 091337" src="https://github.com/user-attachments/assets/05829ca5-7367-4e2f-8bb8-65739bfd56d3" />


* Displays correlations among:

  * Age
  * Blood Pressure
  * Sugar Level
  * Cholesterol
  * Heart Rate

---

## Additional Analysis

### Gender vs Risk Level

```python
data.groupby("Gender")["Risk_Level"].value_counts()
```

Analyzes risk distribution among male and female patients.

### Age vs Average Blood Pressure

```python
data.groupby("Age")["Blood_Pressure"].mean()
```

Shows how blood pressure changes across age groups.

---

## Key Findings

* The dataset contains **10,000 complete patient records**.
* No missing values were detected.
* Approximately **7,463 patients** were classified as High Risk.
* Blood pressure, sugar level, and cholesterol significantly influence risk classification.
* Visualization techniques help identify trends and potential health concerns.
* Correlation analysis provides insights into relationships between health indicators.

---

## Project Workflow

```text
Data Generation
       ↓
Data Cleaning
       ↓
Statistical Analysis
       ↓
Risk Classification
       ↓
High Risk Detection
       ↓
Data Visualization
       ↓
Insights & Reporting
```

---

## Conclusion

This project demonstrates the use of Python-based data analytics in healthcare. By generating and analyzing patient records, the system identifies health risks and provides meaningful insights through statistical analysis and visualizations. Such techniques can support healthcare professionals in monitoring patient health and making informed decisions.

---

## Author

**Healthcare Data Analysis and Risk Prediction Project**

Developed using:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
