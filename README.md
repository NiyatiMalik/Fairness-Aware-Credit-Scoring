# Fairness-Aware Credit Scoring
A Comparative Study and a Hybrid Model Approach
Authors: Niyati Malik, Niket Pathak
Institution: University of Illinois Chicago

## 📚 About the Project
This project explores algorithmic fairness in credit scoring systems using machine learning. It presents a comparative evaluation of 12 models (1 baseline + 11 fairness-aware models) across four real-world credit datasets. The project proposes a new composite metric—Responsibility Score (RS)—and introduces a hybrid model combining pre-processing and in-processing fairness techniques, tested on the HMDA 2018 dataset.

## 🧠 Key Features
- Evaluation of fairness-aware ML models using real-world credit datasets

- Development of a novel Responsibility Score (RS) to balance accuracy and fairness

- Implementation of pre-, in-, and post-processing fairness interventions

- A hybrid fairness pipeline using Disparate Impact Remover (DIR) and Exponentiated Gradient Reduction (EGR)

- Use of counterfactual fairness and SHAP explainability for model transparency

## 📁 Datasets Used
- German Credit (UCI ML Repository)

- Give Me Some Credit (Kaggle)

- Taiwan Credit Default (UCI ML Repository)

- Credit Card Approval (Kaggle)

- HMDA 2018 (filtered for Illinois mortgage applications)

## ⚙️ Models Implemented
**Baseline**: XGBoost (comparative) and Random Forest (HMDA)

**Pre-processing**: Learning Fair Representations (LFR), Disparate Impact Remover, Reweighing

**In-processing**: Exponentiated Gradient, Grid Search Reduction, Prejudice Remover, GerryFair Classifier, Adversarial Debiasing

**Post-processing**: Equalized Odds, Calibrated Equalized Odds, Reject Option Classification

**Hybrid**: Disparate Impact Remover + Exponentiated Gradient

## 📏 Evaluation Metrics
- Accuracy

- Statistical Parity Difference (SPD)

- Equal Opportunity Difference (EOD)

- Disparate Impact (DI)

- Responsibility Score (RS):

**RS=α×Accuracy−β×∣SPD∣−γ×∣EOD∣** (α=1,β=2,γ=2)
- Counterfactual Fairness

- SHAP Explanations

## 📌 Key Findings
- LFR and Equalized Odds ranked highest in RS across datasets.

- Pre-processing models showed the best fairness-accuracy trade-off.

- Hybrid model (Partial Repair + EGR, ε=0.05) delivered high RS with minimal accuracy loss.

- SHAP and counterfactual analysis confirmed the ethical consistency of optimized models.

## 🛠️ Installation & Setup
```bash
git clone https://github.com/<your-username>/fairness-aware-credit-scoring.git
cd fairness-aware-credit-scoring
pip install -r requirements.txt
```

## 🧪 How to Run
1. Data Preparation: Preprocess datasets (scripts provided in data/)

2. Model Training & Evaluation:

- python run_baseline.py

- python run_fair_models.py


3. Hybrid Model Pipeline:

- python hybrid_pipeline.py

4. Fairness Evaluation:

- SHAP: python interpret_shap.py
- Counterfactuals: python counterfactual_eval.py

