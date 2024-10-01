# Assignment 2: NBA Four Factor Model & Player Classification Using KMeans Clustering

## Project Overview

This project applies two advanced analytical approaches to NBA data: replicating the Four Factor Model to predict team success and using KMeans clustering to create a modern classification framework for player positions. The analysis uses data from the 2020-2021 and 2021-2022 NBA regular seasons to help teams understand the key factors driving wins and classify players into new position types that reflect the evolving nature of the game. R was used for the Four Factor Model and Python was used for the KMeans clustering.

### Replication of the Four Factor Model  
Dean Oliver's Four Factor Model emphasizes four key metrics—Effective Field Goal Percentage (EFG), Turnover Percentage (TPP), Rebounding Percentage (ORP), and Free Throw Rate (FTR)—to explain team performance and predict wins. In this analysis, regular season data from the 2021-2022 NBA season was used to replicate Oliver's model using a multiple linear regression framework.

The model achieved an R-squared value of 0.91, explaining 91% of the variance in team wins. Shooting differential was the most significant factor, explaining 65% of the variation in wins, followed by turnover and rebounding differentials. This model accurately predicted the Golden State Warriors’ 2021-2022 season with a margin of error of just 2 wins.

### Player Classification Using KMeans Clustering  
Traditional basketball positions no longer fully reflect the diverse roles of modern NBA players. Inspired by Cheng's (2017) work on redefining player positions, I developed a new classification framework using KMeans clustering. The goal was to group players based on performance metrics into new position types that better represent the modern game.

Data from the 2020-2021 and 2021-2022 seasons were used to classify 601 players across 32 metrics. After addressing multicollinearity through Linear Discriminant Analysis (LDA), KMeans clustering identified seven distinct player types:
- Scoring-Playmaker Wing
- Versatile Guard
- Inside Scoring Forward
- Versatile Wing
- Offensive Big
- Defensive Center
- Ball-Handling Scorer

These new positions reflect today’s dynamic playing styles, offering teams a modern lens to evaluate player contributions and optimize lineups. While some positions overlap with Cheng's classifications, this model provides fresh insights using more recent data. Principal Component Analysis (PCA) was also used to identify the most defining features for each position.

### Conclusion  
This analysis shows that the Four Factor Model effectively identifies the key metrics that drive team success, helping teams prioritize areas that contribute most to winning. The KMeans clustering model suggests there are more than five types of player positions in the modern NBA, providing a clearer understanding of player roles. This classification framework allows teams to optimize lineups, place players in positions that maximize their strengths, and potentially improve overall team performance.

