---
title: "Um brasileiro na conferência de inovação no futebol"
date: 2019-10-17
draft: false
---

Nesse último final de semana viajei até Londres para participar da primeira StatsBomb Innovation in Football Conference, realizada no Stamford Bridge, estádio do Chelsea. Caso você não conheça, a StatsBomb é uma das principais empresas de análise de dados de futebol, além de oferecerem consultoria para clubes eles também coletam dados de 40 ligas ao redor do mundo. Essa conferência reuniu diversos pesquisadores, analistas de clubes, empresas e fãs de futebol que se interessam por uma visão mais analítica e tecnológica do jogo.

Confesso que voltei da conferência com sentimentos contraditórios. Por um lado, estou muito entusiasmado com as possibilidades em termos de soccer analytics, a área está em crescimento exponencial e devemos ver cada vez mais clubes e empresas explorando ferramentas modernas de data science para melhorar tomarem melhores decisões. Por outro lado, fica claro que a vanguarda dessa área está voltada para a Europa e será difícil (porém não impossível) para países da América do Sul, como o Brasil, alcançarem o nível de inovação e pesquisa visto no velho continente.

Não encontrei nenhum outro brasileiro na conferência, acredito que praticamente todos os participantes do evento eram da Europa ou da América do Norte. Se você por acaso é brasileiro, ou de algum outro país da América do Sul, entre em contato (mande um email para algolritmoblog@gmail.com)! Adoraria poder ouvir as visões de mais pessoas que estavam presentes. Além disso, caso você trabalhe em algum clube profissional, projeto na área de futebol ou é mais um entusiasta de soccer analytics também fique à vontade para entrar em contato.

Gostaria de parabenizar a organização do evento, tudo correu muito bem e fiquei extremamente satisfeito com a qualidade das palestras, local e comida, não parecia que era a primeira vez que organizavam a conferência. Minha única “reclamação” é o clima chuvoso de Londres, que não é o ideal para um brasileiro, quem sabe uma próxima edição da conferência possa ser realizada no Brasil? 

![](https://i2.wp.com/algolritmo.com/wp-content/uploads/2019/10/31abf671-82f9-4c1d-ad44-1b1a956563c5.png?fit=640%2C697&ssl=1)

Na esquerda temos a programação da “sala principal” e na direita a “sala de pesquisas”. Durante boa parte do dia a área de pesquisas estava mais lotada.

Abaixo, fiz um resumo dos meus principais aprendizados e reflexões do evento. Além disso, tentei resumir as palestras que assisti (infelizmente o evento tinha palestras simultâneas, portanto era impossível assistir tudo). Em breve, a StatsBomb também deve lançar vídeos de quase todas as apresentações para aqueles que desejarem ver na íntegra. Espero que possam aproveitar tanto quanto eu do material apresentado.

#### **Minhas Conclusões e Lições**

-   A ciência esportiva pode trazer resultados incríveis, principalmente com o apoio de uma robusta análise de dados. O Ajax é o exemplo perfeito disso.
-   Muita gente extremamente inteligente está desenvolvendo modelos semelhantes para entender o valor das diferentes ações no campo. Me parece um caminho natural após a criação e consolidação de modelos de expected goals (xG): agora que conseguimos medir a qualidade de chutes, precisamos saber o valor de passes, dribles, desarmes, interceptações, etc.
-   Tracking data (dados com a posição de cada jogador no campo em todos os momentos do jogo) já está disponível para clubes, mas poucos analistas independentes conseguem ter acesso a esse tipo de dado. Já temos os primeiros resultados de análises com tracking data, mas ainda existe um mar de possibilidades.
-   É um consenso que a comunicação é um aspecto vital para a produzir soccer analytics com efetividade. Técnicos e jogadores geralmente não tem muito tempo (ou interesse) para entender complexos modelos matemáticos, eles apenas querem saber o que devem fazer para melhorar e ganhar a próxima partida. Uma das principais tarefas do analista é saber extrair os principais pontos de uma análise e comunicá-los de forma simples, clara e convincente.
-   Os clubes inteligentes já usam a análise de dados das seguintes maneiras:
    
    -   Análise de oponentes (performance de outros times e jogadores)
    
    -   Autoanálise (performance do próprio time e jogadores) 
    
    -   Definição de modelos de jogo
    
    -   Recrutamento e scouting
    
    -   Pesquisa científica a longo prazo (melhores maneira de se jogar, como avaliar um jogador corretamente, quais treinamentos produzem melhoras técnicas em jogadores de base, etc)
-   Já existe uma enorme distância entre times da América do Sul e as equipes da Europa devido a diferenças orçamentárias. Se os nossos clubes não incorporarem a análise de dados ao seu dia a dia a tendência é que a distância se torne ainda maior. Isso com certeza afetará as seleções nacionais. Não basta ter apenas jogadores sul americanos de ponta atuando na Europa, nossos treinadores e executivos de futebol (os tradicionais “cartolas”) também precisam estar a par daquilo que é mais moderno.
-   Acredito que o Algolritmo pode ajudar a trazer um pouco dessa visão mais analítica para o futebol do brasileiro. Minha ideia é produzir conteúdo que possa levantar outros tipos de debate sobre nossos clubes e jogadores. Porém, quero deixar claro que não sou o tipo de pessoa que desmerece e menospreza visões mais “românticas”, humorísticas e sociológicas do futebol, na verdade sou grande consumidor dessa variedade de material. Acho apenas que também existem outras formas de se desfrutar desse esporte.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/algolritmo5.0Pequeno.png?fit=640%2C256&ssl=1)

#### **Abertura da Conferência**

**Palestrante:** [Ted Knutson](https://twitter.com/mixedknuts), co-fundador e CEO da StatsBomb.

A conferência começou com uma breve abertura feita por Ted Knutson, fundador e CEO da StatsBomb. Segundo Ted, a análise de dados de futebol, conhecido também como soccer (ou football) analytics, já é uma enorme realidade e as principais equipes do mundo cada vez mais percebem o valor dessas ferramentas. O Liverpool, [que conta com 4 profissionais com doutorados](https://epocanegocios.globo.com/Empresa/noticia/2019/06/como-o-liverpool-usou-dados-e-tecnologia-para-chegar-final-da-champions-league.html) em áreas como física, matemática e astrofísica, é um ótimo exemplo disso. A StatsBomb é uma ótima fornecedoras de dados, e no momento são os únicos a incluírem informações como:

-   Pressão Defensiva
-   Localização de todos os jogadores no momento de chutes
-   Altura dos Chutes
-   Pé utilizado em cada ação (direito/esquerdo).

Além disso, Ted também falou sobre alguns dos próximos passos, entre eles a empresa pretende ao longo prazo:

-   Integrar vídeos em suas plataformas de dados
-   Começar a coletar tracking data (dados com a posição de cada jogador no campo em todos os momentos do jogo)
-   Oferecer dados “ao vivo” para serem usado por times (e talvez pela mídia) ao longo dos jogos.

Por último, Ted falou sobre algumas iniciativas da StatsBomb que admiro bastante. A empresa oferece alguns dados de graça para analistas que querem começar a se familiarizar com dados de futebol e testar modelos (no momento, por exemplo, qualquer um tem acesso a todos os jogos da Copa do Mundo de 2018 e a todos os jogos da carreira de Lionel Messi). A empresa também oferece suas plataforma de dados de graça para times femininos.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/statsbomb-social-1.jpg?resize=640%2C137&ssl=1)

#### **Análise de Dados Como Vocabulário: Dando o Poder de Linguagem para Estatísticas**

**Palestrante**: [Seth Partnow](https://twitter.com/SethPartnow), ex-diretor de pesquisa do Milwaukee Bucks (NBA) e analista da NBA no The Athletic.

Seth Partnow era o único palestrante de “fora” do mundo do futebol, ele já trabalhou no Milwaukee Bucks (da NBA) e hoje em dia escreve sobre basketball analytics no The Athletic. Foi muito interessante ouvir alguém que trabalhou em um esporte no qual o analytics já esteja mais avançado. Seth falou um pouco de como existe enorme arbitrariedade de se definir estatísticas em todos os esportes. Muitas vezes, analistas dedicam a maior parte de seu tempo desenvolvendo modelos rebuscados, quando na verdade deveriam discutir quais aspectos fundamentais do jogo precisam ser mensurados. 

O essencial para uma análise de dados bem-feita é saber o que contar e como contar. Isso pode parecer trivial, mas no fundo é complexo e um pouco filosófico. Seth disse algo que já ouvi em outras palestras e concordo plenamente: “O valor de um projeto de data science é inversamente proporcional a sua complexidade”. Em outras palavras, as análises mais úteis e valiosas geralmente são simples, compreensíveis e fáceis de aplicar. A estatística descritiva é uma ferramenta poderosíssima que acaba muitas vezes sendo subestimada. Além disso, as métricas criadas para esporte devem ter boa nomenclatura, que seja fácil de entender e autoexplicativa. Seth mostrou alguns exemplos daquilo que considera bons e maus nomes (veja imagem abaixo).

![](https://i2.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5403.jpeg?fit=640%2C480&ssl=1)

Alguns exemplos (bons e ruin) de nomes de métricas para análise esportiva

Por fim, Seth também comentou um pouco sobre a dificuldade de se avaliar jogadores como “superstars”. A NBA cresceu muito globalmente nos últimos anos e cada vez mais os jogadores são tratados como grandes estrelas. Junto a esse status de fama, também existe a ideia de que esse grupo de indivíduos é tão acima da média que um “superstar” consegue levar o time aos playoffs e torna-lo candidato ao título quase que individualmente. Seth mostrou uma análise com o número de vitórias e probabilidade de título que diferentes jogadores agregaram ao time (sem incluir o nome dos jogadores). Segundo essa análise, são pouquíssimos jogadores que realmente conseguem, por si só, aumentar incrivelmente as chances de título de um time. Na minha experiência assistindo basquete, esses jogadores hoje em dia são: Lebron James, Kevin Durant, Stephen Curry, James Harden e Giannis Antetokounmpo.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5405.jpeg?fit=640%2C480&ssl=1)

Partnow mostrou algumas das análises feitas para avaliar jogadores na NBA em termos de valor ofensivo

#### **Entendendo Zonas de Entrada no Futebol**

**Palestrante**: [Estefania Vidal](https://twitter.com/tefavidal), pesquisadora e candidata a PhD na MPIDS (Max Planck Institute for Dynamics and Self-Organization)

Estefania foi uma das escolhidas pela organização do evento na competição de pesquisas. Em seu estudo, Estefania dividiu o campo em 4 (defesa, meio defensivo, meio ofensivo e ataque). A ideia da pesquisa era entender melhor como os times entram na zona de ataque, quais os padrões mais comuns e quais as estratégias mais efetivas. Alguns dos principais aprendizados e conclusões foram:

-   Se um time não consegue finalizar em até 12 segundos após entrar na zona de ataque, é melhor voltar para a zona de meio campo, se reagrupar e começar uma nova tentativa de ataque. Em outras palavras, quanto um time inicia um ataque ele precisa ser concluí-lo com rapidez para ter maiores chances de marcar um gol.
-   De uma forma geral, os times tendem a entrar no “quarto” final perto das pontas do campo (mais próximas das linhas laterais do que no centro do campo).
    
    -   Quando se entra através de um passe, a bola tende a ser aberta, para perto da linha lateral.
    
    -   Quando se entra através de uma condução de bola, a tendência é ir centralmente, em direção ao gol.
-   Passes no geral são armas mais efetivas para entrar na zona de ataque do que carregar e driblar, mas é claro que isso depende do contexto e dos jogadores disponíveis.

![](https://i2.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5411.jpeg?fit=640%2C303&ssl=1)

Estefania investigou quais tipos de passe são mais eficientes para entrar na zona de ataque

#### **Como Chutar e Como Defender: Análise Futebolística para Pais e Mães**

**Palestrante**: [Łukasz Szczepański](https://twitter.com/footyquant), analista quantitativo na Smartodds

A ideia da pesquisa de Łukasz surgiu quando estava jogando futebol com os filhos em um parque, e percebeu que estava dando conselhos sem a menor base científica para as crianças. Seus filhos perguntavam onde deveriam mirar quando chutavam, e ele respondia “o mais perto possível dos ângulos superiores das traves”. Foi então que Łukasz percebeu que não tinha certeza se essa era a melhor recomendação e fez o que qualquer pai faria: fez uma pesquisa científica para responder à pergunta com mais embasamento. Após muito estudo, Łukasz concluiu que o ideal é mirar a bola baixa e relativamente próxima das traves (mas não colado nas traves). O pesquisador levou em consideração que existe uma margem de erro para chutes. Todos nós já sentimos isso quando tentamos finalizar no ângulo e isolamos a bola para longe. Acertar exatamente o local desejado é extremamente difícil.

![](https://i1.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5415.jpeg?fit=640%2C480&ssl=1)

Probabilidades de gol, e pontos para mirar de acordo com a habilidade do jogador

Łukasz também vez uma análise de goleiros, a principal conclusão é que os goleiros tendem a “fechar” muito a trave mais próxima, deixando a segunda trave exposta demais. O apresentador fez questão de ressaltar os pressupostos do modelo e suas limitações. Por exemplo, ele não tem dados que dizem o onde cada jogador mirou um chute. Por isso, ele pressupôs que na média, os jogadores acertam os chutes onde desejam (mas com uma certa variabilidade e distribuição). 

#### **“Como eles fazem isso?“ – Análise Técnica de Habilidades de Elite no Futebol**

**Palestrante**: Vosse de Boode, chefe de ciências do esporte no AFC Ajax

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/1200px-Ajax_Amsterdam.svg_.png?resize=170%2C170&ssl=1)

Fiquei muito impressionado com o que vi na palestre de Vosse de Boode. O consenso com quem conversei foi que essa apresentação foi um dos grandes destaques da conferência. Vosse mostrou diversos exemplos de como a Ajax usa ciência para entender as melhores formas de se jogar futebol (principalmente em termos de técnica) e como ensinar isso aos jogadores. O Ajax tem um laboratório de verdade para esses estudos, onde conseguem fazer diferentes experimentos aplicando métodos científicos. O foco do trabalho no laboratório do Ajax é gerar conhecimento e tentar transmiti-los para os jogadores, principalmente para os atletas de base, pois ainda estão em formação. É claro que os jogadores do time principal também se beneficiam com as descobertas do laboratório, mas é nas categorias de base onde existe o maior potencial de crescimento técnico.

Um dos exemplos mais interessantes apresentados por Vosse foi sobre a postura dos goleiros. Geralmente, goleiros são aconselhados a manterem as pernas abertas na mesma largura dos ombros, porém perceberam que o goleiro Onana (comprado do Barcelona pelo Ajax) mantinha as pernas mais abertas do que o “recomendado”. Ao invés de tentar mudar a postura do arqueiro camaronês o laboratório do Ajax resolveu estudar aquela pose inusitada. Os pesquisadores concluíram que a postura de Onana era mais eficiente do que a “tradicional recomendação”, pois o goleiro conseguiria cobrir uma área maior do gol e pular melhor (especialmente para baixo, onde a maioria dos chutes são direcionados).

![](https://i2.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5417.jpeg?fit=640%2C360&ssl=1)

O Ajax fez testes com óculos especiais, que conseguem analisar o foco visual do jogador.

Além disso, o Ajax também faz pesquisas com o foco visual dos jogadores. Com óculos especiais, o laboratório consegue analisar aquilo que os jogadores observam e quais seus principais pontos de atenção quando executam diferentes movimentos relacionados ao futebol. Uma das principais conclusões do laboratório é que os melhores finalizadores olham para o alvo com muita atenção uma vez, depois olham diretamente para a bola e chutam. É incrível imaginar as infinitas possibilidades de estudos que esse laboratório pode fazer e como isso pode afetar positivamente o desenvolvimento de atletas.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5422.jpeg?fit=640%2C378&ssl=1)

O Ajax busca descobrir como aprimorar a técnica de seus jogadores, um exemplo é o foco durante a ação de chute.

Infelizmente o vídeo dessa palestra é um dos poucos que não será disponibilizado no YouTube por conta de um acordo com o Ajax. No entanto, muitas das pesquisas feitas pelo Ajax são publicadas em revistas acadêmicas.

#### **Encontrando o Homem Livre: Uma Abordagem Contextual para Identificar Espaços que Importam**

**Palestrante**: [Javi Fernández](https://twitter.com/javiondata?lang=en), chefe de sports analytics no FC Barcelona

![](https://i2.wp.com/algolritmo.com/wp-content/uploads/2019/10/1200px-FC_Barcelona_crest.svg_.png?fit=640%2C649&ssl=1)

Javi é um dos principais nomes na área de soccer analytics e já palestrou em outras conferências que fui, como a Sloan Sports Analytics Conference, no MIT. Como ele trabalha para o Barcelona seus exemplos e vídeos sempre mostram lances do time catalão, o que é sempre prazeroso para quem está na plateia.

O palestrante começou sua apresentação com um questionamento: “Será que não estamos focando demais em chutes durante nossas análises?”. É claro que gols são o objetivo de times de futebol, e é natural que se estude chutes pois são as ações geradoras de gols. No entanto, precisamos estudar mais as diferentes ações que levam até situações de gols. A ideia de Javi era criar um modelo que pudesse gerar esse tipo de análise. Inspirado em modelos da NBA, Javi (junto com Luke Bornn e Dan Cervone) criou o modelo de EPV (Valor Esperado da Posse, do inglês Expected Possession Value), que analisa e atribui um valor para praticamente toda a ação no campo. Se você já conhecesse a ideia de gols esperados (expected goals, também abreviado para xG), pense no EPV como um modelo de xG que tomou esteroides, aprendeu kung fu e comprou uma espada: Ele é bem mais poderoso.

Basicamente, o EPV consegue dizer a probabilidade de um time fazer (ou levar) um gol, dadas diversas características instantâneas do jogo (especialmente a localização de cada jogador no campo). O resultado de um modelo de EPV é sempre um número entre -1 e 1. Quanto mais próximo de 1, maior a chance de o time analisado fazer um gol em determinado momento e quanto mais próximo de -1 maior a chance de sofrer um gol. O EPV considera diferentes ações que um jogador pode executar e como cada uma influencia a probabilidade de um time marcar (ou sofrer) um gol. As decisões incluídas pelo modelo são:

-   Passes (e opções de passes)
-   Chutes
-   Dribles (tentativas de progressão individual com a bola)

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5431.jpeg?fit=640%2C374&ssl=1)

Javi mostrou que o modelo de EPV leva em consideração diferentes contextos de um partida de futebol

Para os leitores mais técnicos, o EPV é um Processo de Decisão Markoviano. Ele leva em consideração o contexto da partida (isto é, onde cada jogador está localizado) e calcula a probabilidade de um time marcar (ou sofrer um gol) dadas diferentes ações que um jogador pode fazer, a probabilidade de um jogador fazer aquela decisão e a probabilidade de conseguir executá-la com sucesso. Segundo Javi, o EPV é um modelo para análise de tomada de decisões a partir de superfícies probabilísticas.

Uma das formas mais interessantes de usar o modelo é ver o EPV antes e depois de uma ação e analisar a diferença. Por exemplo, se o Arthur recebe a bola em uma situação onde o EPV é 0.05 e da um passe para Suárez, que recebe em uma situação onde o EPV é 0.12, dizemos que o Arthur adicionou 0.07 de EPV na jogada. Nessa palestra, Javi focou mais em como diferentes ações geram e encontram espaço para o time algo que é extremamente valioso. Foi interessante ver que o modelo consegue capturar as diferentes formas que jogadores influenciam no jogo, por exemplo:

-   O Arthur gera valor para o time a partir de seus passes verticais, que rompem linhas adversárias. O meia brasileiro tem se destacado muito nesse quesito durante as primeiras rodadas do campeonato espanhol 2019-2020
-   Já o Messi consegue fazer de tudo um pouco, mas sua capacidade de driblar e gerar espaço é um dos atributos que mais ajuda o Barcelona. Javi também já fez um estudo de como o Messi encontra espaço simplesmente andando (e não correndo) pelo campo (o link para a pesquisa está [aqui](http://www.sloansportsconference.com/wp-content/uploads/2018/03/1003.pdf))

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5434.jpeg?fit=640%2C402&ssl=1)

Messi fazendo uma acrobacia, admirado por Arthur e Piqué

#### **Pressão, Quebra de Pressão e Pé Preferido: Explorando os Novos Dados da StatsBomb**

**Palestrante**: [Michael Caley](https://twitter.com/MC_of_A), apresentador do podcast Double Pivot e colaborador de soccer analytics no The Athletic 

Michael Caley tem é um dos poucos pesquisadores que já tem estudado o futebol de forma analítica a pelo menos 7 anos.  Já conhecia seu trabalho através do twitter e recentemente comecei a escutar seu podcast, o “Double Pivot Podcast”, onde participa junto com Michael Goodman. Nessa conferência, Caley apresentou sua pesquisa sobre “pressão” na bola. 

Pressão é a principal ação defensiva no futebol. O ato de encurtar o espaço de alguém para poder recuperar a posse (seja por roubada de bola ou através de um erro do adversário). No entanto, até pouco tempo atrás não tínhamos dados de “pressão” coletados, por isso analistas criaram diferentes métodos para medir e aproximar pressão de um time. Hoje em dia a StatsBomb já coleta esse tipo de ação.

Caley fez uma análise comparativa das diferentes formas de se medir pressão, desenvolvidas por diversos analistas ao longo dos últimos anos. Foi interessante ver que para cada métrica, o “ranking de pressão” dos times era um pouco diferente, mostrando que cada método revela aspectos específicos sobre a “pressão” de um time. A palestra envolveu muitos detalhes técnicos, vou incluir aqui apenas alguns dos principais pontos.

As métricas de pressão apresentadas por Caley foram:

-   **Passes Por Ação Defensiva (Passes per Defensive Action, ou PPDA):**é uma conta simples: (passes completos do oponente descontando bolas paradas) dividido por (ações defensivas do time). Essa métrica analisa quantos passes o oponente completa até que o time de defesa execute qualquer ações defensiva (desarme, interceptação, disputa de bola).
-   **Movimentos do Oponente Quebrados (Moves Broken):**essa métrica analisa situações específicas de jogo, principalmente quando o oponente tenta construir jogadas a partir de seu campo de defesa. A ideia é contar quantas vezes um time consegue “quebrar” uma sequência de ações do oponente.
-   **Passes para a Zona dos Zagueiros (CB Zone Passes):**quantos passes o oponente consegue completar para a região geralmente ocupada pelos zagueiros (em frente da área). A ideia por trás da métrica é que times com boa “pressão” não deixam a bola chegar até essa zona perigosa em seu próprio campo.
-   **Bolas Recuperadas no Ataque (High Turnovers):**Número de vezes que um time consegue roubar a bola (através de um desarme ou interceptação) no campo de ataque (não lembro exatamente a definição de qual zona do campo é considerada). Essa métrica busca capturar a quantidade de “turnovers” (retomadas de posse) que um time consegue em zonas valiosas de ataque.
-   **Número de Pressões (Pressures):** As métricas acima são uma “aproximação” para a pressões de um time, eles medem possíveis efeitos de uma pressão, mas não a pressão em si. Usando os dados da StatsBomb, Caley também analisou as ações de pressão de cada equipe

Em certos momentos, a palestra teve um tom de “propaganda” para os dados da StatsBomb, mas isso é compreensível e justo pois os dados fornecidos pela empresa realmente são excelentes (percebi que acabei de replicar o tom de propaganda nessa frase). Caley também mostrou uma análise dos melhores jogadores que conseguem quebrar a pressão e completar passes, veja a foto abaixo (peço desculpas pois está um pouco tremida):

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5439.jpeg?fit=640%2C569&ssl=1)

Ranking de jogadores que melhor conseguem passar quando pressionados.

Além disso, Michael Caley focou em alguns times durante a palestra, que se destacam de formas diferentes em termos de pressão nos últimos dois anos:

-   Manchester City e Eibar estavam no topo de todos os rankings de pressão.
-   RB Leipzig e Bayern de Munique mostraram ser muito eficientes pressionando, são exemplos do “german press” (a pressão alemã).
-   Torino, Barcelona e PSG são times com uma pressão ineficiente
-   Tottenham e Chelsea apresentaram mudanças táticas em termos de estratégia de pressão entre os dois últimos anos.
-   Real Madrid, Real Sociedad, Burnley, Bournemouth, Olympique de Marselha e Lazio tiveram algumas métricas “estranhas” segundo Caley.
-   Parma foi mal em todos os quesitos de pressão.

![](https://i1.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5438.jpeg?fit=640%2C241&ssl=1)

Caley analisou alguns times específicos ao longo de sua palestra, comparando os desempenhos de acordo com diferentes métricas de pressão

Por fim, todos os presentes gostaram de uma dica dada pelo palestrante ao final da palestra. Ele disse para sempre que fizer uma análise ofensiva de jogadores, verificar se Messi está entre os melhores do ranking. Se o argentino não estiver, então a métrica ou modelo provavelmente está equivocada.

#### **Como o Futebol Poderia Revolucionar a Análise de Dados**

**Palestrante**: Adrien Terascon, chefe de análise de partidas no Paris Saint-Germain

![](https://i2.wp.com/algolritmo.com/wp-content/uploads/2019/10/1200px-Paris_Saint-Germain_F.C..svg_.png?fit=640%2C640&ssl=1)

Nessa palestra, Terascon mostrou como o PSG tem incorporado a análise de dados no dia a dia do clube. O palestrante apresentou alguns dos diversos processos muito bem definidos que o clube utiliza para, segundo ele, produzir uma “compreensão futebolística orientada por dados”. Segundo Terascon, é essencial ter um modelo de jogo claramente definido pelo time. Por exemplo, para o PSG é essencial que o time consiga levar a bola até “área preferidas de cruzamento” (preferred crossing areas, abreviado para PCA). As PCAs são as zonas mais abertas e dentro da área, o time sabe que consegue ser perigoso se levar a bola até lá. O PSG tem diversos pilares para seu modelo de jogo, mas Adrien Terascon não podia revelar todos os segredos de seu time, principalmente pois analistas de potenciais adversários estavam na plateia ouvindo atentamente.

Com o modelo de jogo definido, os analistas desenvolvem diversos indicadores de performance (também conhecidos como Key Performance Indicators, abreviados para KPIs). A ideia é não seja algo abstrato, o plano de jogo precisa ser mensurável e de fácil compreensão. A partir do modelo de jogo, diversos outros modelos e processos são utilizados pelo PSG, como:

-   Modelos “micro” de jogo
-   Modelos individualizados (que inclui a criação de treinos específicos)
-   Processos de scouting
-   Processos de avaliação de jogadores
-   Estudos de adversários

![](https://i1.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5447-1.jpeg?fit=640%2C376&ssl=1)

A foto está um pouco embaçada, mas podemos ver alguns exemplos de instruções personalizadas que o PSG criou para Gueye, Herrera e Marquinhos contra o Real Madrid.

O Chefe de Análises do PSG também falou da necessidade de “individualização” na análise de dados, isto é, um grande esforço de estudar cada jogador para gerar instruções personalizadas (todas unidas por uma mesma ideia de jogo). Terascon ressaltou que cada jogador aprende de uma forma diferente, e a equipe técnica junto dos analistas precisa estar ciente disso. Assim, as instruções podem ser comunicadas da melhor forma para cada jogador. Ele disse, por exemplo, que o Mbappé não é o melhor em entender instruções faladas ou em relatórios. Para o jovem jogador francês, o que funciona melhor são treinos específicos que reproduzam o que ele deve fazer em campo. 

Outro ponto que Terascon enfatizou foi a simplicidade na comunicação. Os técnicos, jogadores e outros funcionários do clube não precisam de toda informação gerada (com inúmeras páginas de gráficos e tabelas) pois podem ficar atolados e desinteressados. Fazer uma curadoria do material é crucial. Terascon foi repetiu diversas vezes que a comunicação precisa ser extremamente clara e direta.

Durante a palestra ele também mostrou um exemplo de análises que fizeram antes da partida contra o Real Madrid (que venceram por 3 a 0 na atual Champions League). Eles sabiam que precisavam tomar cuidado com as transições ofensivas e cruzamentos do Real Madrid (o Real é um dos times de ponta que mais cruza a bola). Para isso, buscaram providenciar diferentes instruções para os jogadores de forma que o time fosse inteligente e controlasse onde perderiam a bola: buscavam arriscar mais em zonas onde o Real Madrid não teria tanta chance de encaixar contra-ataques bem-sucedidos. Além disso tentaram neutralizar jogadores que iniciam a transição e que acertam cruzamentos.

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5448.jpeg?fit=640%2C344&ssl=1)

Terascon explicou que a informação precisa ser transmitida da forma mais simples possível.

Outra coisa interessante que o PSG faz é “ajustar dados” (em inglês o termo usado foi “data tuning”). Isso significa que eles tentam usar jogadores onde sabem que podem render mais além de chamar a atenção de potenciais clubes compradores. Terascon citou um exemplo de um zagueiro (sem falar seu nome) que o clube queria vender recentemente, e começaram a usá-lo como lateral-esquerdo, pois sabiam que desse modo o jogador teria números melhores e seria mais valorizado em uma transferência.

Infelizmente, assim como a palestra de Vosse de Boode (do Ajax), essa apresentação não poderá ser compartilhada em formato de vídeo. De qualquer forma, é bom ficar atento ao PSG pois o clube parece ser mais um a aderir ao movimento do “futebol inteligente”.

#### **Algumas Coisas não são Chutes: Comparando Métodos para Avaliar Ações em uma Partida de Futebol**

**Palestrante**: [Thom Lawrence](https://twitter.com/lemonwatcher), CTO da StatsBomb.

Thom Lawrence, CTO da StatBomb, foi outro palestrante que buscou entender ações no futebol além de chutes. Thom acredita que o futebol tem elementos primordiais que vão muito além de gols e finalizações, mas teme que no fundo talvez o esporte seja uma simples busca por bons chutes para gerar gols com facilidade. O apresentador gosta de modelos como o EPV, mas sabe de suas limitações (difícil definir exatamente o que é uma posse no futebol por exemplo). Por isso ele tentou analisar o problema usando diversos métodos.

![](https://i1.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5467.jpeg?fit=640%2C253&ssl=1)

Thom Lawrence iniciou sua palestra comentando sobre alguns problemas que enxerga em modelos de EPV (Expected Possession Value)

Nessa palestra, Thom falou em detalhes de diferentes técnicas de reinforcement learning (um “tipo” específico de inteligência artificial) que poderiam ser aplicadas para entender o valor de diversas ações no futebol. Segundo o apresentador, alguns desses modelos são extremamente pesados em termos de computacionais, ele brincou que o ideal é “rodar esses modelos em máquinas AWS pagas por seu clube/empresa até que você os leve a declarar falência”. Uma das principais vantagens das técnicas apresentadas é o fato dos modelos poderem ser criados com “dados crus” (raw data). Você não precisa fazer tratamentos extra, como adicionar zonas a partir de coordenadas (x,y).

![](https://i2.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5470.jpeg?fit=640%2C421&ssl=1)

Alguns dos princípios de “desenvolvimento orientado a testes”

Thom também deu dicas para pessoas que desenvolverem modelos desse tipo: sempre tenhas testes para verificar que está funcionando como é esperado (sabemos que teoricamente isso deveria ser feito durante o desenvolvimento de novas ferramentas, mas na realidade raramente acontece). Além disso, achei interessante ele ter ressaltado que esse tipo de modelo geralmente valoriza demais os atacantes e da valor de menos aos zagueiros, isso acontece pois:

-   Atacantes em geral estão em situação com boa chance de serem recompensados (com gols) e poucos riscos (raramente seus erros resultam em gols adversários)
-   Defensores em geral estão em situação com muito risco (erros podem custar caro) e pouca chance de recompensa (as ações defensivas nem sempre são geradoras de gols).

Assim, é interessante “normalizar” o valor de cada ação de acordo com aquilo que o jogador poderia fazer. Dessa forma, é possível avaliar quais jogadores tomam as melhores decisões, pois analisa a ação do jogador dado aquilo que era possível no contexto.

Também houve uma discussão interessante sobre sinal v.s. ruído. Existe pouco sinal e muito ruído. No mundo do futebol, onde praticamente todos os torcedores, técnicos, jornalistas, diretores e jogadores se sentem especialistas é difícil saber o que realmente importa.

#### **Podcast da StatsBomb Ao Vivo:**

**Palestrantes**:

-   [Ted Knutson](https://twitter.com/mixedknuts), co-fundador e CEO da StatsBomb
-   [James Yorke](https://twitter.com/jair1970), chefe de análise na StatsBomb
-   [Benjamin Pugsley](https://twitter.com/benjaminpugsley?lang=en), co-fundador da StatsBomb

O podcast da StatsBomb é um dos mais conhecidos no mundo de soccer analytics, e foi bacana poder vê-lo/ouvi-lo ao vivo. Os participantes falaram um pouco do estado atual de analytics, principalmente na Europa, e como estamos avançando rápido. Times das ligas mais fortes cada vez mais percebem o valor da análise de dados e estão contratando mão de obra qualificada. O Liverpool, que venceu a Champions, por exemplo conta com 4 PhDs e contribuiu muito para a difusão do valor da análise de dados. Segundo os participantes do podcast, estamos vendo cada vez menos transferências “idiotas” de jogadores, principalmente na Inglaterra (acho que o mesmo ainda não pode ser falado com tanta certeza sobre times do Brasil). Depois disso, o principal tópico foi o campeonato inglês. Fizeram breve análises bem-humoradas, porém repletas de informação, sobre os principais times do Premier League. 

![](https://i0.wp.com/algolritmo.com/wp-content/uploads/2019/10/IMG_5472.jpeg?fit=640%2C309&ssl=1)

(Da esquerda para a direita) Pugsley, Knutson e Yorke no podcast da StatsBomb ao vivo

No final, ao falarem sobre o a área de soccer analytics os palestrantes ressaltaram que para crescer nessa área é essencial que você mostra coisas que as pessoas não sabem (por mais que sejam ideias simples). Isso é o que tento fazer aqui no Algolritmo, com foco no futebol jogado no Brasil, onde a análise estatística ainda não chegou com muito peso.

#### **Outras palestras do evento:**

-   **Como quebrar uma defesa fechada** – [David Perdomo](https://twitter.com/dperdomomeza1), [Daniel Girela](https://twitter.com/girela_d) e [Mark Thompson](https://twitter.com/EveryTeam_Mark)
-   **Entendo o valor da influência de jogadores dentro de times** – [Ryan Beal](https://twitter.com/ryanbeal95)
-   **Expected Threat (xT) e mais: Um guia prático** – [Karun Singh](https://twitter.com/karun1710)
-   **Entendo o valor da arte de pressionar o adversário** – [Pieter Robberechts](https://twitter.com/p_robberechts)
-   **Contanto Historias Globalizadas: Como a Mídia Narra o Futebol ao Redor do Mundo** – [Gabriele Marcotti](https://twitter.com/Marcotti), [Raphael Honigstein](https://twitter.com/honigstein) e [Guillem Balague](https://twitter.com/GuillemBalague)
-   **“Nosso Modelo está Aprendendo o que Achamos que ele está Aprendendo?” Estimando o Impacto de Expected Goals em Ações de Futebol Utilizando Modelos interpretáveis** – [Tom Decroos](https://twitter.com/TomDecroos)
-   **Considerando riscos defensivos e modelos de Expected Threat** – [Robert Hickman](https://twitter.com/robert_squared)
-   **Trabalhando no Futebol: Oportunidades e Desafios** – [Ted Knutson](https://twitter.com/mixedknuts), [Emma Hayes](https://twitter.com/emmahayes1) e Vosse de Boode
-   **Melhorando o processo de decisões em chutes** – Benjamin Larousse