# ✈️ Flight Price Analysis & Prediction

An end-to-end data analysis project on airline flight data, exploring what drives ticket prices in India and preparing the dataset for machine learning.

**Developed by:** Anjaly EM
---

## 📌 Project Objective

This project analyzes airline flight data (`airlines_flights_data.csv`) to understand:

- How ticket prices vary by airline, travel class, duration, and booking time
- Which factors influence price the most
- How to prepare the data for a price-prediction model

## 📂 Dataset Overview

| Detail | Value |
|---|---|
| Records | 300,153 |
| Columns | 12 |
| Missing values | 0 |
| Duplicate rows | 0 |
| Airlines | 6 |
| Cities (source / destination) | 6 each |
| Travel classes | Economy, Business |
| Price range | ₹1,105 – ₹1,23,071 |
| Average price | ₹20,889 |

**Key columns:** `airline`, `flight`, `source_city`, `departure_time`, `stops`, `arrival_time`, `destination_city`, `class`, `duration`, `days_left`, `price`

## 🛠️ Tools & Libraries

- **Python**
- **Pandas** & **NumPy**: data handling
- **Matplotlib** & **Seaborn**: visualization
- **Scikit-learn**: encoding, scaling, train-test split
- **Jupyter Notebook**

## 🔄 Project Workflow

1. **Data Loading & Understanding**: shape, data types, summary statistics
2. **Data Cleaning**: duplicate check, whitespace cleanup, missing value check
3. **Outlier Handling**: IQR method (upper bound ₹99,128), capped extreme prices
4. **Exploratory Data Analysis**: airline, class, duration and booking-time analysis
5. **Visualization**: boxplot, countplot, scatterplot, lineplot, heatmap
6. **ML Preparation**: label encoding, train-test split (80/20), feature scaling

## 📊 Visualizations & Insights

The full charts are available in the notebook. Key insights from each:

- **Outlier Detection (Boxplot):** Price is right-skewed (mean ₹20,889 vs median ₹7,425). A few very expensive Business-class fares pull the average up, so outliers were capped using the IQR method.
- **Flights by Airline (Countplot):** Vistara and Air India have the most listings, so they influence overall price trends the most.
- **Duration vs Price (Scatterplot):** Business class fares stay high regardless of duration, while Economy fares stay low and rise only slightly with longer flights. Class matters more than duration.
- **Price vs Days Left (Lineplot):** Prices are higher when very few days are left before departure and drop as bookings are made earlier (roughly 10+ days ahead).
- **Correlation Matrix (Heatmap):** Duration and days_left have weak correlation with price, so categorical features like airline and class are the main drivers.

## 🔍 Key Findings

| Factor | Finding |
|---|---|
| **Travel class** | Business (avg ₹52,533) costs ~8x more than Economy (avg ₹6,572) |
| **Airline** | Vistara (₹30,391) and Air India (₹23,507) are far costlier than AirAsia (₹4,091) and Indigo (₹5,324) |
| **Booking time** | Last-minute bookings cost more, but the trend is volatile, not a straight line |
| **Duration** | Weak effect on price, especially once class is considered |
| **Data quality** | No duplicates or missing values, so cleaning effort was minimal |

## 🤖 Machine Learning Preparation

- Categorical columns encoded using `LabelEncoder`
- Data split into 80% training and 20% testing (`random_state=42`)
- Features scaled using `StandardScaler`

**Next step:** build and compare regression models (Linear Regression, Random Forest, etc.) to predict flight prices.

## 📁 Repository Structure

```
Flight-Price-Analysis-and-Prediction/
│
├── Flight Price Analysis & Prediction.ipynb  # Main notebook
├── airlines_flights_data.csv                 # Dataset
└── README.md
```

## ▶️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/anjalyem/Flight-Price-Analysis-and-Prediction.git

# 2. Install required libraries
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# 3. Open the notebook
jupyter notebook
```

## 👩‍💻 Author

**Anjaly EM**

🔗 [GitHub](https://github.com/anjalyem)
