---
title: "Os Melhores Goleiros do Brasileirão 2018"
date: 2018-12-21
draft: false
---

Durante a pausa do futebol brasileiro, o Algolritmo trará textos sobre a Série A e Série B do brasileirão 2018. Nesse primeiro texto trazemos uma análise estatística sobre os goleiros da Série A. A maioria dos torcedores e comentaristas tende a avaliar o desempenho de goleiros com alguns números simples, entre eles: gols sofridos, jogos sem levar gol ou defesas difíceis (que possui um certo grau de subjetividade). Hoje o Algolritmo mostrará uma outra forma de entender a efetividade dos goleiros, combinando as defesas feitas com a qualidade das finalizações sofridas. Esse texto é inspirado em análises sobre goleiros da Europa feitas pelo site Statsbomb.

Os dados utilizados para essa análise são fornecidos pela Instat, caso se interesse pelos produtos da empresa entre em contato por [esse formulário](https://form.jotformeu.com/80462843333354).

#### **Resultados:**

Calculamos a efetividade dos goleiros através da “porcentagem de defesas acima do esperado”, abreviado para **%DAE**. Resumidamente, essa métrica indica como foi o desempenho de um goleiro em relação àquilo que se espera de um “goleiro médio”. Os goleiros que mais se destacaram com essa estatística foram estes:

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2018/12/imagemGoleiros.png?fit=640%2C990)

Analisando estatisticamente, o melhor goleiro do campeonato seria Santos, goleiro do Athlético Paranaense. Santos fez um ótimo campeonato e foi parte essencial da retomada do CAP no segundo turno. O goleiro do clube paranaense terminou o ano extremamente valorizado e cada vez mais se consolida como um nome relevante no futebol brasileiro.

Outro goleiro que se destacou no campeonato foi Maílson, do Sport. O goleiro ficou marcado por quase fazer um gol contra inacreditável em um jogo contra o Vitória, mas mesmo assim o goleiro teve no geral atuações muito boas principalmente contra a Chapecoense e o São Paulo. Maílson atuou em 13 jogos, e teve grande sequencia no time após o goleiro titular, Magrão, se lesionar. É interessante notar que Maílson conseguiu se destacar positivamente mesmo com seu time terminando o campeonato rebaixado, o que indica que a maioria dos gols que sofre não foram diretamente sua culpa. Talvez se Maílson tivesse jogado mais jogos, e se a defesa do Sport estivesse mais bem postada o clube pernambucano não terminasse o ano rebaixado para a Série B após 5 anos.

O terceiro destaque é Diego Alves, goleiro do Flamengo. O goleiro veio do Valencia ano passado para ser titular da meta do clube rubro negro, e teve bastante sucesso até se lesionar e ter problemas de relacionamento com o novo técnico Dorival Júnior. Até então, Diego era titular absoluto com atuações muito sólidas e poucas falhas. O goleiro está com a situação indefinida na Flamengo e seria um ótimo reforço para clubes que precisam de goleiro.

#### **Pressupostos do Modelo:**

-   Finalizações tem qualidade diferente, não podemos considerar que todos os chutes a gol exigem defesas com o mesmo grau de dificuldade.
-   Goleiros devem ser avaliados de acordo com a qualidade das finalizações sofridas. Se não, podemos acabar “prejudicando” bons goleiros que não possuem defensores que ajudem a evitar chutes do adversário.
-   Apesar de hoje em dia goleiros possuírem muitas funções (como iniciar as transições ofensivas e saber jogar com os pés) vamos comparar os goleiros de acordo com sua função mais crucial: defender finalizações dos adversários.

#### **Glossário de abreviações:**

-   **%FD:** Porcentagem de finalizações defendidas.
-   **%xFD:** Porcentagem de finalizações defendidas esperadas
-   **GSAE:** Gols salvos acima do esperado.
-   **xGSOT:** valor de gols esperados vindo de chutes no alvo.
-   **%DAE:** Porcentagem de defesas acima do esperado.

#### **Metodologia:**

O goleiro moderno possui diversas funções, mas hoje focaremos em sua principal responsabilidade: evitar gols do adversário. Geralmente, goleiros são avaliados de acordo com o número de gols sofridos, jogos sem sofrer gols e quantidade de defesas difíceis. Esses dados, embora úteis, podem acabar sendo enviesados por alguns fatores. Por exemplo, uma defesa muito sólida pode ajudar um goleiro mediano a ter números bons ao evitar que o outro time tenha muitas finalizações.

Primeiramente, para tentar eliminar um pouco da influência de fatores externos vamos olhar para a porcentagem de finalizações defendidas para cada goleiro (**%FD**). Utilizando os dados da Instat, observamos quantas bolas foram em direção de cada goleiro e contamos quantas foram defendidas. A fórmula de **%FD** é bem simples: finalizações defendidas/finalizações a gol sofridas. Abaixo está uma tabela com os valores **%FD** para todos os goleiros do Campeonato Brasileiro 2018 que jogaram pelo menos 10 jogos:

Com essa tabela é possível ver os goleiros mais difíceis de se fazer um gol nesse brasileirão 2018. Santos, do Athlético Paranaense, tem o melhor **%FD** com 87.94% (ou seja, para fazer um gol no goleiro Santos era necessário finalizar um pouco mais de 8 vezes em direção ao gol). A **%FD** nos traz um pouco mais de informação sobre o desempenho de um goleiro, no entanto ainda existe um outro aspecto a ser levado em consideração: a qualidade das finalizações sofridas.

Ao longo de um campeonato, os goleiros precisam fazer defesas de diferentes dificuldades. Algumas defesas são consideradas “milagrosas” pois são de chutes quase indefensáveis, enquanto outras defesas são extremamente simples e frutes de chutes quase despretensiosos. Para incorporar o fator “dificuldade da defesa” nessa análise, usamos uma pequena variação do modelo de valor de gols esperados (expected goals), que já explicado em outros posts, veja esse link caso queira mais detalhes.

Em outros textos, nos quais “expected goals” são analisados, utilizamos todas as finalizações (inclusive as bloqueadas ou para fora) para entender a força ofensiva e defensiva de um time. Para esta análise de goleiros, usamos um modelo parecido, porém que leva em consideração **apenas os chutes que foram em direção ao gol**, pois essas são as situações nas quais a interferência do goleiro é crucial. A métrica utilizada, portanto, é o “valor de gols esperados de chutes no alvo”, que abreviarei para **xGSOT** (do inglês “expected goals for shots on target”). Assim, todas as finalizações em direção ao alvo recebem um valor entre 0 e 1, que representa a probabilidade daquela finalização resultar em um gol. Quanto mais perto de 1 for o valor melhor é a chance de marcar um gol.

Com o **xGSOT** podemos entender a performance dos goleiros de outra perspectiva. Somando o **xGSOT** de todas as finalizações sofridas por cada goleiro calculamos a “quantidade de gols sofridos esperados” para aquele goleiro. Em outras palavras, analisamos todas as finalizações que foram em direção ao gol e vemos quantas gols um “goleiro médio” sofreria. Depois disso, podemos comparar o número de gols esperados com o número de gols realmente sofridos. A diferença entre os dois números (gols sofridos esperados – gols realmente sofridos) traz uma medida de quantos gols cada goleiro conseguiu evitar ou sofrer se comparado com um goleiro médio. Chamamos essa métrica de “Gols salvos acima do esperado”, abreviado para **GSAE**. Abaixo uma tabela com esses valores:

Novamente, o goleiro Santos se destaca. Dado as finalizações no alvo de seus adversários, esperava-se que ele sofresse aproximadamente 15 gols a mais do que de fato ocorreu (seu valor de **GSAE** foi de 15.19 gols). Outros goleiros que se destacaram positivamente foram Cássio (do Corinthians) com **GSAE** de 7.1 gols, e Éverson (do Ceará) com **GSAE** de 6.29 gols. Por outro lado, alguns goleiros de destacaram negativamente, sofrendo mais gols do que o esperado. Entre os nomes que deixaram a desejar no Brasileirão 2018 estão Jandrei (da Chapecoense) com **GSAE** de -12.12 gols, Magrão (do Sport) com **GSAE** de -8.12 gols, e Ronaldo (do Vitória) com **GSAE** de -5.15 gols.

Como podemos ver, as métricas acima (**%FD** e **GSAE**) nos trazem mais informação sobre a performance de cada goleiro, eliminando alguns elementos subjetivos. No entanto, para melhor comparar os goleiros é necessário fazer um pequeno ajuste nas medidas. Os goleiros sofreram quantidades de finalizações diferentes e isso precisa ser levado em conta. As fórmulas desse ajuste estão explicadas nas observações ao final do texto, mas o importante é saber que uma terceira métrica é gerada, que é o percentual de defesas acima do esperado, abreviado para (%DAE). Com isso, podemos ver o comparar melhor o desempenho de goleiro que receberam finalizações de quantidade e qualidade diferentes. Aqui estão esses valores para os goleiros da Brasileirão Série A 2018:

A métrica acima nos permite analisar os goleiros com mais profundidade. É claro que muitos goleiros tiveram excelentes desempenhos ao longo do campeonato mas fica claro que aqueles que tiveram o maior impacto positivo em seus times foram Santos (Athlético Paranaense), Maílson (Sport) e Diego Alves (Flamengo). O goleiro do Athlético Paranaense, fez 10,89% mais defesas do que se esperava de um goleiro médio, enquanto o arqueiro do Sport fez 7,62% mais e o jogador do Flamengo fez 7,18% mais. Ao mesmo tempo, Jandrei (Sport), Ronaldo (Vitória) e Magrão (Sport) tiveram desempenhos abaixo do esperado. É interessante notar que o Sport, que terminou rebaixado, teve um dos melhores e um dos piores goleiros do campeonato. Magrão é um ídolo do clube, mas o desempenho do Sport melhorou quando Maílson, de 22 anos, assumiu a titularidade (após Magrão sofrer uma fratura no braço). Para 2019 seria interessante dar mais oportunidades para o jovem goleiro.

Com esse tipo de análise os clubes podem tomar decisões melhores ao contratar novos goleiros (ou renovar contratos) para a próxima temporada. Com mais inteligência nas contratações os times podem se tornar mais competitivos e administrar melhor seu orçamento.

#### **Observações:**

1.  Se você tem interesse nos dados da Instat preencha [esse formulário](https://form.jotformeu.com/80462843333354) para entrar em contato com a empresa.[](https://bit.ly/2R3QI8X)
2.  Essa análise de goleiros foi inspirada em uma análise feita pelo excelente site Statsbomb, sobre os goleiros da Europa. Aqui está o [link.](https://statsbomb.com/2018/11/intro-to-goalkeeper-analysis/%EF%BB%BF)
3.  Os dados utilizados para calcular o xGSOT foram 60% dos dados do Brasileirão Série A de 2017 e 2018, além dos dados da Série B de 2018.
4.  Nessa análise pênaltis e gols contra não foram incluídos.
5.  Para fazer o ajuste que gerou o %DAE, primeiro vamos calcular qual seria a % de finalizações defendidas esperadas para cada goleiro, abreviado para %xFD. Essa valor foi calculado da seguinte maneira: (chutes no alvo – xGSOT)/chutes no alvo. Depois, para calcular o %DAE simplesmente fazemos a seguinte conta: (%FD – %xFD).