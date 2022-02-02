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

  All of these teams were connected with at least two of the others in the similarity graph, with Crystal Palace, West Ham, and Tottenham being connected to 3 of the 4 others. These teams were also all, besides Crystal Palace, in between 3rd and 7th in the table, so some of the top-quality teams in the league, but unable to really get close to Manchester City (Liverpool, in 3rd, were 5 points from Manchester United but 17 from Manchester City), so really, the strategy seems to have went good, but not great, for each of them this past season, but there's certainly more to the story.
  
  Four out of these five teams depended on finishers. In terms of goals as opposed to expected goals (via sports-reference), Crystal Palace, West Ham, Tottenham, and Leicester City were 4 of the 9 teams with a positive value of goals minus expected goals. Basically, this means that the goal-scorers finished more shots than expected, indicating that they are of high class. Liverpool has a world-renowned front 3 of Salah, Mane, and Firmino, but appears to have had an off season in terms of finishing.
  
  Each of these teams plays a somewhat-rigid style, as we can tell by looking at who scores their goals. For Liverpool, Salah (22), Mane (11), Jota (9) and Firmino (9).  For Leicester City, Vardy (15), Iheanacho (12) Barnes (9) and Maddison (8). For Tottenham, Harry Kane (23), Son-Heung Min (17) and Gareth Bale (11).  For West Ham, Soucek (10), Antonio (10), Lingard (9) and Bowen (8). For Crystal Palace, Zaha (11), Benteke (10) and Eze (4).
  
The aforementioned names scored the following percentage of their team's goals: 51/68 for Liverpool (75%), 44/68 for Leicester (64.7%), 37/62 for West Ham (57.8%), 51/68 for Tottenham (75%), 25/41 for Crystal Palace 60.97%. Manchester City's concentration would be 41/83 using their top four players (Gundogan, Sterling, 2 of Mahrez/Jesus/Foden), equal to 49.39% of their total goals. Chelsea's would be 25/58, equal to 43.1% of their total goals (Jorginho, Mount, Werner, Abraham). Manchester United would be 46/73 (Fernandes, Rashford, Cavani, Greenwood), or 63.01% of all goals. Clearly, these 5 teams are more similar to each other than Chelsea or Manchester City in terms of goal concentration, and we will look at Manchester United in-depth later.

  I think we should go over why the answers for the 5 main clubs we're talking about vary, starting with West Ham. West Ham do at least 2 things differently to the other 4. Firstly, they are deadly on set pieces from dead balls. They led the league in goals from passes on dead balls last season with 13, 4 more than anybody else in the league, and 7 more than any of the 4 other clubs we are talking about. Secondly, they play with a variety of attackers, and they attack with slightly less rigidity than Tottenham or Crystal Palace. We will get to Liverpool and Leicester in a moment. Continuing, either of these qualities about West Ham are evident in Soucek's status as a top scorer for them. He is a midfielder, not a signature attacker as almost every other name on that list is. None of the West Ham attackers played more than 80% of the available league minutes, demonstrating that playing time was split amongst them (Soucek played every available league minute, on the other hand). So, although Soucek's inclusion does make West Ham an interesting case, much of it can be explained by other factors. They are still unique in their choice to allow him to push into the box though, to be on the receiving end of crosses and passes through, which has clearly been successful for them with their recent rise.
  
  Klopp and Liverpool are known for their unique pressing style as well as their tendency to drop a defensive midfielder into the back line when they have the ball, and use Firminho as a number 9 rather than a true striker. Liverpool and Leicester are also unique in their usage of outside backs in the attack. Each of these teams also have their own individual preferences in pressing or sitting back, counter-attacking versus wanting possesion, etc. Clearly, there are significant tactical tweaks between the teams.
  
  Instead, when I say the style is somewhat-rigid, I'm referring to the formation they prefer, and how they prefer to utilize space and fluidity. 
  
  In terms of the success of this kind of strategy, Liverpool's verion has clearly brought them success, having won the title in the previous year. Leicester are famous for winning the title after being a relegation candidate, and have risen to be top-6 contenders season after season. West Ham have risen as well, primarily this year. Tottenham was considered somewhat disappointing last season, finishing 7th, and Crystal Palace finished 14th. So, clearly, this style of play is not perfect, and those who tweak it into fast, counter-attacking football with fullback activity in attack seem to have had the most success.
  
## 2. Teams that Act Normal/Boring

Teams that have many connections in the first graph

## 3. The Cat and Mouse Game of Possesion vs. Counter Attacking Football

Manchester City, Liverpool, Leicester City

## 4. Parking the Bus and Countering or Playing the Game: Top Teams and Relegation Candidates

Chelsea and Brighton as opposites in league and style, but neither can finish, Leicester and Liverpool Counter versus Sheffield or West Brom, good or bad, attack or low block, Risk of playing straight up but also high-reward
Note that Chelsea and Brighton are listed as similar

## 5. If You Want to Punch Above Your Weight, Bring a Unique Gameplan/Bielsa Ball.

Brighton have many connections in the second graph, Leeds, Leicester winning the league, West Ham, Liverpool, Leicester
At some point you have to push numbers forward to pursue chance creation, it's a matter of deciding when you can do so to maximize return and minimize the risk of conceding a goal yourself. 
Why did I group clubs by the similarity of their wins in the first place? I thought this would be best by understanding that unique gameplans utilize unique spaces, allowing them to perform better against certain opposing strategies. In turn, if we look at the similarity of results, we can then deduce who likely plays the most like each other. 
Chelsea, Arsenal, and fear: Man City having to break down low-blocks, while Chelsea and Arsenal don't always have to, because they get less respect
Fluidity (given that each player on a team is capable) is clearly worth it in most cases

The two clubs who saw the most success (Manchester City in winning the league, Chelsea in winning the Champions League) each chose to be unique in how they played the game.

## 6. Manchester United is Confusing

Sample anomaly, no real connection to the others, a club lacking direction

## 7. Conclusion

I hope you enjoyed, and let me know if you'd like me to make more! I think doing Serie A next could be interesting, especially considering the tactics of Atalanta. 

