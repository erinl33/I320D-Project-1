# Week 3 Assignment: Breast Cancer Wisconsin Dataset Analysis

## I 320D: Data Science for Biomedical Informatics | Spring 2026

### 📋 Assignment Version E

---

## 🎯 This Week's Mantra

> **"Every Column Tells a Story"**

In this assignment, you'll apply the 10-Point Data Inspection to a real-world medical imaging dataset focused on breast cancer diagnosis. By the end, you'll understand not just *what* the data contains, but *why* each variable matters for clinical decision-making.

---

## Learning Objectives

By completing this assignment, you will be able to:

1. ✅ Apply the systematic 10-Point Inspection to a new healthcare dataset
2. ✅ Identify and classify feature types (continuous, discrete, categorical, ordinal)
3. ✅ Detect and document data quality issues (missing values, unexpected values)
4. ✅ Research and document clinical meaning for healthcare variables
5. ✅ Create meaningful data groupings based on clinical standards
6. ✅ Formulate answerable research questions about cancer diagnosis factors

---

## About the Dataset

**Dataset:** Wisconsin Diagnostic Breast Cancer (WDBC)  
**Source:** UCI Machine Learning Repository / Kaggle  
**File:** `data.csv`  
**Target Variable:** `diagnosis` (M = Malignant, B = Benign)

### Clinical Context

Breast cancer is the most common cancer among women worldwide, affecting about 2.3 million women annually according to the World Health Organization (WHO). This dataset contains features computed from digitized images of fine needle aspirate (FNA) of breast masses. The features describe characteristics of the cell nuclei present in the image.

Understanding these variables is crucial for:

- Computer-aided diagnosis (CAD) systems
- Early detection of malignant tumors
- Reducing unnecessary biopsies
- Supporting clinical decision-making in oncology

### Feature Categories

The dataset contains **30 numeric features** organized into three measurement types for each of **10 characteristics**:

| Suffix | Meaning | Description |
|--------|---------|-------------|
| `_mean` | Mean | Average value across all nuclei in the image |
| `_se` | Standard Error | Variation in measurements |
| `_worst` | Worst/Largest | Mean of the three largest values |

The **10 cell nuclei characteristics** measured are:
- **radius** - mean distance from center to points on the perimeter
- **texture** - standard deviation of gray-scale values
- **perimeter** - boundary length of the nucleus
- **area** - area of the nucleus
- **smoothness** - local variation in radius lengths
- **compactness** - (perimeter² / area) - 1.0
- **concavity** - severity of concave portions of the contour
- **concave points** - number of concave portions of the contour
- **symmetry** - symmetry of the nucleus
- **fractal dimension** - "coastline approximation" - 1

---

## Getting Started

First, load the dataset and import your libraries:

```python
# Import libraries


# Load the dataset


# Display first few rows to confirm it loaded

```

---

## Part 1: The 10-Point Data Inspection (40 points)

Complete each inspection step and document your findings.

### Step 1: Shape (4 points)

**Your Code:**
```python

```

**Your Findings:**
- How many rows (observations/patients)? _______________
- How many columns (features)? _______________
- What does each row represent in clinical terms? _______________

---

### Step 2: Column Names (4 points)

**Your Code:**
```python

```

**Your Findings:**
- List all column names:

- Do you notice any pattern in the column naming convention?

- Which columns might need further research to understand?

---

### Step 3: Data Types (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns are numeric (int64 or float64)?

- Which columns are categorical (object/string)?

- Are there any data types that seem incorrect?

---

### Step 4: First Look (4 points)

**Your Code:**
```python

```

**Your Findings:**
- What do the actual values look like?

- Do you notice anything unusual or unexpected?

- What are the possible values for the `diagnosis` column?

---

### Step 5: Last Look (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Does the data end cleanly?

- Are the last rows consistent with the first rows?

---

### Step 6: Memory Usage (4 points)

**Your Code:**
```python

```

**Your Findings:**
- How much memory does the dataset use? _______________ KB
- Is this a "small" or "large" dataset by data science standards?

---

### Step 7: Missing Values (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns have missing values (according to `.isnull()`)?

- What percentage of each column is missing?

- ⚠️ **IMPORTANT:** Do you notice any columns that appear to be entirely empty or have suspicious patterns?

---

### Step 8: Duplicates (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Are there any duplicate rows? _______________
- Are all patient IDs unique? _______________

---

### Step 9: Basic Statistics (4 points)

**Your Code:**
```python

```

**Your Findings:**
- What is the radius_mean range in the dataset? _______________ to _______________
- What is the range of area_mean values? _______________ to _______________
- What is the range of concavity_mean values? _______________ to _______________
- Do any min/max values seem impossible or clinically unlikely?

---

### Step 10: Unique Counts (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns have very few unique values (likely categorical)?

- Which columns have many unique values (likely continuous)?

- Does the number of unique IDs match the number of rows? _______________

---

## Part 2: Data Dictionary (20 points)

Complete the following data dictionary for the **key columns**. For each column, you must:
1. **Research** the clinical meaning
2. **Identify** the feature type (Continuous, Discrete, Categorical-Nominal, Categorical-Ordinal, Binary, Identifier)
3. **Document** the valid values/range you observe
4. **Note** any issues or questions

| Column | Description | Feature Type | Valid Values/Range | Notes/Issues |
|--------|-------------|--------------|-------------------|--------------|
| `id` | | | | |
| `diagnosis` | | | | |
| `radius_mean` | | | | |
| `texture_mean` | | | | |
| `perimeter_mean` | | | | |
| `area_mean` | | | | |
| `smoothness_mean` | | | | |
| `compactness_mean` | | | | |
| `concavity_mean` | | | | |
| `concave points_mean` | | | | |
| `symmetry_mean` | | | | |
| `fractal_dimension_mean` | | | | |

### Clinical Research Questions for Version E

Answer these questions based on your research (you may need to use Google):

**1. What is nuclear pleomorphism and why is it important in cancer grading systems like the Nottingham grading system? How does cell symmetry relate to pleomorphism?**

Your answer:

---

**2. What is the biological basis for why cancer cells often show asymmetry? How do abnormal cell division and chromosomal instability contribute to irregular cell shapes?**

Your answer:

---

**3. Explain what the symmetry measurement in this dataset captures mathematically. How is symmetry calculated from the cell nucleus contour?**

Your answer:

---

**4. What is the Breast Imaging Reporting and Data System (BI-RADS)? How do shape and symmetry features factor into the BI-RADS classification of breast masses?**

Your answer:

---

## Part 3: Data Validation (15 points)

### 3.1 Diagnosis Distribution Validation (5 points)

Write code to check:
- How many patients have malignant (M) tumors?
- How many patients have benign (B) tumors?
- What is the percentage of each?

**Your Code:**
```python

```

**Your Findings:**

- Is this dataset balanced or imbalanced between the two classes?

- In the real world, what percentage of breast biopsies are malignant vs benign?

---

### 3.2 Empty Column Validation (5 points)

Write code to examine all columns for any that might be completely empty or contain only null values.

**Your Code:**
```python

```

**Your Findings:**

- Did you find any columns that are entirely empty?

- What should you do with such columns before analysis?

- Why might an empty column exist in a dataset?

---

### 3.3 Feature Range Validation (5 points)

Write code to check if the "worst" measurements are always greater than or equal to the "mean" measurements for the same characteristic.

**Your Code:**
```python

```

**Your Findings:**

- Does `radius_worst` always >= `radius_mean`?

- Does this relationship hold for other features?

- What would it mean if this relationship was violated?

---

## Part 4: Create Cell Symmetry Groups (10 points)

Create a new column called `symmetry_category` that categorizes tumors into clinically-meaningful groups based on `symmetry_mean` (a measure of how symmetrical the cell nuclei are).

### Version E: Symmetry-Based Clinical Categories

Use these categories based on observed symmetry values (where higher values indicate more asymmetry):

| Symmetry Category | Symmetry Range | Clinical Rationale |
|-------------------|----------------|-------------------|
| Highly Symmetric | < 0.14 | Very regular cell shape, typical of benign cells |
| Symmetric | 0.14 - 0.17 | Normal symmetry range, most cells fall here |
| Mildly Asymmetric | 0.17 - 0.20 | Some irregularity, warrants closer examination |
| Asymmetric | 0.20 - 0.25 | Notable asymmetry, associated with abnormal growth |
| Highly Asymmetric | ≥ 0.25 | Significant asymmetry, strong indicator of malignancy |

### Your Code:

```python
# Create the symmetry_category column
# You can use a custom function with .apply() OR pd.cut()
# Remember: if using pd.cut(), use include_lowest=True!


```

### Verify your groupings worked:

```python
# Show counts per symmetry category

```

### Calculate malignancy rate by symmetry category:

```python
# Calculate the percentage of malignant diagnoses in each symmetry category

```

### Analysis Questions:

**1. How many tumors are in each symmetry category?**

Your answer:

---

**2. What is the malignancy rate (percentage) for each symmetry category?**

Your answer:

---

**3. At what level of asymmetry does malignancy rate noticeably increase? Does cell symmetry appear to be a useful diagnostic feature?**

Your answer:

---

**4. Why might highly asymmetric cells be more likely to be malignant? (Think about how cancer cells divide and grow differently from normal cells.)**

Your answer:

---

## Part 5: Research Questions (15 points)

### 5.1 Write Three Answerable Questions (9 points)

Write three questions that THIS dataset can answer. Remember: the data can show relationships and patterns, but cannot prove causation.

**Your questions must explore these specific areas:**

1. **A question about symmetry and compactness together:**


---

2. **A question comparing symmetry_mean vs symmetry_worst:**


---

3. **A question about the relationship between symmetry and area:**


---

### 5.2 Identify One Question the Data CANNOT Answer (3 points)

Write one question about **tumor location or breast density** that this dataset cannot answer, and explain why.

**Question:**


**Why it cannot be answered with this data:**


---

### 5.3 Grouping Analysis (3 points)

Answer this question using a groupby analysis:

**"What is the average symmetry_mean for each diagnosis category (M vs B)?"**

**Your Code:**
```python

```

**Your Interpretation:**

How does symmetry differ between malignant and benign tumors? What does this suggest about the shape characteristics of cancer cells?


---

## Part 6: Target Variable Analysis (Bonus - 5 points)

The `diagnosis` column is our **target variable** - what we're trying to predict. Analyze its relationship with key features.

**Your Code:**
```python
# Show the distribution of diagnosis
# Calculate summary statistics for at least 3 key features, grouped by diagnosis

```

### Bonus Questions:

**1. What percentage of patients in this dataset have malignant tumors?**

Your answer:

---

**2. Which feature shows the largest difference between malignant and benign tumors?**

Your answer:

---

**3. Why does class imbalance matter for machine learning classification? (You may need to research this)**

Your answer:

---

**4. If you were building a diagnostic model, which 3 features would you prioritize based on your analysis? Justify your choices.**

Your answer:

---

## Submission Checklist

Before submitting, verify you have completed:

- [ ] **Part 1:** All 10 inspection steps with code AND written findings
- [ ] **Part 2:** Complete data dictionary with 12 key columns filled in
- [ ] **Part 2:** Answered all 4 clinical research questions
- [ ] **Part 3:** All 3 validation checks with code and answers
- [ ] **Part 4:** Created `symmetry_category` column using **Symmetry-Based Clinical Categories**
- [ ] **Part 4:** Calculated malignancy rate by symmetry category with interpretation
- [ ] **Part 5:** Three research questions (symmetry+compactness, symmetry mean vs worst, symmetry+area)
- [ ] **Part 5:** One unanswerable question about tumor location/breast density
- [ ] **Part 5:** symmetry_mean by diagnosis groupby analysis
- [ ] **Bonus (Optional):** Target variable analysis

---

## Grading Rubric

| Component | Points | Requirements for Full Credit |
|-----------|--------|------------------------------|
| Part 1: 10-Point Inspection | 40 | All 10 steps complete with working code AND thoughtful written analysis |
| Part 2: Data Dictionary | 20 | All 12 columns documented with correct feature types and clinical research |
| Part 3: Data Validation | 15 | All validation checks complete with working code and insightful answers |
| Part 4: Symmetry Groups | 10 | Working code that creates correct groups AND meaningful interpretation |
| Part 5: Research Questions | 15 | Three good questions in specified areas, one clear limitation, groupby analysis complete |
| **Bonus:** Target Analysis | +5 | Thoughtful analysis with real-world connection |
| **Total** | 100 (+5 bonus) | |

---

## Hints (Read Before You Get Stuck!)

### ⚠️ Common Pitfalls:

1. **One column appears to be entirely empty** (all NaN values)
   - Check the last column carefully
   - This often happens with CSV exports that have trailing commas
   - You should drop this column before analysis

2. **The diagnosis column uses single letters** - "M" and "B"
   - Don't forget what these stand for when interpreting results
   - You may need to convert to 0/1 for some calculations

3. **Symmetry values are relatively small** - typically between 0.1 and 0.3
   - Pay attention to the decimal places when creating categories
   - Make sure your bin edges are precise

4. **Continuous features** - most features in this dataset are continuous
   - Think carefully about appropriate grouping strategies

### 💡 Pro Tips:

- Use `value_counts()` liberally to understand categorical columns
- Use `value_counts(dropna=False)` to see if there are any null values
- When using `pd.cut()` with custom bins, include `float('-inf')` or `float('inf')` to catch all values
- The `describe()` method works best with numeric columns
- For comparing groups, `groupby().mean()` is your friend

---

## Useful Resources

- **UCI ML Repository - Original Dataset:** https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)
- **Kaggle Dataset Page:** https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data
- **American Cancer Society - Breast Cancer:** https://www.cancer.org/cancer/breast-cancer.html
- **Nottingham Grading System:** https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3714112/
- **Pandas Documentation:** https://pandas.pydata.org/docs/

---

*Remember: "Every Column Tells a Story" - your job is to figure out what that story is!*

---

**Due Date:** [See Canvas]

**Submission:** Upload your completed Jupyter notebook (.ipynb) to Canvas
