---
title: "Prevendo a Champions League"
date: 2017-02-14
draft: false
---

No começo da semana passada, recebi a grata notícia de que fui selecionado pela StrataBet (um site de apostas de esporte) para receber um material extremamente detalhado sobre ligas europeias de futebol. Utilizando esses dados juntamente com alguns conhecimentos de computação preparei uma simulação da UEFA Champions League, que começa sua fase mata-mata hoje.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/confrontos-300x169.jpg?resize=595%2C335)

**Pressupostos:**

Para esse modelo vamos assumir que o número de gols feito por um time ao longo da partida é decidido ao jogar um “dado em um tabuleiro”. Cada time terá seu próprio dado com um **“peso”** diferente, isto é, cada dado terá probabilidades diferentes para cada número de gols. Por exemplo, o dado lançado por times melhores (como o Barcelona) tem mais chances de cair em valores altos como 4, enquanto o dado lançado por times piores (como o Leicester City) tem maior probabilidade de cair em valores baixos como 1. Resumidamente, o principal pressuposto é que marcar gols é um processo **aleatório**, no entanto times melhores tem **mais** **chances** de fazer gols.

**Metodologia:**

Para prever os resultados da Champions League vamos simular o campeonato 20.000 vezes e analisar os resultados, esse processo se chama Simulação de Monte Carlo. Quando dois times se enfrentam jogamos seus dados para determinar o número de gols feitos, assim geramos um placar fictício para a partida. Criei um programa em R (uma linguagem de programação) que é capaz de simular uma Champions League de “dados de tabuleiro” levando em consideração a qualidade dos times envolvidos no confronto. Nos próximos parágrafos explicarei um pouco melhor alguns detalhes dessa simulação.

Primeiramente, precisamos analisar o “dado de tabuleiro” utilizado por um time de futebol genérico. Se os times utilizassem os “dados tradicionais” (como aquele de banco imobiliário que você joga em um dia chuvoso na praia) a probabilidade do time fazer 1 gol no jogo seria a mesma de fazer 2, 3, 4, 5 ou 6 gols, no entanto sabemos que esse não é o caso. Diversos estudos já mostraram que gols seguem uma distribuição Poisson, isto é, a probabilidade de um time fazer X gols está relacionado com a média de gols feitos pelo time.

Utilizei as informações sobre as principais ligas Europeias e calculei a média de gols feitos por um time durante uma partida: **1,31 gols**. Com esse valor apliquei a fórmula de Poisson para prever a probabilidade de se marcar um número específico de gols ao longo da partida e comparei com o que de fato aconteceu:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/poisson-300x224.png?resize=607%2C454)

Podemos ver que a distribuição Poisson é uma boa aproximação do que acontece de fato. O próximo passo é entender o “peso” do “dado de tabuleiro” de **cada time**. Para isso utilizei uma medida chamada **gols esperados** que calculei com o material detalhado fornecido pela StrataBet. Essa é uma métrica bastante usada por analistas de futebol e é calculada através da qualidade dos chutes e das chances criadas por cada time (em um outro post pretendo entrar em mais detalhes sobre como a medida é feita). No último [post](https://algolritmo.com/index.php/2017/01/31/measuring-goal-relevance/) vimos que o número bruto de gols possui algumas imprecisões, o número de **gols esperados** é uma medida mais precisa da qualidade de um time. Calculei as médias de **gols pró esperados como mandante** (xGP mandante), **gols pró como visitante** (xGP visitante), **gols contra esperados como mandante** (xGC mandante) e **gols contra esperados como visitante** (xGC visitante). Esses valores para os clubes que ainda disputam a Champions League estão resumidos nessa tabela:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/tabXG-300x236.png?resize=607%2C477)

É importante ressaltar que os valores acima foram ajustados de acordo com a qualidade dos adversários enfrentados pelos times. O ajuste foi feito utilizando o “Euro Club Index” que faz um ranking dos clubes na Europa. Se você quer entender melhor como os valores de **gols esperados** foram usados no modelo e como os ajustes foram feitos por favor veja a seção “Observações”.

**Resultados:**

Feitas as 20.000 simulações, o programa contou o número de vezes que cada time foi campeão em nossa Champions League simulada, esses valores estão apresentados no gráfico a seguir (em porcentagens). O tamanho do distintivo de cada clube é proporcional ao número de vezes que o time foi campeão após a simulação:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/campeoes-232x300.png?resize=573%2C741)

O Resultado é bem próximo do esperado, os times mais poderosos da Europa como Barcelona, Real Madrid e Bayern de Munique aparecem entre os mais prováveis para vencer a competição. Porém, o fato da competição ser mata-mata permite que times menores façam campanhas históricas e desbanquem favoritos. É improvável que isso aconteça, mas em cerca de 3% das 20.000 simulações times como o Bayern Leverkusen e o Leicester City venceram o torneio mais cobiçado da Europa.

Caso você tenha se interessado pelo método e esteja pensando em apostar em jogos de futebol, sugiro dar uma olhada no site da StrataBet. Para ajudar os interessados, separei a simulação apenas dos primeiros jogos das oitavas de final, que acontecem nas próximas duas semanas. Abaixo estão as probabilidades de cada resultado:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/02/oitavas-300x230.png?resize=640%2C490)

Não me responsabilizo por eventuais perdas de seu patrimônio, mas aceito parte do lucro em forma de doação caso você ganhe algo!

**Observações:**

1.  Para cada jogo da simulação o programa calcula a média entre **xGP** **mandante** de um time com o **xGC** **visitante** do outro time (resultado 1). Além disso tambem é calculada a média entre o **xGP** **visitante** e o **xGC** **mandante** (resultado 2). O resultado 1 é usado na formula de Poisson para definir o número de gols do mandante e o resultado 2 para definir o número de gols do visitante.
2.  Os dados de **gols esperados** foram ajustados de acordo com a qualidade dos times enfrentados por cada clube, usando o ranking do Euro Club Index. Cada campeonato tem um nível diferente, por isso os ajustes foram necessários. Times que enfrentaram adversários mais difíceis receberam uma bonificação e times que enfrentaram adversários mais fáceis receberam um desconto.
3.  É importante ressaltar que o programa replica o formato da Champions League, isto é, times se enfrentam 2 vezes nas oitavas de final, 2 vezes nas quartas de final, 2 vezes nas semis e 1 vez na final. A cada fase os confrontos são sorteados. Se ocorrer um empate, se classifica o time com maior número de gols fora de casa. Caso uma disputa de pênaltis seja necessária o programa joga uma moeda e define o vencedor.
4.  Os dados utilizados são das principais ligas europeias: Inglaterra, Espanha, Alemanha, França, Itália, Portugal e a Uefa Champions League.
5.  Caso você queira entender mais sobre a distribuição Poisson no futebol sugiro a leitura do primeiro capítulo de “Soccermatics” de David Sumpter.

**Esse artigo foi escrito com a ajuda de StrataData, que é propriedade de [Stratagem](http://www.stratagem.com/) Technologies. StrataData alimenta o [StrataBet Sports Trading Platform](http://www.stratabet.com/), e também o [StrataBet Premium Recommendations](http://app.stratabet.com/recommendations).**