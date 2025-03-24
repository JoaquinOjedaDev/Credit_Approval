# Credit Risk Approval Prediction using Machine Learning

## 🔑 Key Findings
- **High Model Performance**: Gradient Boosting achieved **AUC-ROC (0.96)**, **88% precision**, and **86% recall**, demonstrating robust risk prediction capabilities.
- **Critical Features**: Income, employment history, and credit behavior were strongly correlated with risk outcomes.
- **Imbalance Handling**: SMOTE effectively addressed class imbalance, improving model reliability.
- **Actionable Insights**: The model enables data-driven credit decisions, reducing reliance on subjective assessments.

---

## 📌 Business Problem
Financial institutions face challenges in accurately assessing credit risk. Subjective evaluations can lead to defaults or missed opportunities. This project develops a **machine learning model to predict credit risk** based on applicant profiles, enabling:
- Automated, objective credit approval decisions
- Reduced default rates through high-risk applicant identification
- Streamlined processes for low-risk applicants

---

## 📊 Data Source
- **Dataset**: [Credit Card Approval Prediction](https://www.kaggle.com/datasets/rikdifos/credit-card-approval-prediction/data)
- **Features**:
  - *Demographic*: Gender, age, education, family status
  - *Financial*: Income, property/vehicle ownership, employment history
  - *Credit Behavior*: Months balance, past credit status
- **Size**: 438,557 application records

---

## 🛠 Methods
### **Data Preparation**
- Merged application and credit history datasets
- Engineered features: `age_account` (account age), risk flag conversion
- Handled missing data and outliers

### **Model Development**
- **Class Balancing**: SMOTE for imbalanced classes (high-risk vs low-risk)
- **Feature Scaling**: MinMaxScaler for numerical features
- **Model Selection**: Compared  Gradient Boosting, Logistic Regression, Random Forest and others

### **Evaluation Metrics**
- AUC-ROC, Precision-Recall, F1-Score
- Classification reports and confusion matrices

---

## 💻 Tech Stack
| Category       | Tools/Libraries                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------|
| **Core**       | Python 3.9, Jupyter Notebook                                                                        |
| **Data**       | Pandas, NumPy, Scikit-Learn, Imbalanced-Learn (SMOTE)                                               |
| **Modeling**   | XGBoost, Sklearn, Gradient Boosting, Logistic Regression, Random Forest, etc                        |
| **Viz**        | Matplotlib, Seaborn, Power BI                                                                       |
| **Pipeline**   | Scikit-Learn Pipelines, OneHotEncoder, OrdinalEncoder                                               |

---

## 📈 Results
### **Gradient Boosting Performance**
| Metric         | Class 0 (Low Risk) | Class 1 (High Risk) | Overall    |
|----------------|--------------------|---------------------|------------|
| **Precision**  | 0.87               | 0.90                | 0.88       |
| **Recall**     | 0.90               | 0.86                | 0.88       |
| **F1-Score**   | 0.89               | 0.88                | 0.88       |
| **AUC-ROC**    | -                  | -                   | **0.96**   |

### **Confusion Matrix**
|                | Predicted Low Risk | Predicted High Risk |
|----------------|--------------------|---------------------|
| **Actual Low** | 7,734              | 859                 |
| **Actual High**| 1,205              | 7,402               |

---

## 📚 Lessons Learned
- **Feature Engineering Matters**: Derived features like `age_account` significantly improved predictive power.
- **Imbalance Handling**: SMOTE increased recall for high-risk cases compared to class weighting.


---

## ⚠️ Future Improvements
- Adjusting decision thresholds to balance precision and recall for business needs.
- Incorporate real-time transaction data
- Deploy as API for real-time scoring
- Add NLP analysis of application text fields

---

## 🗂 Repository Structure
```bash
📦 Credit-Risk-Prediction
├── 📂 dashboard 
│   ├── Dashboard Credit Risk.pbix       # Interactive Power BI Dashboard with Machine Learning Predictions
│   └── dashboard1.png                   # Snapshot 1
│   └── dashboard2.png                   # Snapshot 2
│
├── 📂 datasets
│   ├── application_record.csv           # Applicant profiles
│   ├── credit_record.csv                # Credit history data
│   ├── test.csv                         # Applicant profiles
│   └── train.csv                        # Credit history data
│
│
├── 📂 metrics
│   ├── confusion_matrix.png        
│   ├── feature_importance.png      
│   ├── heatmap.png                 
│   ├── metrics.png                 
│   └── roc_curve.png               
│
├── 📂 predictions                  
│   ├── credit_score_predictions3.xlsx   # Excel file with the predictions of the Machine Learning Model 
│   └── pythonfinal.ipynb                # Full analysis pipeline
│
├── requirements.txt                     # Dependency list
└── README.md                            # Project documentation
