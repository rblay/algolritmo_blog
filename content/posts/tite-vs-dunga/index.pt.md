---
title: "Tite vs Dunga"
date: 2017-03-18
draft: false
---

Nessa semana temos a volta das eliminatórias para a Copa do Mundo com o clássico internacional Brasil x Uruguai. A seleção brasileira vem embalada por uma sequência de 6 vitórias consecutivas na competição e é praticamente uma unanimidade que muito do recente sucesso se deve ao novo treinador, Tite. De uma forma geral, a mídia afirma que a seleção do novo treinador é mais confiante, alegre e leve se comparada com a de Dunga. Assim como muitos torcedores concordo em grande parte com essa análise subjetiva, mas acredito que com alguns dados é possível entender melhor o desempenho da seleção comandada por Tite.

**Pressupostos:**

É possível medir e avaliar as diferenças entre os times de Tite e Dunga de análises quantitativas. Uma das métricas mais interessantes para fazer esse tipo de análise é o **valor esperado de gols** (conhecido também como Expected Goals, e abreviado para **xG**).

**Metodologia:**

O valor esperado de gols (xG) é uma medida que vem ganhando muita popularidade entre diferentes analistas de futebol. Basicamente, essa métrica atribui um valor entre 0 e 1 para cada finalização do time de acordo com probabilidade daquela bola entrar no gol. Por exemplo, uma finalização de fora da área com a perna ruim (**finalização 1**) tem menos chance de resultar em gol comparada a uma finalização na pequena área sem goleiro (**finalização 2**), portanto a finalização 1 tem um xG menor que a finalização 2. Com o xG podemos entender melhor a qualidade das chances criadas e sofridas por cada time ao longo da partida.

Assisti a todas as finalizações feitas e sofridas pelo Brasil durante as eliminatórias e utilizei a ferramenta [quasegol.com.br](http://quasegol.com.br/) (criada pelo jornalista Gustavo Fogaça) para obter o xG de cada chute. Foram 6 jogos sob o comando de Dunga (3 como mandante e 3 como visitante) e 6 jogos na era Tite (3 como mandante e 3 como visitante). Abaixo você vê um exemplo de uma finalização computada no _Quase Gol_:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/03/Screen-Shot-2017-03-17-at-3.04.34-PM-300x108.png?resize=619%2C223)

**Resultados:**

Utilizando esses dados criei dois gráficos para comparar os desempenhos de Tite e Dunga. No primeiro é possível analisar o número de chutes feitos pelo Brasil e o valor esperado de gols pró para cada jogo das eliminatórias:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/03/Screen-Shot-2017-03-17-at-3.57.23-PM-300x257.png?resize=640%2C549)

Não é possível notar uma diferença muito clara entre as seleções de Tite e Dunga em termos de ataque. No geral o time de Tite **cria mais** e tem **chances melhores**, mas o desempenho ofensivo do time de Dunga não era tão inferior ao de Tite como muitos imaginam. É quase natural que qualquer time com jogadores como Neymar, Philippe Coutinho, Gabriel Jesus, Douglas Costa e Willian vá criar diversas boas chances.

O segundo gráfico mostra as finalizações sofridas pelo Brasil e o valor esperado de gols contra para cada jogo das eliminatórias, aqui as diferenças começam a ficar mais nítidas:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/03/Screen-Shot-2017-03-17-at-3.57.12-PM-300x261.png?resize=640%2C557)

A distribuição dos pontos nesse gráfico é muito interessante, podemos agrupar de forma bem clara os jogos de acordo com o treinador. O time de Tite além de sofrer **menos chutes** também sofre **finalizações com xG menor** em média. Apesar de poucos jogos, a melhora no comportamento defensivo sob o comando de Tite parece ser muito relevante. O novo treinador consolidou o esquema tático 4-1-4-1 (inicialmente implementado por Dunga) com peças como Marcelo, Renato Augusto, Casemiro e Fernandinho (que entrou após a lesão do volante do Real Madrid).

A seguir vemos um resumo da comparação entre os técnicos:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/03/Screen-Shot-2017-03-17-at-2.24.22-PM-273x300.png?resize=512%2C563)

Admito que a princípio acreditava que o sucesso de Tite se daria por conta de uma grande eficiência ofensiva, principalmente com a chegada de Gabriel Jesus e a afirmação de Philippe Coutinho no time titular, no entanto a eficiência defensiva parece ser o novo grande segredo da seleção. Ao defender, o time diminui os espaços e reduz as opções de ataque para o adversário, que é obrigado a tentar chutes com pouca probabilidade de entrar no gol.

É claro que com apenas 6 jogos não é possível fazer afirmações com um grau de certeza enorme, no entanto é possível dizer que a perspectiva é muito animadora. Vamos ver como o time se comporta no próximo desafio em Montevidéu.

**Observações:**

1.  Como disse no texto utilizei o [www.quasegol.com.br](http://quasegol.com.br/), ferramenta criada pelo Guffo (Gustavo Fogaça) para calcular o xG de cada finalização. É uma ferramenta nova que tende a ficar cada vez mais precisa ao longo do tempo. Por isso, isso normalizei os valores adotando o valor de **0,75** como máximo.