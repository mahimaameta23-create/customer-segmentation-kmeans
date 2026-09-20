# Prodigy InfoTech — Machine Learning Internship

## Task 02: Customer Segmentation using K-Means Clustering

### 📌 Problem Statement
Create a **K-means clustering algorithm** to group customers of a retail store based on their purchase history.

### 📂 Dataset
- **Name:** Mall Customers Dataset
- **File:** `data/Mall_Customers.csv`
- **Records:** 200 customers
- **Features:**
  - `CustomerID` — unique identifier
  - `Gender` — Male / Female
  - `Age` — customer age (years)
  - `Annual Income (k$)` — yearly income in thousand dollars
  - `Spending Score (1-100)` — score assigned by the mall based on customer behavior and spending nature

### 🎯 Objectives
1. Perform Exploratory Data Analysis (EDA)
2. Preprocess the data (encoding, scaling)
3. Determine the optimal number of clusters using the **Elbow Method** (validated with **Silhouette Score**)
4. Apply **K-Means Clustering** on relevant features (Annual Income & Spending Score)
5. Visualize the resulting customer segments
6. Interpret each segment and derive business insights

### 📁 Project Structure
```
Prodigy_ML_Task02/
│
├── data/
│   └── Mall_Customers.csv               # Input dataset
│
├── notebooks/
│   └── Customer_Segmentation_KMeans.ipynb   # Main working notebook
│
├── outputs/                             # Generated after running the notebook
│   ├── Mall_Customers_Segmented.csv     # Original data + Cluster label
│   └── Cluster_Summary.csv              # Per-cluster statistics & segment labels
│
├── requirements.txt                     # Python dependencies
└── README.md                            # This file
```

### ⚙️ Installation & Setup

1. **Clone / extract the project**
   ```bash
   cd Prodigy_ML_Task02
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate     # Linux / Mac
   venv\Scripts\activate        # Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter**
   ```bash
   jupyter notebook notebooks/Customer_Segmentation_KMeans.ipynb
   ```

5. **Run all cells** — outputs (segmented CSV, summary, plots) are generated automatically.

### 🧪 Methodology

| Step | Description |
|------|-------------|
| 1 | Load data and inspect shape, types, missing values |
| 2 | EDA — distributions, gender split, pairplot, correlation heatmap |
| 3 | Preprocess — encode gender, select features, standardize with `StandardScaler` |
| 4 | Elbow Method (WCSS) over k = 1…10 |
| 5 | Silhouette Score validation over k = 2…10 |
| 6 | Fit K-Means with the optimal k (=5) |
| 7 | 2D scatter plot of clusters + centroids |
| 8 | Per-cluster aggregation & auto-labeling into business segments |

### 📊 Key Results

- **Optimal k = 5** (confirmed by both Elbow and Silhouette methods)
- **Five customer segments identified:**
  1. **Target / High Value** — High income, high spending → highest ROI, prioritize loyalty programs
  2. **Careful / Rich Savers** — High income, low spending → luxury previews, trust-building offers
  3. **Careless Spenders** — Low income, high spending → EMI / credit-based promotions
  4. **Sensible / Low Priority** — Low income, low spending → low-cost mass marketing
  5. **Standard / Average** — Middle-of-the-road customers → steady upsell / cross-sell

### 🛠️ Technologies Used
- **Python 3.8+**
- **Pandas**, **NumPy** — data manipulation
- **Matplotlib**, **Seaborn** — visualization
- **Scikit-learn** — StandardScaler, KMeans, silhouette_score
- **Jupyter Notebook** — interactive analysis

### 📈 Business Impact
Segmentation lets the retail store:
- Personalize marketing to each customer group
- Allocate advertising budget where ROI is highest
- Design loyalty programs for the most profitable segment
- Identify and retain at-risk high-spend customers
- Reduce wasted spend on low-priority segments

### 👤 Author
**Prodigy InfoTech — Machine Learning Intern**
Task 02: Customer Segmentation with K-Means

### 📜 License
This project is developed as part of the Prodigy InfoTech ML Internship program and is intended for educational use.
