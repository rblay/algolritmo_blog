---
title: "Brazilian League Probabilities"
date: 2017-10-21
draft: false
---

Using the great data from STRATABET that I receive weekly along with some Computer Science knowledge I prepared a simulation of the Brazilian League (also known as the Brasileirão), which is already 29 weeks in. Below are the probabilities of winning the championship, qualifying to the Copa Liber adores and being relegated. If you are curious to know how mathematicians and statisticians calculate those odd, I suggest you read the whole text.

**Results:**

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/champion-208x300.png?resize=442%2C637)

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/libertadores-2-158x300.png?resize=440%2C835)

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/relegation-179x300.png?resize=430%2C721)

In case you want to understand the model, here are the details:

**Assumptions:**

For this model, we will assume that the number of goals scored by a team throughout the match is decided by throwing a “die on a board”. Each team will have its own die with a different **“weight”**, this is, each die will have different odds for each number of goals. For example, the dice from better teams (like Barcelona) are more likely to land with a high value such as 4, while the dice from worse teams (like Leicester City) are more likely to land with a lower value such as 1. In sum, our main assumption is: scoring goals is a **random** process, however better teams are **more likely** to score goals.

**Methodology:**

To predict the Brasileirão results we will simulate the championship 10,000 times and analyze the results, this process is called Monte Carlo Simulation. When two teams face each other, we play their dice to determine the number of goals they have scored, which generates a fictional score for the game. I created a program in R (a programming language) that can simulate a complete “Dice Brazilian League” and takes into consideration the quality of the teams involved in each match. In the next few paragraphs I will explain some details of this simulation.

First, we need to look at the die used by an ordinary football team. If teams used conventional dice (such as that ones used in board games played during rainy day at the beach) the odds of the team making 1 goal in the game would be the same as making 2, 3, 4, 5 or 6 goals, yet we know that this is not the case. Several studies have already shown that goals follow a Poisson distribution, that is, the probability of a team making X goals is related to the average goals scored by the team.

I used information on the Brazilian League and calculated the average number of goals scored by a team during a game: **1.17 goals/match**. Then, I applied the Poisson formula to that value to predict the probability of scoring a specific number of goals throughout the match and compared that with what actually happened in the data:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/poissonGraph-300x217.png?resize=640%2C463)

We can see that the Poisson distribution is a good approximation of what actually happens in the data. The next step is to understand the “weight” of the die used by **each team**. For this I used a measure called **expected goals**, which I calculated using the detailed material provided by StrataBet. This is a metric widely used by football analysts and is calculated according by the quality of shots and the chances created by each team (I plan on going into more detail about expected goals in a future text).

In previous posts, we saw that the gross number of goals has some inaccuracies, the number of goals expected is a more accurate measure of the quality of a team. I calculated the **expected goals-for playing home** (xGF home), **expected goals-for playing away** (xGF away), **expected goals-against playing home** (xGA home) and the **expected goals-against playing away** (visiting xGC). The expected goals data for clubs that participate in the Brazilian League are summarized in this table:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/tableXg-278x300.png?resize=635%2C685)

After the 10,000 simulations, the program counted the number of times each team won the simulated Brazilian League, qualified to the Libertadores or was relegated, those values are presented in the chart at the beginning of the text

**Observations**:

1.  For each game of the simulation the program calculates the average between the home team’s xGF and the visiting team’s xGA (result 1). Furthermore, the average is also calculated between the visiting team’s xGF and the home team’s xGF (result 2). Result 1 is used in the Poisson formula to generate the number of goals scored by the home team and result 2 to generate the number of goals scored by the visitor.
2.  If you want to understand more about the Poisson distribution in soccer I suggest reading the first chapter of “Soccermatics” by David Sumpter.

**This article was written with the aid of StrataData, which is property of [Stratagem](http://www.stratagem.co/) Technologies. StrataData powers the [StrataBet Sports Trading Platform](http://www.stratabet.com/), in addition to [StrataBet Premium Recommendations](http://app.stratabet.com/recommendations).**