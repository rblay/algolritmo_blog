---
title: "Medindo a Relevância de Gols"
date: 2017-01-31
draft: false
---

Os meses de dezembro e janeiro são marcados por muitas especulações no mundo do futebol, especialmente no Brasil onde os times estão contratando jogadores para a temporada que está por vir. Nessa época do ano é muito comum ver em jornais comparativos entre jogadores sondados por clubes e disponíveis no mercado. Naturalmente o principal dado utilizado nessas comparações, principalmente quando se coloca lado a lado jogadores de ataque, é a quantidade de gols. O número bruto de gols é um dado interessante, mas aliado a um pouco mais de informação é possível extrair comparativos mais relevantes. Abaixo apresento 2 modelos que utilizam dados de gols um pouco mais a fundo.

**Pressupostos**:

O principal pressuposto para ambos modelos é que nem todo gol tem a mesma relevância e dificuldade. Por exemplo, fazer o primeiro gol de um jogo disputado é mais difícil do que fazer o quinto gol do seu time em uma fácil goleada por 5 a 0.

**Metodologia**:

Estou reunindo dois modelos diferentes nesse post, vou explicar cada uma das metodologias separadamente.

 **1) Modelo dos Pontos Marginais dos Gols**

Esse modelo é apresentado e explicado no livro “Os Números do Jogo”, de Chris Anderson e David Sally. Os autores do livro primeiro analisaram o **número médio de pontos** feitos por times que marcaram um número específico de gols. Isto é, usaram uma base de dados com jogos de diversos campeonatos e calcularam a média de pontos conquistados por um time que fez ao longo do jogo 1 gol, 2 gols, 3 gols etc. Para ilustrar, times que fizeram 1 gol no jogo ganharam em média 1,13 pontos enquanto times que fizeram 2 gols no jogo ganharam em média 2,12 (Ao longo do texto apresento uma tabela que resume estes valores). Fiz o mesmo cálculo com os dados do campeonato brasileiro de 2016 e comparei os valores.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/grafico1-300x178.png?resize=640%2C380)

Através do gráfico, é possível ver que os dados do Brasileirão são bem próximo daqueles calculados por Anderson e Sally. Além disso a figura comprova algo bem intuitivo: fazer mais gols gera mais pontos na média. Usarei os dados do livro para as análises, uma vez que os valores foram calculados utilizando um número maior de jogos. O próximo passo é entender os **pontos marginais de cada gol**, isto é, o quantos pontos o gol X adiciona em relação ao gol X-1. A tabela abaixo resume estes valores e será usada como referência:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/tabelaValoresLivro-300x96.png?resize=640%2C205)

Com esses números agora podemos calcular quantos pontos marginais de cada jogador de acordo com seus gols longo do campeonato. Por exemplo, se o jogador X fizer o primeiro e segundo gol do time dele em uma partida, seus gols valeram 0,85 + 0,99, isto é, 1,84 **pontos marginais**. Se outro jogador Y fizer o terceiro e quarto gol nessa mesma partida, ele recebe 0,55 + 0,23, isto é, 0,78 **pontos marginais.** Ambos jogadores fizeram 2 gols, no entanto os gols feitos pelo primeiro garantiram mais pontos para seu time, por isso valem mais.

**2) Modelo dos Gols Impactantes**

No modelo acima é possível ver que de forma geral os primeiros gols são os mais relevantes, no entanto isso nem sempre é o caso. Imagine que um atacante faz um gol no final de uma partida que estava empatada em 3 a 3, esse gol tem um impacto enorme, no entanto contaria apenas como 0.23 pontos para o time. Pensando nisso criei uma métrica que se chama **gols impactantes**. A ideia é bem simples, um gol impactante é aquele que muda o “status” de um jogo, ou seja, se antes do gol o time estava perdendo e com o gol o time empatou o gol foi impactante (o mesmo vale para gols que fazem um time passar à frente no placar). Resumidamente os gols impactantes são aqueles que alteram o resultado de momento da partida.

Por exemplo, vamos supor um jogo imaginário entre time A e time B para deixar o conceito mais claro. O time A abre o placar, esse gol é considerado impactante (1 x 0). Agora o time B empata o placar (1 x 1), este gol também é considerado impactante. O time B vira o jogo, esse gol também é impactante (1 x 2). No começo do segundo tempo o time B faz mais um gol, esse gol não é impactante pois não alterou o resultado de momento do jogo, antes do gol o time B estava ganhado e depois ele continuou na frente, (1 x 3). O time A faz um gol no final do jogo, esse gol não é impactante (2 x 3). **No meu modelo apenas os gols impactantes são contabilizados**, portanto nessa partida apenas o primeiro gol do time A e os dois primeiros gols do time B seriam incluídos.

**Resultados**:

Com as métricas acima fiz 2 novos rankings de jogadores e comparei com a tradicional artilharia.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/imagemComparativo-300x232.png?resize=640%2C495)

Como podemos ver muitos nomes estão presentes nas 3 listas, mas suas posições variam. Todos os jogadores acima são peças interessantes, mas é importante entender as algumas de suas diferenças. Uma boa ilustração disso é o comparativo entre Sassá (do Botafogo) e Marinho (do Vitória), dois jogadores que ficaram empatados com 12 gols na artilharia convencional.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/01/sassavsmarinho-1-300x237.png?resize=553%2C437)

Sassá fez 7 gols impactantes e 10,32 pontos marginais, enquanto Marinho fez 11 gols impactantes e 9,7 pontos marginais. É possível dizer que nesse campeonato os gols de Sassá em geral serviram para ampliar vitórias do Botafogo, uma vez que muitos de seus gols deixaram o placar 2 a 0 ou 3 a 0. Já os gols de Marinho, em sua maioria, mudaram as perspectivas de uma partida para o Vitória e foram essenciais na conquista de empates e vitórias que mantiveram o time na primeira divisão. Assim, ambos jogadores tiveram importante papel ao garantir pontos para seus times, no entanto os gols de Marinho aconteceram com placares de jogo mais delicados.

A quantidade de gols nunca deixará de ser um critério para avaliar o desempenho de jogadores de ataque, no entanto, utilizando alguns outros critérios é possível medir a relevância dos gols marcados e enriquecer a avaliação.

**Observações:**

1.  É bom ressaltar que esse modelo é relevante para jogadores de ataque, especialmente atacantes. Em um próximo post pretendo fazer uma análise parecida com as assistências, que em tese seria mais relevante para os meio-campistas.
2.  Se você quiser entender mais sobre o modelo dos “pontos marginais” de gols sugiro a leitura de “Os Números do Jogo”.