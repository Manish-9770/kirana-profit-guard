# Kirana Profit Guard

An end-to-end retail analytics app for Indian kirana (small grocery) stores. It combines MySQL dashboards with five machine learning modules in one multipage Streamlit app.

> **Note:** The dataset is synthetic (about 26,500 transactions) and was generated to mimic Indian retail patterns. It is not real store data.

## Features

**ML pages**
- **Revenue Predictor**: regression on daily product revenue
- **Stockout Risk**: classification to flag products likely to run out
- **Product Segments**: RFM-style clustering of products
- **Anomaly Review**: Isolation Forest on transactions
- **Sales Forecast**: time-series forecasting with Prophet

**MySQL dashboards**
- Five dashboard pages backed by an 8-table schema, 5 views and 34 SQL queries

**App features**
- Data entry forms (Add Product / Sale / Customer / Supplier, Update Stock)
- Role-based login (admin / manager / cashier) with bcrypt-hashed passwords
- AI Recommendations page
- Model Training page that re-runs the notebook

## Tech Stack

Python, pandas, scikit-learn, Prophet, Plotly, Streamlit, MySQL 8 / MariaDB, SQLAlchemy, PyMySQL, Jupyter, Excel, Chart.js

## Project Structure

```
.
├── app.py                  # Streamlit entry point (st.navigation)
├── pages/                  # ML and dashboard pages
├── sql/                    # Schema, views, queries
├── models/                 # Saved models (joblib)
├── data/                   # Synthetic dataset
├── kirana_profit_guard_ml.ipynb
├── requirements.txt
└── README.md
```

*(Adjust this to match your actual folders.)*

## Run Locally

1. Clone the repo
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Set up MySQL: create a database and run the scripts in `sql/` in order.
4. Set environment variables (never commit these):
   ```bash
   DB_HOST=localhost
   DB_USER=your_user
   DB_PASSWORD=your_password
   DB_NAME=kirana
   ```
5. Start the app
   ```bash
   streamlit run app.py
   ```

## Screenshots

*(Add 4-6 screenshots here, e.g. `![Dashboard](screenshots/dashboard.png)`)*

## Key Findings

- *(Add 3-4 insights from your data, e.g. which segments drive most revenue, how well the stockout model performs.)*

## Author

**Manish**: B.Tech CSE | Data Analyst
[LinkedIn](https://www.linkedin.com/in/your-profile)
