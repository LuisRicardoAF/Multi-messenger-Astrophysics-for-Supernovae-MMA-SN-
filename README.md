# Estrutura MMA-SN
## Luis Ricardo Arantes Filho - Doutorando CAP INPE

## Acesso a estrutura MMA-SN por meio de comandos de dataframes Python. Solução para os dados do acervo OPENSN.

Acesse o notebook para detalhes.

Arquivo dataframe compartilhado via-google drive

Acesse o link: https://github.com/LuisRicardoAF/Multi-messenger-Astrophysics-for-Supernovae-MMA-SN-


## MMA-SN

Entende-se como Cyber-infraestrutura um conjunto de sistemas que permitem a manipulação e armazenamento de dados que podem ser distribuídos de
forma a permitir a ciência dos dados e uma análise robusta e consistente da informação armazenada, para que as pessoas possam manipular e realizar produções científicas, tanto individualmente como em conjunto (ATKINS et al., 2003; BERMAN;
BRADY, 2005; STEWART et al., 2009; STEWART et al., 2010).

A Cyber-infraestrutura desenvolvida foi denominada MMA-Supernovae (MultiMessenger Astrophysics for Supernovae (MMA-SN)) (FILHO et al., 2021), esta estrutura foi desenvolvida com o propósito de tornar o acesso e manipulação de dados de SN algo mais simples tanto para a comunidade científica quanto para pessoas em geral.

A inspiração para o desenvolvimento da estrutura reside no conceito de MMA (ALLEN et al., 2018; ALLEN et al., 2019; GEORGE; HUERTA, 2018), em que o objetivo é providenciar a coleta e análise de objetos astronômicos e os diferentes tipos de dados relacionados ao mesmo. A análise de informações de dados de múltiplas fontes, obtidas por meio de medidas instrumentais de alta resolução, tornou-se uma tarefa fundamental em todas as áreas científicas. O desenvolvimento de métodos especializados capazes de tratar esses objetos astronômicos com dados de várias fontes, com grande variabilidade e extensão de medidas, é um ponto chave para o estudo de fenômenos científicos complexos, especialmente os relacionados à análise sistêmica nas ciências espaciais e ambientais.

<p align="center">
<img src="https://github.com/LuisRicardoAF/Multi-messenger-Astrophysics-for-Supernovae-MMA-SN-/blob/main/Diagrama_MMA_completo.drawio.png">
</p>


Acesse pelos comandos.


<p align="center">
<img src="https://github.com/LuisRicardoAF/Multi-messenger-Astrophysics-for-Supernovae-MMA-SN-/blob/main/comandos.png">
</p>

Arquivo em formato .pkl MMA-SN.

Mais detalhes serão adicionados em breve.



## Importancia das SN
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

## Referências

•	PERLMUTTER, S. et al. 1999. Measurements of omega and lambda from 42 high-redshift supernovae. The Astrophysical Journal, v. 517, n. 2, p. 565, 1999.

•	RIESS, A. G. et al. 1998. Observational evidence from supernovae for an accelerating universe and a cosmological constant. The Astronomical Journal, v. 116, n. 3, p. 1009, 1998.

•	BLONDIN, S.; MANDEL, K. S.; KIRSHNER, R. P. 2011. Do spectra improve distance measurements of Type Ia supernovae? Astronomy & Astrophysics, v. 526, p. A81, 2011.

•	BLONDIN, S. et al. The spectroscopic diversity of type Ia supernovae. The Astronomical Journal, v. 143, n. 5, p. 126, 2012.

•	MATHESON, T. et al. Optical spectroscopy of Type Ia supernovae. The Astronomical Journal, v. 135, n. 4, p. 1598, 2008.

•	MODJAZ, M. et al. Optical spectra of 73 stripped-envelope core-collapse supernovae. The Astronomical Journal, v. 147, n. 5, p. 99, 2014.

• SASDELLI, M.; ISHIDA, E. E. O.; VILALTA, R.; AGUENA, M.; BUSTI, V. C.; CAMACHO, H.; TRINDADE, A. M. M.; GIESEKE, F.; SOUZA, R. S. de;
FANTAYE, Y. T.; MAZZALI, P. A. Exploring the spectroscopic diversity of type ia supernovae with dracula: a machine learning approach. Monthly Notices of the Royal Astronomical Society, v. 461, n. 2, p. 2044–2059, 2016. 20, 21
