# Trabalho Final da Disciplina de Introdução a Data Science
## Aluno: Luis Ricardo Arantes Filho - Doutorando CAP INPE

# Classificação de Fases Espectrais em Supernovas do Tipo Ia

## Introdução
A importância da classificação de supernovas se dá por muitos fatores. A classificação de supernovas de tipo Ia é objeto de diversas pesquisas e aplicações referentes a cosmologia e ao entendimento sobre como o universo se expande.
De maneira fundamental, supernovas são explosões estelares que destroem completamente as estrelas e podem ser causadas pelo colapso gravitacional em estrelas massivas e por reações de acréscimo de massa em anãs brancas que desencadeiam explosões termonucleares de proporções extremas. As supernovas formadas por reações termonucleares em anãs brancas são o foco de diversos estudos e são denominadas supernovas Ia.

A expansão acelerada do universo foi constatada pela observação das supernovas de Tipo Ia como sendo pontos de luminosidade com intensidades bem definidas formadas por estrelas anãs brancas (compostas em essência de Carbono e Oxigênio em condições degeneradas). Esta abordagem rendeu o prêmio Nobel de física para os astrônomos Saul Perlmutter (PERLMUTTER et al., 1999), Adam G. Riess e Brian P. Schmidt (RIESS et al., 1998).

## Abordagem

O entendimento computacional sobre este fenômeno reside na capacidade de análise e interpretação dos dados de supernovas coletados. A tarefa de avaliar e analisar os dados referentes às curvas de luz e aos espectros é estritamente dependente da especialidade de um astrônomo, entretanto executar esta tarefa de maneira prática e consistente é difícil devido à complexidade e a grande quantidade de dados gerados.

A análise espectral de supernovas tem sua importância, pois o espectro é o primeiro tipo de informação que se obtém da observação de uma explosão de supernova. Esta análise permite avaliar os tipos de supernovas de colapso de núcleo e termonucleares (tipo Ia) em um curto espaço de dias. Este curto período é referente ao pico de luminosidade máxima da explosão observada, fora deste período as características dos espectros mudam completamente, sendo difícil sua classificação e análise. A figura 1 ilustra como os espectros sofrem alterações importantes tornando a tarefa de classificação espectral dificil no decorrer dos dias. O ponto indicado como 0 dia é o ponto em que a supernova atinge sua luminosidade máxima.

<p align="center"> Figura 1 - Fases espectrais de uma supernova de tipo Ia</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/phases.png">
</p>

<p align="center"> Fonte: Blondin (2012)</p>

Desta maneira se propõe uma abordagem que possa analisar e avaliar os espectros de supernovas antes e depois do pico de luminosidade máxima para que se possa gerar modelos de classificação que correlacionem estas fases com o tipo de supernovas. Desta maneira é possível avaliar supernovas de tipo Ia pelo espectro antes da luminosidade máxima e nas fases finais quando o brilho é mais fraco, permitindo ampliar as condições de contorno da classificação espectral de supernovas.

## Dados

Os dados a serem utilizados são de acesso gratuito e definidos na tabela 1. Estes dados compreendem espectros de supernovas de diversos tipos de supernovas estando em diversas fases de observação. Os dados são dispostos em arquivos no formato ascii com as colunas para o comprimento de onda em [Å] e o fluxo de radiação em [1e-15 erg/s/cm2/A]. As fases de cada espectro também estão disponíveis nos arquivos de publicação dos espectros.

<p align="center"> Tabela 1 – Identificação de dados </p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/dados.png">
</p>

## Resultados Esperados

Espera-se com a avaliação e organização dos dados de fase espectral aplicando as diversas atividades da disciplina de introdução a DataScience gerar um esquema de classificação seguro que permita avaliar supernovas fora da faixa de dias da luminosidade máxima. Outro ponto importante nesta abordagem é verificar o comportamento das supernovas Ia em cada uma de suas fases de forma a identificar se determinado perfil do espectro dura mais dias em algumas supernovas do que em outras e se o espectro indica se elas evoluem de maneira parecida. Neste sentido, seria possível identificar se o perfil de supernova Ia no brilho máximo dura mais ou menos dias de supernova para supernova.

A figura 2 ilustra a forma como se pretende aplicar a abordagem da divisão de espectros por fases para gerar um agrupamento e classficação dos dados.

<p align="center"> Figura 2 - Resultados para separação e classificação das fases de uma supernova Ia</p>
<p align="center">
<img width="460" height="300" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/fasesAnalysis.png">
</p>

<p align="center"> Fonte: Sandelli (2016)</p>

## Resultados Obtidos

Os resultados obtidos encontram-se nos notebooks python.

O notebook "Manipulando Dados Brutos de Supernovas" ilustra como os dados de arquivo texto são tratados e transformados em objetos do tipo DataFrame para melhor organização das tabelas e das informações.

O notebook "Análise Estatistica de Dados" revela instruções básicas para geração de informaçoes em gráficos de barras, histogramas, box-plots e scatter plots sobre cada informação dos dataframes. Em cada um dos notebooks gerados neste trabalho existe um tratamento estatistico e como as informações foram interpretadas.

O notebook "Extraindo Atributos dos DataFrames" ilustra como são extraidos os atributos de componentes principais dos dataFrames gerados no notebook anterior. São gerados os componentes principais (PCA) das informações de larguras e intensidades das linhas espectrais, bem como dos valores de comprimento de onda e de fluxo de radiação de cada espectro de supernova.

O notebook "Agrupamento de dados K-means" introduz o algoritmo k-means para o agrupamento das informações dos componentes principais dos espectros. Este notebook revela o agrupamento de cada fase de supernova e também ilustra como os dados foram agrupados, neste caso o algoritmo demonstrou ineficiencia ao gerar grupos com muitos exemplos parecidos, isto mostra que o agrupamento não conseguiu separar corretamente as peculiaridades de cada fase espectral de supernova.

O notebook "Agrupamento de dados DBscan" revela uma alternativa bem sucedida ao algoritmo anterior. O agrupamento pelo DBscan revela uma boa separação das supernovas em 8 grupos diferentes com uma homogeneadade de fase para fase indicando os perfis das supernovas Ia no decorrer do tempo.

## Experiência com a Ferramenta orange

A ferramenta orange é baseada em programação visual e permite manipular bases de dados, fazer transformações e pré-processamento, visualizar os dados de forma interativa, executar e avaliar algoritmos de Machine Learning apenas com widgets e metodos encapsulados. Desta maneira a pericia de um programador ou de um cientista de dados não um fator determinante para gerar vizualizações e análises cientificas.

Neste trabalho a ferramenta orange foi desenvolvida para gerar uma bateria de testes eficiente e em tempo reduzido, inidcando quais ferramentas e caminhos produziriam uma estimativa melhor para a separação de fases de supernovas. Todos os dataFrames gerados neste trabalho foram submetidos a testes gerados pelo Orange para gerar uma estimativa preliminar de sucesso ou insucesso em tecnicas de machine learning.

As fases de supernova foram separadas seguindo o criterio de dias de acordo com a tabela 2.

<p align="center"> Tabela 2 - Separação de fases para supernovas Ia</p>
<p align="center">
<img width="460" height="300" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/tabela2.png">
</p>

A distribuição de fases nas bases de dados de supernovas de tipo Ia é mostrada na figura 3.

<p align="center"> Figura 3 - Distribuição de Fases</p>
<p align="center">
<img width="460" height="300" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/dist_fases.png">
</p>

A distribuição dos redshifts das supernovas Ia é mostrada na figura 4. Esta informação é importante pois revela a quantidade de supernovas Ia nas regioes próximas e a quantidade de supernovas Ia capturadas pelos telescópios em regioes mais distantes no universo. Este é um dos fatores que implicam nas correlações de supernovas de tipo Ia como medidas da expansão cósmica acelerada.

<p align="center"> Figura 4 - Distribuição de Redshifts</p>
<p align="center">
<img width="460" height="300" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/dist_red.png">
</p>

As vizualizações das variaveis de componentes principais (PCA) realizadas nos notebooks indicam uma homogenedade nos dados e uma não-lineariedade elevada. Desta forma é possivel, antes de implementar qualquer medida de classificação eliminar algumas alternativas, ou seja, a vizualização dos dados implica na ineficiencia prévia de classificadores lineares e regressoes. A figura 5 ilustra uma estrutura gerada em orange para gerar testes em algoritmos de classificação com eficiência.


<p align="center"> Figura 5 - Estrutura Orange para aprendizado de máquina</p>
<p align="center">
<img width="600" height="600" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/orange.png">
</p>

A tabela 3 ilustra testes de classificadores diversos e seus desempenhos em separar pelos componentes principais (PCA) dos dataframes as fases espectrais de supernovas.

<p align="center"> Tabela 3 - Resultados de Classificação de fases espectrais</p>
<p align="center">
<img width="460" height="300" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/tabela3.png">
</p>

Os resultados gerados pelo método de Random Forest são superiores à outras tecnicas de classificação, este algoritmo separou melhor os dados não lineares e desta forma foi o mais eficiente. A tabela 4 indica a matriz de confusão para a classificação por random forest.

<p align="center"> Tabela 4 - Resultados de Classificação pelo Random Forest</p>
<p align="center">
<img width="460" height="300" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/matriz1.png">
</p>

Random Forest é um algoritmo de aprendizagem de máquina flexível e fácil de usar que produz excelentes resultados a maioria das vezes, mesmo sem ajuste de hiperparâmetros. É também um dos algoritmos mais utilizados, devido à sua simplicidade e o fato de que pode ser utilizado para tarefas de classificação e também de regressão. As árvores de decisão são excelentes preditores. No entanto, podem apresentar alguma dificuldade, pois nem sempre generalizam bem. A figura 6 ilustra como os dados são classificados.

<p align="center"> Figura 6  - Random Forest</p>
<p align="center">
<img width="460" height="300" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/arv.png">
</p>

## Conclusões e Discussões sobre as abordagens

A abordagem gerada pelo Random Forest indica resultados expressivos, entretanto o encapsulamento da ferramenta prejudica uma anáise profunda do caso e desta forma este resultado não pode ser avaliado completamente.

Em contrapartida, os resultados gerados pelo agrupamento com o algoritmo DBscan revela uma separação de perfis de fases espectrais de supernovas melhor do que o algoritmo K-means. A avaliação dos grupos gerados com o DBscan apresentam contribuição no que diz respeito a separar as fases espectrais de maneira mais homogênea identificando perfis homogêneos para cada fase. Desta forma, com o agrupamento gerado de maneira não supervisionada é possivel aplicar os classificadores como perceptrons e regressoes e gerar classificações e análises mais seguras. A figura 7 ilustra os agrupamentos gerados, nestes agrupamentos é possivel correlacinar as fases espectrais e como as explosões de supernovas se comportam no decorrer do tempo.

<p align="center"> Figura 7  - Agrupamento pelo algoritmo DBscan </p>
<p align="center">
<img width="460" height="300" src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/clusters.png">
</p>

Devido à abordagem proporcionada este modelo inicial cumpre os requisitos solicitados em relação à geração de uma estrutura computacional, para análise científica de dados. Espera-se que com o aprimoramento deste modelo inicial seja possível identificar com acurácia e precisão elevada as fases espectrais de supernovas para que tomadas de decisão sejam feitas em tempo reduzido permitindo a otimização e melhor desempenho do processo. 

Espera-se que com esta abordagem inicial gerada na Disciplina de Introdução à Data Science a pesquisa proposta para classificação de fases espectrais em supernovas seja feita em um caminho seguro, pois a disciplina propiciou artificios em relação à estatistica, vizualização e manipulação de informações que permitem o desenvolvimento científico em alto nível.



## Referências

•	PERLMUTTER, S. et al. 1999. Measurements of omega and lambda from 42 high-redshift supernovae. The Astrophysical Journal, v. 517, n. 2, p. 565, 1999.

•	RIESS, A. G. et al. 1998. Observational evidence from supernovae for an accelerating universe and a cosmological constant. The Astronomical Journal, v. 116, n. 3, p. 1009, 1998.

•	BLONDIN, S.; MANDEL, K. S.; KIRSHNER, R. P. 2011. Do spectra improve distance measurements of Type Ia supernovae? Astronomy & Astrophysics, v. 526, p. A81, 2011.

•	BLONDIN, S. et al. The spectroscopic diversity of type Ia supernovae. The Astronomical Journal, v. 143, n. 5, p. 126, 2012.

•	MATHESON, T. et al. Optical spectroscopy of Type Ia supernovae. The Astronomical Journal, v. 135, n. 4, p. 1598, 2008.

•	MODJAZ, M. et al. Optical spectra of 73 stripped-envelope core-collapse supernovae. The Astronomical Journal, v. 147, n. 5, p. 99, 2014.

• SASDELLI, M.; ISHIDA, E. E. O.; VILALTA, R.; AGUENA, M.; BUSTI, V. C.; CAMACHO, H.; TRINDADE, A. M. M.; GIESEKE, F.; SOUZA, R. S. de;
FANTAYE, Y. T.; MAZZALI, P. A. Exploring the spectroscopic diversity of type ia supernovae with dracula: a machine learning approach. Monthly Notices of the Royal Astronomical Society, v. 461, n. 2, p. 2044–2059, 2016. 20, 21
