# 📊 Day 10 Python Challenge

## Data Drift Detection using Shallow Copy vs Deep Copy

---

## 📌 Overview

This project simulates a **student data analysis system** to demonstrate the difference between **Shallow Copy** and **Deep Copy** in Python.

It focuses on how data mutations impact original datasets and introduces the concept of **data drift detection** using statistical analysis.

---

## 🚀 Features

* Generate random student dataset
* Apply controlled mutations based on roll number
* Perform statistical analysis using:

  * Mean
  * Median
  * Standard Deviation
* Normalize data values
* Detect **data drift**
* Classify system behavior:

  * Stable Data
  * Minor Drift
  * Critical Drift
  * Copy Failure Detected
* Compare:

  * Shallow Copy behavior
  * Deep Copy behavior

---

## 🛠️ Technologies Used

* Python 3
* NumPy
* Pandas
* Built-in modules:

  * `random`
  * `copy`
  * `math`

---

## 📂 Project Structure

```bash
DAY_10/
│── day_10.py
│── README.md
```

---

## 🔍 Key Concepts

### 🔹 Shallow Copy

* Copies only outer structure
* Nested objects (like lists inside dictionaries) are **shared**
* Changes affect original data

### 🔹 Deep Copy

* Fully independent copy
* No shared references
* Safe for data manipulation

---

## ⚙️ Workflow

1. Generate student dataset with:

   * Marks
   * Attendance
   * Scores (nested list)

2. Create:

   * Shallow copy
   * Deep copy

3. Apply mutation:

   * Modify marks using square root logic
   * Update scores and attendance

4. Analyze data:

   * Convert to DataFrame
   * Compute mean, median, standard deviation
   * Normalize marks

5. Detect drift:

   * Compare original vs modified mean

6. Classify results:

   * Based on drift threshold and memory behavior

---

## 📊 Sample Output (Concept)

```text
--- DRIFT VALUES ---
Shallow Drift: High
Deep Drift: Low

--- FINAL CLASSIFICATION ---
Shallow Copy: Copy Failure Detected
Deep Copy: Stable Data
```

---

## ⚠️ Important Insight

Shallow copy shares nested objects (like `scores`).
So modifying shallow copy also changes original data, leading to **incorrect drift detection**.

Deep copy avoids this issue by creating independent data structures.

---

## ▶️ How to Run

```bash
py day_10.py
```

OR

```bash
python day_10.py
```

---

## 🎯 Learning Outcomes

* Understand shallow vs deep copy deeply
* Learn how data mutation affects analysis
* Implement basic data science concepts:

  * Mean, median, standard deviation
  * Normalization
* Detect and classify data drift

---

## 💡 Real-World Applications

* Data pipelines
* Machine learning preprocessing
* Financial data analysis
* API data handling
* Preventing unintended data corruption

---

## 👩‍💻 Author

**Jayasri**

---

## ⭐ If you found this useful

Give this repo a ⭐ on GitHub!
