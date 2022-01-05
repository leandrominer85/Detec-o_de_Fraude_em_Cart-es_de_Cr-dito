[![author](https://img.shields.io/badge/author-LeandroMinervino-red.svg)](https://www.linkedin.com/in/leandro-minervino-b469681b/) [![](https://img.shields.io/badge/python-3.7.12+-blue.svg)](https://www.python.org/downloads/release/python-365/) [![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)]()


![image](https://user-images.githubusercontent.com/48839817/148154049-9bda9b00-f8fc-47fb-a2d7-eea9bef16359.png)


# Detecção de Fraudes em Cartões de Crédito

# Introdução
Esse projeto é parte do curso Data Science na Prática e tem como intuito demonstrar uma abordagem introdutória ao aprendizado de máquina.

Neste projeto, iremos abordar o problema das fraudes em cartões de crédito, uma das principais preocupações das instituições financeiras como bancos e fintechs. Apenas no Brasil, cerca de 12,1 milhões de pessoas já foram vítimas de algum tipo de fraude financeira no último ano. Traduzindo em valores, os golpes financeiros ultrapassaram a cifra de R$ 1,8 bilhão de prejuízo por ano para os últimos 12 meses.

O Objetivo desse projeto é criar um modelo de machine learning básico que possa servir como base para posterior refinamento.

# Dados

Os dados que usaremos neste projeto foram disponibilizados por algumas empresas européias de cartão de crédito. O dataset representa as operações financeiras que aconteceram no período de dois dias, onde foram classificadas 492 fraudes em meio a quase 290 mil transações.

As features são todas numéricas, e foram descaracterizadas (por problemas ligados à privacidade e segurança). 
Na página original dos [dados](https://www.kaggle.com/mlg-ulb/creditcardfraud), também é informado que as variáveis passaram por uma transformação conhecida como Análise de Componentes Principais (Principal Component Analysis - PCA).

As variáveis resultantes são nomeadas V1 até V28. Adicionalmente temos as variáveis Time, Amount e Class que não foram transformadas.

O dataset tem 284807 linhas e 31 colunas, não possui valores nulos e se encontra desbalanceado com a classe de fraude com 0,17% do total. 



####


## Alguns exemplos de visualizações

Exponho aqui algumas visualizações disponíveis:

Mortes por Covid no mundo:

![image](https://user-images.githubusercontent.com/48839817/145810992-8adc8f31-97fa-4f8b-a62f-ee08d8e15111.png)


Bar Chart Race de casos de Covid por continente:


https://user-images.githubusercontent.com/48839817/145811307-df02fc5e-84cc-4435-9d85-c87b11d9996f.mp4


Gráfico interativo de mortes no Brasil e e, u, país selecionado:

![image](https://user-images.githubusercontent.com/48839817/145812185-05f60e85-3208-4ae7-998f-7b9afe0abe57.png)


## Conclusão

A pandemia causada pela COVID-19 continua infectando e causando mortes pelo mundo. Vimos que os casos e mortes se somam ao longo do tempo mas isso não ocorre de maneira linear. Antes temos as chamdas ondas, com fluxos e refluxos mundiais causados por diversas razões - dentre elas o surgimento de variáveis e vacinas.

Ao fragmentar essa análise para o nível continental ficam claras as diferenças regionais. Vemos como cada onda da doença afetou de maneira diferente essas regiões. A primeira e segunda ondas se pronunciam na Europa com uma forte terceira nas américas e posteriormente as ondas asiáticas que afetaram sobretudo a Índia. Atualmente vemo o Novo Continente liderando em mortes por milhão, seguidos do Velho Continente e da Ásia - Oceania é um caso constante de controle da doença.

Descendo mais um nível de desagregação dos dados chegamos aos países. Mesmo nesse nível as disparidades internas impactam na pandemia. Mas é a partir desse nível que podemos ver mais claramente como as diferentes características afetam o desenvolvimento da pandemia.

O caso brasileiro se apresenta como um dos piores mundialmente. Tendo a primeira infecção detectada em 26 de Fevereiro de 2020 e a primeira morte 20 dias depois, a vacinação só iniciou em 17 de Janeiro de 2021. Após uma primeira onda entre Abril e Outubro de 2020 uma segunda onda mais forte veio próxima de Março de 2021. Essa nova onda alcança um pico em Abril e começa a arrefecer então - em parte pelo avanço da vacinação que nesse mesmo mês começa a acelerar.

Esse cenário coloca o Brasil como segundo país com mais mortes totais atrás de EUA e à frente de Índia e entre os 10 países com mais mortes por milhão de habitantes.

O que leva cada país a ter um cenário melhor ou pior na pandemia ainda é incerto. Mas  a correlação dos dados apontam como possíveis causas a idade da população, a pobreza e doenças cardiovasculares. Outras relações poderiam ser feitas, mas seriam necessários dados mais desagregados para afirmar com maior grau de certeza - como é o caso de mulheres fumantes .




## Software & Bibliotecas

O Projeto utilizou Python 3 e as seguintes bibliotecas:

-   [Pandas](http://pandas.pydata.org/)
-   [Seaborn](https://seaborn.pydata.org/index.html)
-   [Matplotlib](https://matplotlib.org/)
-   [ipywidgets](https://ipywidgets.readthedocs.io/en/latest/)
-   [bar_chart_race](https://pypi.org/project/bar-chart-race/)


**Meus Links:**
* [Artigo desse projeto no Medium](https://epp-minervino.medium.com/an%C3%A1lise-explorat%C3%B3ria-da-covid-19-fac91234ccee)
* [LinkedIn](https://www.linkedin.com/in/leandro-minervino-b469681b/)
* [Colab](https://colab.research.google.com/drive/1o4dzudIzvU1XIkGKI29nh7yPBMh9avuv?usp=sharing)





## Outros Projetos Meus:


* **[Scrap sites de notícia](https://github.com/leandrominer85/Scrap_sites_noticias)**

* **[Políticas Raciais no ensino superior](https://github.com/leandrominer85/Pol-tica-Racial-no-Ensino-Superior-2009-2019-)**
 
* **[Disaster-Response-Pipelines](https://github.com/leandrominer85/Disaster-Response-Pipelines)**

* **[Dados do Airbnb Lisboa](https://github.com/leandrominer85/Dados-do-Airbnb-Lisboa/blob/main/README.md)**
