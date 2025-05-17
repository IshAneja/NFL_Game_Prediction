# 🏈 NFL Game Outcome Prediction

This project uses machine learning models to predict the outcome of NFL games — win or loss — based on historical game statistics. Various classification models such as Support Vector Machines (SVM), Logistic Regression, Stochastic Gradient Descent (SGD), Random Forest, and XGBoost were evaluated. 

---

## 📌 Project Goals

- Predict whether the home team wins an NFL game.
- Compare performance of different classification models.
- Build a reproducible and interpretable ML pipeline.
- Compare models using different evaluation techniques F1 Score, Recall, Accuracy, Precision and ROC curve

---

## 📁 Repository Structure

```bash
nfl-game-prediction/
├── nfl_game_prediction.ipynb        # Main notebook with EDA, modeling, evaluation
├── nfl_game_prediction.html         # html export for quick viewing
├── requirements.txt                 # Dependencies list
├── README.md                        # This file
├── images/                          
│   └── model_comparison.png         # Accuracy/F1 score plots

📊 Dataset
Source: nflfastR [dataset](https://github.com/nflverse/nflverse-pbp)

### Features used include:

- total_home_epa
- home_pass_epa, home_rush_epa
- series_success, touchdowns, interceptions, qb_hits, etc.
- Target variable: home_win (binary: 1 if home team won)

⚙️ Models Evaluated

| Model          | Accuracy  | F1 Score  | Precision | Recall    |
| -------------- | --------- | --------- | --------- | --------- |
| Random Forest  | 0.679     | 0.696     | 0.694     | 0.699     |
| XGBoost        | 0.659     | 0.677     | 0.674     | 0.681     |
| GridSearch SVM | **0.687** | **0.715** | 0.685     | **0.748** |

✅ The GridSearch-optimized SVM model performed best in terms of F1 score and recall.

🔍 Key Insights
- EPA (Expected Points Added) metrics were strong predictors of wins.

- Interceptions and successful series had a significant impact on model decisions.

- Random Forest and Gradient Boosting showed competitive performance but slightly underperformed   compared to tuned SVM.

🚀 Getting Started

1. Clone the repository:
```sh 
git clone https://github.com/yourusername/nfl-game-prediction.git
cd nfl-game-prediction
```

2. Install dependencies:
```sh
pip install -r requirements.txt
```
3. Run the notebook:

Open nfl_game_prediction.ipynb in Jupyter or VS Code.

📌 To-Do
- Add more seasons or player-level stats for better generalization
- Deploy a Streamlit web app to allow live predictions
- Try ensemble stacking or deep learning models

👤 Author
Ish Aneja
📫 Ish.Aneja@outlook.com
🔗 LinkedIn
📘 Portfolio

📄 License
This project is open-source under the MIT License.