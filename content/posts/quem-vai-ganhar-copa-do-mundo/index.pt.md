---
title: "Quem vai ganhar a Copa do Mundo"
date: 2018-06-11
draft: false
---

Copa do Mundo: Um evento esportivo, cultural, social, político, econômico e acima de tudo apaixonante. A Copa do Mundo é o grande foco do mundo do futebol no momento e é claro que o Algolritmo não poderia deixar de trazer uma perspectiva estatística e matemática desse incrível torneio que toma conta dos noticiários, nossas conversas e nossa rotina a cada 4 anos. Hoje trazemos as probabilidades de cada seleção ser campeã, apresentamos os resultados no início do post e logo em seguida uma explicação mais detalhada do modelo para aqueles que desejam se aprofundar. Em próximos posts traremos mais conteúdo, como um guia para bolão e os confrontos de mata-mata mais provável de acontecer, por isso fique ligado no blog e lembre-se de curtir nossa [página no Facebook](https://www.facebook.com/algolritmo/)!

**Resultados:**

De acordo com o modelo desenvolvido pelo Algolritmo, essas são as chances de cada seleção vencer a tão sonhada Copa do Mundo:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/06/Screen-Shot-2018-06-11-at-8.32.53-AM-275x300.png?resize=578%2C630)

Segundo nosso modelo, o principal candidato a ganhar o torneio na Rússia é o Brasil. A Seleção brasileira cresceu muito de rendimento desde a chegada do técnico Tite e desponta como um dos favoritos a buscar o a taça e conquistar o Hexa campeonato. Como esperado, as outras seleções que possuem boas chances de levar a Copa do Mundo são a Alemanha, França, Espanha, Argentina e Bélgica. É claro que existe muita imprevisibilidade em um torneio tão curto quanto a Copa, no entanto é muito improvável que algum das seleções citadas não seja campeã.

E você, qual é seu palpite para essa tão aguardada Copa? Você, assim como o Algolritmo, está confiante que o Brasil será capaz de trazer o Hexa? Na sua opinião quem são os principais adversários e possíveis obstáculos?

Se você quer entender mais detalhadamente como as probabilidades acima foram calculadas, aqui está a explicação do modelo:

**Pressupostos do Modelo:**

-   **Amistosos** tem menos importância do que jogos de competições oficiais ao analisar a capacidade de um time.
-   **Partidas recentes** são mais relevantes que aquelas que acontecerem em um passado mais distante.
-   Jogos contra **adversários mais fortes** e tradicionais são mais significativos do que jogos contra times mais fracos e sem tradição. Por exemplo, ganhar de 3 a 0 da Argentina é mais expressivo do que golear San Marino por 5 a 0.
-   Marcar gols é um processo que envolve **aleatoriedade**, no entanto times melhores tem **mais** **chances** de fazer gols. Para capturar o efeito da aleatoriedade, usaremos a distribuição Poisson, pois diversos estudos já mostraram que o número de gols feitos por um time segue esse tipo de distribuição. (Veja mais nas observações ao final do texto).
-   Vamos assumir que o número de gols feito por um time ao longo da partida em uma simulação é decidido ao jogar um “dado em um tabuleiro”. Cada time terá seu próprio dado com um **“peso”** diferente, isto é, cada dado terá probabilidades diferentes para cada número de gols. Por exemplo, o dado lançado por seleções melhores (como o Espanha) tem mais chances de cair em valores altos como 4 enquanto o dado lançado por times piores (como o Coréia do Sul) tem maior probabilidade de cair em valores como baixos como 1.

**O Modelo:**

A ideia do modelo é poder simular a Copa do Mundo de “dados de tabuleiro” **10000 vezes** e analisar quais foram os resultados mais prováveis, esse processo chama-se simulação Monte Carlo. Para definir o peso dos “dados de tabuleiro” lançados pelas seleções em cada jogo primeiro necessitamos de alguma medida da qualidade ofensiva e defensiva de cada seleção.

Geralmente, o **poder de ataque e defesa de times** de futebol pode ser simplesmente calculado e aproximado pela média de gols feitos e sofridos ao longo de um ano. No entanto, para seleções de futebol esse métrica seria bastante imprecisa pelos seguintes fatores:

-   **Seleções jogam poucas vezes** durante um ano, assim a média seria muito sensível a qualquer resultado novo.
-   Uma **boa** **parte dos jogos de seleção são amistosos**, onde o nível de competitividade é mais baixo. Além disso, nem sempre as seleções usam suas escalações mais fortes pois muitos testes são feitos.
-   Os países jogam contra **adversários muito distintos** ao longo de um ano, alguns times chegam a enfrentar diversos campeões do mundo enquanto outro jogam contra seleções com muito menos qualificadas.

Com isso em mente, **os indicadores de qualidade do ataque e da defesa** de cada seleção foram calculados utilizando os dados das partidas internacionais disputadas nos últimos 8 anos (mais especificamente desde o dia 1 de agosto de 2010) além das seguintes variáveis:

-   **Número de gols feitos** em cada jogo.
-   **Número de gols sofridos** em cada jogo.
-   **Intervalo de tempo** (em número de semestres) entre o jogo e a data de início da Copa do Mundo 2018.
-   **Tipo de partida**, isto é, se a partida era um amistoso ou parte de uma competição oficial.
-   **Dificuldade do confronto**, calculado através do Elo rating (um índice avalia a qualidade dos times).
-   **Mando do confronto**, se o time analisado jogava em casa, fora ou em campo neutro.

(Para ver mais detalhes de como esses diferentes fatores foram utilizados, veja a seção “Observações”).

Dessa forma, foi possível obter um indicador ofensivo e defensivo de cada seleção, que pode ser entendido com **versões mais precisas e ajustadas da média de gols feitos e da média de gols sofridos**. Aqui estão esses valores para cada país:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/06/Screen-Shot-2018-06-11-at-8.37.01-AM-276x300.png?resize=516%2C561)

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/06/Screen-Shot-2018-06-11-at-8.37.08-AM-278x300.png?resize=523%2C564)

É claro que é possível questionar alguns dos valores acima, que podem não parecer muito intuitivos. Acredito que o principal dele é o Irã ser o time com o melhor valor no indicador defensivo. Isso acontece, pois, o Irã realmente tem uma defesa difícil de ser vazada pela maioria dos adversários, muitas vezes conseguindo sair do resultado sem levar gol. Por mais que o modelo faça um ajuste por conta da qualidade dos países que o Irã geralmente enfrenta, a seleção Iraniana realmente tende a ter um grande ímpeto defensivo, por exemplo na copa passada o time fez um confronto duro contra a Argentina e foi derrotado apenas por conta de um gol de Messi nos acréscimos, aos 46 do segundo tempo. Vale ressaltar, que a apesar de certa consistência defensiva o time é extremamente improdutivo no ataque, a seleção iraniana tem o 4<sup>o&nbsp;</sup> pior indicador ofensivo entre aqueles que disputarão a Copa do mundo.

Para simular o número de gols feitos por um time, é necessário um parâmetro que estime a “média de gols esperados” para aquele time naquele confronto. Para cada jogo, isso é calculado com uma média entre o indicador ofensivo de um time e o indicador defensivo do outro time. Por exemplo, o parâmetro para simular o número de gols feitos pela Rússia contra a Arábia Saudita é: **(indicador ofensivo da Rússia + indicador defensivo da Arábia Saudita)/2**, os valores numéricos são **(1,47 + 1,51)/2** que resulta em **1,49**. Para obter o parâmetro necessário para simular o número de gols feitos pela Arábia Saudita nesse mesmo jogo, a fórmula seria: **(indicador ofensivo da Arábia Saudita + indicador defensivo da Rússia)/2**, numericamente **(1.19 + 0.97)/2** que resulta em **1,08**.

Uma vez que esses resultados foram calculados, escrevi um programa em R que é capaz de simular a Copa do Mundo que está por vir **10000** vezes e analisar as probabilidades de cada time vencer. Os dados dessas simulações serão utilizados em próximas postagens, então fique ligado em nosso blog!

**Observações:**

-   Para ver mais sobre a distribuição Poisson e sua relação com o número de gols feitos  está mais detalhadamente explicada [nesse post que fiz sobre a Champions League de 2017.](https://algolritmo.com/index.php/2017/02/14/prevendo-a-champions-league/)
-   A Rússia, por ser país cede, ganhou uma “bonificação” de +0.1 e -0.1 nos índices ofensivos e defensivos respectivamente
-   No cálculo dos índices ofensivos e defensivos, considerei os amistosos com o peso de 0,5x um jogo normal.
-   Para incorporar o efeito do intervalo de “tempo” entre o jogo analisado e o início da Copa do Mundo, usei um peso que diminui exponencialmente com a seguinte fórmula (utilizada de forma similar no livro _Mathletics_):![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/06/Screen-Shot-2018-06-11-at-8.53.45-AM.png?resize=173%2C49)
    1.  t = número de semestres entre o jogo e a Copa do Mundo.
    2.  w = “peso temporal” da partida
    3.  Dessa forma, jogos que aconteceram no mesmo semestre da copa tem peso 1, jogos que aconteceram um semestre antes tem peso 0.9, dois semestres antes possui peso 0.9\*0.9, e assim sucessivamente.
    4.  O valor de 0.9 é recomendado para alguns esportes no livro citado.
-   Para entender as diferenças entre times, usei o índice Elo. Esse índice traz uma fórmula que permite analisar a probabilidade de um time “não perder” um jogo dado o seu número de pontos no ranking e o número de pontos de seu adversário.
    1.  O peso de cada jogo foi (1 – probabilidade do time não perder), dessa forma os jogos mais difíceis tiveram peso maior
    2.  Caso o time jogasse em casa, foram adicionados 100 pontos em seu índice Elo.
    3.  A fórmula é a seguinte:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/06/Screen-Shot-2018-06-11-at-8.52.14-AM-300x126.png?resize=204%2C86)

1.  Ea = probabilidade do time A não perder
2.  Rb = pontos do time B no índice Elo
3.  Ra = pontos do time A no índice Elo