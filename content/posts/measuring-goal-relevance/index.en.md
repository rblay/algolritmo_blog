---
title: "Measuring Goal Relevance"
date: 2017-01-31
draft: false
---

December and January are characterized by several transfer rumors in the soccer world, notably in Brazil, where teams are currently looking to sign new players for the upcoming season. In this time of the year it is very common to see in newspapers comparative charts regarding potential signings and players available at the market. Usually, the main data analyzed in those comparisons are the number of goals, especially when the comparison involves attacking players. The raw number of goals is an interesting measure, but with some extra information it is possible to draw more relevant comparisons. Below I present 2 models which use data regarding goals scored more deeply.

**Assumptions:**

The main assumption behind both models is that goals have different levels of difficulty and relevance. For example, scoring an opener of a tight game is harder than scoring the fifth goal of a 5 x 0 blowout.

**Methodology**:

This post includes 2 different models; I will explain each methodology separately.

**1)  Marginal Points Produced by Goals Model**

This model is presented and explained in the book “The Numbers Game”, written by Chris Anderson and David Sally. The authors first analyzed the **average number of points** earned by teams that scored a specific number of goals. In other words, they used a database which included games from tournaments played in several countries and calculated the average points a team received in games they scored 1 goal, 2 goals, 3 goals etc. To illustrate, teams that scored 1 goal during the whole game earn on average 1.13 points while teams that score 2 goals earned on average 2.12 pointes (Further down this text there is a table which sums up these values). I did the same calculations using data from the latest 2016 Brazilian national league (Brasileirão) and I compared the values.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/graph-300x154.png?resize=640%2C329)

Através do gráfico, é possível ver que os dados do Brasileirão são bem próximo daqueles calculados por Anderson e Sally. Além disso a figura comprova algo bem intuitivo: fazer mais gols gera mais pontos na média. Usarei os dados do livro para as análises, uma vez que os valores foram calculados utilizando um número maior de jogos. O próximo passo é entender os **pontos marginais de cada gol**, isto é, o quantos pontos o gol X adiciona em relação ao gol X-1. A tabela abaixo resume estes valores e será usada como referência:

Using the graph, it is possible to see that the values obtained with the Brasileirão data are very close to those calculated by Anderson and Sally. Moreover, the figure proves something very intuitive: scoring more goals ensures more points on average. Since the values presented in “The Numbers Game” were calculated with a greater amount of data, I will those numbers for further analysis. The next step is to understand the **marginal points produced by each goal**, this is, how many points goal X adds compared to goal X-1. The table below summarizes those values and will be used as reference:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/bookValues-300x96.png?resize=628%2C201)

With those values, we can now calculate how the marginal points earned by each player per goal during the tournament. For example, if player X scores the first and second goals of his team in a match, his goals are worth 0.85 + 0.99, this is, 1.84 **marginal points.** If another player Y scores the third and fourth in that same match, his goals are worth 0.55 + 0.23, this is, 0.78 **marginal points.** Both players scored 2 goals, however the goals scored by player X ensured more points to the team, therefore are worth more.

**2) Relevant Goals Model**

In the above model, it is possible to see that generally the initial goals scored in a match are the most important ones, yet, that is not always the case. Imagine a striker who scores a goal at the end of a match that was tied 3 x 3, this goals has an enormous impact, however it would only count as 0.23 marginal points for the team. With that in mind, I created a metric that is called **relevant goals**. The idea is very straightforward, relevant goals are the ones that change the “status” of a match, this is, if before the goal was scored the team was losing and with the goal the team equalized it was a relevant goal (the same goes to goals in which the team takes the lead). In short, relevant goals are the one that change the momentary result of a match.

To illustrate and make things clearer, imagine an match between ficticious teams A and B. Team A scores the opener, this goal is considered relevant (1 x 0). Team B quickly equalizes (1 x 1), this goal is also considered relevant. Team B scores another goal and takes the lead (1 x 2), this is also a relevant goal. In the beginning of the second half team B scores another goal (1 x 3), this is not a relevant goal since it did not change the current result of the match, team B is still winning. Team A scores a goal at the end of the match (2 x 3), this goal is not relevant. In my model, only relevant goals are accounted for, therefore, in the fictitious match above only team A’s first goal and team B’s first would goals would be included.

**Results:**

With the metrics described above I produced 2 new player rankings, and compared them to the traditional top scorers list:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/comparativeImage-300x232.png?resize=640%2C495)

It is possible to see that many names are present in all three lists, but their rankings vary. All of them are interesting and talented players, however it is important to understand some of their differences. A good illustration of those differences is a comparison between Sassá (who plays for Botafogo) and Marinho (who plays for Vitória), both players ended up tied with 12 goals in the conventional top scorers list.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/marinhoVSsassa-300x238.png?resize=571%2C453)

Sassá scored 7 relevant goals and produced 10.32 marginal points, while Marinho scored 11 relevant goals and produced 9.7 marginal points. It is possible to say that in this tournament Sassá’s goals mostly helped enlarge Botafogo’s wins, since many of his goals changed to score to 2 x 0 or 3 x 0. On the other hand, most of Marinho’s goals changed the perspective of matches for Vitória and were essential in keeping the team in the first division. Therefore, both players had an important role in guaranteeing points for their teams, yet Marinho’s goals happened at tighter moments of the game.

The number of goals will always be an important criterion to evaluate attacking player’s performance, yet, with some extra information and criterion it is possible to measure goal relevance and enrich the evaluation.

**Observations:**

1.  It is good to emphasize that this model is meaningful to attacking players, specially strikers. In a future post, I plan on doing a similar analysis with assists, which in theory would be more meaningful to midfielders.
2.  If you want to understand more about the “Marginal Points Produced by Goals Model” I suggest reading “The Numbers Game”