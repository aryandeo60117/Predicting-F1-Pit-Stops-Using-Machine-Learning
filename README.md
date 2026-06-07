🏎️ Predicting F1 Pit Stops Using Machine Learning
📌 Project Overview

Formula 1 race strategy plays a crucial role in determining race outcomes. One of the most important strategic decisions is deciding when to make a pit stop. This project uses machine learning to predict whether a driver will pit on the next lap using historical race data, tire information, performance metrics, and race conditions.

The objective is to build a classification model capable of identifying pit-stop opportunities and understanding the factors that influence race strategy.

🎯 Problem Statement

Given the current state of a race, predict whether a driver will make a pit stop on the next lap.

Target Variable:

PitNextLap
1 → Driver pits on the next lap
0 → Driver continues on track
📊 Dataset Features
Feature	Description
id	Unique identifier
Driver	Driver name
Compound	Current tire compound
Race	Grand Prix name
Year	Race season
PitStop	Number of pit stops already completed
LapNumber	Current lap number
Stint	Current stint number
TyreLife	Number of laps on current tire set
Position	Current race position
LapTime (s)	Lap time in seconds
LapTime_Delta	Change in lap time compared to previous lap
Cumulative_Degradation	Accumulated tire degradation
RaceProgress	Percentage of race completed
Position_Change	Change in race position
PitNextLap	Target variable
🔍 Feature Engineering

Several race-strategy-related features were used to improve predictive performance:

Tire Health Features
TyreLife
Compound
LapTime_Delta
Cumulative_Degradation
Strategy Features
PitStop
Stint
LapNumber
RaceProgress
Performance Features
Position
Position_Change
LapTime (s)
Context Features
Driver
Race
Year
🤖 Machine Learning Pipeline
Data Preprocessing
Missing value handling
Label Encoding of categorical variables
Feature selection
Train-test split
Model Training

Models evaluated:

Logistic Regression
Random Forest Classifier
XGBoost Classifier
Evaluation Metrics
Accuracy
Precision
Recall
F1 Score
Confusion Matrix

Since pit stops are relatively rare events, F1 Score and Recall were emphasized over accuracy.

📈 Key Insights
Tire age is one of the strongest indicators of an upcoming pit stop.
Increasing lap-time degradation significantly increases pit-stop probability.
Different tire compounds exhibit distinct degradation patterns.
Race progress and previous pit stops strongly influence strategic decisions.
Circuit-specific characteristics affect pit-stop timing.
🛠️ Technologies Used
Python
Pandas
NumPy
Scikit-learn
XGBoost
Matplotlib
Seaborn
Jupyter Notebook
🚀 Results

The trained model successfully identifies patterns in tire degradation and race strategy to predict upcoming pit stops. Feature importance analysis highlights the critical role of tire wear and performance decline in pit-stop decisions.

🔮 Future Improvements
Incorporate weather and track temperature data
Add Safety Car and Virtual Safety Car events
Include team-specific strategy patterns
Deploy a Streamlit dashboard for real-time predictions
Use telemetry and sector-level data for enhanced accuracy
📜 License

This project is developed for educational and portfolio purposes. Formula 1 data belongs to its respective owners and data providers.
