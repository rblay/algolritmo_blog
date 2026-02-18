---
title: "Previsões Champions League 17-18 Oitavas (Ida)"
date: 2018-02-12
draft: false
---

O Algolritmo está de volta com previsões sobre a UEFA Champions League, que inicia sua fase mata-mata amanhã. Utilizando os excelentes dados providenciados pela Stratabet, calculei as probabilidades de cada time ser campeão do torneio mais disputado da Europa, assim como as probabilidades de vitória, empate ou derrota dos confrontos de ida das oitavas de final. Pretendo ao longo das próximas fases do campeonato publicar mais textos com novas previsões. Primeiro apresento duas imagens e uma análise que resumem os resultados da simulação. Após isso detalho o método utilizado para os leitores que tem interesse em estatística, matemática e computação (além de futebol, é claro).

Lembre-se de curtir nossa _[página no Facebook](https://www.facebook.com/algolritmo)_!

**Resultados:**

A imagem a seguir apresenta a atual probabilidade de cada time ser campeão:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/02/campeoes-231x300.png?resize=617%2C802)

O resultado e bastante próximo daquilo que eu esperava. Manchester City, Bayern de Munique, PSG e Barcelona estão liderando com folga suas ligas nacionais (Inglaterra, Alemanha, França e Espanha, respectivamente), é de se esperar que esses times sejam os favoritos para vencer Liga dos Campeões.

O Real Madrid e o Liverpool aparecem logo a seguir com probabilidades próximas de vencer o campeonato, porém em momentos distintos da temporada. O time de Madrid não tem conseguido repetir as incríveis atuações das últimas temporadas que o tornaram o time mais poderoso da Europa. Enquanto isso, o Liverpool vem fazendo uma empolgante temporada, com boas performances de jogadores como Mohammed Salah e Roberto Firmino. No entanto, ainda não é claro se o time será capaz de manter o alto nível após ter perdido Philippe Coutinho, um de seus principais jogadores que foi vendido para o Barcelona.

A segunda imagem ilustra as probabilidades de vitória, empate e derrota nos jogos de ida das oitavas de final da Champions League, que acontecem nas próximas duas semanas. Caso você tenha se interessado pelo método e esteja pensando em apostar em jogos de futebol, sugiro dar uma olhada no site da StrataBet. Não me responsabilizo por eventuais perdas de seu patrimônio, mas aceito parte do lucro em forma de doação caso você ganhe algo!

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/02/oitavasIda-300x225.png?resize=630%2C472)

Para os leitores mais curiosos aqui está um detalhamento do método utilizado.

**Pressupostos:**

Para esse modelo vamos assumir que o número de gols feito por um time ao longo da partida é decidido ao jogar um “dado em um tabuleiro”. Cada time terá seu próprio dado com um **“peso”** diferente, isto é, cada dado terá probabilidades diferentes para cada número de gols. Por exemplo, o dado lançado por times melhores (como o Manchester City) tem mais chances de cair em valores altos como 4 enquanto o dado lançado por times piores (como o Shakhtar Donetsk) tem maior probabilidade de cair em valores como baixos como 1. Resumidamente, o principal pressuposto é: marcar gols é um processo **aleatório**, no entanto times melhores tem **mais** **chances** de fazer gols.

**Metodologia:**

Para prever os resultados da Champions League vamos simular o campeonato 50.000 vezes e analisar os resultados, esse processo se chama Simulação de Monte Carlo. Quando dois times se enfrentam jogamos seus dados para determinar o número de gols feitos, assim geramos um placar fictício para a partida. Criei um programa em R (uma linguagem de programação) que é capaz de simular uma Champions League de “dados de tabuleiro” levando em consideração a qualidade dos times envolvidos no confronto. Nos próximos parágrafos explicarei um pouco melhor alguns detalhes dessa simulação.

Primeiramente, precisamos analisar o “dado de tabuleiro” utilizado por um time de futebol comum. Se os times utilizassem os “dados tradicionais” (como aquele de banco imobiliário que você joga em um dia chuvoso na praia) a probabilidade do time fazer 1 gol no jogo seria a mesma de fazer 2, 3, 4, 5 ou 6 gols, no entanto sabemos que esse não é o caso. Diversos estudos já mostraram que gols seguem uma distribuição Poisson, isto é, a probabilidade de um time fazer X gols está relacionado com a média de gols feitos pelo time.

Utilizei as informações sobre as princip

ais ligas Europeias (na temporada 2016-2017) e calculei a média de gols feitos por um time durante uma partida: **1,31 gols**. Com esse valor apliquei a fórmula de Poisson para prever a probabilidade de se marcar um número específico de gols ao longo da partida e comparei com o que de fato aconteceu:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/02/poisson-300x224.png?resize=615%2C459)

Podemos ver que a distribuição Poisson é uma boa aproximação do que acontece de fato. O próximo passo é entender o “peso” do “dado de tabuleiro” de **cada time**. Para isso utilizei uma medida chamada **gols esperados** que calculei com o material detalhado fornecido pela StrataBet. Essa é uma métrica bastante usada por analistas de futebol e é calculada através da qualidade dos chutes e das chances criadas por cada time. Em um post mais antigo vimos que o número bruto de gols possui algumas imprecisões, o número de **gols esperados** é uma medida mais precisa da qualidade de um time. Calculei as médias de **gols pró esperados como mandante** (xGP mandante), **gols pró como visitante** (xGP visitante), **gols contra esperados como mandante** (xGC mandante) e **gols contra esperados como visitante** (xGC visitante). Esses valores para os clubes que ainda disputam a Champions League estão resumidos nessa tabela:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/02/tabXgOitavasIda-300x261.png?resize=589%2C512)

É importante ressaltar que os valores acima foram ajustados de acordo com a qualidade dos adversários enfrentados pelos times. O ajuste foi feito utilizando o “Euro Club Index” que faz um ranking dos clubes na Europa. Se você quer entender melhor como os valores de **gols esperados** foram utilizados e como os ajustes foram feitos por favor veja a seção “Observações”.

**Observações:**

1.  Para cada jogo da simulação o programa calcula a média entre **xGP** **mandante** de um time com o **xGC** **visitante** do outro time (resultado 1). Além disso tambem é calculada a média entre o **xGP** **visitante** e o **xGC** **mandante** (resultado 2). O resultado 1 é usado na formula de Poisson para definir o número de gols do mandante e o resultado 2 para definir o número de gols do visitante.
2.  Os dados de **gols esperados** foram ajustados de acordo com a qualidade dos times enfrentados por cada clube, usando o ranking do Euro Club Index. Cada campeonato tem um nível diferente, por isso os ajustes foram necessários. Times que enfrentaram adversários mais difíceis receberam uma bonificação e times que enfrentaram adversários mais fáceis receberam um desconto.
3.  É importante ressaltar que o programa replica o formato da Champions League, isto é, times se enfrentam 2 vezes nas oitavas de final, 2 vezes nas quartas de final, 2 vezes nas semis e 1 vez na final. A cada fase os confrontos são sorteados. Se ocorrer um empate, se classifica o time com maior número de gols fora de casa. Caso uma disputa de pênaltis seja necessária o programa joga uma moeda e define o vencedor.
4.  Os dados utilizados são de algumas ligas europeias: Inglaterra, Espanha, Alemanha, França, Itália, Portugal, Suiça e a Uefa Champions League. A STRATABET não cobre a liga da Turquia e da Ucrânia, os dados dos times dessas ligas (Shakhtar e Besiktas) foram aproximados com os da Champions League.
5.  Caso você queira entender mais sobre a distribuição Poisson no futebol sugiro a leitura do primeiro capítulo de “Soccermatics” de David Sumpter.

**Esse artigo foi escrito com a ajuda de StrataData, que é propriedade de [Stratagem Technologies](http://www.stratagem.co/). StrataData alimenta o [StrataBet Sports Trading Platform](https://app.stratabet.com/), e também o [StrataBet Premium Recommendations](https://stratatips.co/).**