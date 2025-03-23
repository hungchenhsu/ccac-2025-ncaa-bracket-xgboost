# NCAA Basketball Bracket Prediction (Kaggle Competition) [3rd Place]

## 🏀 Project Overview

This repository contains our complete solution for the "NCAA Basketball Bracket Prediction" Kaggle competition. The primary goal was to predict outcomes of the NCAA Basketball Tournament matches accurately. Our final model ranked **3rd** on the private leaderboard.

We used **XGBoost**, a powerful gradient-boosted decision tree model, combined with comprehensive feature engineering and hyperparameter tuning to optimize predictions.

## 📌 Motivation & Technology

### Why XGBoost?
- **Efficiency:** Handles large datasets quickly.
- **Accuracy:** Provides superior predictive performance.
- **Robustness:** Handles missing values and categorical features efficiently.
- **Tuning Flexibility:** Allows detailed hyperparameter optimization for maximizing performance.

### Why Feature Engineering?
- Captures nuanced interactions between teams, regional factors, and historical performance metrics.
- Provides more predictive power to the models, boosting accuracy significantly.

## 📚 Repository Contents

Note: Final submission files and competition datasets are not included in this repository due to Kaggle’s competition data rules. Please refer to the [official dataset](https://www.kaggle.com/competitions/crossroads-classic-analytics-challenge-25/data) to download required files after accepting the competition rules.

- `bracket_training.csv`: Training dataset provided by Kaggle.
- `bracket_test.csv`: Testing dataset for generating predictions.
- `CCAC 2025 - Institutions.csv`: Additional information about institutions.
- `submission_template.csv`: Template for Kaggle submission.
- **Final Notebook** (`ccac2025_ncaa_bracket_prediction.ipynb`): Complete Python script containing:
  - Data Loading
  - Preprocessing & Cleaning
  - Feature Engineering
  - Model Training and Evaluation
  - Hyperparameter Tuning
  - Generating Kaggle Submission

## 🚀 Project Workflow

### Step 1: Data Exploration & Cleaning
- Handled missing data using median and constant imputation.
- Extracted numerical postal code information from categorical data.

### Step 2: Advanced Feature Engineering
- Created regional interaction features (`East_West_Diff`, `South_Midwest_Diff`).
- Calculated distances using the Haversine formula to capture geographic proximity.
- Merged aggregated team performance statistics from historical contests (average wins, losses, tournament seed, attendance, and win percentage).

### Step 3: Modeling
- Implemented `XGBClassifier` with tuned hyperparameters:
  - Learning rate, max depth, min_child_weight, gamma, and subsample.
- Employed cross-validation strategies to avoid overfitting.

### Step 4: Ensembling & Final Predictions
- Tested multiple hyperparameter configurations and selected the best-performing model based on validation accuracy.
- Generated final predictions for Kaggle submission, achieving our highest public (2nd Place) and private (3rd Place) leaderboard ranking.

## 📖 Table of Contents

- [🏀 Project Overview](#-project-overview)
- [📌 Motivation & Technology](#-motivation--technology)
- [📚 Repository Contents](#-repository-contents)
- [🚀 Project Workflow](#-project-workflow)
  - [Step 1: Data Exploration & Cleaning](#step-1-data-exploration--cleaning)
  - [Step 2: Advanced Feature Engineering](#step-2-advanced-feature-engineering)
  - [Step 3: Modeling](#step-3-modeling)
  - [Step 4: Ensembling & Final Predictions](#step-4-ensembling--final-predictions)
- [🏆 Kaggle Competition Results](#-kaggle-competition-results)
- [📄 License](#-license)
- [🤝 Citation](#-citation)

## 🏆 Kaggle Competition Results
- **Final Ranking:** 3rd Place (Private Leaderboard)
- **Best Public Score:** 0.63070
- **Best Private Score:** 0.63324

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Citation

If you find this repository helpful in your research, teaching, or other work,  
please consider citing or linking back to the repository:

Hung-Chen Hsu. NCAA Bracket Prediction for CCAC 2025 using XGBoost. GitHub, 2025.
Repository: https://github.com/hungchenhsu/ccac-2025-ncaa-bracket-xgboost

This helps acknowledge the original work and supports open sharing in the ML community 🙌

---

Created with 💻 and 🎯 by Hung-Chen Hsu
