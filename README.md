# NBADecisionTree
![image](https://github.com/james-zhou1/NBADecisionTree/assets/32371970/74662218-9e5d-4181-b995-343d4f345e01)

Open Issues:
Right now, we have a few open issues.
1. We are able to figure out what the training accuracy, validation accuracy, false positive rate, and true positive rate of the program is. However, what we would really like to figure out is what percentage of years the program will be able to classify the correct champion. Keep in mind that we have also found that some of the probabilities are equal, which means that the model might predict multiple champions for one year. That is an issue.
2. We need someone to write a better README that illustrates the structure of this code. What does every file do? What does the data mean?
3. We need a separate notebook for the feature selection. We already did it, but we need to rewrite it.
4. Instead of using max_depth as the stopping criterion, we should use pruning instead.
5. 
6.
7. 


Variables and meanings

- Season 
- Year
- Team/Season
- Team
- Team ID
- Connection value, which team is which
- Team ID/Season
- Season+Team ID
- Conference
- Conference/Season- Conference+season
- Conference 5=> rec- Percent of games with a less than 5 point difference
- Conference OR- Average offensive rating of the conference
- Conference SRS- Average SRS of the conference
- Conference Age- Average age of the conference
- pre playoff odds- Odds calculated pre-playoff
- pre playoff odds rank- Teams ranked by playoff odds
- pre season odds- Odds to win the pre-season
- champion- Were they the champion?
- champion share- How likely a team was to be the champion. Computer calculated
- make playoffs- Did they make playoffs?
- top 3 conference- Were they top 3 for their conference?
- rk conference- The conference ranking a team falls in at the end of regular season
- overall record- W/L Ratio
- over500 rec- Winrate against teams with a 50% winrate
- over600 rec- Winrate against teams with a 60% winrate
- 20 =< wins- Wins by over 20 points
- 5 => rec- Wins by less than 5 points
- sum coach playoff games- Number of playoff games coaches have coached on a team
- sum coy shares- Number of Coaches of the Year awards gained by coaches on a team
- sum playoff games- Number of playoff games played by players on a team
- sum champion- Number of championships won by players on the team
- sum champion share- Number of games attributed to championship winners on a team
- sum mvp shares- Number of games attributed to an MVP per franchise
- sum all defense- Number of all-defense awards granted to players on a team
- sum all nba- Number of all-nba awards granted to players on a team
- sum dpoy shares- Number of Defensive Player of the Year awards granted to players on a team
- sum smoy shares- Number of games attributed to the winner of the Sixth Man of the Year Award (best bench player)
- sum mip shares- Number of games attributed to Most Improved Players on a team
- sum all stars- Number of all stars on a team
- sum player L1Y cs- Sum of the number of wins attributed to individual players in the previous year
- sum player L3Y cs- Sum of the number of wins attributed to individual players in the previous 3 years
- sum player L5Y cs- Sum of the number of wins attributed to individual players in the previous 5 years
- sum player L8Y cs- Sum of the number of wins attributed to individual players in the previous 8 years
- sum player L10Y cs- Sum of the number of wins attributed to individual players in the previous 10 years
- sum L3Y mvp shares- Sum of the number of wins attributed to MVP players in the previous 3 years
- sum L5Y mvp shares- Sum of the number of wins attributed to MVP players in the previous 5 years
- sum franchise L1Y cs- The previous year's champion winning chances
- sum franchise L3Y cs- The previous 3 years' champion winning chances
- sum franchise L5Y cs- The previous 5 years' champion winning chances
- sum franchise L8Y cs- The previous 8 years' champion winning chances
- sum franchise L10Y cs- The previous 10 years' champion winning chances
- curr/past mvp or past fmvp- (TEST) does the team have a former/current MVP or FMVP?
- FG- Field Goals (NOT free throws)/game
- FGA- Field Goal Attempts/game
- FG%- Field Goal %/game
- 3P- 3 points/game
- 3PA- 3 point attempts/game
- 3P%- 3 point %/game
- 2P- 2 points/game
- 2PA- 2 point attempts/game
- 2P%- 2 point % made/game
- FT- Free Throws per game
- FTA- Free Throw Attempts per game
- FT%- Free throw attempts percentage/game
- ORB- Offensive Rebounds (Rebounds grabbed while on offense) per game
- DRB- Defensive Rebounds (Rebounds grabbed while on defense) per game
- TRB- Total Rebounds per game
- AST- Assists per game
- STL- Steals per game
- BLK- Blocks per game
- TOV- Turnovers per game
- PF- Personal Fouls per game
- PTS- Points per game
- Age- Average age of players on Feb 1
- W- Wins
- L- Losses
- PW- Pythagorean Wins (Number of wins a team should have based on their performance)
- PL- Pythagorean Losses (Number of losses a team should have based on their performance
- MOV- Margin of Victory
- SOS- Strength of Schedule (How hard of opponents they had to play vs them during regular season, - means easier)
- SRS- Simple Rating System. This is SOS+point differential, basically how a team performed vs how well they were expected to perform
- ORtg- Offensive Rating (Points scored per 100 possessions)
- DRtg- Defensive Rating (Points allowed per 100 posessions)
- NRtg- Neutral Rating (Whether a team is better on offense vs defense, it literally is Offense - Defense rating)
- Pace- Pace Factor (Number of posessions per 48 minutes)
- FTr- Free Throw Rate
- 3PAr- 3 point rate
- TS%- How good you can shoot (PTS/2*TSA)
- Offense Four Factors|eFG%- Effective Field Goal %(Field Goal % taking into account that 3 points are more valuable than 2 points(FG + 0.5 * 3P) / FGA) while on offense
- Offense Four Factors|TOV%- Offensive turnover %, percent of turnovers per 100 plays while on defense
- Offense Four Factors|ORB%- Offensive Rebound %, percent of offensive rebounds grabbed
- Offense Four Factors|FT/FGA- Free Throws/Field Goal Attempts while on offense
- Defense Four Factors|eFG%- Effective Field Goal %(Field Goal % taking into account that 3 points are more valuable than 2 points(FG + 0.5 * 3P) / FGA) while on defense
- Defense Four Factors|TOV%- Defensive turnover %, percent of turnovers per 100 plays while on defense
- Defense Four Factors|DRB%- Defensive Rebound %, percent of rebounds grabbed while on defense
- Defense Four Factors|FT/FGA- Free Throws/Field Goal Attempts while on defense

- TSA- True Shooting Attempts (FGA*.44FTA



