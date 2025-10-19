# 🛒 Customer Segmentation for Walmart

### 📊 Executive Summary
This project analyzes **Walmart’s customer segmentation** using clustering techniques to uncover distinct consumer groups and their spending patterns. Through **data preprocessing, dimensionality reduction (PCA), and model evaluation**, we identified six unique customer segments that can help Walmart **enhance marketing personalization, optimize inventory management, and strengthen customer loyalty**.

---

### 💼 Business Problem
Walmart operates in a highly competitive retail environment. To stay ahead, understanding customer behavior and tailoring strategies accordingly is critical.  

**Goal:**  
Identify key customer segments based on spending and demographic variables to answer:  
> “How do spending-based customer segments differ in their demographic and socioeconomic characteristics, and what actionable trends emerge within each group?”

These insights enable Walmart to:
- Personalize marketing campaigns  
- Target high-value customer groups  
- Improve inventory allocation efficiency  

---

### 🧩 Methodology

1. **Data Preprocessing & Cleaning**
   - Source: https://www.kaggle.com/code/gopalkrushnasahu/walmart-sales-prediction-by-customer-segmentation/input
   - 2000 records × 8 features (CustomerID, Gender, Age, Annual Income, Spending Score, Profession, Work Experience, Family Size)  
   - Replaced missing values (`Profession` = ‘Unknown’), removed invalid ages, and encoded categorical variables.

2. **Exploratory Data Analysis (EDA)**
   - **Age & Income Distribution:** Majority aged 20–80; income skewed below \$150k.  
   - **Spending Score:** Uniform distribution (1–100), showing diverse purchasing behavior.  
   - **Correlation Heatmap:** Weak correlation between income and spending; positive correlation between age and work experience.

3. **Modeling & Clustering**
   - Implemented three clustering algorithms:
     - **K-Means**
     - **Gaussian Mixture Model (GMM)**
     - **DBSCAN**
   - Initial results were weak (Silhouette ≈ 0.12–0.15).  
   - Applied **PCA (Principal Component Analysis)** for dimensionality reduction → improved cluster separability.  
   - Post-PCA Silhouette Scores:  
     - K-Means: `0.3388`  
     - GMM: `0.3347`  
     - DBSCAN: `0.4404` (no meaningful structure)  
   - Selected **K-Means (K=6)** for best interpretability and stability.

4. **Model Evaluation**
   - Metrics used: Silhouette Score, Calinski-Harabasz Index, Davies-Bouldin Index.  
   - Robustness tested with **Bootstrapping** and **Noise Perturbation**.  
   - K-Means outperformed GMM across consistency and separability metrics.

---

### 🧠 Skills Highlighted
- **Python Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn  
- **Data Science Techniques:** EDA, feature encoding, PCA, clustering (K-Means, GMM, DBSCAN)  
- **Statistical Validation:** Silhouette analysis, Calinski-Harabasz, Davies-Bouldin  
- **Business Analytics:** Customer segmentation, behavioral insights, data-driven marketing strategy  
- **Visualization:** Cluster distributions, density plots, PCA projections  

---

### 📈 Results & Business Insights

Six distinct customer clusters emerged:

| Cluster | Description | Spending Score | Demographic Traits |
|----------|--------------|----------------|--------------------|
| 0 | Moderate spenders with mixed demographics | ~52 | Young professionals / students |
| 1 | High-income large families, cautious spenders | ~40 | Stable, career-oriented, family-centric |
| 2 | Older, mid–high income, conservative spenders | ~22 | Middle-class, risk-averse |
| 3 | Young, high-spenders with moderate income | ~75 | Trend-driven consumers |
| 4 | Small families or low-income individuals | ~36 | Early-career professionals |
| 5 | Young earners, strong spending habits | ~77 | High engagement potential |

**Key Takeaways:**
- Younger consumers (Clusters 3 & 5) exhibit the **highest spending activity**.  
- Middle-class customers (Cluster 2) show conservative purchase behavior.  
- Families with higher income but low spend (Cluster 1) represent an opportunity for **cross-sell and upsell** initiatives.

---

### 🚀 Business Recommendations
1. **Targeted Marketing:**  
   - Design age-specific and lifestyle-driven campaigns for Clusters 3 & 5.  
   - Encourage repeat purchases and brand loyalty through rewards.

2. **Inventory Strategy:**  
   - Stock fast-moving products favored by younger clusters in high-traffic stores.  
   - Use conservative cluster insights for price-sensitive product placement.

3. **Loyalty & Retention:**  
   - Track **visit frequency, ticket size**, and **category spending**.  
   - Integrate **online vs. in-store** behavior data for omnichannel insights.

4. **Future Data Enhancement:**  
   - Add behavioral metrics like churn, purchase recurrence, and promotion response.  
   - Include demographic enrichments (education, marital status, housing).

---

### 🔮 Next Steps
- Integrate **transaction-level and loyalty data** for predictive segmentation.  
- Apply **classification models** to predict customer movement between segments.  
- Visualize clusters using **Power BI / Tableau dashboards** for stakeholder insights.  
