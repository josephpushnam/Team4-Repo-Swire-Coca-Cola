# Team4-Repo-Swire-Coca-Cola

# 🚚 Swire Coca-Cola Customer Segmentation & Delivery Optimization

This project delivers a data-driven approach to help Swire Coca-Cola identify and classify its customers into appropriate delivery service models—either high-cost Red Truck services or cost-effective White Truck services—based on historical ordering behavior. 

## 📌 Business Problem

Swire Coca-Cola's Western USA operations face high logistical costs due to indiscriminate allocation of Red Truck services. The goal is to **predict which customers should be whitelisted for White Truck service** to maximize delivery efficiency and retain valuable revenue streams.

---

## ✅ Business Goals & Results

- **Forfeited Opportunity Cost (Red Customers Not Optimized):** ~$52M–$74M/year  
- **Year 2 Cost Savings (Offboarding Low-volume Customers):** ~$7.6M  
- **Revenue Retained (High-potential Partners):** $170.6M at 20% PM  

### Suggested Thresholds

| Customer Segment       | Threshold (Annual) | Monthly Avg | Model Used              |
|------------------------|--------------------|-------------|-------------------------|
| All Customers (Gallons + Cases) | 615 Gallons + Cases   | 51.25       | XGBoost (43% accuracy) |
| LMP Fountain Only (Gallons Only) | 350 Gallons           | 21.17       | Logistic Regression (46% accuracy) |

---

## 🧠 Modeling Approach

We used both **supervised** and **unsupervised** learning techniques:

### 🔍 Supervised Models
- **XGBoost Classifier:** Best-performing model to identify high-value customers in Gallons + Cases segment
- **Logistic Regression:** Effective for LMP Fountain-only partners with gallons-only data
- **Random Forest:** Used to identify misclassified non-LMPs (60% show LMP-like traits)

### 📊 Unsupervised Clustering
- **Customer Profiles via Monthly AGI:** Clustered by order growth, channel preference, and delivery type
- **Geographic Clustering:** State-level density maps visualized growth/decline patterns

---

## 🛠️ Data Processing

- Cleaned missing values and transformed categorical columns like `ORDER_TYPE` and `PRIMARY_GROUP_NUMBER` to Boolean
- Generated yearly aggregations (Y1_, Y2_) for ordered gallons, cases, and delivery costs
- Used AGI (Average Growth Index) to assess order trends monthly and yearly

---

## 🧪 Key Insights

- Most **medium-volume gallon customers** ordered 150–250 gallons/year, median at 201 gallons
- **Year-over-year drop in average order volume**, especially in the first 7 months of Year 2
- Many non-LMP customers share characteristics with LMPs—offering conversion potential

---

## 🚀 Business Recommendations

### Cost-effective Offboarding Strategy
Introduce a **Brown Truck Program** (FedEx/UPS/USPS) for non-qualifiers:
- Saves physical expansion costs
- Improves delivery time and service levels

### Whitelist Thresholding Program
Automate onboarding/offboarding using model predictions and volume thresholds, similar to:
- Amazon FBA/FBM
- Shopee SSL
- Walmart Fulfillment Services (WFS)

---

## 🧑‍💼 Team

**Team 4 (University of Utah MSBA):**  
- Joseph Pushnam  
- Elham Mirza  
- Andy Pan  
- Chris Joyce  

---

## 📂 Repository Structure

```
📁 Swire-CocaCola-Delivery-Optimization/
│
├── 📊 Team 4 Swire Coca-Cola Presentation.pdf         # Final stakeholder summary
├── 📈 Business Problem Statement.pdf                  # Project scope and problem framing
├── 🧪 Team 4 Swire Coca Cola EDA.ipynb                # Data exploration & feature generation
├── 🤖 Team_4_Modeling_(Swire_Coca_Cola).ipynb         # Model training and evaluation
├── README.md                                         # 🔥 This file
```
