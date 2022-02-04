# Premier League 2020-2021 - Skylar Shafer
A description of the tactical nature of teams during the 2020-2021 Premier League season. All data taken from sports-reference or transfrmarkt, respectfully. 

To begin, I want to go over some of the code I produced to run this analysis. I used numpy to make a matrix on the results of each team against each other (.5 for a draw, 1 for a win, 0 for a loss) in the league, adding the values of home and away matches into a single value between 0 and 2 (0 if team 1 lost against team 2 both times, 2 if they won both, 1.5 if a win and a draw, and so on). From there, I tested the correlation coefficient between the wins of each team compared to every team, to find teams that were the most similar in terms of who they beat and who they lost to. From there, I found the teams that were most similar to each base team in terms of who they beat, and the teams that were most different from the base team, for all 20 teams. You can look over the code in the premier_league.ipynb file attached, if you'd like. I've also attached the data files from sports-reference.

Now, let's look at the data!

First, here is a graph of the MOST similar teams, with each team's top 3 attached to them (some have more than 3, meaning they were in the top 3 most correlated of other separate teams not in their top 3, as well). 

![image](https://user-images.githubusercontent.com/56563084/152068839-21502e90-37b1-4a98-bd0a-d5ca98ca1559.png)

Next is bottom 3/4 least similar teams associated with each team. Teams that are connected with each other are the LEAST similar in terms of who they win and lose against (some have more than 4, meaning they were in the bottom 4 most correlated of other separate teams not their top 4, as well). 

![image](https://user-images.githubusercontent.com/56563084/152070834-4b74122f-5c69-42a1-b998-2d6acabff0ce.png)

Now let's look deeper into these two graphs and what we can learn from them. The following sections are insights derived from a combination of these graphs and external information which will be explained.

# 1. Playstyles and Their Ability to Match Up

## 1. Liverpool, Leicester City, West Ham, Tottenham, and Crystal Palace Show Similarities

  All of these teams were connected with at least two of the others in the similarity graph, with Crystal Palace, West Ham, and Tottenham being connected to 3 of the 4 others. These teams were also all, besides Crystal Palace, in between 3rd and 7th in the table, so some of the top-quality teams in the league, but unable to really get close to Manchester City (Liverpool, in 3rd, were 5 points from Manchester United but 17 from Manchester City), so really, the strategy seems to have went good, but not great, for each of them this past season, but there's certainly more to the story.
  
  Four out of these five teams depended on finishers. In terms of goals as opposed to expected goals (via sports-reference), Crystal Palace, West Ham, Tottenham, and Leicester City were 4 of the 9 teams with a positive value of goals minus expected goals. Basically, this means that the goal-scorers finished more shots than expected, indicating that they are of high class. Liverpool has a world-renowned front 3 of Salah, Mane, and Firmino, but appears to have had an off season in terms of finishing.
  
  Each of these teams plays a somewhat-rigid style, as we can tell by looking at who scores their goals. For Liverpool, Salah (22), Mane (11), Jota (9) and Firmino (9).  For Leicester City, Vardy (15), Iheanacho (12) Barnes (9) and Maddison (8). For Tottenham, Harry Kane (23), Son-Heung Min (17) and Gareth Bale (11).  For West Ham, Soucek (10), Antonio (10), Lingard (9) and Bowen (8). For Crystal Palace, Zaha (11), Benteke (10) and Eze (4).
  
The aforementioned names scored the following percentage of their team's goals: 51/68 for Liverpool (75%), 44/68 for Leicester (64.7%), 37/62 for West Ham (57.8%), 51/68 for Tottenham (75%), 25/41 for Crystal Palace 60.97%. Manchester City's concentration would be 41/83 using their top four players (Gundogan, Sterling, 2 of Mahrez/Jesus/Foden), equal to 49.39% of their total goals. Chelsea's would be 25/58, equal to 43.1% of their total goals (Jorginho, Mount, Werner, Abraham). Manchester United would be 46/73 (Fernandes, Rashford, Cavani, Greenwood), or 63.01% of all goals. Clearly, these 5 teams are more similar to each other than Chelsea or Manchester City in terms of goal concentration, and we will look at Manchester United in-depth later.

![image](https://user-images.githubusercontent.com/56563084/152237633-6ad87d91-ccca-453d-8091-1f6ea8d16c93.png)

  I think we should go over why the answers for the 5 main clubs we're talking about vary, starting with West Ham. West Ham do at least 2 things differently to the other 4. Firstly, they are deadly on set pieces from dead balls. They led the league in goals from passes on dead balls last season with 13, 4 more than anybody else in the league, and 7 more than any of the 4 other clubs we are talking about. Secondly, they play with a variety of attackers, and they attack with slightly less rigidity than Tottenham or Crystal Palace, which we will explain momentarily. We will get to Liverpool and Leicester in a moment. Continuing, either of these qualities about West Ham are evident in Soucek's status as a top scorer for them. He is a midfielder, not a signature attacker as almost every other name on that list is. None of the West Ham attackers played more than 80% of the available league minutes, demonstrating that playing time was split amongst them (Soucek played every available league minute, on the other hand). So, although Soucek's inclusion does make West Ham an interesting case, much of it can be explained by other factors. They are still unique in their choice to allow him to push into the box though, to be on the receiving end of crosses and passes through, which has clearly been successful for them with their recent rise.
  
  Klopp and Liverpool are known for their unique pressing style as well as their tendency to drop a defensive midfielder into the back line when they have the ball, and use Firminho as a number 9 rather than a true striker. Liverpool and Leicester are also unique in their usage of outside backs in the attack, allowing them to overlap and put in crosses, playmakers operating from the outside. So, despite their high goal concentration, they express their tactical adjustments and fluidity in their outside backs who often get assists instead, so they, like West Ham, have their own tweaks to the system which are are certainly fluid, and both Liverpool and Leicester have certainly seen success from it, especially compared to the last two teams, the seemingly most rigid, Tottenham and Crystal Palace. 
  
  When I say the style is somewhat-rigid, I'm referring to how staunchly they follow a static playing structure. Clearly, it appears that Tottenham is hesitant to push others forward besides the attacking front 3, given that we only included 3 top scorers for them, and they still were tied for the highest goal concentration. Their dependency on their front 3 to attack and score goals is in line with traditional, standard structured football. Crystal Palace seem to be rigid as well. We only included 3 top scorers for them as well, and it was up there with the rest that included 4 top scorers, in goal concentration. To see more evidence that Crystal Palace plays comparatively rigid, standard structured football, please look to the next section after this one, titled "Teams that Act Normal/Boring". 
  
  To summarize in terms of the success of this kind of strategy, Liverpool's verion has clearly brought them success, having won the title in the previous year. Leicester are famous for winning the title after being a relegation candidate, and have risen to be top-6 contenders season after season. West Ham have risen as well, primarily this year. Tottenham was considered somewhat disappointing last season, finishing 7th, and Crystal Palace finished 14th. So, clearly, this style of play is not perfect, and those who tweak it to fit some degree of fluidity and take chances by moving certain players forward seem to have had the most success.
  
## 2. Teams that Act Normal/Boring

How could we know if teams seem to have a strategy that produces expected results, beating bad teams and losing good teams more consistently than others, acting as expected? We can look at who has the highest summed correlations with all other teams, in terms of who they beat and lost to. We will get into the exciting teams later (I love you Brighton). Here is the graph.

![image](https://user-images.githubusercontent.com/56563084/152572916-a652faa0-74d2-41c5-9dad-2b8ae8fbadf2.png)

First, I'd like to note, Manchester City are not boring. Anyone who pays attention to the league knows that. I think part of the reason they are up so high in this graph is just because they beat almost everyone last season, they were so dominant. The other three of the top four, on the other hand, make sense. We've already been over how standard it seems Tottenham and Crystal Palace play, lacking uniqueness and creativity, and this chart tends to back that up. Southampton appears to be a similar team, very much just a regular team in the lower half of the table, which is unfortunate, but at least they avoided relegation! Can't argue with the results, I suppose. You may have noticed that none of the bottom 3 are here, but when you barely beat anybody, it does get harder to be correlated with other teams and their wins, and I think that most people who watched their matches would agree that the relegated teams last season played fairly standard, pedestrian football. You may be wondering if I'm going to comment on Leicester, West Ham, or Leeds, who are next in line. No, because I think they play at least slightly more unique styles, and thus, although they may beat expected teams and lose to expected teams, they do it in an interesting fashion. In particular, Leeds is a very unique team for the bottom half of the table!

## 3. Parking the Bus and Countering or Playing the Game: Top Teams and Relegation Candidates

Possession versus counter-attacking is a constant cat and mouse game in football. Traditionally, relegation candidates park the bus against the top teams, attacking with pace when they can, with only a couple players forward, hoping to take advantage of the top teams pushing players forward pursuing goals. Top teams seek to control possession, taking their team, trying to pick apart the defense gradually. The relegation candidates look scared, and the top teams can look frustrated with the defensive style. Honestly, these kinds of games can be boring. I can't blame either team, though, for this kind of strategy. From a relegation candidate's perspective, it can lock out the big teams, potentially chasing a draw for even a single key point to avoid relegation, and it can provide opportunities with lots of space in the few moments of attack that are generated. Leicester won the league on a blistering counter attack and a solid defense, remember. From a top team's perspective, they have to react to this low-block, bus-parking strategy by trying to move the ball to break down the structured, deep defense. 

Every match, each team reacts to each other, and lower-table team decides how much respect to give the top team. For example, so many lower-league teams, when they play Manchester City, park the bus, because they know how good Manchester City is. They have a surplus of respect, which would at first appear to be a good thing, but it really isn't always. The following graph gives the average score (on the previously discussed 0-2 scale) of the top 8 teams against the bottom 4, minus the average score against the top 15 (I've excluded Brighton, which I will explain later).

![image](https://user-images.githubusercontent.com/56563084/152584426-af97f4d8-3ea6-4af4-8bee-b2e1c97eaf36.png)

As you can see, some teams comparatively struggle to secure wins against bad teams. Manchester United is an inconsistent anomaly (which we will discuss later), but Manchester City and Liverpool, the winners of the league in this season and the season before it, clearly have some of the lowest values in the graph. To me, this is evidence of the struggle of breaking down teams that use a low-block defensive strategy against you, out of a surplus of respect. Manchester City loves to have the ball at least, so it is at least associated with their natural playing style, but the low-block is still evidently hard even for them to break down. Liverpool love to attack directly, to attack with pace, find open space on the counter, and to press teams that have the ball. This does not match up at all with how they have to play against bad teams who park the bus and take few chances, which is why they actually get more average points on our scale against the top 15, and less against the bottom 4!

An interesting contrast in this discussion is Brighton and Chelsea. Chelsea, particularly under the Tuchel era, love to play with wingbacks, very defensively (especially for a top team), and have often struggled to find goals (much of the blame of this has come upon their strikers, such as Werner). Brighton, on the other hand, attack and play much more fluidly and openly than other relegation candidate teams, even when they're against top opposition, and by expected goals, would've taken 5th in the league last season, but instead took 16th, based on bad finishing and debatably bad luck. These two teams are also listed as similar in our graphs from the beginning, showing a comparatively strong correlation in the teams they beat. The value is negative as it is for Brighton with many clubs, but less so than the others. So, a top team that plays defensively, and a lower-league team that plays openly, are more correlated than Brighton against other teams. 

Brighton is such a unique sample in our data set, in general. They are the only team in our data set which has a negative summed correlation with every other team, from the previous graph on the topic. They are more likely to beat good teams than other lower-table teams, but are less likely to beat other lower-league teams, it seems. Maybe, as they go out and attack lower-table teams, they get caught in the cat and mouse game of a low-block, same as Manchester City and Liverpool. They play better when they play teams that are also willing to attack. Chelsea are more likely to win the cat and mouse game against better teams, as they are the ones who play defensively and pick their moments, but against bad teams, neither attacks with as much tenacity, both playing the role of hesitancy. So Chelsea is a good team acting as a bad team, and Brighton is a bad team acting as a good team. In either case, they beat good teams more often than they should, and struggle to secure wins against worse teams.

## 5. If You Want to Punch Above Your Weight, Bring a Unique Gameplan/Bielsa Ball.

So, what have we learned from this analysis so far? I think, in order to best summarize what we can bring from our insights so far, we must look at the (unfortunate) core of premier league football, money.

How do teams of various levels of investment in players stack up against each other? What strategies seem to create the most success for the least cost?



Leeds, Leicester winning the league, West Ham, Liverpool, Leicester
At some point you have to push numbers forward to pursue chance creation, it's a matter of deciding when you can do so to maximize return and minimize the risk of conceding a goal yourself. 
Why did I group clubs by the similarity of their wins in the first place? I thought this would be best by understanding that unique gameplans utilize unique spaces, allowing them to perform better against certain opposing strategies. In turn, if we look at the similarity of results, we can then deduce who likely plays the most like each other. 
Chelsea, Arsenal, and fear: Man City having to break down low-blocks, while Chelsea and Arsenal don't always have to, because they get less respect, that's why Arsenal and Mahcester City are so unrelated, Arsenal gets to play bad teams straightup, Manchester City does not
Fluidity (given that each player on a team is capable) is clearly worth it in most cases
Leeds

The two clubs who saw the most success (Manchester City in winning the league, Chelsea in winning the Champions League) each chose to be unique in how they played the game.

## 6. Manchester United Needs Direction

Sample anomaly, no real connection to the others, a club lacking direction

## 7. Conclusion

I hope you enjoyed, and let me know if you'd like me to make more! I think doing Serie A next could be interesting, especially considering the tactics of Atalanta. Let me know if you want me to do one for next season as well, so I can talk about Brentford, another interesting lower-half team that is willing to take chances, which you love to see!

