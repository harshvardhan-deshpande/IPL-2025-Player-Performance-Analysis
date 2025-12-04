# IPL-2025-Player-Performance-Analysis

Overview

This project analyzes IPL 2025 player performance using separate batting and bowling datasets.
It includes:

Data cleaning & preprocessing

Feature engineering (Retention Score)

Aggregations & summary statistics

Visualizations for batting and bowling

Insights for team composition & player evaluation

The analysis is structured in two notebooks:

Batters_Analysis.ipynb

Bowlers_Analysis.ipynb

 **Data Cleaning & Preparation
**
Conversion of numeric columns using pd.to_numeric

Handling missing values

Removing invalid entries

Creating new computed features (e.g., Retain/Not Retain)

🟦 Batters Analysis (Batters_Analysis.ipynb)
🔹 1. Top 10 Run Scorers

A bar chart visualizing the batters with the highest total runs.
Helps identify consistent, high-scoring players who anchor the innings.

🔹 2. Top 10 Strike-Rate Performers

Shows players with the highest strike rate.
Useful for identifying hard-hitters ideal for powerplay and death overs.

🔹 3. Runs vs Strike Rate (Scatter Plot)

Displays the relationship between scoring ability and attacking intent.
Annotations added for each player point.

🔹 4. Team-wise Average Runs

Using GroupBy on Team, this visualization highlights which teams have the strongest batting units based on average runs.

🔹 5. Retained Players Visualization

A bar plot of players marked as “Retain” based on custom feature engineering (below).
Shows top impactful players worth keeping in future seasons.

** Retention Feature Engineering (Batters)**

To simulate realistic IPL retention decisions, a new column Retain or Not is made based on:

Batting Average (AVG) – consistency

Strike Rate (SR) – attacking ability

Matches Played (MAT) – reliability/experience

A player is classified as "Retain" if:

AVG ≥ Overall average AVG
AND
SR ≥ Overall average SR
AND
MAT ≥ Median MAT

This adds an ML-style scoring logic to the analysis.

Bowlers Analysis (Bowlers_Analysis.ipynb)
🔹 1. Average Wickets Per Team

Shows which team’s bowling unit is strongest based on total wickets taken divided by matches played.

🔹 2. Average Economy Per Team

Highlights teams that restrict runs the best.
A lower economy rate indicates tighter bowling units.

🔹 3. Top 10 Most Economical Bowlers

Bar chart of bowlers with the lowest economy rate.
Useful for death-overs and middle-overs strategy.

🔹 4. Top 10 Most Expensive Bowlers

Shows bowlers with the highest economy rate.
Helps identify weak links in bowling attacks.

🔹 5. Wickets vs Economy (Scatter Plot)

Understanding the trade-off between wicket-taking ability and run containment.
Labeled points for readability.

🔹 6. Economy Rate Distribution (Histogram)

Shows how economy rates are distributed across the league.
Useful to compare individual bowlers to league norms.


