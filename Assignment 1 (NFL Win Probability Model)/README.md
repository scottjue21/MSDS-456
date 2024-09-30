# Assignment 1: NFL Win Probability Model

## Project Overview
This project involves the development of a win probability model for NFL games using play-by-play data from the 2021 and 2022 seasons, obtained through the nflfastR library in R. The objective was to create a model that predicts a team's win probability at any point during a game based on several factors such as the game quarter, down, yards to go, time remaining, score differential, and field position. The project also includes a visualization of win probability for a specific game—the 2023 NFC Championship game between the San Francisco 49ers and the Philadelphia Eagles—illustrating the model's accuracy in predicting the outcome.

## Model Creation
- **Data Source**: NFL play-by-play data for the 2021 and 2022 seasons from the nflfastR library.
- **Exclusions**: 2020 season (due to COVID-19), kickoffs, extra points, penalties, overtime plays, and Super Bowl.
- **Data Cleaning**: Removed plays with missing values in possession and downs to ensure the model focuses on standard gameplay.
- **Training and Test Split**: 80/20 train-test split, with 77,450 plays used for analysis.
- **Modeling Approach**: Generalized Linear Model (GLM) using variables like quarter, down, yards to go, time remaining, yards to end zone, and score differential.
- **Evaluation**: Root Mean Squared Error (RMSE) was used to assess model performance, with a final RMSE of 0.066 on test data. The model was also validated by comparing predicted and actual win probabilities using methods similar to Lopez (2017).

## Model Performance
The win probability model performed well across quarters 1 through 3 but exhibited some inaccuracies in the 4th quarter, particularly underpredicting win probabilities for teams with high win percentages and overpredicting low percentages. Despite these discrepancies, the model's performance was impressive and did not require further adjustments.

## Game Visualization: 2023 NFC Championship Game
The model's accuracy was visualized using the NFC Championship game between the San Francisco 49ers and the Philadelphia Eagles. This game was held out from the training data to evaluate how well the model predicted win probabilities.

### Key Insights:
- The model closely tracked nflfastR’s win probability for both teams, though some discrepancies were observed early and late in the game.
- Notable win probability changes occurred during pivotal moments, such as the Eagles’ 4th down conversion and 49ers' turnovers.
- The model captured the influence of early-game events and demonstrated the substantial impact of turnovers and 4th down conversions on a team’s win probability.

## Conclusion
This win probability model produces reasonably accurate results when predicting game outcomes based on score, time remaining, and field position. However, it has several limitations, including its inability to predict win probability for plays involving penalties, kickoffs, extra points, or 2-point conversions. Additionally, Super Bowl and overtime plays were excluded from the model due to their unique nature, and the model does not account for injuries, on-field personnel, or play strategies, all of which can significantly impact game outcomes. Despite these limitations, the model offers insights into the impact of turnovers, 4th down conversions, and early leads on win probabilities. Its performance closely aligns with other public models, such as nflfastR, except in some cases during the fourth quarter.
