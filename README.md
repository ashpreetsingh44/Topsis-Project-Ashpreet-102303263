# TOPSIS Project – Ashpreet Singh (Roll No: 102303263)

## Introduction

TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) is a
multi-criteria decision making method used to rank alternatives based on their
distance from the ideal best and ideal worst solutions.

The best alternative should have the shortest distance from the ideal best
and the farthest distance from the ideal worst.

---

## Objective

To rank different alternatives using multiple criteria by applying the TOPSIS
method using Python and Google Colab, and to provide the solution through
package distribution and web-based service.

---

## Dataset Description

The input dataset is a CSV file containing:

- First column: Name of alternatives
- Remaining columns: Criteria values

Example:

Alternative, C1, C2, C3, C4  
M1, 1, 2, 3, 4  
M2, 2, 3, 4, 5  
M3, 3, 4, 5, 6  

---

## Methodology (Step-by-Step)

### Step 1: Read Input Data

The CSV file is uploaded and read using pandas library.

### Step 2: Normalization

Each criterion is normalized using:

Xij / sqrt(sum(Xij²))

This removes the effect of different units of measurement.

### Step 3: Weighted Normalized Matrix

Each normalized value is multiplied by its corresponding weight to represent
importance of each criterion.

### Step 4: Ideal Best and Ideal Worst

For each criterion:

- If impact is positive (+):  
  Ideal Best = maximum value  
  Ideal Worst = minimum value

- If impact is negative (-):  
  Ideal Best = minimum value  
  Ideal Worst = maximum value

### Step 5: Distance Calculation

Euclidean distance is calculated:

Distance from Ideal Best (D+)  
Distance from Ideal Worst (D-)

### Step 6: TOPSIS Score

Score is calculated using:

Si = D- / (D+ + D-)

Higher score means better alternative.

### Step 7: Ranking

Alternatives are ranked in descending order of TOPSIS score.

---

## Result Table Explanation

The output table contains:

- Original criteria values
- Topsis Score: closeness to ideal solution
- Rank: position based on score

Rank 1 indicates the best alternative.

---

## Result Graph Explanation

A bar graph is plotted between:

- X-axis: Alternatives
- Y-axis: TOPSIS Score

Higher bar indicates better performance of alternative.

This helps in visual comparison of ranking.

---

## Part 1: Google Colab Notebook Implementation

The complete implementation of TOPSIS is provided in a Google Colab notebook.

It includes:

- Data upload
- Step-by-step TOPSIS calculation
- Result table
- Graph visualization

The notebook explains each stage of the algorithm clearly.

Files are available in the folder:

Colab-Notebook/

---

## Part 2: Python Package Published on PyPI

The TOPSIS algorithm is also implemented as a Python package and published on PyPI.

### Package Name

Topsis-Ashpreet-102303263

### PyPI Link

https://pypi.org/project/Topsis-Ashpreet-102303263/

### Installation Command

pip install Topsis-Ashpreet-102303263

### Command Line Usage

topsis input.csv "0.25,0.25,0.25,0.25" "+,+,-,+" result.csv

### Output

The output CSV file contains:

- Topsis Score
- Rank of each alternative

### Error Handling

The package validates:

- File existence
- Numeric criteria values
- Correct number of weights
- Valid impacts (+ or -)
- Proper CSV format

---

## Part 3: Web Service Implementation

A web-based interface is developed where the user can apply TOPSIS online.

### Website Features

- Upload CSV file
- Enter weights
- Enter impacts
- Download result CSV

### Live Website Link

https://topsis-web-ashpreet-singh-102303263.vercel.app/

### Working

1. User uploads CSV file
2. Inputs weights and impacts
3. TOPSIS is calculated in browser
4. Result CSV is downloaded automatically

This allows users to apply TOPSIS without installing any software.

---

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Google Colab
- HTML
- Vercel Hosting

---


## Conclusion

TOPSIS provides an effective way to rank alternatives using multiple criteria.
It is useful in decision-making problems where several factors are involved.
The method is simple, logical, and easy to implement using Python.

The project demonstrates TOPSIS through:

- Notebook-based analysis
- Software packaging
- Web-based application

