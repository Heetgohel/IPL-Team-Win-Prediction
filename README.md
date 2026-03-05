# 🏏 IPL Match Win Probability Predictor

A machine learning project that predicts the **real-time win probability** of IPL teams 
during the 2nd innings, based on match situation like current score, balls left, 
wickets in hand, and required run rate.

## 📊 Demo
![Win Probability Chart](assets/sample_chart.png)  <!-- add a screenshot -->

## 🎯 How It Works
- Trained on IPL data from **2008–2019** (756 matches, 150,000+ deliveries)
- Uses **Logistic Regression** with One-Hot Encoding for teams and cities
- Predicts win/lose probability ball-by-ball during the 2nd innings
- Achieved **~80.3% accuracy** on test data

## 🗂️ Project Structure
ipl-win-predictor/
├── data/
│   ├── matches.csv        # Match-level data (756 matches)
│   └── deliveries.csv     # Ball-by-ball data (150k+ rows)
├── IPL_Winning_Predictor.ipynb  # Full analysis + model training
├── pipe.pkl               # Trained model pipeline (optional)
├── requirements.txt
└── README.md

## 🧠 Features Used
| Feature | Description |
|---|---|
| batting_team | Team currently batting |
| bowling_team | Fielding team |
| city | Match venue city |
| runs_left | Runs needed to win |
| balls_left | Balls remaining |
| wickets | Wickets in hand |
| crr | Current run rate |
| rrr | Required run rate |

## 🚀 Run Locally
git clone https://github.com/Heetgohel/IPL-Team-Win-Prediction
cd IPL-Team-Win-Prediction
pip install -r requirements.txt
jupyter notebook IPL_Winning_Predictor.ipynb

## 📦 Tech Stack
- Python 3.8
- Pandas, NumPy
- Scikit-learn (Logistic Regression, Pipeline, ColumnTransformer)
- Matplotlib

## 📈 Results
The model achieves **80.3% accuracy**. Win probability updates after each over 
and responds correctly to wickets falling and scoring acceleration.

---
