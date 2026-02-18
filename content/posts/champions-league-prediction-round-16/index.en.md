---
title: "Champions League 17-18 Predictions Round of 16"
date: 2018-02-12
draft: false
---

Algolritmo is back with predictions about the UEFA Champions League, which begins its knockout phase tomorrow. Using the excellent datasets provided by Stratabet, I calculated the odds of each team being champion of the most important tournament in Europe, as well as the odds of a win, draw or defeat in the first leg of the round of 16. I intend to publish more texts with new forecasts throughout the next phases of the championship. First, I present two images and an analysis that summarize the results of the simulation. After this I detail the method used for readers who have an interest in statistics, mathematics and computing (in addition to soccer, of course).

Remember to like our _[Facebook page](https://www.facebook.com/algolritmo)_!

**Results:**

The following image presents the current probability of each team winning the UEFA Champions League:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/02/probUCL18ChampionRound16Leg1-230x300.png?resize=626%2C817)

The result is quite close to what I expected. Manchester City, Bayern Munich, PSG and Barcelona are leading their national leagues (England, Germany, France and Spain respectively), it is to be expected that these teams will be favorites to win the Champions League.

Real Madrid and Liverpool appear soon to follow with near odds to win the tournament, but with diferente momentum. The Madrid team has not been able to repeat the incredible performances of the last seasons which have made them the most powerful team in Europe. Meanwhile, Liverpool has been making an exciting season with good performances from players like Mohammed Salah and Roberto Firmino. However, it is not yet clear if the team will be able to maintain the high level after losing one of its main players, Phillippe Coutinho, sold to Barcelona.

The second image illustrates the chances of win, draw and defeat in the first leg of the UEFA Champions League round of 16, which will happen in the next two weeks. If you are interested in the method presented and are considering betting on soccer games, I suggest you take a look at the StrataBet website. I am not responsible for any losses of your assets, but I accept part of the profit in the form of a donation if you win something!

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/02/probUCL18Round16Leg1-300x226.png?resize=631%2C475)

For the more curious readers here is a detail of the method used.

**Assumptions:**

For this model, we will assume that the number of goals scored by a team throughout the match is decided by throwing a “die on a board”. Each team will have its own die with a different **“weight”**, this is, each die will have different odds for each number of goals. For example, the dice from better teams (like Manchester City) are more likely to land with a high value such as 4, while the dice from worse teams (like Leicester City) are more likely to land with a lower value such as 1. In sum, our main assumption is: scoring goals is a **random** process, however better teams are **more likely** to score goals.

**Methodology:**

To predict the Champions League results we will simulate the championship 50,000 times and analyze the results, this process is called Monte Carlo Simulation. When two teams face each other, we play their dice to determine the number of goals they have scored, which generates a fictional score for the game. I created a program in R (a programming language) that can simulate a complete “Dice Champions League” and takes into consideration the quality of the teams involved in each match. In the next few paragraphs I will explain some details of this simulation.

First, we need to look at the die used by an ordinary football team. If teams used conventional dice (such as that ones used in board games played during rainy day at the beach) the odds of the team making 1 goal in the game would be the same as making 2, 3, 4, 5 or 6 goals, yet we know that this is not the case. Several studies have already shown that goals follow a Poisson distribution, that is, the probability of a team making X goals is related to the average goals scored by the team.

I used information on the top European leagues and calculated the average number of goals scored by a team during a game: **1.31 goals**. Then, I applied the Poisson formula to that value to predict the probability of scoring a specific number of goals throughout the match and compared that with what actually happened in the data:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/02/poisson-1-300x219.png?resize=601%2C439)

We can see that the Poisson distribution is a good approximation of what really happens in the data. The next step is to understand the “weight” of the die used by **each team**. For this I used a measure called **expected goals**, which I calculated using the detailed material provided by StrataBet. This is a metric widely used by football analysts and is calculated according by the quality of shots and the chances created by each team. In a previous post, we saw that the gross number of goals has some inaccuracies, the number of goals expected is a more accurate measure of the quality of a team. I calculated the **expected goals-for playing home** (xGF home), **expected goals-for playing away** (xGF away), **expected goals-against playing home** (xGA home) and the **expected goals-against playing away** (visiting xGC). The expected goals data for clubs that still compete for the Champions League are summarized in this table:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/02/tableUCL18XgRoundOf16Leg1-1-300x260.png?resize=593%2C514)

It is important to emphasize that the above values were adjusted according to the quality of the opponents faced by the teams. The adjustment was made using the “Euro Club Index” which makes a ranking of the clubs in Europe. If you want to better understand how the expected goal values were used and how the adjustments were made please see the “Observations” section.

**Observations**:

1.  For each game of the simulation the program calculates the average between the home team’s **xGF** and the visiting team’s **xGA** (result 1). Furthermore, the average is also calculated between the visiting team’s **xGF** and the home team’s xGF (result 2). Result 1 is used in the Poisson formula to generate the number of goals scored by the home team and result 2 to generate the number of goals scored by the visitor.
2.  The expected goals data were adjusted according to the quality of teams faced by each club using the Euro Club Index ranking. Each tournament has a different level, so adjustments were needed. Teams that faced tougher opponents received a bonus and teams that faced easier opponents were given a deduction.
3.  It is important to note that the program replicates the format of the Champions League, ie teams face 2 times in the round of 16, 2 times in the quarterfinals, 2 times in the semis and 1 time in the final. At each stage the matches are drawn. If a tie occurs, the team with the highest number of away goals is scored. If a penalty shootout is required, the program flips a coin to decide the winner.
4.  The data used are from the main European leagues: England, Spain, Germany, France, Italy, Portugal, Switzerland and the UEFA Champions League. A STRATABET does not have data on Turkey and Ukraine, the data of team’s from those leagues (Shakhtar e Besiktas) were approximates with the ones from the Champions League.
5.  If you want to understand more about the Poisson distribution in soccer I suggest reading the first chapter of “Soccermatics” by David Sumpter.

**This article was written with the aid of StrataData, which is property of [Stratagem Technologies](http://www.stratagem.co/). StrataData powers the [StrataBet Sports Trading Platform](https://app.stratabet.com/), in addition to [StrataBet Premium Recommendations](https://stratatips.co/).**