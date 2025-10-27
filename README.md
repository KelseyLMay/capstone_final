### Analzying Key Features in Determining Whether NHL Teams Win or Lose Games
**Kelsey May**

#### Executive summary

#### Rationale
Why should anyone care about this question?

#### Research Question
What are you trying to answer?

#### Data Sources
What data will you use to answer you question?

#### Methodology
What methods are you using to answer the question?

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