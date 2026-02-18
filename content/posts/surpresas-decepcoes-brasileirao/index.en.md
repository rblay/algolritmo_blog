---
title: "Brazilian League’s Over and Under Achievers"
date: 2017-01-07
draft: false
---

As the Brazilian National League off-season period is currently underway, I bring you a new method to analyze each club’s performances in last year’s tournament (Brasileirão 2016). The goal of the model is to understand which teams performed better than anticipated and which teams failed to meet expectations. Virtually all soccer specialists agree that to win the Brasileirão (or any national league as a matter of fact) it is necessary to have a talented group of players, hence we will compare the quality of rosters with their achievements in the tournament.

**Assumptions:**

Costlier squads have better players, which implies on having a better chance of fighting for the championship. The average market value of a player from each team (calculated by dividing the total team market value by the number of players) is a good indicator of squad quality.

**Methodology:**

First, I used transfermarkt.com to collect data regarding the market value for each team. Most values were from May 2016 (when the Brasileirão was just starting), this means that player performances during the tournament still had not influenced the values. Then, I calculated the average player market for of each team and ordered them accordingly, here is a table with this calculated squad quality ranking:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/Screen-Shot-2017-01-09-at-8.06.42-PM-300x287.png?resize=552%2C528)

Last, I compared the squad quality ranking with the team’s final standings by calculating the difference. A negative difference means the team underachieved while a positive one means it overachieved.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/Screen-Shot-2017-01-09-at-8.07.01-PM-300x274.png?resize=555%2C507)

**Results:**

(DISCLAIMER: If you are afraid by statistical terms please skip the next paragraph, I promise that it will be simple to understand if you choose to read it)

At first we can see that there is a moderate correlation between the final league standings and the squad rankings (a correlation of 0.598 to be more precise). In other words, teams with higher average market values tend to finish in the top of the table while team with lower average values tend to get closer to the relegation zone. Also, we see that the average difference is of 4 positions, which means that there is a good chance that your team will finish 4 positions above or below of what the squad ranking predicted. In sum, the model has issues predicting a team’s exact final standing, however it generally gets the “table region” right.

With this initial analysis done, I separated the 4 teams with the greatest positive differences (Botafogo, Santos, Atlético-PR and Ponte Preta) and the 4 teams with the greatest negative differences (Internacional, Cruzeiro, São Paulo and Fluminense). Those were the clubs which the model was the most unsuccessful at predicting performance, we can say they are the season’s biggest over and under achievers.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/surpresasDecepcoesENmenor-300x300.png?resize=568%2C568)

Now that a quantitative analysis made it clear who were the big surprises and disappointments of the tournament we can look qualitatively at the reasons behind those performances. By analyzing the team’s decisions during 2016 it is clear that **knowledge about the players** **in the club’s squad** is essential in order to perform well.

It interesting to note that the only overachiever club who had a managerial change during the Brasileirão was Botafogo, where Jair Ventura replaced Ricardo Gomes. Yet, Jair Ventura was an assistant coach at Botafogo and already knew and dealt with all the athletes he ended up managing for the rest of the season. Meanwhile, Santos, Atlético-PR and Ponte Preta trusted their head coaches (Dorival Júnior, Paulo Autuori and Eduardo Baptista respectively) and kept them at their jobs during the whole tournament, a decision that brought extremely positive results. On the other hand, all the underachieving clubs changed the their head coaches at least once, special highlight to Internacional that had 4 different managers along the 38 games. Even with an extremely qualified squad, it is difficult to achieve good results without a decent amount of time to work and get to know the players’ characteristics.

Observations:

1.  Another explanation for the results above is the difficulty to make a valuation of some players before the tournament begins. For example, Vitor Bueno (one of Santos’ main players and winner of the rookie of the year award) had a market value of 1 Million Euros, while some other more well-known players such as Eduardo Sasha had a market value of 2.5 Million Euros. The process of translating athlete performance into market value has a few problems and difficulties, yet it is still an interesting analysis tool.
2.  If you plan in reproducing the model, in order to calculate the average difference you should use absolute values, otherwise negative values will probably have a great interference in the final results