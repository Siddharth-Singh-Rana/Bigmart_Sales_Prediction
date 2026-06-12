# BigMart Sales Prediction using Machine Learning 🛒📈

An End-to-End Machine Learning Regression project designed to predict product sales across various BigMart outlets. By analyzing product attributes (MRP, visibility, weight) and store characteristics (size, location type, establishment year), the model forecasts the `Item_Outlet_Sales`, helping the retail company optimize inventory and strategy.

## 🎯 Objective & Business Problem
BigMart aims to understand the key properties of products and stores that play a significant role in increasing sales. The core objective is to build a predictive regression model to estimate sales, allowing stakeholders to identify underperforming products and plan supply chain management efficiently.

## 🛠️ Tech Stack & Libraries Used
- **Language:** Python
- **Data Preprocessing & EDA:** Pandas, NumPy
- **Data Visualization:** Seaborn, Matplotlib
- **Machine Learning Workflow:** Scikit-Learn
- **Algorithm Used:** Linear Regression (with Log Transformation)

## 📊 Dataset Features Description
The dataset contains corporate retail tracking details split into training and testing sets with the following key attributes:
- `Item_Identifier`: Unique product ID.
- `Item_Weight`: Weight of the product.
- `Item_Fat_Content`: Low Fat / Regular.
- `Item_Visibility`: The percentage of total display area allocated to the product in a store.
- `Item_Type`: Category of the product (Dairy, Snacks, Soft Drinks, etc.).
- `Item_MRP`: Maximum Retail Price of the product.
- `Outlet_Identifier`: Unique store ID.
- `Outlet_Establishment_Year`: The year the store was established.
- `Outlet_Size`: The size of the store (Small, Medium, High).
- `Outlet_Location_Type`: The type of city/location (Tier 1, Tier 2, Tier 3).
- `Outlet_Type`: Grocery Store or Supermarket Type (1, 2, 3).
- `Item_Outlet_Sales`: Target Variable (Sales revenue for the product in that particular store - available in Train data).

## 📈 Machine Learning Workflow & Key Steps
- **Data Cleaning:** Handled missing values systematically in categorical (`Outlet_Size`) and continuous (`Item_Weight`) columns.
- **Feature Engineering:** Corrected inconsistent labels in `Item_Fat_Content` (mapping 'reg', 'Regular', and 'low fat', 'Low Fat' properly) and implemented structured encoding for categorical levels.
- **Log Transformation:** Applied `np.log1p` on the skewed target variable during training to optimize the linear predictor, and later reverted predictions using `np.expm1`.
- **Model Training:** Built a baseline **Linear Regression** framework evaluating multi-variable feature inputs.

## 📂 Project Directory Structure
- `Train.csv` - Historical dataset containing target sales metrics used for model optimization.
- `Test.csv` - Evaluation dataset used for generating independent final predictions.
- `bigmart_project.ipynb` - Complete Jupyter Notebook documenting EDA, feature parsing, logging transformations, and predictive operations.
- `README.md` - Technical portfolio documentation.

## 💻 How to Run This Project Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/bigmart-sales-prediction.git](https://github.com/YOUR_USERNAME/bigmart-sales-prediction.git)
