Objetivo:

Empregar algoritmos de Machine Learning no contexto instituições financeiras com dois conjuntos de dados: um relativo a aprovação de empréstimo e outro relativo a aprovação de cartão de crédito.

Fonte dos Dados:

*South German Credit Data Set
Os dados são de uma amostra com 1 mil classificações de crédito (entre “bom” e “ruim”) coletados entre 1973 e 1975 de um grande banco do sul da Alemanha.
O dataset corresponde a um conjunto de variáveis descrevendo aspectos do proponente de um empréstimo e as características da solicitação. Temos, além da variável objetivo risco_credito que utiliza 0 para risco bom ou 1 para risco ruim, 20 atributos sendo 3 variáveis numéricas e 17 variáveis categóricas.
O conjunto de dados está disponível no link: [South German Credit Data Set](https://archive.ics.uci.edu/ml/datasets/South+German+Credit+%28UPDATE%29)


*Statlog (Australian Credit Approval) Data Set
Este conjunto de dados diz respeito a aprovação ou não de solicitações de cartão de crédito. Todos os nomes e valores originais foram disponibilizados com alterações para símbolos para fins de confidencialidade dos dados.
O conjunto de dados possui 14 atributos sendo 6 numéricos e 8 categóricos. Havia valores ausentes, sendo que em 37 casos (5%) tinha-se um ou mais valores ausentes que foram substituídos pela moda do atributo, no caso de atributos categóricos, e pela média, no caso de atributo numérico.
O conjunto de dados está disponível no link: [Statlog (Australian Credit Approval) Data Set](https://archive.ics.uci.edu/ml/datasets/Statlog+%28Australian+Credit+Approval%29)

Resultados: 

Utilizamos a abordagem de validação cruzada aninhada (Nested Cross-Validation) em
conjunto com a função RandomizedSearchCV para busca no espaço de hiperparâmetros e
avaliação dos modelos. A validação cruzada aninhada faz um melhor trabalho em garantir uma
medida de generalização mais robusta, confiável e que é mais próxima de como o modelo se
sairia em ambiente de produção. Na validação cruzada aninhada utiliza-se a validação cruzada
interna para seleção dos hiperparâmetros e a validação cruzada externa para avaliar o
desempenho do modelo preditivo.
Quanto ao desempenho dos algoritmos entre si, no conjunto de dados Alemão o algoritmo de Regressão Logística apresentou os melhores resultados e no caso do conjunto de dados Australiano o algoritmo de Floresta Aleatória apresentou os melhores resultados



