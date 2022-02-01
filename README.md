# Premier League 2020-2021 - Skylar Shafer
A description of the tactical nature of teams during the 2020-2021 Premier League season. All data taken from sports-reference or transfrmarkt, respectfully. 

To begin, I want to go over some of the code I produced to run this analysis. I used numpy to make a matrix on the results of each team against each other (.5 for a draw, 1 for a win, 0 for a loss) in the league, adding the values of home and away matches into a single value between 0 and 2 (0 if team 1 lost against team 2 both times, 2 if they won both, 1.5 if a win and a draw, and so on). From there, I tested the correlation coefficient between the wins of each team compared to every team, to find teams that were the most similar in terms of who they beat and who they lost to. From there, I found the teams that were most similar to each base team in terms of who they beat, and the teams that were most different from the base team, for all 20 teams. You can lookover the code in the premier_league.ipynb file attached, if you'd like. I've also attached the data.


