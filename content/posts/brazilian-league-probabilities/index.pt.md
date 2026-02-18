---
title: "Probabilidades no Brasileirão"
date: 2017-10-21
draft: false
---

Utilizando os ótimos dados que recebo semanalmente STRATABET juntamente com alguns conhecimentos de computação preparei uma simulação da Brasileirão 2017, que está em sua reta final. Abaixo estão as probabilidades de ganhar o campeonato, se classificar para a libertadores e ser rebaixado. Se você tem curiosidade de saber como matemáticos e estatísticos calculam esses valores recomendo ler o texto inteiro.

**Resultados:**

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/campeoes-210x300.png?resize=366%2C523)

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/libertadores-159x300.png?resize=367%2C692)

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/rebaixamento-179x300.png?resize=369%2C618)

Caso queira entender o modelo usado abaixo estão os detalhes:

**Pressupostos:**

Para esse modelo vamos assumir que o número de gols feito por um time ao longo da partida é decidido ao jogar um “dado em um tabuleiro”. Cada time terá seu próprio dado com um **“peso”** diferente, isto é, cada dado terá probabilidades diferentes para cada número de gols. Por exemplo, o dado lançado por times **melhores** tem mais chances de cair em valores altos como 4 enquanto o dado lançado por times **piores** tem maior probabilidade de cair em valores como baixos como 1. Resumidamente, o principal pressuposto é: marcar gols é um processo **aleatório**, no entanto times melhores tem **mais** **chances** de fazer gols.

**Metodologia:**

Para prever os resultados do Brasileirão vamos simular o campeonato 10.000 vezes e analisar os resultados, esse processo se chama Simulação de Monte Carlo. Quando dois times se enfrentam jogamos seus dados para determinar o número de gols feitos, assim geramos um placar fictício para a partida. Criei um programa em R (uma linguagem de programação) que é capaz de simular um Campeonato Brasileiro de “dados de tabuleiro” levando em consideração a qualidade dos times envolvidos no confronto. Simulei apenas os jogos que ainda não aconteceram, ou seja, a partir da 30<sup>a</sup> rodada. Nos próximos parágrafos explicarei um pouco melhor alguns detalhes dessa simulação.

Primeiramente, precisamos analisar o “dado de tabuleiro” utilizado por um time de futebol comum. Se os times utilizassem os “dados tradicionais” (como aquele de banco imobiliário que você joga em um dia chuvoso na praia) a probabilidade do time fazer 1 gol no jogo seria a mesma de fazer 2, 3, 4, 5 ou 6 gols, no entanto sabemos que esse não é o caso. Diversos estudos já mostraram que gols seguem uma distribuição Poisson, isto é, a probabilidade de um time fazer X gols está relacionado com a média de gols feitos pelo time.

Utilizei as informações sobre o Campeonato Brasileiro e calculei a média de gols feitos por um time durante uma partida: **1,17 gols por jogo**. Com esse valor apliquei a fórmula de Poisson para prever a probabilidade de se marcar um número específico de gols ao longo da partida e comparei com o que de fato aconteceu:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/poisson-300x225.png?resize=640%2C480)

Podemos ver que a distribuição Poisson é uma boa aproximação do que acontece de fato. O próximo passo é entender o “peso” do “dado de tabuleiro” de **cada time**. Para isso utilizei uma medida chamada **gols esperados**, abreviado para **xG,** que calculei com o material detalhado fornecido pela StrataBet. Essa é uma métrica bastante usada por analistas de futebol e é calculada através da qualidade dos chutes e das chances criadas por cada time (já utilizei essa métrica em outros textos do blog). Basicamente, essa métrica atribui um valor entre 0 e 1 para cada finalização do time de acordo com probabilidade daquela bola entrar no gol. Por exemplo, uma finalização de fora da área com a perna ruim (**finalização 1**) tem menos chance de resultar em gol comparada a uma finalização na pequena área sem goleiro (**finalização 2**), portanto a finalização 1 tem um **xG** menor que a finalização 2.

Em posts passados vimos que o número bruto de gols possui algumas imprecisões, o número de **gols esperados** é uma medida mais precisa da qualidade de um time. Calculei as médias de **gols pró esperados como mandante** (xGP mandante), **gols pró como visitante** (xGP visitante), **gols contra esperados como mandante** (xGC mandante) e **gols contra esperados como visitante** (xGC visitante). Esses valores para os clubes que disputam o Campeonato Brasileiro estão resumidos nessa tabela:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/10/tabelaXg-1-280x300.png?resize=640%2C685)

Feitas as 10.000 simulações, o programa contou o número de vezes que cada time foi campeão, se classificou para libertadores ou foi rebaixado em nosso Brasileirão simulado, esses valores estão apresentados nos gráficos apresentados no início do texto.

**Observações:**

1.  Para cada jogo da simulação o programa calcula a média entre **xGP** **mandante** de um time com o **xGC** **visitante** do outro time (resultado 1). Além disso tambem é calculada a média entre o **xGP** **visitante** e o **xGC** **mandante** (resultado 2). O resultado 1 é usado na formula de Poisson para definir o número de gols do mandante e o resultado 2 para definir o número de gols do visitante.
2.  Caso você queira entender mais sobre a distribuição Poisson no futebol sugiro a leitura do primeiro capítulo de “Soccermatics” de David Sumpter.

**Esse artigo foi escrito com a ajuda de StrataData, que é propriedade de [Stratagem Technologies](http://www.stratagem.co/). StrataData alimenta o [StrataBet Sports Trading Platform](https://www.stratabet.com/), e também o [StrataBet Premium Recommendations](https://app.stratabet.com/recommendations).**