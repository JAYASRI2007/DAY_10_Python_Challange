# Day 10 — Challenges

This folder contains Day 10 challenge files.

## Notes

* Requires Python 3.x. Use quotes around the filename if your shell requires them because of spaces.
* Requires external libraries: `numpy` and `pandas`. Install using:
  `pip install numpy pandas`
* Inspect the script for usage or required inputs.

## Challenge Description

`student drift analyzer.py` simulates student performance data and analyzes the effect of shallow and deep copy mutations. It generates student records, applies controlled mutations based on a roll number, calculates statistical measures, detects data drift, and classifies the results. It highlights how shallow copy can unintentionally modify original data, while deep copy preserves data integrity.

## Approach / Logic Used

* Generate student dataset with `marks`, `attendance`, and `scores`.
* Apply mutation based on `roll_number % 3` to selectively modify records.
* Use both shallow copy and deep copy to compare behavior.
* Convert data into a DataFrame and compute mean, median, standard deviation, and normalized values.
* Compute manual mean without using NumPy for validation.
* Detect drift as the difference between original and modified means.
* Classify results into Stable, Minor Drift, Critical Drift, or Copy Failure.
* Detect shallow copy issue by checking shared references in nested objects (`scores`).

## Algorithm / Steps

1. Generate a list of student records with random values.
2. Create both shallow copy and deep copy of the original data.
3. Apply mutation logic based on roll number to both copies.
4. Convert datasets into DataFrames and calculate statistics (mean, median, standard deviation, normalization).
5. Compute manual mean using a loop (without NumPy).
6. Calculate drift between original and modified datasets.
7. Detect copy failure by checking if nested objects are shared.
8. Classify results based on drift and copy behavior.
9. Print all datasets, statistics, drift values, and final classification.
