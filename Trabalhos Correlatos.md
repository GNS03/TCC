- DBSCAN
- MLP
- Python
- Dados

# Trabalhos Correlatos

## MultiLayer Perceptron

Redes Neurais podem assumir diversas formas, baseadas na arquitetura original do perceptron, porém o perceptron possui apenas uma camada escondida, sendo capaz de aprender apenas padrões simples, para solucionar esse defeito foi desenvolvido o MultiLayer Perceptron, ou de maneira mais geral, Redes Neurais com múltiplas camadas escondidas. 

Em *A comparison of machine learning algorithms for diabetes prediction* (2021) de Jobeda Jamal Khanam, Simon Y. Foo, foram desenvolvidos diversos modelos de Redes Neurais a fim de comparar suas performances, "Primeiro foi construído uma rede neural como uma camada escondida junto com uma camada de entrada e uma de saída. A camada de entrada foi definida com cinco neurônios, já que os dados possuem cinco características. A camada escondida possui cinco neurônios e com a função de ativação ReLu (Unidade Linear Retificada). A camada de saída tem um neurônio e a função de ativação sigmoide", essa é a versão mais simples e a mais parecida com o perceptron original. 

Foram desenvolvidas também Redes Neurais de duas e três camadas escondidas, "Foi definido um modelo de Rede Neural com quatro densas camadas. A primeira e a última são a entrada e saída respectivamente, tendo a mesma forma, quantidade de neurônios e função de ativação que o modelo de uma camada escondida. A segunda camada consiste de uma camada escondida de vinte e seis neurônios, e a terceira camada consiste de uma camada escondida de cinco neurônios. A função de ativação dos neurônios de cada camada escondida é a ReLu (Unidade Linear Retificada)", este modelo utiliza da mesma técnica que o MultiLayer Perceptron para funcionar. 

Este é o modelo mais complicado contendo com três camadas escondidas, "Foi desenvolvido um modelo com cinco densas camadas. A primeira e a quinta camada são as de entrada e saída respectivamente, tendo a mesma forma, quantidade de neurônios e função de ativação que o modelo de uma camada escondida.As segunda, terceira e quarta camadas tem, respectivamente, dezesseis, dez, cinco neurônios cada. A função de ativação dos neurônios é a ReLu (Unidade Linear Retificada)."

Para ser possível comparar os resultados dos três modelos definidos previamente, o artigo testa o modelo de 1 camada escondida em 200 épocas três vezes, mudando o parâmetro de learning rate para 0.1, 0.01, 0.005 entre testes. O teste com melhor performance foi o que utilizou o learning_rate igual a 0.01. Por isso todos testes realizados posteriormente utilizam o learning_rate igual a 0.01.

Para a comparação entre os modelos de rede neural, o artigo determina que os parâmetros utilizados fossem learning_rate igual 0.01, variando as épocas entre 200, 400, 800. A partir da comparação dos resultados o artigo determina que o modelo com a melhor performance foi o modelo de duas camadas escondidas de 400 épocas, com uma acurácia de 88.6%.

## DBSCAN

O DBSCAN é um algoritmo de classificação não supervisionada, muito utilizado quando não se conhece o resultado esperado ou quando a forma do cluster não é convexa.

Em um estudo de 2025, "USO DE ALGORITMOS SUPERVISIONADOS E NÃO SUPERVISIONADOS
PARA DETECÇÃO DE FRUTOS DE CAFÉ EM NUVENS DE PONTOS LIDAR", realizado por Glória Maria Padovani Ederli, Aluir Porfírio Dal Poz, Nilton Nobuhiro Imai, Adilson Berveglieri e Gleice Aparecida de Assis, da Universidade Estadual Paulista. O DBSCAN foi utilizado para analisar os dados de LIDAR de plantações de café, a fim de determinar a quantidade de frutos. 

Para isso o DBSCAN foi desenvolvido com certas características, descritas na metodologia do trabalho, "Para o desenvolvimento do DBSCAN, os dados com aplicação da UMAP foram utilizados como entrada. O UMAP reduz a dimensionalidade preservando a estrutura topológica, o que clarifica a separação entre os clusters e simplifica o trabalho do DBSCAN, um método de clustering baseado em densidade que não necessita de um número pré-definido de clusters. Este pré-processamento é especialmente valioso para dados LiDAR, dada a sua complexidade e alta dimensionalidade, permitindo que o DBSCAN identifique clusters com maior precisão e menor dependência de parâmetros. Herrmann et al.,2024, também demonstram que a combinação de UMAP e DBSCAN pode superar outros métodos em conjuntos de dados complexos"

"No que diz respeito aos parâmetros do DBSCAN, MinPts e eps, foi seguida a metodologia proposta por [9], que sugere usar MinPts igual a duas vezes o número de dimensões do conjunto de dados, neste caso, totalizando 6 para MinPts. Para determinar o parâmetro Eps, a abordagem recomendada envolve a utilização de um gráfico de k-distância ordenada com k sendo igual a MinPts - 1. Após calcular a distância até o k-ésimo vizinho mais próximo e ordenar essas distâncias, o ponto de corte é identificado no primeiro vale do gráfico, e a distância deste ponto é usada como Eps [9]. Este gráfico foi utilizado para encontrar o valor de Eps, que foi estabelecido em 0,14."

"Como o DBSCAN é um algoritmo de clustering não supervisionado, a métrica utilizada para avaliação foi o índice de Davies-Bouldin [10]. Este índice mede a qualidade dos clusters formados, baseando-se na relação entre a dispersão dentro dos clusters e a separação entre eles, considerado ideal quando apresenta um valor mínimo."

"O algoritmo DBSCAN apresentou um valor de IDB de 1,2947 sem a utilização do UMAP como pré-processamento. Com o uso do UMAP, o valor de IDB foi reduzido para 0,0875, indicando uma melhora significativa na qualidade do agrupamento."

O algoritmo desenvolvido nesse trabalho teve um bom resultado diante do problema proposto, isso se dá pelo cuidado e preparo que os pesquisadores tiveram ao desenvolver o modelo, utilizando parâmetros e métricas bem definidos, como UMAP, k-distância ordenada, índice de Davies-Bouldin.


## Python

