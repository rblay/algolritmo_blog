---
title: "The Best Goalkeepers in the 2018 Brazilian League"
date: 2018-12-21
draft: false
---

Amid the break on the Brazilian soccer calendar, Algolritmo will provide you texts about the Brazil’s top leagues, the Série A and the Série B. In this first text, we bring a statistical analysis on the goalkeepers of the Brazil’s Série A. Usually, fans and pundits tend to evaluate goalkeepers with simple numbers, such as: goals conceded, clean sheets or difficult saves (which has an inherent degree of subjectivity). Today, Algolritmo will show another way to understand the effectiveness of goalkeepers, combining the saves made with the quality of shots faced. This text is inspired in European goalkeeper analyzes made by the company Statsbomb.

The data used in this analysis is provided by Instat, if you are interested in the products of the company contact them through [this form](https://form.jotformeu.com/80462843333354).

#### Results:

We calculated the effectiveness of goalkeepers through the “percentage of saves above expected”, abbreviated to **%SAE**. Briefly, this metric indicates how a goalkeeper performed in relation to what is expected of an “average goalkeeper”. The goalkeepers who stood out with this statistic were these:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/02/imagensGoleiros_en.png?resize=640%2C885)

Analyzing statistically, the best goalkeeper of the tournament would be Santos, goalkeeper of Athlético Paranaense (usually abbreviated to CAP in Brazil). Santos performed very well on the tournament and had a major role in CAP’s comeback during the second half of the season. The goalkeeper of the club from Paraná ended the year extremely valued and increasingly consolidated as a relevant name in Brazilian football.

Another goalkeeper who stood out in the tournament was Maílson, from Sport. The goalkeeper will likely by remembered for scoring a ridiculous own goal unbelievable in a game against Vitória (you can see it [here](https://www.youtube.com/watch?v=A3Q2xpVDBnA)), but still, the goalkeeper had overall very good performances, especially against Chapecoense and São Paulo. Maílson played in 13 games, and had a good sequence of games in the starting eleven after the usual starter, Magrão, got injured. It is interesting to note that Maílson managed to stand out positively even with his team being relegated, indicating that most of the goals he suffered were most likely not directly his fault. Perhaps if Maílson had played more games, and if the Sport’s defense had better performances, the Pernambuco club might not have been relegated after 5 years at the top division.

The third highlight is Diego Alves, Flamengo’s shot stopper. The goalkeeper came from Valencia last year to be the starter of Rio de Janeiro club, and had a lot of success until getting injured and having personal problems with new coach Dorival Júnior. Until then, Diego was the guaranteed name in the starting eleven, with very solid performances and few mistakes. The goalkeeper has an indefinite situation in Flamengo and would be a great signing for clubs looking for goalkeepers.

#### Model Assumptions:

-   Shots differ in quality; you cannot consider that all shots on target involve the same level of difficulty for the keeper.
-   Goalkeepers should be evaluated according to the quality of shots faced. If not, we might end up “harming” good goalkeeper’s numbers if they don’t have effective defenders preventing chances for the opposing teams.
-   Even though nowadays goalkeepers serve several functions (such as beginning offensive transitions and playing with their feet) we will compare goalkeepers according their most crucial function: making saves.

#### Acronym Glossary:

-   **%CS**: Percentage of chances saved
-   **%xSE**: Percentage saves expected
-   **GSAE**: Goals saved above expected
-   **xGSOT**: Expected goals from shots on target
-   **%SAE**: Percentage of saves above expected

#### Methodology:

The modern goalkeeper is charge of several functions, but today we will focus on his main responsibility: stopping shots from the opposition. Generally, goalkeepers are evaluated according to the number of goals conceded, games without conceding goals and number of difficult saves. These values, while useful, may be biased by some factors. For example, a very solid defense can help a middle goalkeeper have good numbers by preventing the other team from having too many shots.

Firstly, to eliminate some of the influence of factors external to the goalkeeper, we will look at the percentage of chances saved by each goalkeeper (**%CS**). Using Instat’s data, we observe the number of shots that went towards each goalkeeper and count how many were saved. The **%CS** formula is very simple: shots saved/shots faced. Below is a table with **%CS** values for all goalkeepers of the Brazilian Série A 2018 who played at least 10 games:

With this table, it is possible which keepers are the ones players had a lowest chance of scoring on during the Brasileirão 2018. Santos, Athlético Paranaense, has the best **%CS** with 87.94% (i.e.  to score a goal on Santos it was necessary to shoot a little over 8 times on target). The **%CS** brings us a bit more information on the performance of a goalkeeper, however there is still another aspect to be taken into account: the quality of the shots faced.

Throughout a tournament, goalkeepers need to make saves of different difficulties. Some saves are considered “miraculous” because they are close to certain goals, while other saves are extremely simple and routine. To incorporate the “save difficulty” factor in this analysis, we used a small variation of the expected goals model, which has already been explained in other posts, see this link if you want more details.

In other posts, in which “expected goals” are analyzed, we use all shots (including the ones blocked or out of target) to understand a team’s offensive and defensive strength. For this analysis of goalkeepers, we use a similar model, however considering **only the shots that went on target** because these are the situations in which the goalkeeper’s interference is crucial. The metric used, therefore, is the “expected goals from shots on target”, which I will abbreviate to **xGSOT**. Thus, all shots on target are given a value between 0 and 1, which represents the probability of that shot resulting in a goal. The closer the value is to 1 the more likely it is that the chance would be a goal.

With **xGSOT** we can understand the performance of goalkeepers from another perspective. Adding the **xGSOT** of all the shots faced by each goalkeeper we calculate the “expected goals conceded” for that every single goalkeeper. In other words, we analyzed all the shots that went towards the target and we observe the number of goals an “average goalkeeper” would conceded. After that, we can compare the expected number of expected goals conceded with the number of goals conceded in reality. The difference between the two numbers (expected goals conceded – goals conceded in reality) generates a metric that show how many goals each goalkeeper managed to avoid or allow compared to an average goalkeeper. We call this metric “goals saved above expected,” abbreviated to **GSAE**. Below is a table with these values:

Again, goalkeeper Santos (from CAP) stands out. Given the shots his opponents had on target, he was expected to concede about 15 more goals than he actually did (his **GSAE** score was 15.19 goals). Other goalkeepers who stood out positively were Cássio (of Corinthians) with **GSAE** of 7.1 goals, and Éverson (of Ceará) with **GSAE** of 6.29 goals. On the other hand, some goalkeepers scored negatively, allowing more goals than expected. Among the names that have been subpar in the 2018 Brasileirão are Jandrei (from Chapecoense) with **GSAE** of -12.12 goals, Magrão (from Sport) with **GSAE** of -8.12 goals, and Ronaldo (from Vitória) with **GSAE** of -5.15 goals.

As we can see, the metrics above (**%CS** and **GSAE**) show more information about the individual goalkeeper performance, eliminating some subjective elements. However, to better compare the goalkeepers it is necessary to make a final small adjustment in those metrics. The goalkeepers have faced different quantities of shots, and this needs to be considered. The formulas of this adjustment are explained in the comments at the end of the text, but the important thing is to know that a third metric is generated, which is the percentage of saves above expected, abbreviated to (**%SAE**). This allows us to better compare the goalkeeper performances accounting for the fact that they faced a varied number of shots and with different average quality. Here are the **%SAE** values for the goalkeepers of the Brasileirão Série A 2018:

The metric above allows us to analyze the goalkeepers in more depth. It is clear that many goalkeepers have had excellent performances throughout the tournament but it is clear that those who had the greatest positive impact on their teams were Santos (Athlético Paranaense), Maílson (Sport) and Diego Alves (Flamengo). Goalkeeper of Athlético Paranaense, made 10.89% more defenses than was expected of an average goalkeeper, while the Sport’s shot stopper made 7.62% more and the Flamengo player made 7.18% more. At the same time, Jandrei (Sport), Ronaldo (Vitória) and Magrão (Sport) performed below expectations. It is interesting to note that the Sport, which was relegated, had simultaneously one of the best and one of the worst goalkeepers of the championship. Magrão is club legend, but Sport’s performance greatly improved when Maílson, 22 years old, took over the spot on the starting squad (after Magrão suffered a broken arm). In 2019 it would be interesting to give more opportunities to the young goalkeeper.

With this type of analysis, clubs can make better decisions by signing new goalkeepers (or renewing their contracts) for upcoming seasons. With more intelligence involved in the hiring process, teams can become more competitive and better manage their budget.

#### Observations:

1.  If you are interested in Instat’s data fill out [this form](https://form.jotformeu.com/80462843333354) to get in touch with the company
2.  This analysis of goalkeepers was inspired by an analysis done by the excellent site Statsbomb, regarding the goalkeepers of Europe. Here is the [link](https://statsbomb.com/).
3.  The data used to calculate the **xGSOT** were 60% of the data of the 2017 and 2018 Brasileirão Série A, in addition to the data of 2018 Brasileirão Série B.
4.  In this analysis penalties and own goals were not included.
5.  To make the adjustment that generated the **%SAE**, first let’s calculate what the percentage of saves expected for each goalkeeper, abbreviated to **%xSE** would be. This value was calculated as follows: (shots on target – **xGSOT**)/shots on target. Then, to calculate the **%SAE** we simply make the following count: (**%CS** –**%xSE**).