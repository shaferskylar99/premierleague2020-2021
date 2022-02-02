# Premier League 2020-2021 - Skylar Shafer
A description of the tactical nature of teams during the 2020-2021 Premier League season. All data taken from sports-reference or transfrmarkt, respectfully. 

To begin, I want to go over some of the code I produced to run this analysis. I used numpy to make a matrix on the results of each team against each other (.5 for a draw, 1 for a win, 0 for a loss) in the league, adding the values of home and away matches into a single value between 0 and 2 (0 if team 1 lost against team 2 both times, 2 if they won both, 1.5 if a win and a draw, and so on). From there, I tested the correlation coefficient between the wins of each team compared to every team, to find teams that were the most similar in terms of who they beat and who they lost to. From there, I found the teams that were most similar to each base team in terms of who they beat, and the teams that were most different from the base team, for all 20 teams. You can look over the code in the premier_league.ipynb file attached, if you'd like. I've also attached the data files from sports-reference.

Now, let's look at the data!

First, here is a graph of the MOST similar teams, with each team's top 3 attached to them (some have more than 3, meaning they were in the top 3 most correlated of other separate teams not in their top 3, as well). 

![image](https://user-images.githubusercontent.com/56563084/152068839-21502e90-37b1-4a98-bd0a-d5ca98ca1559.png)

Next is bottom 4 least similar teams associated with each team. Teams that are connected with each other are the LEAST similar in terms of who they win and lose against (some have more than 4, meaning they were in the bottom 4 most correlated of other separate teams not their top 4, as well).

![image](https://user-images.githubusercontent.com/56563084/152070834-4b74122f-5c69-42a1-b998-2d6acabff0ce.png)

Now let's look deeper into these two graphs and what we can learn from them. The following sections are insights derived from a combination of these graphs and external information which will be explained.

# 1. Playstyles and Their Ability to Match Up

## 1. Liverpool, Leicester City, West Ham, Tottenham, and Crystal Palace Show Similarities

  All of these teams were connected with at least two of the others in the similarity graph, with Crystal Palace, West Ham, and Tottenham being connected to 3 of the 4 others. These teams were also all, besides Crystal Palace, in between 3rd and 7th in the table, so some of the top-quality teams in the league, but unable to really get close to Manchester City (Liverpool, in 3rd, were 5 points from Manchester United but 17 from Manchester City), so really, the strategy seems to have went good, but not great, for each of them. 
  
  Each of these teams plays a somewhat-rigid style, as we can tell by looking at who scores their goals. For Liverpool, 
  
  That's not to say that their systems are the same. Klopp and Liverpool are known for their unique pressing style as well as their tendency to drop a defensive midfielder into the back line when they have the ball, and use Firminho as a number 9 rather than a true striker. Liverpool and Leicester are also unique in their usage of outside backs in the attack. Each of these teams also have their own individual preferences in pressing or sitting back, counter-attacking versus wanting possesion, etc. Clearly, there are significant tactical tweaks between the teams.
  
  Instead, when I say the style is somewhat-rigid, I'm referring to the formation they prefer, and how they prefer to utilize space and fluidity. 
  
  In terms of the success of this kind of strategy, Liverpool's verion has clearly brought them success, having won the title in the previous year. Leicester are famous for winning the title after being a relegation candidate, and have risen to be top-6 contenders season after season. West Ham have risen as well, primarily this year, 

## 2. Manchester United is Confusing

## 3. The Cat and Mouse Game of Possesion vs. Counter Attacking Football

## 4. Parking the Bus or Playing the Game: Top Teams and Relegation Candidates

## 5. If You Want to Punch Above Your Weight, Bring a Unique Gameplan.

