# 🎬 IMDB Movie Recommender System

<p align="center">
  <b>Content-Based Recommendation System with User Profiling & Genre Encoding</b>
</p>

---

## 📌 Project Overview

This project implements a **Movie Recommendation System** using the IMDB dataset provided by GroupLens.

The goal is to:

* Build a Content-Based Recommender System
* Perform User Profiling based on genre preferences
* Apply data preprocessing and feature engineering
* Generate personalized movie recommendations

This project is implemented in **Python (Pandas, NumPy, Matplotlib)** inside a Jupyter Notebook environment.

---

## 📂 Dataset Description

The dataset consists of two CSV files:

### 1️⃣ movies.csv

| Column  | Description                         |   |
| ------- | ----------------------------------- | - |
| movieId | Unique movie identifier             |   |
| title   | Movie title (includes release year) |   |
| genres  | Movie genres separated by `         | ` |

### 2️⃣ ratings.csv

| Column    | Description                      |
| --------- | -------------------------------- |
| userId    | Unique user identifier           |
| movieId   | Movie rated by the user          |
| rating    | Rating given by user (0.5 – 5.0) |
| timestamp | Rating submission time           |

Source: [https://grouplens.org](https://grouplens.org)

---

## ⚙️ Project Pipeline

### 🔹 1. Data Loading

* Load datasets using Pandas
* Inspect structure and data types

### 🔹 2. Data Preprocessing

* Extract release year from movie title
* Clean movie titles
* Split genres into lists
* One-Hot Encode genres
* Remove unnecessary columns

### 🔹 3. User Simulation (Cold-Start Scenario)

* Create a hypothetical user
* Assign ratings to selected movies
* Map titles to movieId

### 🔹 4. User Profile Construction

* Extract genre vectors for rated movies
* Weight genres by user ratings
* Compute user preference vector

### 🔹 5. Recommendation Scoring

* Multiply user profile by global genre matrix
* Normalize scores
* Remove already rated movies
* Return Top-N recommendations

---

## 🧠 Mathematical Formulation

User profile vector:

```
User_Profile = Genre_Matrixᵀ × Rating_Vector
```

Recommendation score:

```
Score(movie) = (Genre_Vector · User_Profile) / sum(User_Profile)
```

---

## 🎯 Example Output

Top 10 Recommended Movies:

| Rank | Title           | Year | Score |
| ---- | --------------- | ---- | ----- |
| 1    | Example Movie 1 | 1999 | 0.842 |
| 2    | Example Movie 2 | 2001 | 0.831 |
| ...  | ...             | ...  | ...   |

---

## 🚀 How to Run

1️⃣ Clone the repository

```
git clone https://github.com/your-username/movie-recommender-system.git
```

2️⃣ Install dependencies

```
pip install -r requirements.txt
```

3️⃣ Open Jupyter Notebook

```
jupyter notebook
```

4️⃣ Run all cells in order

---

## 📦 Project Structure

```
movie-recommender-system/
│
├── data/
│   ├── movies.csv
│   └── ratings.csv
│ recommender.ipynb
│
├── README.md
└── requirements.txt
```

---

## 🛠 Requirements

* Python 3.10+
* pandas
* numpy
* matplotlib

Example `requirements.txt`:

```
pandas
numpy
matplotlib
```

---

## 🔍 Key Features

✔ Clean and modular notebook structure
✔ Efficient One-Hot Encoding (no loops)
✔ Cold-start user simulation
✔ Normalized recommendation scoring
✔ GitHub-ready documentation

---

## 📈 Possible Improvements

* Add Collaborative Filtering (User-Based / Item-Based)
* Apply Matrix Factorization (SVD)
* Add Clustering (KMeans) for user segmentation
* Build a simple web interface (Streamlit)
* Deploy as an API

---

## 👨‍💻 Author

mohammad hossein
Machine Learning & Data Science Enthusiast

---

## ⭐ If you found this project useful, consider giving it a star!
