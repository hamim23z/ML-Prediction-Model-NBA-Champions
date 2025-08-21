# NBA Champions Prediction - First Part (Basic)

The reason why this is called the first part (basic) is because this dataset, the .csv file, only has information about finals matchups, score, the finals winner, and conference runner ups. The NBA season is extremely unpredictable, I have to account for injuries, trades, player ratings, history, games, storylines, etc. That will all be covered in part two using a much larger dataset that I found on Kaggle. (https://www.kaggle.com/datasets/eoinamoore/historical-nba-data-and-player-box-scores/) will be used next. 

This project uses historical NBA Finals data to **predict future champions** from 2026 to 2050, using Python and machine learning. It emphasizes modern teams over the old ones and there is a recency bias to produce more realistic outcomes (When I ran it the first time, the Syracuse Nationals and Washington Bullets were up there lol)

---

## 🚀 Project Overview

The goal of this project is to simulate and predict future NBA champions based on historical performance, with a focus on:
- Post-1990 data to focus on relevant modern teams.
- Recency bias champs, giving more importance to recent champs.
- Got rid of old teams because they either don't exist or have been renamed. For example, the St. Louis Hawks, Minneapolis Lakers, Seattle Supersonics, etc.
- Producing probabilistic predictions, rather than deterministic results.

---

## 📂 Dataset

The CSV contains historical NBA Finals data, with columns including:

| Column | Description |
|--------|-------------|
| `year` | NBA season (e.g., "2023/24") |
| `winner` | Finals champion |
| `runnerup` | Finals runner-up |
| `easternConfRunnerUp` | Eastern Conference runner-up |
| `westernConfRunnerUp` | Western Conference runner-up |
| `finalscore` | Series result |

---

## 🛠 Tech Stack
- **Python 3.9+**
- **Jupyter Notebook**
- **Kaggle**
- **Pandas**
- **NumPy**
- **scikit-learn -> Random Forest classifier**

---

## ⚙️ How It Works
1. **Load and clean data**: Fix year format and remove outdated teams.
2. **Feature engineering**: Compute past champs, finals appearances, and conference finals appearances.
3. **Recency bias**: Recent championships are weighted more heavily.
4. **Model training**: Random Forest classifier predicts the likelihood of a team winning based on the features.
5. **Future simulation**: Predict champions from 2026–2050 using probabilistic sampling from the model.

---

## 🏆 Sample Predictions
```
FIRST RUN: 
🏆 Predicted NBA Champions from 2026-2050:
2026 -> San Antonio Spurs
2027 -> Los Angeles Clippers
2028 -> San Antonio Spurs
2029 -> Dallas Mavericks
2030 -> Dallas Mavericks
2031 -> San Antonio Spurs
2032 -> Phoenix Suns
2033 -> Detroit Pistons
2034 -> Utah Jazz
2035 -> Detroit Pistons
2036 -> Memphis Grizzlies
2037 -> San Antonio Spurs
2038 -> Dallas Mavericks
2039 -> Los Angeles Lakers
2040 -> Boston Celtics
2041 -> Indiana Pacers
2042 -> Cleveland Cavaliers
2043 -> Los Angeles Lakers
2044 -> San Antonio Spurs
2045 -> Boston Celtics
2046 -> New York Knicks
2047 -> Toronto Raptors
2048 -> Dallas Mavericks
2049 -> Miami Heat
2050 -> Golden State Warriors
```

<br>
<br>

```
SECOND RUN: 
🏆 Predicted NBA Champions from 2026-2050:
2026 -> Boston Celtics
2027 -> Chicago Bulls
2028 -> Boston Celtics
2029 -> Cleveland Cavaliers
2030 -> Phoenix Suns
2031 -> Dallas Mavericks
2032 -> Utah Jazz
2033 -> Phoenix Suns
2034 -> Golden State Warriors
2035 -> San Antonio Spurs
2036 -> Cleveland Cavaliers
2037 -> Golden State Warriors
2038 -> Houston Rockets
2039 -> Memphis Grizzlies
2040 -> Toronto Raptors
2041 -> Chicago Bulls
2042 -> Dallas Mavericks
2043 -> Utah Jazz
2044 -> Boston Celtics
2045 -> Detroit Pistons
2046 -> Boston Celtics
2047 -> Chicago Bulls
2048 -> Houston Rockets
2049 -> Phoenix Suns
2050 -> Utah Jazz
```

<br>
<br>

```
THIRD RUN: 
🏆 Predicted NBA Champions from 2026-2050:
2026 -> Denver Nuggets
2027 -> Houston Rockets
2028 -> Houston Rockets
2029 -> Dallas Mavericks
2030 -> Dallas Mavericks
2031 -> Detroit Pistons
2032 -> Orlando Magic
2033 -> Toronto Raptors
2034 -> Oklahoma City Thunder
2035 -> Denver Nuggets
2036 -> Los Angeles Lakers
2037 -> Los Angeles Clippers
2038 -> San Antonio Spurs
2039 -> Golden State Warriors
2040 -> Denver Nuggets
2041 -> Detroit Pistons
2042 -> Orlando Magic
2043 -> Cleveland Cavaliers
2044 -> Denver Nuggets
2045 -> Toronto Raptors
2046 -> Oklahoma City Thunder
2047 -> New York Knicks
2048 -> Denver Nuggets
2049 -> Indiana Pacers
2050 -> Detroit Pistons
```
