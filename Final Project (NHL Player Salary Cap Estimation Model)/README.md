# NHL Player Salary Cap Prediction

## Project Overview

This project tackles the problem of how to value NHL players effectively under the league's salary cap restrictions. With the recent adjustments to the cap, organizations are seeking data-driven solutions to allocate financial resources efficiently. The objective is to develop predictive models that estimate an ideal salary cap hit for players based on their demographic and past performance data.

### Data and Models

Data for the 2021-2022 NHL season was sourced from [CapFriendly](https://www.capfriendly.com/)
Using player statistics from the 2021-2022 regular season, we developed separate models for forwards and defensemen. Players on entry-level contracts were excluded from the analysis. Multiple modeling approaches were tested, including linear regression, random forest models, and PCA for dimensionality reduction.

- For **forwards**, a linear regression model was the best fit. Key explanatory variables included:
  - Points per Games Played (P/GP)
  - Assists per Games Played (A/GP)
  - Age
  - Expected Goals For (xGF)
  - **Model performance**:  
    - R-squared = 0.63  
    - RMSE = 1,652,445

- For **defensemen**, a ridge regression model proved to be the most effective, with the following explanatory variables:
  - Points per Games Played (P/GP)
  - Shots per Games Played (Sh/GP)
  - Corsi Against (CA)
  - **Model performance**:  
    - R-squared = 0.73  
    - RMSE = 1,469,652

## Conclusion

The predictive models developed in this project offer a strong baseline for assessing NHL player salary cap hits, providing valuable insights into player valuation based on performance metrics. For forwards, shooting and scoring statistics such as Points per Game (P/GP) and Expected Goals For (xGF) are critical factors, while for defensemen, metrics like Corsi Against (CA) play a significant role. These models help identify undervalued or overvalued players, aiding in more informed decision-making during negotiations and free agency.

However, certain factors like leadership, injury history, and the effects of long-term contracts are not fully captured in these models. Players nearing the end of extended contracts, for instance, often show greater discrepancies between predicted and actual cap hits. This presents an opportunity for future improvement by incorporating these variables and expanding the dataset.

In summary, these models serve as a useful tool for NHL teams to enhance data-driven player valuation strategies, with the potential for further refinement in subsequent iterations.

### Contributors

This project was completed by:

- Scott Jue
- Laken Rivet

