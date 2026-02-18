---
title: "Predicting the Champions League"
date: 2017-02-14
draft: false
---

Last week, I received the great news that I was selected by StrataBet (a sports betting website) to receive extremely detailed material on European soccer leagues. Using this data along with some Computer Science knowledge I prepared a simulation of the UEFA Champions League, which begins its knockout phase today.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/confrontos-1-300x169.jpg?resize=640%2C360)

**Assumptions:**

For this model, we will assume that the number of goals scored by a team throughout the match is decided by throwing a “die on a board”. Each team will have its own die with a different **“weight”**, this is, each die will have different odds for each number of goals. For example, the dice from better teams (like Barcelona) are more likely to land with a high value such as 4, while the dice from worse teams (like Leicester City) are more likely to land with a lower value such as 1. In sum, our main assumption is: scoring goals is a **random** process, however better teams are **more likely** to score goals.

**Methodology:**

To predict the Champions League results we will simulate the championship 20,000 times and analyze the results, this process is called Monte Carlo Simulation. When two teams face each other, we play their dice to determine the number of goals they have scored, which generates a fictional score for the game. I created a program in R (a programming language) that can simulate a complete “Dice Champions League” and takes into consideration the quality of the teams involved in each match. In the next few paragraphs I will explain some details of this simulation.

First, we need to look at the die used by an ordinary football team. If teams used conventional dice (such as that ones used in board games played during rainy day at the beach) the odds of the team making 1 goal in the game would be the same as making 2, 3, 4, 5 or 6 goals, yet we know that this is not the case. Several studies have already shown that goals follow a Poisson distribution, that is, the probability of a team making X goals is related to the average goals scored by the team.

I used information on the top European leagues and calculated the average number of goals scored by a team during a game: **1.31 goals**. Then, I applied the Poisson formula to that value to predict the probability of scoring a specific number of goals throughout the match and compared that with what actually happened in the data:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/poisson-1-300x219.png?resize=627%2C458)

We can see that the Poisson distribution is a good approximation of what actually happens in the data. The next step is to understand the “weight” of the die used by **each team**. For this I used a measure called **expected goals**, which I calculated using the detailed material provided by StrataBet. This is a metric widely used by football analysts and is calculated according by the quality of shots and the chances created by each team (I plan on going into more detail about expected goals in a future text). In the previous post, we saw that the gross number of goals has some inaccuracies, the number of goals expected is a more accurate measure of the quality of a team. I calculated the **expected goals-for playing home** (xGF home), **expected goals-for playing away** (xGF away), **expected goals-against playing home** (xGA home) and the **expected goals-against playing away** (visiting xGC). The expected goals data for clubs that still compete for the Champions League are summarized in this table:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/tabXG-1-300x234.png?resize=640%2C499)

It is important to emphasize that the above values were adjusted according to the quality of the opponents faced by the teams. The adjustment was made using the “Euro Club Index” which makes a ranking of the clubs in Europe. If you want to better understand how the expected goal values were used and how the adjustments were made please see the “Observations” section.

**Results:**

After the 20,000 simulations, the program counted the number of times each team won the simulated Champions League, these values are presented in the following. The size of the badge of each club is proportional to the number of times the team was champion:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/tabChampsOficial-230x300.png?resize=640%2C835)

The result are close to what was expected, Europe’s most powerful teams like Barcelona, Real Madrid and Bayern Munich are among the most likely to win the competition. However, the fact that the competition is a knockout allows smaller teams to make historic campaigns and beat the favorites. This is unlikely to happen, but in about 3% of the 20,000 simulations teams like Bayern Leverkusen and Leicester City won the most coveted tournament in Europe.

In case you are interested in the model and are thinking about betting on soccer games, I suggest you look at the StrataBet website. To help those interested, I’ve separated the simulation of only the first legs of the Round-of 16 games, which will happen in the next two weeks. Below are the probabilities of each outcome:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/oitavas-1-300x236.png?resize=640%2C504)

I don’t take responsibility for any losses of your assets, but I accept part of the profit in the form of a donation if you win something!

**Observations:**

1.  For each game of the simulation the program calculates the average between the home team’s xGF and the visiting team’s xGA (result 1). Furthermore, the average is also calculated between the visiting team’s xGF and the home team’s xGF (result 2). Result 1 is used in the Poisson formula to generate the number of goals scored by the home team and result 2 to generate the number of goals scored by the visitor.
2.  The expected goals data were adjusted according to the quality of teams faced by each club using the Euro Club Index ranking. Each tournament has a different level, so adjustments were needed. Teams that faced tougher opponents received a bonus and teams that faced easier opponents were given a deduction.
3.  It is important to note that the program replicates the format of the Champions League, ie teams face 2 times in the round of 16, 2 times in the quarterfinals, 2 times in the semis and 1 time in the final. At each stage the matches are drawn. If a tie occurs, the team with the highest number of away goals is scored. If a penalty shootout is required, the program flips a coin to decide the winner.
4.  The data used are from the main European leagues: England, Spain, Germany, France, Italy, Portugal and the UEFA Champions League.
5.  If you want to understand more about the Poisson distribution in soccer I suggest reading the first chapter of “Soccermatics” by David Sumpter.

**This article was written with the aid of StrataData, which is property of [Stratagem](http://www.stratagem.co/) Technologies. StrataData powers the [StrataBet Sports Trading Platform](http://www.stratabet.com/), in addition to [StrataBet Premium Recommendations](http://app.stratabet.com/recommendations).**