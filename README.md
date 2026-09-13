# E-Commerce Exploratory Data Analysis (EDA) & Business Insights

## Project Description
This project analyzes e-commerce order records using Python to uncover key revenue drivers, customer purchasing habits, and return patterns. The goal is to clean messy transaction data, perform statistical feature analysis, evaluate multi-variable relationships, and provide actionable business recommendations to increase sales and reduce refund leakage.

---

## Dataset Information
* **Source:** Kaggle (E-commerce Sales Transactions Dataset by Miadul)
* **Records:** 34,500 rows × 17 columns
* **Data Types:** Categorical, Continuous Numerical, Timestamps, Identifiers, and Booleans
* **Key Features:** `order_id`, `price`, `discount`, `quantity`, `category`, `returned`, `order_date`, `delivery_time_days`, `customer_age`, `customer_gender`, `region`, `payment_method`

---

## Technologies Used
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / Google Colab
* **Version Control:** Git, GitHub

---

## Analysis Performed
1. **Data Import & Exploration:** Inspected dataset shape, schema types, and initial summary statistics.
2. **Data Cleaning:** Imputed missing values using medians and modes, removed exact duplicates, cast date features to `datetime`, and filtered out non-sensical non-positive values.
3. **Feature Analysis:** Measured distribution skewness and identified high-value order outliers using the Interquartile Range (IQR) method.
4. **Correlation Analysis:** Generated a Pearson correlation heatmap to evaluate linear dependencies between price, quantity, discount, delivery times, and order revenue.
5. **Data Visualization:** Built 12 custom charts (histograms, bar plots, line charts, box plots, stacked area graphs) to show sales trends and category performance.

---

## Key Findings
* **Top Categories:** Electronics ($3.4M+) and Home ($1.1M+) drive over 70% of total store revenue.
* **Price Drives Sales:** Unit price shows a strong positive correlation ($r = 0.80$) with total order value. High-priced products drive top-line growth more than item volume.
* **Ineffective Discounts:** Discount percentage shows zero link to total sales revenue ($r = 0.00$) and item quantity (r = -0.01). Price cuts currently fail to enlarge cart sizes.
* **High Return Leakage:** Fashion (8.2%) and Electronics (7.3%) record the highest return rates. Delivery times are identical across returned and non-returned items (4 days), proving refunds are not caused by shipping delays.
* **Millennial Spending:** Customers aged 30–44 generate over 40% of store sales, spending heavily on premium Electronics and Home goods.

---

## Business Recommendations
1. **Focus Procurement on Top Categories:** Direct 60% of inventory budget to Electronics and Home products targeting 30–44 year-olds, while reducing warehouse space for stagnant Beauty and Grocery stock.
2. **Switch to Minimum Spend Thresholds:** Replace site-wide flat discounts with spend incentives like "Spend $200, get 15% off" to boost cart quantity (r = 0.31).
3. **Cut Return Losses in Fashion & Electronics:** Add interactive sizing guides for Fashion and mandate pre-shipment quality checks for Electronics to fix product expectation gaps.
4. **Optimize Card Checkouts & Promote Wallets:** Keep credit/debit card processing fast since cards handle 60%+ of checkouts. Offer 5% cashback on digital wallets to raise adoption above 10%.
5. **Bundle Slow Stock with Bestsellers:** Offer low-performing Beauty, Toy, or Grocery items as checkout add-ons with Electronics or Fashion orders to clear inventory.

---

## Instructions to Run the Notebook
1. **Clone the Repository:**
    ```bash
   git clone [https://github.com/Aramish44/E-commerce-Data-Analysis.git](https://github.com/Aramish44/E-commerce-Data-Analysis.git)
   cd E-commerce-Data-Analysis
```bash
   pip install pandas numpy matplotlib seaborn jupyter
   jupyter notebook Task_01_EDA_Analysis.ipynb
