---
title: "Tite vs Dunga"
date: 2017-03-18
draft: false
---

This upcoming week the South America World Cup Qualifiers returns with a big match between Brazil and Uruguay. The Brazilian team comes motivated by 6-game winning streak in the competition, and most of the team’s recent success is credited to its new coach, Tite. Almost every media outlet claims that, under the new management, the team has become more confident and cheerful, especially when compared to the games in which Dunga was the head coach. I agree largely to this subjective analysis, but I believe that with some data it is possible to better understand Brazil’s performance with Tite.

**Assumptions:**

It is possible to measure and evaluate the differences between Tite’s and Dunga’s teams with quantitative analyzes. One of the most interesting metrics for doing this type of assessment is **expected goals** (abbreviated to **xG**).

**Methodology:**

Expected goals is a measurement that has gained a lot of popularity among different football analysts. Basically, this metric assigns a value between 0 and 1 for each shot according to the probability of that attempt being scored. For example, a shot from outside the box with the weak foot (**shot 1**) is less likely to result in a goal compared to a shot inside the small box with an open net (**shot 2**), therefore shot 1 has a lower expected goal value than shot 2. With xG we can better understand the quality of the chances created and conceded by each team throughout the match.

I watched all the shots attempted by Brazil and its opponents during the World Cup Qualifiers and I used the website [quasegol.com.br](http://quasegol.com.br/) (created by journalist Gustavo Fogaça) to get the xG of each chance. There were 6 games under Dunga (3 home and 3 away) and 6 games in the Tite era (3 home and 3 away). Below you see an example of a shot computed in _Quase Gol_:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/03/Screen-Shot-2017-03-17-at-3.04.34-PM-1-300x108.png?resize=608%2C219)

**Results:**

Using this data, I created two charts to compare the performances of Tite and Dunga. In the first it is possible to analyze the number of shots attempted by Brazil and the expected goals for each game of the WC Qualifiers:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/03/Screen-Shot-2017-03-17-at-11.05.31-PM-300x252.png?resize=607%2C510)

There is not a very clear difference between Tite’s and Dunga’s teams in terms of attacking. Overall Tite’s team creates **more chances** and is **expected to score more goals**, but the offensive performance of Dunga’s team is not as inferior to Tite’s as many imagine. It is almost natural that any team with players like Neymar, Philippe Coutinho, Gabriel Jesus, Douglas Costa and Willian will create several good chances throughout any given match.

The second chart shows the chances Brazil’s opponents had and their expected value of goals conceded for each game of the WC Qualifiers, here the differences start to become clearer:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/03/Screen-Shot-2017-03-17-at-11.07.42-PM-300x259.png?resize=600%2C518)

The distribution of the points in this chart is very interesting, we can clearly group the games according to who was the coach at the occasion. Tite’s team tend to not only allow **fewer** **shots** but also **shots with smaller xG** on average. Despite the small number of games played, the improvement in defensive behavior under Tite seems to be very relevant. The new coach consolidated the 4-1-4-1 formation (initially implemented by Dunga) with players like Marcelo, Renato Augusto, Casemiro and Fernandinho (who became a regular starter after the Real Madrid’s midfielder injury).

The following is a summary of the comparison between the managers:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/03/Screen-Shot-2017-03-17-at-11.01.12-PM-273x300.png?resize=532%2C584)

I admit that at first I believed that Tite’s success would be due to a great offensive efficiency, especially with the arrival of Gabriel Jesus and Philippe Coutinho in the starting XI, however the defensive efficiency seems to be the key to Brazil’s recent accomplishments. During the defensive moments of the game, the team narrows the spaces and reduces the options for the opposing team’s attack. The opponent ends up being forced to attempt shots with little probability of scoring.

Obviously, it is not possible to make conclusions with a huge degree of certainty after only 6 matches, however it is possible to say that Brazil’s perspective is very exciting. Let’s see how the team deals with the next big challenge in Montevideo. 

**Observations:**

1.  As I said in the text I used [www.quasegol.com.br](http://quasegol.com.br/), a tool created by Guffo (Gustavo Fogaça) to calculate the xG of each shot. It is a new tool that tends to get more and more accurate over time. Therefore, I normalized the values by adopting the value of **0.75** as a maximum.