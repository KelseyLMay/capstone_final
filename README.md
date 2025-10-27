### Analzying Key Features in Determining Whether NHL Teams Win or Lose Games
**Kelsey May**

#### Executive summary
This research project applied machine learning techniques to analyze NHL hockey data and identify the factors that most strongly influence whether a team wins or loses a game. Using a cleaned and filtered datset derived from MoneyPuck.com, several classification models were developed to predict game outcomes based on game-level performance metrics. The accuracy of the models ranged from 80-84%, indicating a high level of consistency and predictive reliability. The influence of different features was also stable across modeling approaches, suggesting the relationships are not dependent on algorithmic variation.

Overall, the models indicated that scoring metrics were the strongest prediction of success, but not all shot-related metrics were benficial. The findings suggested that shot quality and conversion efficiency are more important than sheer volume. Similarly, contextual factors such as game location play smaller yet significant roles. On the other hand, penalties, fatigue, and late-season team disruptions increasee the likelihood of losing.

While this analysis confirms that scoring is the strongest predictor of success, this conclusion is largely intuitive. The next phase of research should focus on understanding the underlying mechanics of goal creation and prevention rather than the outcomes themselves. This could include analyzing more granular event-level and tracking data to understand details about how possession, player positioning, shot quality, and play sequences affect scoring opportunities. Moving beyond the surface-level metrics to explore how scoring opportunities occur will provide more actionable insights for coaches, analysts, and decision-makers seeking to improve team performance.

#### Rationale
Hockey games generate large amounts of performance data, from player-level statistics to team-level tactical metrics. While the final outcome of a game is influenced by numerous factors (player skills, team strategy, in-game dynamics, etc.), the ability to predict game results remains a major challenge.

This analysis aims to develop machine learning models that predict the likelihood of a hockey team winning a game, and analyze which factors most heavily influence game outcomes. By leveraging historical game data, in-game statistics, and relevant contextual information, this analysis creates predictive models capable of capturing complex patterns and interactions that other analysis might miss.

The significance of this research extends across multiple stakeholder perpsectives:
1) Hockey Teams: Teams want to optimize performance, both on and off the field. Insights derived from predictive models can inform tactical decisions, roster management, and training priorities. By understanding which factors most heavily influence game outcomes, teams can allocate resources more effectively, enhance player development, and maximize the likelihood of winning. This succcess directly impacts revenues from sale of tickets, merchandise, and sponsorships. 
2) Players' Agents: Agents are invested in their clients' careers and market value. By understanding the statistical factors that contribute most to team success, agents can better advocate for players whose performance metrics align with winning outcomes, negotiate contracts, and identify teams where their clients are most likely to succeed.
3) Journalists and Media Outlets: Predictive analytics and key factor identification provide journalists with data-supported narratives for reporting. Understanding which elements influence game outcomes enhances pre-game predictions, commentary, and post-game analysis, offering audiences deeper insights into the game beyond traditional reporting.
4) Sports Gambling Companies: Accurate predictive models enable bookmakers to set informed odds and provide bettors with data-driven strategies, translating statistical insights into financial returns within betting margins.

This project combines analytics with domain-specific expertise to bridge the gap between raw data and actionable insights. By predicting game outcomes and highlighting the most influential factors, it supports strategic decision-making in team management, player representation, sports journalism, and betting markets, demonstrating the potential of maching learning to enhance data analysis in professional hockey.

#### Research Question
Which features most strongly influence hockey game outcomes, and how accurately can machine learning models predict a team's likelihood of winning based on those factors?

#### Data Sources
This analysis uses the team-level data for all NHL games since 2008 provided by [MoneyPuck.com](https://moneypuck.com/data.htm).

#### Methodology
Data Understanding
A thorough review was conducted of the data documentation provided by MoneyPuck.com to understand the meaning and structure of different features. To maintain analytical consistency, fields containing aggregate or pre-processed statistics were removed, ensuring that only game-level performance variables were included in the modeling process.

Data Preparation and Filtering
A series of data cleaning and preprocessing steps were applied to create a conssitent and interpretable dataset:
1) Filtered game context: Excluded playoff games and statistics recorded during special game circumstance (such as during a power play or penalty kill) to focus exclusively on even-strength play.
2) Removed incomplete or rescheduled games: Games that were not completed or were partially rescheduled were excluded to control for discrepancies in game length and conditions.
3) Excluded overtime results: Games that extended into overtime were removed to maintain consistent play duration across samples.
4) Calculated win/loss: Whether a team won or lost was derived from the "goals for" and "goals against" variables.
5) Removed duplicate team entries: Each game appears twice in the dataset (once from each team's perspective), statistics for the opposing team were removed to avoid duplication.
6) Season phase categorization: The month of each game was mapped into an early, mid, or late season category to capture temporal dynamics in team performance.
7) Outlier removal: Outliers were removed from the dataset using the interquartile range. Specifically, any observations below Q1 - (1.5 x IQR) or above Q3 + (1.5 x IQR) were removed.
8) Assessed feature relevance: Box plots illustrated the distribution of each feature by game outcome. Features showing little differentiation between wins and losses were considered non-predictive and removed from further analysis.

Analysis
The cleaned dataset was divided into training and testing datasets to evaluate model performance on unseen data. Numerical features were standardized, and categorical variables were one-hot encoded to ensure compatibility with the algorithms. Cross validation was used to ensure model reliability and mitigate overfitting. This preprocessed dataset was then used to build a number of models aimed at predicting game outcomes and identifying the variables most influential in determining a team's likelihood of winning. 

#### Results
Accuracy across several models hovers from 80 - 84% and the influence of the different features is pretty consistent across different models. 

The key positive predictors that influenced the likelihood that a team would win the game were as follows:
1) number of goals. Teams with more goals were substantially more likely to win the game. All types of goal quality metrics were strong contributors, indicating that scoring in any danger category drives success.
2) playing at home. 
3) takeaways and low danger shots. Puck possession and consistent offensive pressure influenced the outcome.
4) mid-season games. Although the effect was smaller than the other features, this could reflect improved team cohesion or mid-season form, especially for teams that had a lot of turnover in the off season.

The key predictors that influenced the likelihood that a team would lose the game were as follows:
1) play continued in zone and blocked shot attempts. Extended defensive zone play and blocked attempts might indicate the defense is struggling to clear the puck, allowing the opposing team more opportunities to shoot.
2) medium and high danger shots. This finding is counterintuitive, but could indicate a team with high volume but low conversion, either because the shots were poorly placed or the opposing goalie was especially strong.
3) saved shots, freezes, and saved unblocked attempts. While it is good if the goalie stops pucks from going in the net, having a high number of those opportunities indicates the opposing team is able to shoot a lot, potentially increasing the likelihood that they will score.
4) penalty minutes. More penalty minutes reduces the likelihood of winning a game since they have fewer players on the penalty kill. Nonetheless, the history and culture of fighting and vigilanteeism in hockey is strong.
5) late season. Although the effect is low, this could be a factor if a team experiences a high rate of injuries or injuries among key players later in the season, or if the team clinches a playoff spot early and starts sitting its typical starters
6) hits and play continued outside of the zone. This finding suggests that physical play and neutral-zone time don't translate to wins.

Overall, the models indicate that scoring metrics dominate the likelihood of winning. However, not all shot metrics are beneficial. Some shot quantity metrics are negatively correlated, demonstrating that shot quality and conversion matter more than just volume. Finally, there are some additional contextual factors that influence the likelihood of winning, such as whether the team is playing at home or whether the team has had an opportunity to coalesce, especially after significant turnover. Conversely, penalties and late season factors such as injuries, fatigue, or sitting starters after clinching playoff positions increase the likelihood that a team will lose.


#### Next steps
While this analysis shows that certain metrics such as goal scored are among the strongest predictors of a team's likelihood of winning, this finding is somewhat intuitive. Scoring more goals naturally leads to more wins, and while this validates the model's baseline accuracy, it's also of limited utility without a better understanding of more granular performance indicators that contribute to goal creation and prevention.

Future work should focus on analyzing the factors that lead to goals, such as passing sequences, shot quality, possession dynamics, and player positioning. Adding event-level or tracking data could reveal how specific decisions, player movements, or situations influence scoring opportunities. Similarly, examining interactions between features (for example, how positioning choices interact with shot quality or how defensive errors create higher danger chance) could create a more nuanced picture of game outcomes. Expanding the dataset to including additional context features such as fatigue, injuries, or opponent strength would also furthr enhance the robustness of the models.

While the current models identify general predictors of success, the next phase of the analysis should focus on understanding the mechanisms behind the predictors. These additional findings would provide more actionable insights to coaches, analysts, and decision-makers trying to improve and better understand team performance.

#### Outline of project
- [Jupyter Notebook](https://github.com/KelseyLMay/capstone_final/blob/main/capstone.ipynb)
- [Images](https://github.com/KelseyLMay/capstone_final/tree/main/images) contains the boxplots used to develop an initial understanding of the impact of different features on game outcome.
- [Dataset](https://github.com/KelseyLMay/capstone_final/blob/main/data/all_teams_full.csv)
