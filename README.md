# 🏏 IPL Match Win Probability Predictor

A machine learning project that predicts the **real-time win probability** of IPL teams during the 2nd innings, based on live match conditions like current score, balls remaining, wickets in hand, and run rates.

---

## 🎯 How It Works

- Trained on IPL data from **2008–2019** (756 matches, 150,000+ deliveries)
- Uses **Logistic Regression** with One-Hot Encoding for teams and cities
- Predicts win/lose probability **ball-by-ball** during the 2nd innings
- Achieved **~80.3% accuracy** on test data

---

## 🗂️ Project Structure

```
IPL-Team-Win-Prediction/
│
├── data/
│   ├── matches.csv                  # Match-level data (756 matches)
│   └── deliveries.csv               # Ball-by-ball data (150,000+ rows)
│
├── IPL_Winning_Predictor.ipynb      # Full analysis, feature engineering & model training
├── requirements.txt                 # Python dependencies
└── README.md                        # Project documentation
```

---

## 🧠 Features Used

| Feature        | Description                        |
|----------------|------------------------------------|
| `batting_team` | Team currently batting             |
| `bowling_team` | Team currently fielding            |
| `city`         | Match venue city                   |
| `runs_left`    | Runs needed to win                 |
| `balls_left`   | Balls remaining in the innings     |
| `wickets`      | Wickets in hand                    |
| `crr`          | Current Run Rate                   |
| `rrr`          | Required Run Rate                  |

---

## 📦 Tech Stack

- **Language:** Python 3.8
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib
- **Model:** Logistic Regression inside a Scikit-learn Pipeline
- **Preprocessing:** OneHotEncoder + ColumnTransformer

---

## 🚀 Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/Heetgohel/IPL-Team-Win-Prediction.git
cd IPL-Team-Win-Prediction
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Launch the notebook**
```bash
jupyter notebook IPL_Winning_Predictor.ipynb
```

---

## 📈 Results

The model achieves **80.3% accuracy** on the test set. Win probability updates dynamically after each delivery and correctly responds to key in-match events like wickets falling and scoring acceleration.

---

## 🏟️ Supported Teams

- Sunrisers Hyderabad
- Mumbai Indians
- Royal Challengers Bangalore
- Kolkata Knight Riders
- Kings XI Punjab
- Chennai Super Kings
- Rajasthan Royals
- Delhi Capitals
