---
title: "Artilharia BR17 Sorte, Azar e Competência"
date: 2017-07-22
draft: false
---

Recentemente, recebi acesso a dados detalhados da Stratabet sobre o Campeonato Brasileiro de 2017. Com isso, a tendência é que no futuro próximo o blog seja mais dedicado ao Brasileirão, vale lembrar que estou sempre aceitando sugestões e ideias para futuros estudos! Hoje falarei um pouco sobre os artilheiros utilizando algumas métricas e conceitos presentes em textos passados.

**Pressupostos**:

Pressupomos que, é possível medir e avaliar as diferenças entre os artilheiros do Brasileirão 2017 através de uma métrica chamada **valor esperado de gols** (conhecido também como **Expected** **Goals**, e abreviado para **xG**). O **xG** é uma medida que vem ganhando muita popularidade entre diferentes analistas de futebol. Basicamente, essa métrica atribui um valor entre 0 e 1 para cada finalização do time de acordo com probabilidade daquela bola entrar no gol. Por exemplo, uma finalização de fora da área com a perna ruim (**finalização 1**) tem menos chance de resultar em gol comparada a uma finalização na pequena área sem goleiro (**finalização 2**), portanto a finalização 1 tem um **xG** menor que a finalização 2.

O **xG** é muito interessante pois traz informação sobre as finalizações. A ideia é que ao final da partida se possa somar o **xG** de todas as finalizações feitas por um jogador e dizer que “era esperado que o jogador fizesse Y gols ao longo desse jogo”. Em outras palavras, o **xG** nos permite avaliar se um jogador conseguiu ou não aproveitar as oportunidades que teve. Também é possível entender o quão improvável são alguns gols.

**Metodologia**:

Utilizei os dados da Stratabet sobre o Campeonato Brasileiro e criei um “Artilharia de **xG** (Valor Esperado de Gols)”. Basicamente, somei os valores de **xG** de cada finalização de cada jogador para criar essa artilharia. Depois, coloquei esse ranking ao lado da artilharia “tradicional” (na qual se considera apenas os gols feitos por cada jogador). Após isso, calculei a diferença entre os gols esperados e os gols feitos por cada jogador, ou seja, fiz a seguinte subtração: VALOR DE GOLS ESPERADOS – GOLS FEITOS. A ideia é poder saber o quão distante do esperado está a performance dos finalizadores do Campeonato Brasileiro.

É importante ressaltar que os dados estavam atualizados até a 14<sup>a</sup> rodada do campeonato, portanto não inclui os gols e finalizações dos jogos da última quarta e quinta-feira (19 e 20 de julho). Assim que os dados forem atualizados pretendo postar novas versões da artilharia de **xG**.

**Resultados**:

Aqui está a tabela que traz, lado a lado, a artilharia “normal” e a artilharia de gols esperados:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/07/artilhariaXG_tabela_pt-296x300.png?resize=640%2C649)

Podemos ver que muitos nomes possuem números próximos em ambas listas. Um bom exemplo é Henrique Dourado que tem o **xG** de 8,79 e marcou 9 gols, ou seja, esperava-se que o atacante do Fluminense fizesse 8,79 gols e ele anotou 9. Outro exemplo é Lucca, da Ponte Preta, que tem o **xG** de 6,53 e 7 gols feitos. O número de gols feitos por esses jogadores está de acordo com a quantidade e qualidade de chances que tiveram até agora no campeonato brasileiro, não desperdiçaram chances muito claras, mas também não marcaram gols demasiadamente improváveis. Em outras palavras, os jogadores que possuem um **xG** próximo ao número de gols feitos estão aproveitando as oportunidades ao longo da partida de forma esperada.

No entanto, alguns nomes possuem uma grande diferença entre seu **xG** (valor esperado de gols) e o número de gols. Vamos primeiro analisar aqueles que possuem um **xG** maior que seu número de gols:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/07/azarados_pt-1-300x249.png?resize=640%2C532)

A imagem acima traz os jogadores que possuem a maior diferença entre o **xG** (valor esperado de gols) e a quantidade de gols feitos, portanto, estão fazendo menos gols do que o esperado. Essa diferença entre o **xG** e o número de gols pode ser compreendida de 2 maneiras distintas. A primeira é que esses jogadores simplesmente estão vivendo um período de “azar”. Eles finalizam diversas vezes e criam boas oportunidades, mas as vezes a bola simplesmente não entra. A segunda visão possível é que eles têm sido ineficientes. Pode-se entender que jogadores como **Pratto**, **Luan** e **Everaldo**, mesmo figurando entre os artilheiros do campeonato, estão desperdiçando chances demais e “devendo” em termos de gols.

Agora, vamos olhar para o outro extremo, os jogadores com um número de gols significativamente maior que seu **xG**:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2017/07/sortudos_pt-300x244.png?resize=640%2C520)

Os jogadores presentes no quadro acima possuem o número de gols maior que o seu **xG**, pode-se dizer que esses estão fazendo mais gols do que esperado de acordo com suas finalizações e oportunidades. Novamente, a diferença entre o número de gols e o **xG** pode ser entendida de 2 formas. Por um lado, é possível enxergar esses jogadores como “sortudos”, fazendo gols improváveis e com atuações nas quais tudo parece dar incrivelmente certo. Por outro lado, pode-se dizer que os números desses jogadores não estão relacionados a sorte e sim a eficiência e competência. De acordo com essa teoria, atacantes como **Copete**, **Everton** e **Jô** conseguem ser cirúrgicos e transformar um grande número de suas finalizações em gol.

O debate entre azar/sorte v.s. ineficiência/eficiência no futebol (e na vida) é muito interessante e subjetivo. Não é simples entender de forma exata o quanto um jogador é competente ou sortudo. Mesmo após ter números muito impressionantes ao longo de um ano, é difícil dizer ao certo se o jogador realmente é mais competente do que o esperado ou se apenas teve uma temporada de sorte. Acredito que seja mais fácil entender sorte/azar e competência/ineficiência quando se olha um nível mais macroscópico e se analisa o time ao longo da temporada como um todo, pretendo fazer isso em próximo post.

**Observações:**

1.  Os dados são utilizados são referentes até a 14<sup>a</sup> rodada do campeonato brasileiro
2.  Nesse texto dei um enfoque aos finalizadores, mas uma análise parecida pode ser feita com os assistentes.
3.  Os pênaltis perdidos podem tem um grande peso nos dados de xG e são um ingrediente a mais na discussão sobre sorte v.s. competência. Fica sempre a pergunta, o pênalti perdido foi de fato incompetência do batedor ou apenas falta de sorte estatisticamente esperada?

**Esse artigo foi escrito com a ajuda de StrataData, que é propriedade de [Stratagem](http://www.stratagem.com/) Technologies. StrataData alimenta o [StrataBet Sports Trading Platform](http://www.stratabet.com/), e também o [StrataBet Premium Recommendations](http://app.stratabet.com/recommendations).**