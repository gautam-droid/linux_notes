#### **Elements**

1. **Elements** are the individual items or subjects we collect data about.
    
2. Each **element** can be a person, object, event, or place.
    
3. In a data table, each row usually represents an **element**.
    
4. Examples include students in a class, products in a store, or countries in a survey.
    
5. We study **elements** to observe their characteristics or behaviors.
    
---

#### **Variables**

1. A **variable** is a property or characteristic of an element that can change.
    
2. It can be measured or recorded for each element.
    
3. Examples: age, height, weight, price, temperature.
    
4. Variables can be **quantitative** (numerical) or **qualitative** (categorical).
    
5. Each **variable** has a name (like "age") and values (like 21, 25, etc.).
    


---

### 🔹 **Data Categorization (Definition)**

1. It is the **process of organizing data** into specific groups or types.
    
2. Helps in **understanding**, **analyzing**, and **managing data** efficiently.
    
3. Based on **nature**, **characteristics**, or **measurement level** of data.
    
4. Useful in **data analysis**, **statistics**, and **decision-making**.
    
5. Makes data **structured** and **easier to handle**.
    
---

### 🔹 **Classification of Data**

#### 1. **Based on Nature**

- **Qualitative (Categorical) Data**:
    
    - Describes qualities or characteristics.
        
    - E.g., color, gender, type.
        
- **Quantitative (Numerical) Data**:
    
    - Represents numeric values.
        
    - E.g., age, height, marks.
        

#### 2. **Based on Measurement**

- **Nominal**: Labels only (e.g., blood group).
    
- **Ordinal**: Order matters but not the difference (e.g., ranks).
    
- **Interval**: Order + difference meaningful, no true zero (e.g., temperature).
    
- **Ratio**: Order + difference + true zero (e.g., weight, height).
    

#### 3. **Based on Source**

- **Primary Data**: Collected firsthand by the researcher.
    
- **Secondary Data**: Already collected and used from other sources.
    

#### 4. **Based on Time**

- **Cross-sectional Data**: Collected at a single point in time.
    
- **Time-series Data**: Collected over a period of time.

---
# LEVELS OF MEASUREMENT

It tells us **how data is categorized, ordered, and calculated** — from simple labeling to full mathematical analysis.
### 🔹 **1. Nominal Level**

1. Used for **labeling or naming categories**.
    
2. No **order or ranking** between values.
    
3. Examples: gender, religion, blood group.
    
4. Can only be **counted**, not measured.
    
5. Basic level of measurement.
    

> **Keywords**: _nominal, labels, categories, no order, classification_

---

### 🔹 **2. Ordinal Level**

1. Data can be **ranked or ordered**.
    
2. **Differences** between values are **not meaningful**.
    
3. Examples: satisfaction levels (high, medium, low), ranks in a race.
    
4. Only **order matters**, not exact gaps.
    
5. Cannot perform arithmetic operations.
    

> **Keywords**: _ordinal, order, rank, no fixed difference, levels_

---

### 🔹 **3. Interval Level**

1. Data is **ordered** with **equal intervals** between values.
    
2. **No true zero** point.
    
3. Examples: temperature (Celsius/Fahrenheit), IQ score.
    
4. Can add and subtract values.
    
5. Ratios are not meaningful.
    

> **Keywords**: _interval, equal spacing, no true zero, add/subtract_

---

### 🔹 **4. Ratio Level**

1. All properties of interval scale **plus a true zero**.
    
2. **Meaningful ratios** can be calculated.
    
3. Examples: height, weight, age, income.
    
4. Can do **all arithmetic operations**.
    
5. Most informative level.
    

> **Keywords**: _ratio, true zero, full operations, measurements, comparison_

---

# Indexing and Data management ,sampling ,resampling (some parts are here)from notes

# Resampling
Here are **short notes** on **Cross-Validation** and **Bootstrapping** – ideal for quick revision:

---

### ✅ **Cross-Validation (CV) – Short Notes**

- **Definition**: A resampling method used to **evaluate model performance** by splitting data into multiple parts (folds).
    
- **No replacement** – each data point appears in test set only once per fold.
    
- **Types**:
    
    - **k-Fold CV**: Split data into _k_ parts; train on _k–1_, test on 1.
        
    - **Leave-One-Out CV (LOOCV)**: Use one sample as test, rest as train; repeat for all samples.
        
    - **Stratified k-Fold**: Maintains class balance in each fold (useful in classification).
        
    - **Repeated k-Fold**: k-Fold CV repeated multiple times with different splits.
        
- **Use**: Model evaluation, **hyperparameter tuning**, avoiding overfitting.
    

---

### 🔁 **Bootstrapping – Short Notes**

- **Definition**: A resampling method where **samples are drawn with replacement** from the original dataset.
    
- **Each sample may contain duplicates**; some original points may be missing.
    
- **Used to estimate**:
    
    - Confidence intervals
        
    - Variance and bias of statistics
        
    - Model stability
        
- **Use**: Statistical estimation when data is small or distribution is unknown.
    

---

# **Statistical Inference** and **Descriptive Statistics**:

### 🔹 **Descriptive Statistics**

Used to **summarize and describe** the features of a dataset.

1. **Measures of Central Tendency** – Mean, Median, Mode.
    
2. **Measures of Dispersion** – Range, Variance, Standard Deviation.
    
3. **Data Visualization** – Bar graphs, Histograms, Pie charts.
    
4. **Describes** what the data shows without making predictions.
    
5. Useful for **presenting raw data in a meaningful way**.
    

**Keywords**: Mean, Median, Mode, Standard Deviation, Data Summary

---

### 🔹 **Statistical Inference**

Used to **make conclusions or predictions** about a population based on a sample.

1. Involves **hypothesis testing** and **confidence intervals**.
    
2. Helps in **estimating population parameters**.
    
3. Uses **probability theory** to draw conclusions.
    
4. Two main types: **Estimation** and **Hypothesis Testing**.
    
5. Requires **random sampling** for valid results.
    

---

### 🔹 **Measures of Central Tendency**

These are used to **find the center or average** of a dataset.

1. **Mean (Average)**
    
    - Sum of all values divided by the number of values.
        
    - Affected by **extreme values (outliers)**.
        
        
        
        
$$
\text{Mean} = \frac{\sum_{i=1}^{n} x_i}{n}
$$

2. **Median**
    
    - The **middle value** when data is sorted.
        
    - Not affected by outliers.
        
    - If even number of values, median = average of two middle values.
        
3. **Mode**
    
    - The value that occurs **most frequently**.
        
    - Can have more than one mode or no mode.
        
    - Useful for **categorical data**.
        
4. **Comparison**
    
    - Mean is best for **symmetric data**.
        
    - Median is best for **skewed data**.
        
    - Mode is best for **categorical or repeating data**.
        
5. **Use in Real Life**
    
    - Mean: Average marks in a class.
        
    - Median: Middle income in a city.
        
    - Mode: Most sold shoe size in a store.
        

---

# **Measures of Location** and **Measures of Dispersion** in points:

---

### 🔹 **Measures of Location**

(Used to identify the position of a value in the dataset)

1. **Median**
    
    - The **middle value** in an ordered dataset.
        
    - Divides the data into two equal halves.
        
2. **Quartiles (Q1, Q2, Q3)**
    
    - Divide the data into **four equal parts**.
        
    - Q1 = 25th percentile, Q2 = Median, Q3 = 75th percentile.
        
3. **Percentiles**
    
    - Divide the data into **100 equal parts**.
        
    - 90th percentile means 90% of values fall below it.
        
4. **Deciles**
    
    - Divide the data into **10 equal parts**.
        
    - D1 = 10th percentile, D9 = 90th percentile.
        
5. **Mode**
    
    - The most frequently occurring value in the data.
        
    - A type of location measure for categorical data.
        

**Keywords**: Median, Quartiles, Percentiles, Deciles, Mode

---

🔹 Measures of Dispersion  
(Describe the spread or variability in the data)

**Range**

Difference between maximum and minimum values.  
Simple but affected by outliers.  
Formula: Range = Max - Min

**Variance**

Average of squared differences from the mean.  
Formula: Variance = (Σ(xᵢ − x̄)²) / n

**Standard Deviation (SD)**

Square root of variance.  
Shows how much values deviate from the mean.  
Lower SD = data is close to the mean.  
Formula: SD = √[(Σ(xᵢ − x̄)²) / n]

**Interquartile Range (IQR)**

Spread of the middle 50% of data.  
Formula: IQR = Q3 - Q1

**Mean Absolute Deviation (MAD)**

Average of absolute deviations from the mean.  
Less sensitive to outliers than variance.  
Formula: MAD = (Σ|xᵢ − x̄|) / n
