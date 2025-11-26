**PROJECT NAME: Fraud Detection using Machine Learning (Supervised + Unsupervised)**
**Dataset Access:** The dataset used in this project is large, so it has been uploaded separately.
**Download Dataset**:https://drive.google.com/drive/my-drive
**Colab Link:** https://colab.research.google.com/drive/1OLr9thdJRgONyhsQWa1Qs0WktvD4RmT8#scrollTo=uKXeq1Iw4Ecd
<img width="578" height="455" alt="image" src="https://github.com/user-attachments/assets/62efb9f1-6d10-46ff-b553-50bcd45fe99c" />
<img width="941" height="551" alt="image" src="https://github.com/user-attachments/assets/585e3068-3e1a-4b11-88b4-76840813dd26" />
<img width="589" height="455" alt="image" src="https://github.com/user-attachments/assets/dc7a3374-7007-4052-823e-6627285bc02b" />
**Model Development Pipeline**
Exploratory Data Analysis
Imbalanced Class Handling (fraud cases < 0.2%)
Model Training (RandomForest + XGBoost)
Threshold Optimization
Business Cost Evaluation
Deployment (Flask API)

| Category      | Tools                           |
| ------------- | ------------------------------- |
| Languages     | Python                          |
| ML Libraries  | Scikit-Learn, XGBoost, LightGBM |
| Deployment    | Flask API                       |
| Visualization | Matplotlib, Seaborn             |
| Dashboard     | Power BI                        |
| Environment   | Google Colab                    |

**MODEL PERFORMANCE:**
| Metric                  | Score    |
| ----------------------- | -------- |
| Accuracy                | **0.99** |
| ROC-AUC                 | **0.97** |
| Recall (Fraud Class)    | **0.84** |
| Precision (Fraud Class) | **0.17** |
| F1 Score (Fraud Class)  | **0.28** |


**FINAL RESULT: Threshold vs Business Cost Optimization**
| Threshold | FP Rate | FN | Recall | Business Cost |
|----------|---------|----|--------|---------------|
| 48       | 0.49    | 12 | 0.84   | ₹216,600      |
| 47       | 0.48    | 12 | 0.84   | ₹220,500      |
| 46       | 0.47    | 12 | 0.84   | ₹223,500      |
| 45       | 0.46    | 12 | 0.84   | ₹228,600      |
| 44       | 0.45    | 12 | 0.84   | ₹231,900      |
| 43       | 0.44    | 12 | 0.84   | ₹236,100      |
| 42       | 0.43    | 12 | 0.84   | ₹240,900      |
| 41       | 0.42    | 12 | 0.84   | ₹245,400      |
| 40       | 0.41    | 12 | 0.84   | ₹250,200      |
| 39       | 0.40    | 12 | 0.84   | ₹255,000      |

**Model Performance Summary**
| Metric | Score |
|--------|-------|
| Accuracy | 0.99 |
| ROC-AUC | 0.97 |
| Recall (Fraud Class) | 0.84 |
| Precision (Fraud Class) | 0.17 |
| F1 Score (Fraud Class) | 0.28 |
The model prioritizes high Recall to reduce missed fraud cases (FN), which is important for AML use cases.

**Fraud Detection System Architecture**
                    ┌────────────────────────────┐
                    │        Raw Data            │
                    │ Transactions, Customers,   │
                    │ Merchants Dataset (CSV)    │
                    └───────────────┬────────────┘
                                    │
                                    ▼
                     ┌──────────────────────────────┐
                     │  Data Ingestion & Cleaning   │
                     │ (Pandas / PySpark / Colab)   │
                     └───────────────┬──────────────┘
                                     │
                                     ▼
                   ┌──────────────────────────────────┐
                   │     Feature Engineering           │
                   │ - Encoding                        │
                   │ - Scaling                         │
                   │ - Risk Profiling                  │
                   │ - Velocity Features               │
                   │ - Anomaly Scores                  │
                   └───────────────┬──────────────────┘
                                   │
              ┌────────────────────┴─────────────────────┐
              │                                          │
              ▼                                          ▼
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │   Unsupervised ML Models     │          │    Supervised ML Models      │
 │  - Isolation Forest          │          │  - Random Forest             │
 │  - Autoencoder Neural Net    │          │  - XGBoost                   │
 │                              │          │                              │
 │ Output → anomaly_prob        │          │ Output → fraud_probability   │
 └──────────────────────────────┘          └──────────────────────────────┘
              │                                          │
              └─────────────────────┬────────────────────┘
                                    │
                                    ▼
                     ┌──────────────────────────────────┐
                     │ Threshold Optimization            │
                     │ - Precision/Recall Tradeoff       │
                     │ - Business Cost Function          │
                     │ - ROC / PR Curve Analysis         │
                     └─────────────────┬─────────────────┘
                                       │
                                       ▼
                      ┌─────────────────────────────────┐
                      │ Model Deployment (Flask API)     │
                      │ Endpoint: /predict               │
                      │ Output: Fraud / Not Fraud        │
                      └─────────────────┬────────────────┘
                                        │
                                        ▼
                     ┌────────────────────────────────────┐
                     │ Power BI Monitoring Dashboard      │
                     │ - Fraud Alerts                     │
                     │ - Model KPIs                       │
                     │ - Cost Savings Metrics             │
                     │ - Drift Tracking                   │
                     └────────────────────────────────────┘


**Conclusion**
By optimizing the threshold, the model significantly reduces false negatives (missed fraud), ensuring early detection of suspicious activity.  
The optimal threshold (~0.48) balances the trade-off between **business cost** and detection accuracy.

