# Customer Churn Analysis

## Project Overview
This project analyzes customer data to predict **customer churn**—the likelihood of a customer leaving a company. By uncovering patterns in customer behavior, we can help businesses take proactive steps to retain high-value customers.

The project uses the **Telco Customer Churn dataset** from Kaggle and implements a complete machine learning pipeline: **EDA → Data Cleaning → Feature Engineering → Modeling → Evaluation → Insights**.

---

## Dataset
- **Source:** [Kaggle: Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)  
- **Description:** The dataset contains 7,043 customer records with demographic information, account details, and service usage. Key columns include `tenure`, `MonthlyCharges`, `TotalCharges`, and churn status (`Churn`).

---

## Project Workflow

### 1. Data Collection
- The notebook **downloads the dataset directly from Kaggle** using the Kaggle API.
- This makes the notebook **fully reproducible**.

### 2. Exploratory Data Analysis (EDA)
- Visualized **churn distribution**, **tenure**, and **monthly charges**.
- Correlation heatmaps to identify patterns between numeric features.

### 3. Data Cleaning & Feature Engineering
- Dropped irrelevant columns like `customerID`.
- Converted `TotalCharges` to numeric and handled missing values.
- Applied **one-hot encoding** to categorical variables.

### 4. Model Building
- **Logistic Regression** and **Random Forest Classifier** were implemented.
- Features were scaled for Logistic Regression.

### 5. Model Evaluation
- Metrics include **Accuracy, Precision, Recall, F1-score, ROC-AUC**.
- Random Forest achieved **ROC-AUC ≈ 0.85**, indicating strong predictive power.

### 6. Insights
- Shorter tenure → higher churn probability.
- High monthly charges → higher likelihood of churn.
- Services like **TechSupport** and **OnlineSecurity** help reduce churn.
- Feature importance from Random Forest helps identify key factors for targeted retention strategies.

---

## How to Run

### Option 1: Google Colab (Recommended)
1. Open this notebook in [Google Colab](https://colab.research.google.com/).
2. Upload your `kaggle.json` API token.
3. Run all cells—the notebook **automatically downloads the dataset** and executes the full pipeline.

### Option 2: Local Jupyter Notebook
1. Install dependencies from `requirements.txt`:
```bash
pip install -r requirements.txt
```
2. Place the dataset in the data/raw/ folder.
3. Run the notebook locally.

## Folder Structure
Customer_Churn_Analysis/
├── data/                  # Raw and processed datasets
├── notebooks/             # Colab/Jupyter notebooks
├── visuals/               # Graphs and charts
├── src/                   # Optional scripts for models/functions
├── README.md
└── requirements.txt

## Skills Gained

- Data Analysis & Visualization: Pandas, NumPy, Matplotlib, Seaborn

- Data Cleaning & Feature Engineering: Handling missing values, encoding, scaling

- Machine Learning: Logistic Regression, Random Forest, ROC-AUC evaluation

- Business Insight: Translating data analysis into actionable recommendations

## Optional Next Steps

- Deploy model as a simple web app (using Streamlit or Flask) to demonstrate real-time churn prediction.

- Perform hyperparameter tuning with GridSearchCV to improve model performance.

- Extend analysis to customer segmentation for personalized retention strategies.

## License

- This project is open-source and for learning purposes.


---

💡 **Pro Tips for GitHub Portfolio:**  
1. Include screenshots of key visualizations in the `visuals/` folder and reference them in README.  
2. Link your **Google Colab notebook** in the README for interactive viewing:  
   ```markdown
   [Open in Colab](https://colab.research.google.com/github/yourusername/Customer_Churn_Analysis/blob/main/notebooks/Customer_Churn_Analysis.ipynb)
   ```
