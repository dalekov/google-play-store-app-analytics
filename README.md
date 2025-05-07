
# 📊 Google Play Store App Analytics

This project analyzes app data from the Google Play Store to uncover insights into app pricing, popularity, and category trends.

## 📁 Project Structure

```
.
├── Google Play Store App Analytics.ipynb
├── README.md
├── data/
│   └── googleplaystore.csv
├── plots/
│   └── boxplots, histograms, etc.
```

## 📌 Objectives

- Load and inspect the dataset
- Handle missing and inconsistent data
- Perform exploratory data analysis (EDA)
- Visualize trends across app categories, pricing, ratings, and installs

## 🛠️ Setup

1. **Install dependencies**  
   Run this in your terminal or notebook:

   ```bash
   pip install pandas plotly matplotlib seaborn
   ```

2. **Launch the Jupyter Notebook**  
   Open the notebook with:

   ```bash
   jupyter notebook "Google Play Store App Analytics.ipynb"
   ```

## 📊 Key Analysis Steps

- Check DataFrame shape and missing values
- Clean and convert data types (e.g., price, installs)
- Analyze price distributions using `.median()` and `.mean()`
- Plot box plots by category (`plotly.express`)
- Use log scale to handle skewed price data

## 📈 Sample Visualization Code

```python
import plotly.express as px

box = px.box(df_paid_apps, x='Category', y='Price', title='Pricing by category comparison')
box.update_layout(
    xaxis_title='Category',
    yaxis_title='Paid App Price',
    xaxis={'categoryorder': 'max descending'},
    yaxis=dict(type='log'),
    template='plotly_white'
)
```

## ✅ Output

- Cleaned dataset ready for modeling or deeper analysis
- Visual insights into app pricing trends
- Summary statistics of key metrics
