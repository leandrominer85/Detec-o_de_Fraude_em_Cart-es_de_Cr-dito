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

As variáveis resultantes são nomeadas V1 até V28. Adicionalmente temos as variáveis Time, Amount e Class que não foram transformadas. Todas as variáveis são numéricas

O dataset tem 284807 linhas e 31 colunas, não possui valores nulos e se encontra desbalanceado com a classe de fraude com 0,17% do total. 

As demais estatísticas descritivas podem ser verificadas no notebook

## Tratamento da base

Por se tratar de uma base desbalanceada e com a variável alvo binária é necessário balancear o dataset e normalizar essas duas variáveis.
Primeiramente dividi o dataset em treino e teste. Para o balanceamento e posterior utilização nos modelos de machine learning utilizei três métodos de sampling:

![image](https://user-images.githubusercontent.com/48839817/148216159-456b560d-4f26-42a2-acca-0638200259ed.png)

A parte de standarização das variáveis foi incorporada dentro de um pipeline encapsulado dentro de uma função que gera as estatísticas dos modelos de Machine Learning.


## Machine Learning

Por se tratar de um modelo de classificação com aprendizado de máquina supervisionado optei pelos seguintes modelos para análise: LogisticRegression, DecisionTreeClassifier,
RandomForestClassifier, LinearSVC e Adaboost. Todos esses modelos foram encapsulados na supracitada função e utilizados com seus parâmetros padrão e randomstate = 42.
Como mencionado a parte de tratamento das variáveis foi incorporada nessa função. Ela fornece prints com as principais estatísticas para esses modelos.
Para cada método de sampling foi rodada essa função. Um exemplo de parte do output dela:

![image](https://user-images.githubusercontent.com/48839817/148216922-15deb466-3494-418a-9677-09c98d6e8c54.png)

![image](https://user-images.githubusercontent.com/48839817/148216975-237893c1-01c9-431e-bc8c-ef58917e8bcc.png)



## Conclusão

A escolha da métrica de avaliação de um modelo de aprendizado de máquina deve ser atrelada ao problema que se quer atacar.
Por se tratar de uma um projeto de detecção de fraudes, que lesam tanto o cliente quanto as empresas, queremos minimizar a presença de falsos negativos - quando se trata de uma fraude mas classificamos como normal.
Por isso, a métrica principal que levei em conta na escolha dos modelos foi Recall:

![image](https://user-images.githubusercontent.com/48839817/148217331-d21d3dc7-5dd1-424a-a844-02fc3483e6f5.png)



Mas essa não pode ser a única métrica a ser considerada. Caso fosse teríamos como melhor modelo o RandomForest com undersampling com:

| RandomForestClassifier |                      |
|------------------------|----------------------|
| Accuracy:              | 0.7534262607820418   |
| Precision:             | 0.004781744153015813 |
| Recall:                | 0.6824324324324325   |
| F1:                    | 0.009496944052656324 |
| Roc_auc:               | 0.7179909392363228   |


Mas utilizando a mesma técnica de sampling o Adaboost se revela levemente superior em Acurácia:


| AdaBoostClassifier |                      |
|--------------------|----------------------|
| Accuracy:          | 0.7620284868274756   |
| Precision:         | 0.004856988667026443 |
| Recall:            | 0.668918918918919    |
| F1:                | 0.00964395304661244  |
| Roc_auc:           | 0.7155544826143923   |


Ambos os modelos estão muito próximos e deveriam ser levados em consideração ao melhorarmos os hiperparâmetros. Mas o Adaboost aparenta ser menos sensível à variação dos dados ao ser mais estável nas três técnicas de sampling.

Outras conclusões:

* Mesmo em um dataset previamente trabalhado temos a necessidade de uma análise exploratória minuciosa
* Em datasets desbalanceados um ponto crítico que interfere nos modelos é as escolhas que fazemos de sampling
* Mesmo testando diversos modelos e diversas métricas a conclusão pelo melhor modelo só pode ser feita quando otimizarmos os hiperparâmetros, mas já temos pistas que indicam que Adaboost ou Random Forest podem ser boas escolhas.


## Software & Bibliotecas

O Projeto utilizou Python 3 e as seguintes bibliotecas:

-   [Pandas](http://pandas.pydata.org/)
-   [Seaborn](https://seaborn.pydata.org/index.html)
-   [Matplotlib](https://matplotlib.org/)
-   [sklearn](https://scikit-learn.org/stable/)
-   [imbalanced-learn](https://imbalanced-learn.org/stable/)
-   [scikitplot](https://scikit-plot.readthedocs.io/en/stable/Quickstart.html)
-   [datetime](https://docs.python.org/3/library/datetime.html)
-   [numpy](https://numpy.org/)


**Meus Links:**

* [LinkedIn](https://www.linkedin.com/in/leandro-minervino-b469681b/)
* [Colab](https://colab.research.google.com/drive/1SkgqRVi2Y6016fKROhCkTVGpUivDyu3G?usp=sharing)



## Outros Projetos Meus:


* **[Scrap sites de notícia](https://github.com/leandrominer85/Scrap_sites_noticias)**

* **[Políticas Raciais no ensino superior](https://github.com/leandrominer85/Pol-tica-Racial-no-Ensino-Superior-2009-2019-)**
 
* **[Disaster-Response-Pipelines](https://github.com/leandrominer85/Disaster-Response-Pipelines)**

* **[Dados do Airbnb Lisboa](https://github.com/leandrominer85/Dados-do-Airbnb-Lisboa/blob/main/README.md)**

* **[Panorama COVID-19](https://github.com/leandrominer85/Panorama_Covid-19)**
