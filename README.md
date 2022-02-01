# Premier League 2020-2021 - Skylar Shafer
A description of the tactical nature of teams during the 2020-2021 Premier League season. All data taken from sports-reference or transfrmarkt, respectfully. 

To begin, I want to go over some of the code I produced to run this analysis. I used numpy to make a matrix on the results of each team against each other (.5 for a draw, 1 for a win, 0 for a loss) in the league, adding the values of home and away matches into a single value between 0 and 2 (0 if team 1 lost against team 2 both times, 2 if they won both, 1.5 if a win and a draw, and so on). From there, I tested the correlation coefficient between the wins of each team compared to every team, to find teams that were the most similar in terms of who they beat and who they lost to. From there, I found the teams that were most similar to each base team in terms of who they beat, and the teams that were most different from the base team, for all 20 teams. You can lookover the code in the premier_league.ipynb file attached, if you'd like. I've also attached the data files from sports-reference.

Now, let's look at the data!

First, here is a graph of the MOST similar teams, with each team's top 3 attached to them (some have more than 3, meaning they were in the top 3 most correlated of other separate teams not in their top 3, as well). 

![image](https://user-images.githubusercontent.com/56563084/152068839-21502e90-37b1-4a98-bd0a-d5ca98ca1559.png)

Next is bottom 4 least similar teams associated with each team. Teams that are connected with each other are the LEAST similar in terms of who they win and lose against (some have more than 4, meaning they were in the bottom 4 most correlated of other separate teams not their top 4, as well).

![image](https://user-images.githubusercontent.com/56563084/152068861-68e29eba-b644-46db-8f39-0f8a2010785e.png)

Now let's look deeper into these two graphs and what we can learn from them. The following sections are insights derived from a combination of these graphs and external information which will be explained.

## 1. Playstyles and Their Ability to Match Up

# 1. Liverpool, Leicester City, West Ham, Tottenham, Crystal Palace

All of these teams were connected with at least two of the others in the similarity graph, with Crystal Palace, West Ham, and Tottenham being connected to 3 of the 4 others. These teams were all, besides Crystal Palace, in between 3rd and 7th in the table. 

