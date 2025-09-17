## 📷 Screenshots
> ![ScreenShot](images/Screenshot%202025-09-17%20113743.png) 

# 📊 SpreadLocator Analysis

Welcome to the SpreadLocator Project! 🚀  
This repository contains the dataset and Jupyter notebook where statistical operations and distribution fitting have been performed on transaction-level data.

---

## 📂 Project Files
- spread_locator_dataset.csv → Transaction dataset (customer, region, status, amount, etc.).  
- SpreadLocator.ipynb → Jupyter notebook with statistical modeling and visualizations.  

---

## 🗂️ Dataset Overview
The dataset captures customer transactions with the following key fields:
- `transaction_id` → Unique identifier for each transaction.  
- `customer_id` → Unique customer reference.  
- `transaction_amount` → Monetary value of transaction.  
- `transaction_date` → Date of the transaction.  
- `transaction_count` → Count of transactions within a period.  
- `region` → Region of the transaction (`North`, `South`, `East`, `West`).  
- `transaction_status` → Status outcome (`Success` / `Fail`).  

Example preview (first few rows):

| transaction_id | customer_id | transaction_amount | transaction_date | transaction_count | region | transaction_status |
|----------------|-------------|---------------------|------------------|-------------------|--------|---------------------|
| e98aa092... | CUST2824 | 3821.34 | 2023-01-26 | 3 | North | Fail |
| 11ba6918... | CUST1409 | 2781.84 | 2023-01-28 | 0 | East | Fail |
| 82b7654b... | CUST5506 | 4120.97 | 2023-01-28 | 0 | South | Fail |
| f7166574... | CUST5012 | 6383.78 | 2023-01-18 | 2 | South | Success |
| 8632fe26... | CUST4657 | 2651.61 | 2023-01-04 | 4 | North | Success |

---

## 🛠️ Operations Performed

1. Distribution Fitting (Discrete Events)
   - Bernoulli & Binomial: Modeled transaction occurrence and weekly counts.
   - Poisson: Modeled number of transactions per day.

2. Continuous Modeling (Transaction Amounts)
   - Log-Normal & Power Law fitted to transaction amounts.  
   - Q-Q Plot generated to test normality assumption.

3. Variance Stabilization
   - Applied Box-Cox Transformation to normalize skewed data.

4. Outlier Detection & Probability
   - Calculated Z-scores for transaction amounts.  
   - Estimated probability of transactions exceeding 25,000.

5. Distribution Analysis
   - Plotted PDF & CDF for transaction amounts.  
   - Interpreted distribution shapes and tail behavior.

---

## 📈 Key Insights
- Transaction counts follow Poisson distribution, reflecting rare-event modeling.  
- Transaction amounts exhibit Log-Normal characteristics with heavy right skew, suggesting high-value outliers.  
- Variance stabilization improved interpretability for decision-making.  
- Probability of extremely large transactions ( >25,000 ) is very low but non-negligible, useful for fraud detection and risk assessment.  

---

## 💡 Business Implications
- Risk Management → Helps in setting thresholds for fraud detection.  
- Regional Analysis → Comparing transaction success/failure rates by region.  
- Revenue Forecasting → Using fitted distributions to simulate future transaction volumes.  
- Customer Segmentation → Identifying high-value vs. low-value customers.  

---

## 📊 Visualizations
The notebook includes:  
- ✅ Q-Q plots  
- ✅ PDF & CDF curves  
- ✅ Box-Cox transformation plots  
- ✅ Z-score based outlier detection  

---

## 🚀 How to Run
1. Clone this repo:  
   ```bash
   git clone <your-repo-link>
   cd SpreadLocator
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Open Jupyter Notebook:  
   ```bash
   jupyter notebook SpreadLocator.ipynb
   ```

---

## 📌 Conclusion
The Log-Normal distribution best fits the transaction amounts, while Poisson models transaction counts effectively.  
These insights can guide business decision-making, fraud monitoring, and financial planning.  

---

✨ Built with love for Data Science & Statistics!  
