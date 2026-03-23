# 🏀 HoopVision AI — Player Performance Clustering System

HoopVision AI is a data-driven basketball analytics application that uses **machine learning (KMeans clustering)** and **dimensionality reduction (PCA)** to analyze NBA player performance and group players based on production patterns.

This project transforms raw basketball statistics into **actionable insights**, helping coaches, analysts, and developers better understand player roles, efficiency, and impact.

---

## 🚀 Overview

This application:

- Loads NBA regular season data (2012–2023)
- Cleans and engineers advanced performance metrics
- Calculates a custom **Total Production Score**
- Uses **PCA (Principal Component Analysis)** to reduce feature complexity
- Applies **KMeans clustering** to group similar players
- Visualizes clusters interactively using **Streamlit**

📎 Source Code: :contentReference[oaicite:0]{index=0}

---

## 🧠 Core Features

### 1. Data Processing
- Removes unnecessary columns
- Standardizes season format
- Converts categorical data into numerical representations

### 2. Custom Performance Metric
A proprietary **Total Production** formula combining:

#### Shooting Production
- 2PT, 3PT, FT efficiency

#### Ancillary Production
- Assists
- Rebounds (offensive + defensive)
- Steals
- Blocks
- Turnovers (negative impact)
- Fouls

---

### 3. Machine Learning Pipeline

- **StandardScaler** → Normalizes features
- **PCA** → Reduces dimensions for better clustering
- **KMeans** → Groups players into performance clusters

---

### 4. Interactive Dashboard (Streamlit)

Users can:
- Explore dataset columns and transformations
- View engineered metrics
- Analyze PCA explained variance
- Use the **Elbow Method** to determine optimal clusters
- Filter by:
  - Season
  - Team
  - Number of clusters
- Visualize player clusters in real-time

---

## 📊 How It Works

1. Load dataset (`Regular_Season.csv`)
2. Clean and transform data
3. Engineer production metrics
4. Scale numerical features
5. Apply PCA → reduce to 2D
6. Run KMeans clustering
7. Visualize results

---

## 🧩 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Streamlit

---

## 📦 Installation

```bash
git clone https://github.com/iteachai/hoopvision-ai.git
cd hoopvision-ai
pip install -r requirements.txt
streamlit run nbaKMeans.py
