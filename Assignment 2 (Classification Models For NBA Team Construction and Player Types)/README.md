# NBA Four Factor Model & Player Classification Using KMeans Clustering

## Project Overview

This project applies two advanced analytical approaches to NBA data: replicating the Four Factor Model to predict team success and using KMeans clustering to create a modern classification framework for player positions. The analysis uses data from the 2020-2021 and 2021-2022 NBA regular seasons to help teams understand the key factors driving wins and classify players into new position types that reflect the evolving nature of the game.

### Replication of the Four Factor Model  
Dean Oliver's Four Factor Model emphasizes four key metrics—Effective Field Goal Percentage (EFG), Turnover Percentage (TPP), Rebounding Percentage (ORP), and Free Throw Rate (FTR)—to explain team performance and predict wins. In this analysis, I used regular season data from the 2021-2022 NBA season to replicate Oliver's model using a multiple linear regression framework.

The model achieved an R-squared value of 0.91, explaining 91% of the variance in team wins. Shooting differential emerged as the most significant factor, explaining 65% of the variation in wins, followed by turnover and rebounding differentials, while free throw differential had a smaller impact. For example, a 0.01 increase in shooting differential could result in an additional 3.6 wins, while reducing turnovers by the same amount could add 4.1 wins. This model accurately predicted the Golden State Warriors’ 2021-2022 season with a margin of error of just 2 wins.

### Player Classification Using KMeans Clustering  
Traditional basketball positions no longer fully reflect the diverse roles of modern NBA players. Inspired by Cheng's (2017) work on redefining player positions using KMeans clustering, I developed a new classification framework to group players based on their performance metrics. The goal was to create new position types that better represent how the game is played today.

I used two datasets—Per 100 Possessions and Shooting Data—from basketball-reference.com for the 2020-2021 and 2021-2022 seasons. After merging the datasets and removing unnecessary variables, I filtered the data to include only players who played at least 40 games in the 2021-2022 season (36 games for 2020-2021 due to the COVID-19 shortened season). This resulted in 601 player observations across 32 explanatory variables.

To address multicollinearity among the variables, I applied Linear Discriminant Analysis (LDA) for dimensionality reduction. LDA reduced the dataset to two dimensions while capturing 62% of the variance, allowing for better interpretability. KMeans clustering was then applied to these two dimensions, and using silhouette scores, I determined that 7 clusters would best represent distinct player types.

The seven new position types are:
- **Scoring-Playmaker Wing**
- **Versatile Guard**
- **Inside Scoring Forward**
- **Versatile Wing**
- **Offensive Big**
- **Defensive Center**
- **Ball-Handling Scorer**

These positions differ slightly from the positions determined by Cheng (2017). Classification models are somewhat subjective, as inputs such as the number of clusters are determined at the modeler’s discretion. The process of labeling clusters is also subjective. Additionally, Cheng used data from multiple years and included advanced stats for each player, which could explain the differences between our clusters. However, there are notable similarities between the positions. For example, the **Defensive Center** and **Offensive Big** positions in my model correspond to Cheng’s **Defensive Centers** and **Offensive Centers**, respectively. Similarly, **Scoring-Playmaker Wing** is equivalent to **Scoring Wings**, **Versatile Guard** aligns with **Combo Guard**, and **Ball-Handling Scorer** parallels **Floor Generals**.

After identifying these clusters, I used Principal Component Analysis (PCA) to extract the most important features that defined each cluster, making it easier to interpret the characteristics of each new position. Players were then classified into these seven new positions, and scatter plots were created to visualize the groupings.

This classification framework offers a modern lens for analyzing player roles in the NBA, providing teams with deeper insights into optimizing lineups and evaluating player contributions.

### Conclusion  
This analysis provides actionable insights for both predicting team success and optimizing player lineups. By replicating Dean Oliver's Four Factor Model, I demonstrated that certain factors—such as shooting differential, turnover differential, and rebounding differential—are critical in determining the number of games won by a team. The model revealed that shooting differential is the most important factor, highlighting the need for teams to prioritize offensive and defensive efficiency in this area. Teams can use these insights to focus on improving key areas that contribute to winning more games.

The KMeans clustering analysis introduced a modern classification of NBA player positions, identifying seven distinct player types that more accurately reflect the diverse roles in today’s game. The classification model demonstrated that traditional positions like "center" or "guard" no longer fully capture player roles, with new types such as "Ball-Handling Scorer" and "Versatile Wing" offering a more nuanced understanding of player performance. By analyzing the best 5-man lineups, such as the Golden State Warriors’ 2021-2022 postseason lineup, teams can assess how different combinations of these position types impact team performance. For example, the Warriors’ most successful lineup during the postseason featured two Ball-Handling Scorers, though this may have been due to the unique style of play the team employs.

The analysis can also serve as a valuable tool for teams looking to optimize roster construction. Teams can use the new classification model to understand the types of players they have and identify gaps in their lineup. This knowledge can guide roster changes, such as acquiring players that fit an optimal position type or finding suitable replacements for departing players. Additionally, different teams have different playing styles, so lineup combinations that work for one team may not work for another. This means that any recommendations for lineup construction should be tailored to the specific strategies and needs of each team.

However, several limitations should be noted. The data collection process was manual and limited to two seasons, which may have affected the robustness of the model. Additionally, the subjectivity involved in defining clusters and determining player positions means that some classifications may not fully capture a player’s role. For example, Draymond Green was classified as a Ball-Handling Scorer, a designation that many experts might challenge. There is also the issue of players being classified differently across seasons, as seen with LeBron James, which could introduce inconsistencies. Lastly, matchups against opposing lineups were not considered in the evaluation of the best 5-man lineup, which could impact the generalizability of these findings.

Despite these limitations, this project demonstrates the potential of data-driven approaches in improving roster decisions and team performance. The Four Factor Model helps teams focus on key performance metrics, while the KMeans clustering model provides a better understanding of player roles in the modern NBA. By applying these models, teams can make more informed decisions to optimize their lineups and increase their chances of success.

Python was used for all data cleaning, modeling, and analysis.
