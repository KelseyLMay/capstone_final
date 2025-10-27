### Analzying Key Features in Determining Whether NHL Teams Win or Lose Games
**Kelsey May**

#### Executive summary

#### Rationale
Hockey games generate large amounts of performance data, from player-level statistics to team-level tactical metrics. While the final outcome of a game is influenced by numerous factors (player skills, team strategy, in-game dynamics, etc.), the ability to quantify and predict game results remains a major challenge.

This analysis aims to develop machine learning models that predict the likelihood of a hockey team winning a game, and analyze which factors most heavily influence game outcomes. By leveraging historical game data, in-game statistics, and relevant contextual information, this analysis creates predictive models capable of capturing comple patterns and interactions that traditional statistical analysis might miss.

The significance of this research extends across multiple stakeholder perpsectives:
1) Hockey Teams: Teams want to optimize performance, both on and off the field. Insights derived from predictive models can inform tactical decisions, roster management, and training priorities. By understanding which factors most heavily influence game outcomes, teams can allocate resources more effectively, enhance player development, and maximize the likelihood of winning. This succcess directly impacts revenues from sale of tickets, merchandise, and sponsorships. 
2) Players' Agents: Agents are invested in their clients' careers and market value. By understanding the statistical factors that contribute most to team success, agents can better advocate for players whose performance metrics align with winning outcomes, negotiate contracts, and identify teams where their clients are most likely to succeed.
3) Journalists and Media Outlets: Predictive analytics and key factor identification provide journalists with compelling, data-backed narratives for reporting. Understanding which elements influence game outcomes enhances pre-game analysis, commentary, and post-game evaluations, offering audiences deeper insights into the game beyond traditional reporting.
4) Sports Gambling Companies: Accurate predictive models enable bookmakers to set informed odds and provide bettors with data-driven strategies, translating statistical insights into financial returns within betting margins.

This project combines analytics with domain-s-specific expertise to bridge the gap between raw data and actionable insights. By predicting game outcomes and highlighting the most influential factors, it supports strategic decision-makiing=ng in team management, player representation, sports journalism, and betting markets, demonstrating the transformatie potential of maching learning in professional hockey.

#### Research Question
Which features most strongly influence hockey game outcomes, and how accurately can machine learning models predict a team's likelihood of winning based on those factors?

#### Data Sources
This analysis uses the team-level data for all NHL games since 2008 provided by [MoneyPuck.com](https://moneypuck.com/data.htm).

#### Methodology
Data Cleaning

Analysis
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
What suggestions do you have for next steps?

#### Outline of project

- [Link to notebook 1]()
- [Link to notebook 2]()
- [Link to notebook 3]()


##### Contact and Further Information